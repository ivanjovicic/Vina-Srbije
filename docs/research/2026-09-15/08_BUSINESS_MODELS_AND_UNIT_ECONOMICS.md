# Business Models & Unit Economics

## 1. Principles

Every number below is a **scenario**, not a forecast. Serbian willingness-to-pay and conversion are largely UNKNOWN. The purpose is to expose what must be true.

## 2. Business model ranking

| Model | Payer | Margin potential | Operational load | Near-term fit | Recommendation |
|---|---|---:|---:|---:|---|
| Qualified lead / booking fee | Winery | high | low-medium | high | TEST FIRST |
| Winery subscription | Winery | high | low | medium | after ROI proof |
| Booking commission | Winery/customer | high | medium | medium-high | after request-booking proof |
| Repeat-purchase attribution fee | Winery | high | low-medium | high | TEST FIRST |
| Sponsored discovery | Winery | high | low | medium | later; strict labeling |
| Affiliate/direct commerce | Merchant | high | low | medium | good bridge |
| Full marketplace commission | Winery | medium | high | low | BLOCKED |
| Corporate gifting | Company | medium | medium-high | high experiment | MANUAL TEST |
| Wine club | Consumer | medium | high | low | LATER/DROP unless demand |
| HORECA/export leads | Business | high | medium | unknown | adjacent validation |

## 3. Subscription economics

Potential local pricing hypothesis after ROI proof:

- Free verified profile;
- Pro: €19–39/month;
- Growth: €49–79/month only if analytics/lead volume supports it.

Benchmark warning: global DTC platforms charge more, but include far more functionality and operate in wealthier winery markets. Commerce7 starts at $59/month in its Lite plan (US/Canada), while WineDirect starts at $79/month + transaction fee. [S12][S13]

### Supply ceiling thought experiment

If 120 wineries pay €39:

`120 × €39 = €4,680 MRR`

If 150 pay €49:

`150 × €49 = €7,350 MRR`

This shows why **subscription alone is not sufficient** for ambitious Serbia-only economics.

## 4. Booking economics

Current Serbia experiences on WineTourism indicate roughly €9–€65+ per person. [S05]

### Base scenario assumption

- €30 / person;
- 2.2 guests / booking;
- booking GMV €66;
- 12% platform take (hypothesis, below major marketplace benchmark);
- revenue = €7.92/booking before costs.

At 400 monthly bookings:

`400 × €7.92 = €3,168 MRR`

At 1,000 bookings:

`1,000 × €7.92 = €7,920 MRR`

This is useful, but demands meaningful volume. Booking is therefore stronger as part of a combined model.

## 5. Lead-fee model

Simpler pilot model:

- free listing;
- winery pays only for confirmed qualified action;
- example hypothesis €3–10/confirmed booking lead depending on party/value;
- or monthly cap/subscription.

Advantage: easier to explain ROI and avoids money-holding complexity.

Risk: attribution/disintermediation.

## 6. Repeat-purchase economics

Possible models to validate:

### Affiliate/deep-link

Winery/merchant pays commission if trackable.

### Attributed-order fee

Fixed fee or % of confirmed order.

### Subscription value

Repeat-purchase analytics/CRM-lite bundled in winery plan.

No chosen model should be implemented until real post-tasting reorder rate is measured.

## 7. Corporate gifting

### Manual base scenario

Assumptions:

- 20 corporate orders in season;
- €600 average order;
- 20% contribution margin after product/packaging but before sales labor.

`20 × €600 × 20% = €2,400 contribution per season`

At 100 orders × €1,000 × 20% = €20k seasonal contribution.

Attractive as cash generator, but not recurring monthly SaaS and requires operations.

## 8. Full marketplace economics

Formula:

`Contribution = GMV × take rate - payment fees - shipping subsidy - refunds - breakage - support - discounts - fraud`

### Multi-winery example

Customer buys 6 bottles from 3 wineries. If each ships separately, 3 shipping charges can erase convenience/value. Platform subsidizing them can erase margin. Consolidation requires inventory/hub/handling and creates a different company.

Therefore “one cart across wineries” is not an MVP feature; it is a later logistics thesis.

## 9. Scenario model — total revenue

### Conservative early business

- 20 paying wineries × €25 = €500;
- 50 monthly qualified paid actions × €5 = €250;
- occasional sponsored/affiliate = €100;

**~€850 MRR equivalent**.

### Base strong Serbia

- 120 paying wineries × €39 = €4,680;
- 400 monthly bookings/actions with ~€7.9 revenue = €3,168;
- B2B/sponsor/affiliate contribution = €1,000–2,000;

**~€8,800–9,800 MRR.**

### Upside Serbia

- 180 wineries × €49 = €8,820;
- 1,000 monthly booking events × €7.9 = €7,900;
- corporate gifting/lead/affiliate contribution averaged through year €5–10k;

**~€22k–27k monthly equivalent.**

This upside already assumes excellent penetration and substantial transaction volume. It demonstrates why **€50k MRR Serbia-only is not base-case plausible**.

## 10. What €50k MRR probably requires

At least one:

- regional supply/demand expansion;
- much larger commerce GMV;
- high-value B2B corporate gifting/distribution;
- more valuable winery software beyond tourism;
- export/HORECA business with validated economics.

## 11. Sensitivity analysis

Booking model is especially sensitive to:

1. booking volume;
2. average party size;
3. take rate;
4. acquisition cost;
5. supplier retention.

If conversion or booking volume is 50% below base, transaction revenue halves immediately. SaaS can stabilize revenue, but only if winery ROI is visible.

### Numeric booking sensitivity

Base formula:

`Revenue = Monthly bookings × Average guests × Price/person × Take rate`

Using base assumptions 2.2 guests, €30/person, 12% take:

| Monthly bookings | Revenue |
|---:|---:|
| 200 (-50%) | €1,584 |
| 400 (base) | €3,168 |
| 600 (+50%) | €4,752 |

At 400 bookings:

| Variable | Low | Base | High |
|---|---:|---:|---:|
| Price/person | €20 -> €2,112 revenue | €30 -> €3,168 | €45 -> €4,752 |
| Take rate | 8% -> €2,112 | 12% -> €3,168 | 18% -> €4,752 |
| Guests/booking | 1.6 -> €2,304 | 2.2 -> €3,168 | 3.0 -> €4,320 |

Ovo pokazuje da transaction model nema mnogo prostora za skupu plaćenu akviziciju ili intenzivnu ljudsku podršku dok booking volume/AOV nisu dokazani.

## 12. Winery CAC / LTV

Measure, do not assume.

`CAC = sales hours × loaded hourly cost + research + onboarding + travel + data entry`

`LTV = monthly gross contribution × average paid months`

Target bootstrap discipline: recover winery acquisition/onboarding cost within ~6 months; if not, refine segment/price/onboarding before scaling sales.

## 13. Consumer CAC

Do not buy traffic before organic/partner conversion is understood. Test:

- winery QR;
- SEO landing pages;
- Wine Vision/events;
- hotel/tourism partners;
- micro-creators.

Paid ads become meaningful only when value per qualified session is measured.

## 14. Business conclusion

Most plausible economic architecture:

**free discovery -> attributable winery actions -> subscription/lead fee -> later booking transaction -> affiliate/reorder -> optional corporate gifting.**

Marketplace is not required for a profitable first business.

## 15. Reproducible scenario data

Repo sadrži `data/unit_economics_scenarios.csv` sa formulama/pretpostavkama koje treba ažurirati realnim pilot podacima.
