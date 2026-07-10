---
document_id: DIR-DECISIONS
title: Decisions Directory
version: 0.1
status: approved
owner: Kenny Bush
reviewer: null
approved_by: Kenny Bush
approved_date: 2026-07-10
next_review: 2026-10-10
supersedes: null
authoritative_path: decisions/README.md
---

# decisions/

**Purpose**: Architecture Decision Records (ADRs). The authoritative record of all significant company and architectural decisions, including rationale and alternatives considered.

## What Belongs Here

- Architectural decisions (technology choices, repository boundaries, etc.)
- Strategic decisions (service offerings, market positioning, pricing)
- Organizational decisions (team structure, responsibilities, approval authority)
- Process decisions (how we work, governance, standards)
- Any decision that affects multiple teams or has lasting impact

## What Does NOT Belong Here

- ❌ Tactical decisions (single-project choices)
- ❌ Operational details (those go in 08-operations/)
- ❌ Strategy documents (those go in 01-company/)
- ❌ Service definitions (those go in 04-services/)
- ❌ Incident reports or troubleshooting

## Naming Convention

`ADR-NNNN-decision-title.md` where:
- `NNNN` is a zero-padded sequential number (0001, 0002, etc.)
- `decision-title` is a slug describing the decision (e.g., `company-repository-boundaries`)

**Examples**:
- ADR-0001-company-repository-boundaries.md
- ADR-0002-service-pricing-model.md
- ADR-0003-technology-stack.md

## Approval Authority

**Kenny Bush** — Principal

All ADRs start as `proposed` (not binding). Only after Kenny approves do they become authoritative company decisions.

## ADR Lifecycle

| Status | Meaning | Can be referenced by | Next step |
|--------|---------|----------------------|-----------|
| **proposed** | Initial draft awaiting review | Internal discussion | Reviewed by Kenny |
| **in_review** | Under consideration, comments open | Discussion | Approved or rejected |
| **approved** | Approved decision, now binding | All teams and repositories | Implementation |
| **superseded** | Replaced by newer ADR | Historical reference | Keep for audit trail |

## Creating an ADR

1. Identify a decision that needs to be recorded
2. Copy `/templates/decision-record-template.md`
3. Number sequentially (ADR-0001, ADR-0002, etc.)
4. Fill in YAML front matter with status `proposed`
5. Write clearly:
   - Context: Why this decision matters
   - Decision: The choice being made
   - Rationale: Why this is better than alternatives
   - Consequences: Impact of the decision
   - Alternatives considered: What we considered and rejected
6. Create feature branch
7. Open draft PR with decision record
8. Kenny reviews and approves

## Updating ADRs

ADRs can evolve:
1. Only update approved ADRs if new information emerges
2. Increment version number
3. Mark status as `in_review`
4. Document the change and new information
5. Get Kenny's approval
6. Supersede previous version if decision fundamentally changes

**Do not** delete ADRs — keep them in history for audit trail.

## Referencing ADRs

Other documents should reference related ADRs:
- Use YAML front matter field: `related_decisions: [ADR-0001, ADR-0002]`
- Link in Markdown: `See [ADR-0001](../decisions/ADR-0001-*.md) for the repository boundaries decision.`

Implementation repositories should:
- Link to supporting ADRs when implementing decisions
- Request new ADRs if they encounter missing decisions

---

## Current ADRs

| ADR | Title | Status | Approved Date |
|-----|-------|--------|----------------|
| [ADR-0001](./ADR-0001-company-repository-boundaries.md) | Company Repository Boundaries | **proposed** | Awaiting approval |

---

**Owner**: Kenny Bush  
**Last Updated**: 2026-07-10
