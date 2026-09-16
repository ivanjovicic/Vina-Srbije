# Risks, Pre-Mortem, Kill Criteria & Pivot Tree

## 1. Pre-mortem: septembar 2029, projekat je propao

| # | Razlog | Probability | Impact | Early warning | Mitigation |
|---:|---|---|---|---|---|
| 1 | Google/direct workflow je dovoljno dobar | H | H | low action conversion | narrow to repeat/ROI |
| 2 | Vinarije neće da plaćaju | H | H | no paid pilot conversion | pay-per-result / pivot |
| 3 | Vinarije ne održavaju podatke | H | H | stale >20% | managed data/minimize fields |
| 4 | Passport se ne koristi drugi put | M-H | H | low 30/60d return | remove as core |
| 5 | Repeat purchase je ređi nego očekivano | M | H | low reorder click/order | booking/gifting pivot |
| 6 | Wine tourism frequency je preniska | M | H | weak retention | B2B/revenue-focused model |
| 7 | WineTourism/Viator uzmu booking | M | M-H | foreign users prefer OTA | partner/affiliate or local supply moat |
| 8 | Vivino proširi tourism | M | H | feature launch | offline supply/attribution moat |
| 9 | Local directories copy features | H | M | QR/booking added | focus proprietary behavior/ROI |
| 10 | SEO preskup/spor | M | H | no rankings after quality work | QR/partners/direct GTM |
| 11 | Consumer acquisition > LTV | M | H | paid CAC high | supplier-distributed acquisition |
| 12 | Winery onboarding preskup | H | H | >4h/profile persistent | narrower data, import/managed tools |
| 13 | Booking leakage/disintermediation | H | M | direct calls off-platform | ROI attribution, benefits, subscription |
| 14 | Payment model blokira marketplace | M | H | no PSP structure | stay lead/affiliate |
| 15 | Tourism law complicates bundling | M | H | counsel flags license | do single-service lead, partner agency |
| 16 | Shipping destroys commerce margin | H | H | multi-shipment high cost | no cart; affiliate/direct |
| 17 | Alcohol regulation/age logistics | M | H | courier cannot verify | merchant/courier partner only |
| 18 | Global wine demand weakens | M-H | M | falling premium demand | tourism/gifting diversified |
| 19 | Q4 gifting too seasonal | H | M | revenue concentration | treat as side business |
| 20 | Founder bandwidth consumed by sales/data | H | H | coding < bottleneck | outsource data/sales after proof |
| 21 | Users prefer social content vs utility | M | M | low search/save | content partnership or stop |
| 22 | Foreign tourists too few for direct model | M | M | low English conversion | domestic first / OTA affiliate |
| 23 | Winery trust/conflict over rankings | M | M | partner complaints | ranking integrity/sponsored labels |
| 24 | Content/image rights block rich profiles | M | M | no permission | partner-provided media |

## 2. Whole-project kill criteria

Strong recommendation to STOP/PIVOT if after 30–45 days:

- <5 of 20–30 qualified wineries commit to pilot;
- target problems are not top-3 pain for >=20% of segment;
- consumers show little planning/reorder friction;
- no credible path to measurable winery ROI.

After pilot, stop if:

- fewer than 3 wineries are willing to pay after demonstrated actions;
- QR Passport save rate is persistently <15%;
- repeat-purchase/booking actions are negligible;
- maintaining data requires unsustainable manual effort.

## 3. Feature kill criteria

### Taste Match

Kill advanced recommender if occasion/basic filters match or beat taste UX and users do not repeatedly engage with technical preference profile.

### Passport

Remove from core if staff-supported QR exposure yields <15% save or 60-day return is negligible.

### Booking

Do not build calendar/payment if request workflow has low conversion or winery response SLA is poor.

### Marketplace

Do not build if <50 monthly real purchase-intent actions, <10 willing sellers, or shipping/payment/legal model fails.

### Native mobile

Do not build if web/PWA satisfies scan/passport and push does not have clear retention case.

### Winery SaaS

Do not expand to POS/CRM if partners mainly want demand/revenue rather than software operations.

## 4. Pivot tree

### If consumer discovery fails but repeat purchase works

Pivot -> **Winery Guest Retention / QR DTC tool**.

Product becomes B2B-light:

visit -> QR -> saved wines -> consent -> winery follow-up/reorder analytics.

### If repeat purchase fails but booking works

Pivot -> **Serbia Winery Experience Booking/Lead Platform**, potentially partner with existing OTAs for foreign traffic.

### If tourism usage is weak but corporate demand strong

Pivot -> **Serbian Premium Corporate Gifting** with curated producer network.

### If consumer side weak but HORECA interviews reveal sourcing pain

Evaluate -> **B2B Serbian Wine Sourcing/Lead Platform**.

### If winery supply is willing but no payer

Do not keep building “for engagement”. Test sponsorship/TO partnership once; otherwise stop.

### If everything requires manual operations and margins are thin

DO NOT BUILD software platform. A service business may exist, but that is a separate choice.

## 5. Incumbent attack resilience

A durable strategy should survive:

- Vivino adds winery booking;
- local directory adds taste filters;
- WineTourism doubles Serbian supply;
- Google improves reservation links.

The defensible remainder should be:

**partner QR distribution + verified local operational data + offline attribution + visitor-to-repeat graph.**

If we fail to build those, moat remains weak.
