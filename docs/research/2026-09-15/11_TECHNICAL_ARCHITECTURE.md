# Technical Architecture

## 1. Architecture decision

**Default: SEO-first web + modular monolith.**

Suggested stack:

- .NET 10 / ASP.NET Core;
- PostgreSQL;
- PostGIS for geospatial queries if needed;
- EF Core;
- React + TypeScript with SSR/SSG-capable framework;
- object storage + CDN for authorized images;
- simple background job mechanism;
- transactional email;
- web push/PWA only after value is clear.

No microservices initially.

## 2. Context diagram

```text
Users / Tourists            Winery Staff
       |                         |
       v                         v
   SEO Web / PWA -------- Winery Portal
          |                    |
          +---------+----------+
                    v
              ASP.NET Core
          Modular Monolith API
                    |
     +--------------+----------------+
     |              |                |
 PostgreSQL      Object Storage   Email/Jobs
 + PostGIS           / CDN
     |
 External integrations (only when justified)
 Maps / Geocoding / Payment / Winery links
```

## 3. MVP modules

### Catalog

Winery, wine, vintage, grape, official/tourism region.

### Geography

Coordinates, distance, cluster filters.

### Experience

Tasting programs, price, language, amenities, direct/request flow.

### Passport

Save wine/vintage, verified context, note/reaction.

### Search

Postgres filtering/full-text/trigram.

### Identity & Claims

Consumer account + winery business role + manual claim verification.

### Data Quality

Source/provenance/freshness/moderation.

### Analytics

Qualified actions, QR scan/save, repeat action.

### Content/SEO

Region/winery/wine/experience pages and editorial landing pages.

## 4. BLOCKED modules

- Payments;
- Commerce/Orders;
- Inventory;
- Shipping;
- sophisticated Booking Calendar;
- Reviews;
- Recommendation ML;
- Native Mobile.

They enter only through gates.

## 5. Database design principles

- UUID/internal IDs;
- business keys for aliases/external source IDs;
- temporal/freshness fields;
- provenance tables rather than untraceable overwritten text;
- WineLabel -> WineVintage relationship;
- soft-delete/archive for source history;
- audit trail for winery-owned critical edits.

## 6. Geospatial

MVP needs:

- winery point;
- distance from city/user-entered point;
- cluster membership;
- map bounding boxes.

PostGIS is reasonable but not mandatory on day one if hosting supports it cheaply.

Do not build custom routing engine. Use existing directions provider/link until route demand is proven.

## 7. Map provider strategy

Evaluate OpenStreetMap ecosystem + MapLibre/Leaflet first for cost control and display. Geocoding/routing providers must be separately reviewed for terms/caching. Google Maps can remain link-out for current directions/hours even if not the rendered map.

Provider decision criteria:

- commercial license;
- geocoding quality Serbia;
- directions;
- price;
- caching/storage restrictions;
- attribution requirements.

## 8. Search

### Phase 1

Postgres:

- structured filters;
- `pg_trgm` fuzzy names;
- full-text for descriptions.

### Trigger for external engine

Only if:

- relevance becomes material bottleneck;
- dataset/query volume exceeds Postgres comfort;
- multilingual faceting needs justify it.

No vector DB just to say “AI search”.

## 9. Natural-language query

Optional later:

> “Vinarija do 90 min od Beograda, ručak i crvena vina.”

LLM parses to verified structured filters. Deterministic query executes them. LLM never invents availability/price.

## 10. QR design

QR should encode opaque/signed identifier, not sensitive user data.

Possible routes:

- winery-level QR -> select wines tasted;
- wine/vintage QR -> direct Passport save.

Metrics:

- scans;
- completed saves;
- anonymous -> account conversion;
- return/reorder events.

## 11. Auth/security

### Consumer

Magic link/email or mainstream social login; avoid password friction if possible.

### Winery

- verified claim;
- MFA;
- roles: Owner/Editor;
- audit log;
- critical changes review if suspicious.

### Admin

Strong MFA, least privilege, full audit.

## 12. Security threat summary

- fake winery claim;
- malicious price/contact edits;
- QR tampering;
- spam booking requests;
- account takeover;
- PII exposure;
- unauthorized bulk scraping;
- admin misuse.

Mitigate proportionally; no enterprise theater.

## 13. Background processing

Use simple scheduled/background jobs for:

- freshness reminders;
- stale checks;
- email follow-up;
- analytics aggregation;
- source re-verification queue.

No RabbitMQ/Kafka until durable cross-service/event volume actually requires them.

## 14. Caching

Start with HTTP/CDN + application/database optimization. Redis only when measured hot data/scale justifies it.

## 15. Observability

MVP:

- structured logs;
- request/error tracing;
- health endpoints;
- uptime alerts;
- database backup verification;
- business funnel metrics.

Business observability is as important as technical observability.

## 16. SEO architecture

Indexable page types:

- `/vinarije/{slug}`
- `/vina/{slug}/{vintage?}`
- `/regioni/{slug}`
- `/iskustva/{slug}`
- curated intent pages only when data-rich.

Requirements:

- SSR/SSG output;
- canonical URLs;
- sitemap split by entity;
- structured data where semantically correct;
- real editorial context;
- image rights/alt text;
- no thin AI-generated combinatorial pages.

## 17. Internationalization

MVP:

- sr-Latn;
- en.

Separate canonical names from translations. Wine/brand names should not be mechanically translated.

## 18. Expected infrastructure cost

At pilot scale infrastructure should be tens to low hundreds of euros/month, depending on image/maps/email providers. It is not the main cost. Main cost is:

- data curation;
- winery sales/onboarding;
- content rights;
- verification;
- operations.

## 19. Architecture evolution triggers

### Add booking module when

manual requests convert and winery response workflow is proven.

### Add payment when

legal/provider model is signed off and GMV justifies integration.

### Add mobile when

QR/passport/push behavior shows material retention uplift.

### Add recommendation ML when

there are enough cross-user/wine behavior events to outperform deterministic rules.

### Split services when

organizational/load boundaries exist, not in anticipation.
