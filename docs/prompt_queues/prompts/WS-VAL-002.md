# WS-VAL-002 — Consumer Workflow Audit

**Status:** READY  
**Gate:** G2

## Global rules

- Read `AGENTS.md`, `docs/VALIDATION_GATES.md`, `docs/DECISION_LOG.md`, and relevant research before starting.
- This is validation work, not product implementation.
- Use FACT / ESTIMATE / ASSUMPTION / HYPOTHESIS / UNKNOWN.
- Current claims require source + access date.
- Do not fabricate interview data, willingness-to-pay, bookings, conversion, or user behavior.
- If real-world evidence is unavailable, produce the research instrument/work package and mark execution as pending.
- Create/update a run log under `.ai/runs/`.

## Objective

Validate real past behavior around:
1. winery discovery/visit planning;
2. confirmation/booking friction;
3. safe transport;
4. remembering exact wines/vintages;
5. later reorder behavior.

## Sample

Target >=25 relevant interviews:
- >=15 domestic visitors;
- >=10 foreign/recent-tourist users or credible proxies.

## Method

Ask about the last real trip/purchase, not hypothetical interest.
Capture:
- sources used;
- time/steps;
- calls/messages;
- failure points;
- spend;
- wines remembered;
- reorder attempt/outcome;
- what would justify account/email/QR usage.

## Outputs

- `docs/validation/WS-VAL-002_CONSUMER_WORKFLOWS.md`
- journey maps;
- friction frequencies;
- substitute satisfaction;
- G2 recommendation.

## Pass candidate

Evidence of a repeated material workflow problem plus concierge/action behavior; not survey enthusiasm.
