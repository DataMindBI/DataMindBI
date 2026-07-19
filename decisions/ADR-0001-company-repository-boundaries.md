---
document_id: ADR-0001
title: Company Repository Boundaries and Authority
version: 0.1
status: proposed
owner: Claude (Foundation Setup)
reviewer: Kenny Bush
approved_by: null
approved_date: null
next_review: null
supersedes: null
authoritative_path: decisions/ADR-0001-company-repository-boundaries.md
---

# ADR-0001: Company Repository Boundaries and Authority

## Status
**PROPOSED** — This decision record awaits explicit approval from Kenny Bush. Only after approval does it become binding company policy.

---

## Context

DataMind operates multiple repositories serving different governance functions:

1. **This repository (DataMind BI)** — Business architecture and strategy
2. **DataMind Forge** — Project management and execution governance
3. **Implementation repositories** — Code and product delivery (datamind-website, product repos, etc.)

Without clear boundaries, authority becomes ambiguous: unclear who is responsible for what, whether strategy can be silently redefined, and how implementation repositories relate to company strategy.

This decision establishes:
- What each repository is authoritative for
- How strategy flows from company architecture to implementation
- What constraints protect approved strategy from being overridden
- How missing decisions are handled

---

## Decision

### This Repository (DataMind BI) is Authoritative For:
1. **Company strategy and vision** — Strategic blueprint, market positioning, value propositions
2. **Brand and messaging** — Brand guidelines, tone, messaging frameworks, visual identity
3. **The DataMind Method** — Repeatable service delivery methodology and quality standards
4. **Service architecture** — Service definitions, service tiers, delivery models
5. **Client journey design** — Client engagement flow, success criteria, relationship architecture
6. **Website strategy and page briefs** — Website positioning, page outlines, content strategy
7. **Market credibility and thought leadership** — Publication strategy, competitive differentiation
8. **Product roadmap and strategy** — Product vision, feature prioritization, market approach
9. **Operating standards** — How we work, what we value, governance standards
10. **Architecture and business decisions** — ADRs documenting why major decisions were made

### DataMind Forge is Authoritative For:
1. **Execution governance and PMO** — Project tracking, resource allocation, delivery sequencing
2. **EWOs (Engagement Work Orders)** — Client contracts, statement of work details
3. **Standards enforcement and compliance** — Checking that work follows company operating standards
4. **Delivery evidence and reporting** — Results, metrics, evidence of delivery quality

### Implementation Repositories (e.g., datamind-website) are Responsible For:
1. **Consuming** approved strategy and requirements from this repository
2. **Implementing** those requirements using version-pinned references or Git commit links
3. **Requesting new ADRs** if they discover a strategic decision gap
4. **Reporting results back** to this repository via updates to related ADRs

### Key Constraint: No Silent Redefinition
- Implementation repositories **cannot silently diverge** from approved strategy.
- If an implementation repository discovers that approved strategy is incomplete, misguided, or needs change, they must:
  1. Request an ADR in this repository
  2. Wait for approval before proceeding with the divergence
  3. Once approved, update the relevant strategy document in this repository

### How Decisions Flow
```
Company Architecture (this repo)
    ↓ (approved requirements flow outward)
    ├→ DataMind Forge (execution governance consumes and enforces)
    └→ Implementation Repositories (consume and implement)
         ↑ (decision requests flow back)
         └→ This repo (ADRs approved here before implementation changes)
```

### Handling Missing Decisions
When a strategic decision is needed but not yet made:
- **Do not invent strategy or guess.**
- **Create a decision request** (ADR-draft) in this repository.
- **Escalate to Kenny** for decision.
- **Do not proceed** with implementation until the decision is approved.

---

## Rationale

### Why This Matters
- **Consistency**: Company strategy cannot be rewritten by individual implementation projects.
- **Accountability**: Everyone knows who is responsible for what.
- **Scalability**: As DataMind grows, clear boundaries prevent chaos.
- **Audibility**: Strategic decisions are recorded and approvals are traceable.
- **Protection**: Approved strategy is preserved from silent erosion by implementation changes.

### Why This Design
- **Separation of concerns**: Strategy (this repo) is distinct from execution (Forge) from implementation (product repos).
- **Authority clarity**: Kenny approves company strategy. PMO enforces it. Implementation repositories follow it.
- **Escalation path**: When implementation discovers a gap, a clear decision process handles it.
- **Traceability**: Every strategic decision is an ADR with approval timestamp and rationale.

### Trade-offs
- **Adds process**: Requires creating ADRs instead of "just implementing."
  - *Benefit*: Company doesn't inadvertently change strategy without realizing it.
- **Slows some decisions**: Must route through this repository.
  - *Benefit*: Ensures Kenny sees all strategic changes.
- **Requires discipline**: Everyone must resist the urge to "just fix it locally."
  - *Benefit*: Preserves company coherence as the team grows.

---

## Consequences

### Immediate
- This repository becomes the authoritative source for all company strategy.
- All ADRs in `/decisions/` become company decision records.
- Implementation repositories reference this repository for approved guidance.

### For DataMind Forge
- Becomes the enforcement layer, checking that work aligns with approved strategy.
- Escalates strategic gaps back to this repository via decision requests.

### For Implementation Repositories
- Must reference approved documents from this repository.
- Cannot diverge from approved strategy without ADR approval.
- Report results and findings back to strategy documents.

### Process Impact
- Adds governance overhead: More formality, more approvals, clearer paper trail.
- Reduces rework: Strategy doesn't change mid-implementation without being noticed.
- Enables scaling: As team grows, clarity about authority prevents coordination chaos.

---

## Alternatives Considered

### Alternative 1: Fully Distributed Strategy
**Approach**: Let each implementation repository define its own strategy.  
**Why rejected**: Leads to inconsistency, silent redefinition, and uncoordinated company messaging. Not scalable.

### Alternative 2: Forge as Single Source of Truth
**Approach**: Consolidate all strategy into DataMind Forge.  
**Why rejected**: Forge is a project-management tool, not a strategy document store. Mixes execution tracking with strategic reasoning.

### Alternative 3: No Formal Decision Records
**Approach**: Make decisions ad-hoc without ADRs.  
**Why rejected**: Loses institutional memory, makes it unclear why decisions were made, enables decisions to be accidentally reversed.

---

## Related Decisions
None yet — this is the foundational decision record.

## Dependent Decisions
- **All future ADRs** depend on this decision for their authority.
- **All directory README files** in this repository reference this ADR.
- **CLAUDE.md** (session instructions) enforces this boundary.

---

## Approval

- **Proposed by**: Foundation setup (Claude session, 2026-07-10)
- **Awaiting review by**: Kenny Bush
- **Status**: **PROPOSED** (not yet binding)

---

## Implementation Notes
*(Only fill in after Kenny approves this ADR)*

When approved, implementation steps:
1. Make this ADR binding by changing status to `approved`
2. Update all directory README files to reference ADR-0001
3. Brief implementation repository owners on the decision
4. Establish decision-request process in DataMind Forge

---

## Revision History
| Version | Date | Author | Change |
|---------|------|--------|--------|
| 0.1 | 2026-07-10 | Claude (Foundation) | Initial proposal based on specified governance model |

---

**Current Status**: PROPOSED  
**Not yet binding** — Awaiting Kenny Bush approval
