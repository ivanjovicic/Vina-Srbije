# Data Ontology & Quality Strategy

## 1. Data can become the moat only if it is trustworthy

A dataset copied from directories is not a moat. Valuable data must be:

- canonical;
- deduplicated;
- provenance-aware;
- fresh;
- winery-verified where possible;
- vintage-aware;
- useful for transactions/decisions.

## 2. Core entity model

### Legal / producer layer

- LegalEntity
- Producer
- WineryBrand
- WineryLocation

### Geography

- Country
- OfficialWineRegion
- Rayon/Subregion
- Vineyard (later)
- TourismCluster

Official wine geography and tourism naming should be distinct.

### Wine

- WineLabel
- WineVintage
- GrapeVariety
- BlendComponent
- Bottle/SKU (later commerce)
- TasteProfile
- Award

### Tourism

- Experience
- ExperiencePrice
- Language
- Amenity
- OpeningSchedule
- ReservationPolicy
- Accommodation/Restaurant flags

### User

- User
- PreferenceProfile
- PassportEntry
- PrivateRating
- Visit/VerifiedVisit
- Consent

### Commercial

- QualifiedAction
- BookingRequest
- ReorderLead
- Merchant/Product/Stock/Order only when commerce gate opens.

## 3. Vintage specificity

Award/rating/taste/availability can belong to a vintage, not generic label. Data model must not flatten:

`Prokupac Reserve 2022` and `Prokupac Reserve 2023`

into an indistinguishable object.

## 4. Canonical identity

Each producer/winery needs:

- internal immutable ID;
- legal name if known;
- consumer brand name;
- normalized Latin form;
- original Cyrillic form if relevant;
- aliases;
- official website/domain;
- location coordinates;
- source references.

Merge rules must handle renames and duplicate directories.

## 5. Provenance model

Every critical field should support:

- value;
- SourceType;
- SourceUrl/SourceId;
- ProvidedBy;
- VerifiedAt;
- Confidence;
- IsWineryConfirmed;
- EffectiveFrom/To where needed.

Example:

`TastingPrice = 1800 RSD`

without `source + verified date` should not be displayed as current fact after freshness threshold.

## 6. Freshness classes

| Class | Primer | Target refresh | UX when stale |
|---|---|---|---|
| Static | region, coordinate | annual/on change | show normally |
| Semi-dynamic | wine catalogue, amenities | 90–180d | last verified |
| Dynamic | opening hours, tasting price | 30–60d | warn/reconfirm |
| Highly dynamic | availability, stock, event status | real-time/days | do not claim current if not connected |

Targets are initial hypotheses.

## 7. Data sources hierarchy

1. official registry/geography;
2. winery-owned source;
3. platform manual verification;
4. trusted partner feed;
5. editorial/public web candidate;
6. AI extraction candidate;
7. user suggestion.

Lower level never silently overwrites higher-authority data.

Registry/public-source ingestion must respect access terms and anti-bulk controls. APR explicitly warns against unauthorized scripted bulk access in its Tourism Registry context; use this as a general governance reminder and verify terms for each source before automating. [S23]

## 8. AI extraction

Allowed flow:

`source page -> extraction candidate -> source link -> validation queue -> publish`

Forbidden flow:

`source page -> LLM -> public fact`

AI may extract aroma descriptors or hours into a candidate, but humans/winery confirmation determine publication for critical fields.

## 9. Taste ontology

Separate:

### Wine properties

- sweetness;
- acidity;
- tannin;
- body;
- alcohol perception;
- oak;
- aromatic families;
- intensity.

### User preferences

Same axes or high-level likes, but never assume one from the other without behavior/questionnaire.

### Source types

- producer;
- expert;
- crowd aggregate;
- platform editorial;
- AI-extracted candidate.

## 10. Recommendation explainability

Instead of opaque score:

> “Preporučujemo jer si sačuvao dva puna, suva crvena vina i ovo vino ima sličan profil; cena je u tvom izabranom rasponu.”

Confidence should fall when source data is weak.

## 11. Reviews

Do not launch public reviews in MVP. With small local volume:

- low sample makes scores misleading;
- moderation/legal burden;
- incumbent review platforms are stronger.

Private reactions can train personalization without creating public reputation disputes.

## 12. Awards

Model:

- Competition;
- AwardYear;
- Medal/Score;
- WineVintage;
- OfficialSource.

Do not attach award to generic wine if vintage-specific.

## 13. Data quality KPIs

- % winery profiles verified <90d;
- % dynamic fields within freshness SLA;
- duplicate rate;
- conflict rate;
- correction turnaround;
- % wine records vintage-specific;
- % displayed claims with provenance;
- winery-confirmed data share.

## 14. Registry access work item

Investigate official Vinski registar access/reuse:

- public UI/API?
- stable identifier?
- downloadable dataset?
- license/reuse terms?
- update frequency?

Until confirmed, it is a **promising canonical source hypothesis**, not an ingest dependency.
