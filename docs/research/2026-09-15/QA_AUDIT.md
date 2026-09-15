# Due Diligence QA Audit — 2026-09-15

## Verdict

The original due-diligence pack was directionally strong and its main recommendation remains valid:

**VALIDATE BEFORE BUILDING**

However, it was not fully complete against the master prompt. This repo-ready revision closes the most material gaps.

## Material corrections made

1. **Current winery count:** replaced reliance on a 2023 ~450-producer figure with the May 2026 government statement of **529 registered wineries**, while explicitly separating registry count from consumer-visible and tourism-ready supply.
2. **Competitive landscape:** added Winalist, CellarPass and Tock as important booking/hospitality/DTC benchmarks.
3. **Macro risks:** added climate/supply volatility, moderation/no-low and younger-consumer behavior as strategic context; explicitly marked global evidence as non-Serbia-specific.
4. **Wine-law transition:** added the 2026 draft/public-consultation status and a guardrail not to treat proposed 2027/2028 dates as enacted law.
5. **Payment due diligence:** expanded provider checklist beyond “Stripe availability” to Serbian acquiring, IPS, wallets, refunds, recurring/tokenization and multi-merchant capability.
6. **Wedge scoring:** added reproducible raw data in `data/wedge_scores.csv`.
7. **Unit economics:** added numeric sensitivity tables and a reproducible scenario CSV.
8. **Founder decision:** added the required `IF THIS WERE MY MONEY` section.
9. **Repo governance:** added canonical product/roadmap/decision/gate docs and validation-only agent queue.

## Remaining blocking unknowns

These are not document defects; they require real-world evidence:

- current reusable access/API/export rights for official wine registry data;
- actual winery booking/repeat-purchase pain prevalence;
- real QR save and 30/60-day repeat behavior;
- winery willingness-to-pay after attributable ROI;
- named Serbian PSP/acquirer support for future transaction structures;
- lawyer/accountant confirmation for specific booking/payment/commerce flows;
- courier alcohol/age/breakage operational terms;
- Serbia-specific consumer wine/no-low trend data;
- real winery-tourism visit volume.

## Quality standard

Any future agent must preserve the distinction between:

- FACT
- ESTIMATE
- ASSUMPTION
- HYPOTHESIS
- UNKNOWN

and must not promote blocked commerce/mobile/ML work merely because it appears in long-term architecture.
