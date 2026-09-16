# Wine Serbia Validation Queue

Last aligned: 2026-09-16
Status: validation only — implementation remains blocked until gates pass.

| ID | Status | Task | Gate |
|---|---|---|---|
| WS-VAL-001 | READY | Winery pain + payer interviews | G1 |
| WS-VAL-002 | READY | Consumer workflow interviews | G2 |
| WS-VAL-003 | READY | Winery digital-maturity/data-maintenance audit | G1 |
| WS-VAL-004 | READY / TIME-SENSITIVE | Wine Vision 2026 field-research preparation + execution | G1 |
| WS-VAL-005 | BLOCKED | Manual concierge winery-day test | G1/G2 |
| WS-VAL-006 | BLOCKED | QR Wine Passport real tasting pilot | G1 |
| WS-VAL-007 | BLOCKED | 30/60-day repeat-purchase test | G3 |
| WS-VAL-008 | BLOCKED | Paid winery conversion test | G4 |

Canonical Wine Vision milestone:
`docs/research/WINE_VISION_VALIDATION_MILESTONE_2026_10.md`

## Selection rule

Until Wine Vision 2026 (10–12 October), prioritize WS-VAL-001/003/004 because the concentrated winery-access window is time-limited.

WS-VAL-002 can run in parallel.

Do not build production functionality for the event.

## WS-VAL-001 — Winery pain + payer interviews

**Goal:** determine whether acquisition, booking or repeat-purchase is a top commercial pain and whether a measurable pilot is acceptable.

**Scope:** 20–30 qualified tourism-ready Serbian wineries, segmented by region and digital maturity.

For each interview capture:
- recent real example of visitor acquisition / tasting / post-visit follow-up;
- current workflow and tools;
- post-visit relationship owner;
- direct-sale/reorder path;
- frequency/severity of the problem;
- current workaround;
- measurable outcome that matters;
- buyer/payer role;
- pilot willingness;
- concrete next step.

**Output:**
- anonymized interview evidence table;
- pain-frequency ranking;
- current workflow map;
- payer/willingness evidence;
- pilot commitments;
- objections;
- recommended gate decision.

**Do not:** infer willingness-to-pay from “interesting”; count free-listing interest as product demand; build product code.

**Pass candidate:** >=5 credible pilot commitments plus repeated unprompted pain.

## WS-VAL-002 — Consumer workflow interviews

**Goal:** validate discovery/booking and post-tasting memory/reorder friction.

**Scope:** at least 15 domestic + 10 foreign/recent-tourist relevant interviews.

Focus on actual prior behavior:
- last winery visit;
- how they remembered wines;
- whether exact wine/vintage was later forgotten;
- whether they tried to reorder/contact/visit again;
- what blocked them;
- whether a QR/save action at tasting would have had immediate value.

**Output:** current journey, alternatives, failure points, frequency, actual past purchases/visits, account/QR willingness, G2 recommendation.

## WS-VAL-003 — Winery digital-maturity audit

**Goal:** quantify how much supply is actually serviceable and who can maintain dynamic data.

**Sample:** 30–50 wineries across pilot clusters and digital-maturity bands.

**Fields:** web, English, Google, social, tasting, price, booking, restaurant, stay, shop, current vintages, update owner, response time, direct-sales/reorder channel, CRM/wine club if any.

**Output:** scored dataset + recommended pilot segment; no unsupported nationwide extrapolation.

Explicitly separate:
- registered winery universe;
- tourism-ready winery;
- digitally maintainable winery;
- pilot-ready winery;
- plausible paying winery.

## WS-VAL-004 — Wine Vision 2026 field-research preparation + execution

**Goal:** turn Wine Vision into structured validation, not networking.

**Dates:** 10–12 October 2026.

### Before event

- shortlist target wineries by tasting traffic, direct-sales maturity and digital readiness;
- contact at least 15 in advance where practical;
- prepare 10-minute interview script;
- prepare one QR Wine Passport mock / pilot proposition;
- prepare pilot commitment form;
- prepare daily evidence sheet and synthesis template;
- schedule interviews/meeting windows when possible.

### During event

Target across the event:
- 20–30 qualified winery interviews minimum;
- >=5 credible QR/Post-Visit pilot commitments;
- buyer/tourism/distributor conversations only where they clarify payer/distribution economics.

A credible pilot requires:
- named owner/contact;
- concrete winery/test context;
- approximate timing;
- willingness to expose QR/workflow to real guests;
- permission to measure scan/save/follow-up behavior;
- post-pilot review commitment.

Do not count:
- compliments;
- generic "interesting";
- free directory/listing interest;
- business cards with no next step.

### Daily synthesis

At the end of each event day record:
- repeated unprompted pains;
- current workarounds;
- pilot commitments;
- objections;
- staff/QR adoption concerns;
- reorder/contact maturity;
- reasons to kill/narrow the current wedge.

### Post-event gate decision

PASS candidate:
- >=5 credible pilots;
- repeated post-visit relationship/reorder pain;
- willingness to measure business outcomes;
- named winery owners for the workflow.

FAIL/NARROW signal:
- <5 credible pilots after 20–30 good conversations;
- wineries mainly want publicity/listing;
- no staff owner for QR exposure;
- no practical reorder/contact path;
- current wedge is not among the top commercial pains.

If weak, do not build a broader directory/marketplace as a rescue.

## WS-VAL-005 — Manual concierge winery-day test

Blocked until sufficient G1/G2 evidence.

No route engine. Manually serve real users and measure accepted plan -> contact/request -> visit.

Use only if discovery/visit-planning emerges as a meaningful validated pain; do not let it displace the stronger post-visit thesis without evidence.

## WS-VAL-006 — QR Passport pilot

Blocked until partner wineries agree.

Mobile web only. Track:
- exposed guests denominator;
- scans;
- saved exact wine/vintage;
- consent;
- return.

Denominator rule:
count guests with a real visible/staff-supported opportunity to use the QR, not all winery visitors.

## WS-VAL-007 — Repeat-purchase test

Blocked until QR cohort exists.

Use consented follow-up; track:
- reorder/contact action;
- revisit action where relevant;
- confirmed purchase/serious inquiry where winery can report it;
- attributable vs already-existing customer behavior where practical.

Measure 30/60-day behavior before claiming repeat-purchase value.

## WS-VAL-008 — Paid conversion

Blocked until attributable value exists.

Offer a real subscription/action-fee/hybrid price.

A pass requires concrete commercial evidence such as:
- paid pilot;
- invoice-ready commitment;
- signed/confirmed paid continuation;
- equivalent procurement next step.

“Would pay” is not a pass; actual paid commitment is.
