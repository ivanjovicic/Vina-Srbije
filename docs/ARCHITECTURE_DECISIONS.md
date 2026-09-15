# Architecture Decision Log — Provisional

These decisions are conditional on build authorization. They prevent speculative complexity during validation.

## ADR-001 — Web before native mobile

**Status:** Accepted provisional  
**Decision:** responsive SEO-first web/PWA is the first production surface.  
**Trigger to revisit:** G8.

## ADR-002 — Modular monolith by default

**Status:** Accepted provisional  
**Decision:** .NET 10 / ASP.NET Core modular monolith + PostgreSQL.  
**Why:** product boundaries and load are unproven; distributed systems would add operational cost without evidence.

## ADR-003 — Provenance and freshness are domain concerns

**Status:** Accepted provisional  
**Decision:** business data that can become stale must carry source/verification/freshness metadata where relevant.

## ADR-004 — AI may propose, not establish facts

**Status:** Accepted  
**Decision:** AI extraction produces candidates with provenance/confidence; it may not publish price, availability, award, taste property or legal classification as verified fact without an approved source/workflow.

## ADR-005 — No full marketplace payment architecture before G7

**Status:** Accepted  
**Decision:** initial booking/reorder flow is link/request/lead based. Payment design follows named provider + legal/accounting confirmation.

## ADR-006 — Search starts in PostgreSQL

**Status:** Accepted provisional  
**Decision:** relational filters + trigram/full-text first.  
**Trigger:** measured search quality/performance limitation.

## ADR-007 — Route logic is deterministic

**Status:** Accepted provisional  
**Decision:** actual distances, hours, appointments and travel constraints use geospatial/routing systems; LLM may explain but not calculate the authoritative route.

## ADR-008 — No consumer review network in MVP

**Status:** Accepted provisional  
**Decision:** avoid moderation/fake-review burden until research proves reviews solve a material trust problem not already addressed by verified data.
