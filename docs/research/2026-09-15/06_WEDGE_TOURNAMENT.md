# Wedge Tournament

## 1. Metod

Ocene su **analitičke hipoteze**, ne empirijski rezultati. Svaki kriterijum je 1–10 gde je 10 povoljnije. Težine naglašavaju problem, diferencijaciju, willingness-to-pay, retention i moat.

Kriterijumi i težine:

- pain 10;
- frequency 6;
- differentiation 10;
- competitive advantage 8;
- willingness-to-pay 10;
- margin 7;
- acquisition 6;
- retention 8;
- capital efficiency 6;
- operational feasibility 7;
- regulatory feasibility 5;
- technical feasibility 5;
- moat 9;
- Serbia opportunity 6;
- regional scalability 5;
- solo-founder fit 7.

## 2. Rezultat

| Rang | Wedge | Weighted score /10 | Stav |
|---:|---|---:|---|
| 1 | Repeat-purchase bridge | 7.97 | VALIDATE FIRST |
| 2 | Winery lead generation | 7.79 | Strong monetization layer |
| 3 | Hybrid discover-visit-save-reorder | 7.66 | RECOMMENDED PRODUCT HYPOTHESIS |
| 4 | Wine Passport | 7.53 | Strong feature if behavior validates |
| 5 | Winery CRM/DTC-lite | 6.80 | Only with local-specific pain |
| 6 | HORECA discovery | 6.78 | Adjacent B2B test |
| 7 | Taste Match | 6.63 | Feature, not standalone business |
| 8 | Corporate gifting | 6.45 | Best parallel revenue experiment |
| 9 | Experience booking | 6.38 | Valuable but competitive/regulatory |
| 10 | Tourism discovery | 6.34 | Acquisition layer |
| 11 | Wine events | 6.30 | Retention/content layer |
| 12 | Wine discovery | 6.29 | Crowded |
| 13 | Export/importer discovery | 6.04 | Wine Vision pressure |
| 14 | Full marketplace | 5.97 | Too much early complexity |
| 15 | Smart routes | 5.71 | Useful, low moat |
| 16 | Directory/map | 5.55 | Do not build as core |
| 17 | Wine club | 5.44 | Logistics/churn/inventory |

## 2A. Reproducibility

Konačni score nije empirijska istina. Sirove ocene po kriterijumima nalaze se u repo fajlu:

`data/wedge_scores.csv`

Formula:

`weighted_score = SUM(score_i * weight_i) / SUM(weight_i)`

Budući agent mora menjati raw score i obrazložiti dokaz koji ga menja; ne sme ručno menjati samo konačni zbir. Score treba ponovo izračunati posle Phase 1 i Phase 3 validacije.

## 3. Zašto Repeat Purchase rangira #1

Acquire intent je već nastao fizičkom posetom. Korisnik je probao proizvod, a vinarija želi da monetizuje odnos i kasnije. To smanjuje discovery uncertainty i povezuje platformu sa merljivim revenue outcome-om.

Problem: repeat-purchase bridge sam nema acquisition engine. Zato je preporučeni product wedge širi hybrid:

> **verified experience discovery + Passport + repeat bridge**

Discovery dovodi gosta, a Passport/reorder pravi retention i B2B ROI.

## 4. Zašto lead generation i Corporate Gifting treba testirati paralelno

Winery lead generation po raw scoring modelu završava iznad hybrid wedge-a kao pojedinačni revenue mehanizam, ali nema isti consumer retention/discovery loop. Zato ga tretirati kao monetization layer unutar hybrid hipoteze, ne kao konačnu platformsku definiciju.

Corporate gifting potential advantages:

- veći order size;
- B2B payer;
- jasna lokalna priča;
- lak manual presale;
- može generisati prihod bez consumer app-a.

Risks:

- Q4 seasonality;
- packaging/fulfillment;
- procurement cycle;
- konkurencija gift kompanija/vinoteka;
- inventory coordination.

Preporuka: landing + 20 corporate outreach-a pre bilo kakvog dedicated software-a.

## 5. Zašto marketplace pada

Marketplace ima visok WTP/GMV potencijal, ali ga ruše:

- payments;
- multi-merchant money flow;
- alcohol age obligations;
- fulfillment;
- stock freshness;
- shipping cost;
- breakage;
- refunds;
- high operational burden.

Ne odbacuje se zauvek. Samo je **BLOCKED** dok ne postoji realan purchase intent i potvrđena ekonomika.

## 6. Zašto Taste Match nije business wedge

Može poboljšati discovery, ali:

- Vivino već dominira consumer taste/review graph-om;
- local structured taste data je skupo;
- korisnici možda bolje razumeju occasion/food/price nego tannin/body;
- bez transaction/retention layer-a teško monetizuje.

Preporuka: manual A/B test “taste attributes” vs “occasion” pre recommender razvoja.

## 7. Fund only one hypothesis for 90 days

Ako bih finansirao samo jedan 90-dnevni eksperiment:

> **5–10 vinarija + verified experience leads + QR Passport + 30–60 day reorder measurement.**

Success nije broj page views. Success je dokaz da platforma stvara atribuiranu winery action/revenue vrednost.
