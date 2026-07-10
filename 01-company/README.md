---
document_id: DIR-COMPANY
title: Company Directory
version: 0.1
status: approved
owner: Kenny Bush
reviewer: null
approved_by: Kenny Bush
approved_date: 2026-07-10
next_review: 2026-10-10
supersedes: null
authoritative_path: 01-company/README.md
---

# 01-company/

**Purpose**: Company strategy, vision, market positioning, and strategic blueprint. The authoritative source for "who we are and where we're going."

## What Belongs Here

- Strategic blueprint (long-term vision and market positioning)
- Company mission, vision, values
- 5-year and annual strategic plans
- Market analysis and competitive positioning
- Growth strategy
- Investment and resource allocation strategy
- Key milestones and success metrics
- Strategic initiatives and major projects

## What Does NOT Belong Here

- ❌ Brand guidelines or visual identity (see 02-brand/)
- ❌ Service definitions (see 04-services/)
- ❌ Product roadmaps (see 07-products/)
- ❌ Methodology (see 03-methodology/)
- ❌ Website content (see 05-website/)
- ❌ Marketing or thought leadership (see 06-market/)
- ❌ Operational processes (see 08-operations/)

## What Documents Are Here

### strategic-blueprint.md
The definitive strategic direction for DataMind. Updated annually or when major strategic shifts occur.

**Current Status**: See [STATUS.md](../STATUS.md)

## Approval Authority

**Kenny Bush** — Principal  
All strategic documents require Kenny's explicit approval.

## Document Format

All documents use YAML front matter:
- `document_id` — Unique identifier (e.g., STRATEGY-001)
- `version` — Semantic versioning (0.1, 0.2, 1.0, etc.)
- `status` — proposed, draft, in_review, approved, superseded
- `owner` — Document owner
- `reviewer` — Who reviewed it
- `approved_by` — Kenny Bush (or null if pending)
- `approved_date` — Approval timestamp

See `/templates/document-template.md` for structure.

## Creating New Strategic Documents

1. Use `/templates/document-template.md` as starting point
2. Fill in YAML front matter completely
3. Mark status as `draft`
4. Create feature branch (`feature/strategic-initiative-name`)
5. Open draft PR with:
   - Clear business case
   - How this supports DataMind's mission
   - Links to any related decisions (ADRs)
   - Success metrics
6. Kenny reviews and approves

## Updating Approved Strategy

- Increment version number (e.g., 0.1 → 0.2)
- Mark status as `in_review`
- Document changes in Git commit
- Open draft PR with detailed justification
- Get Kenny's explicit approval before merging

## Related Decisions

See `/decisions/` for ADRs related to company strategy:
- [ADR-0001](../decisions/ADR-0001-company-repository-boundaries.md) — Repository boundaries

## Relationship to Implementation Repositories

Implementation repositories should reference approved company strategy when:
- Making major architectural decisions
- Prioritizing features or initiatives
- Communicating company positioning
- Setting roadmaps

Request an ADR if implementation discovers missing or conflicting strategy.

---

**Owner**: Kenny Bush  
**Last Updated**: 2026-07-10
