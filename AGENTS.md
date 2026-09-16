# AGENTS.md — Wine Serbia

## Mission

Find and validate a profitable, defensible problem in Serbian wine/wine-tourism before building a broad product.

## Current product decision

**Status: VALIDATE BEFORE BUILDING**

Current leading hypothesis:

`verified winery experience -> Wine Passport -> repeat purchase -> measurable winery ROI`

This is a hypothesis, not an implementation authorization.

## Source of truth order

1. `docs/DECISION_LOG.md`
2. `docs/VALIDATION_GATES.md`
3. `docs/ROADMAP.md`
4. `docs/PRODUCT_SPEC.md`
5. `docs/research/2026-09-15/00_EXECUTIVE_DECISION.md`
6. current prompt queue
7. supporting research docs

When documents conflict, stop and record the conflict. Do not silently choose the most convenient interpretation.

## Evidence discipline

All market/legal/current-product claims must be one of:

- FACT
- ESTIMATE
- ASSUMPTION
- HYPOTHESIS
- UNKNOWN

Current facts must have a source and access date.

Never turn a draft law, vendor claim, directory count, or global trend into a Serbia-specific fact without qualification.

## Work that is allowed now

- interviews/research;
- source verification;
- structured data sampling;
- landing/prototype/Figma-level validation;
- manual concierge tests;
- QR Passport pilot;
- analytics for validation;
- scripts that support research/data QA without creating production product scope.

## Work blocked now

Until relevant gates pass, do not implement:

- marketplace checkout;
- split payouts/wallet/escrow;
- multi-winery cart;
- fulfillment;
- native Flutter app;
- advanced ML/recommender;
- social feed;
- public review system;
- microservices/Kubernetes;
- full winery CRM/POS;
- regional alcohol commerce.

## Engineering principles after build authorization

Default:

- .NET 10 / ASP.NET Core
- PostgreSQL
- modular monolith
- SEO-first web
- React + TypeScript
- simple deployment
- provenance/freshness built into data model
- deterministic systems before AI
- no infrastructure component without a measured need

## Validation honesty

Do not say an experiment passed unless real observations satisfy its written threshold.

Do not replace real user/winery evidence with synthetic agent analysis.

## Current next work

Use `docs/prompt_queues/validation.md`.

Implementation prompts remain blocked until the corresponding validation gate is explicitly marked Passed in `docs/VALIDATION_GATES.md`.
