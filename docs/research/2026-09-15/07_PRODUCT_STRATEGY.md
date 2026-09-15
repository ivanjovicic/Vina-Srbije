# Product Strategy

## 1. Product definition

**Working product statement:**

> Pronađi provereno iskustvo u srpskoj vinariji, sačuvaj vina koja si probao i lako ih pronađi ili kupi ponovo.

Ovo namerno nije “marketplace svih vina” niti “mapa svih vinarija”.

## 2. Primary job

MVP mora rešavati jedan glavni job:

> **Pretvori interesovanje za posetu vinariji u pouzdanu akciju i zadrži digitalni trag vina koje je gost probao, tako da odnos ne prestane kada napusti vinariju.**

## 3. Core loop

1. **Discover:** korisnik nalazi vinariju/experience po lokaciji, prilici i praktičnim filterima.
2. **Act:** šalje booking/request ili ide kroz verified direct handoff.
3. **Visit:** vinarija potvrđuje posetu/QR je dostupan na licu mesta.
4. **Save:** korisnik čuva konkretno vino + berbu u Passport.
5. **Remember:** privatna beleška/rating + history.
6. **Re-engage:** 30–60 dana kasnije personalizovan, permission-based follow-up.
7. **Reorder/Return:** direct buy link, contact ili sledeća experience preporuka.
8. **Attribution:** vinarija vidi merljive qualified actions.

## 4. Where loop can break

| Transition | Rizik | Signal |
|---|---|---|
| Discover -> Act | Google/direct je dovoljno dobar | low profile-to-action conversion |
| Act -> Visit | winery response spor | >24–48h response, cancellation |
| Visit -> Save | QR nema vrednost | <15–20% scan/save |
| Save -> Re-engage | user ne želi account/notification | opt-in nizak |
| Re-engage -> Reorder | nema realne repeat kupovine | <5% meaningful action |
| Value -> Payment | winery ne želi da plati | pilot success bez conversion-to-paid |

## 5. MVP scope

### Consumer

- Home/search landing;
- region/cluster pages;
- winery profile;
- experience profile;
- practical filters: distance/region, restaurant, accommodation, tasting, language, price range, family/accessibility only if verified;
- map;
- “Request/Contact/Book” qualified action;
- save wine/vintage;
- Wine Passport;
- private note / simple like-neutral-dislike;
- direct reorder link where winery has a shop;
- email follow-up only with explicit consent;
- sr-Latn + English.

### Winery

- claim profile;
- manual verification;
- edit critical fields;
- experience details;
- QR generator;
- basic analytics;
- action confirmation (optional simple workflow).

### Admin/data

- provenance;
- last verified;
- moderation;
- duplicate merge;
- stale flags;
- source conflict resolution.

## 6. Explicitly out of MVP

- checkout;
- platform payment;
- multi-winery cart;
- inventory sync;
- shipping;
- public user reviews;
- social following/feed;
- achievements/badges;
- label scan;
- sophisticated Taste Match;
- AI chatbot;
- automatic route optimization;
- transport sales;
- hotel bundling;
- native iOS/Android app.

## 7. Discovery UX: occasion first

Before building detailed sommelier-style preference onboarding, test simple jobs:

- “Vikend blizu Beograda”;
- “Vinarija sa ručkom”;
- “Degustacija na engleskom”;
- “Poklon vino do 3.000 RSD”;
- “Crveno uz steak”;
- “Želim da probam Prokupac”.

Hypothesis: novice user may understand occasion + budget more readily than tannin/acidity/body.

## 8. Wine Passport design

Minimum entry:

- winery;
- wine;
- vintage if known;
- date;
- private reaction;
- optional note;
- verified-at-winery flag if QR context proves it.

Do not require long review.

### Value order

1. memory;
2. reorder;
3. better recommendations;
4. history;
5. only later gamification.

Badges are BLOCKED until Passport has natural repeat use.

## 9. Taste strategy

### V0

No “94% match”. Filters + occasions.

### V1

Structured attributes where source is known:
- sweetness;
- acidity;
- tannin;
- body;
- oak influence;
- intensity;
- key aroma families.

### V2

Weighted preference similarity with explanation.

### V3

Behavioral feedback from saves/visits/reorders.

### V4

Hybrid recommender only after sufficient cross-user data.

Each attribute must have source/confidence. AI extraction is candidate data, not fact.

## 10. Booking evolution

### Stage A — Direct action / request

User sends structured request or clicks verified official contact.

### Stage B — Platform request workflow

Winery accepts/rejects; no payment.

### Stage C — Deposit / pay-at-winery

Only after legal/payment review.

### Stage D — Instant full booking

Only if supply can maintain availability and payment economics justify it.

## 11. Responsible tourism

Any route/itinerary UX must visibly account for alcohol + driving:

- designated driver;
- driver/transfer partner;
- taxi;
- stay overnight;
- limited stop count;
- responsible-consumption text.

Do not optimize “maximum tastings per day”.

## 12. Product integrity

Content must visibly distinguish:

- VERIFIED FACT;
- WINERY-PROVIDED;
- EDITORIAL;
- USER PRIVATE DATA;
- SPONSORED.

Paid winery placement must never silently change organic recommendation rank.

## 13. Mobile decision

Responsive web/PWA is default. Native Flutter app becomes justified only if cohort evidence shows mobile-specific behaviors materially drive retention:

- repeated QR scanning;
- push re-engagement;
- offline itinerary;
- high Passport repeat frequency.

Until then, mobile app is cost without proof.
