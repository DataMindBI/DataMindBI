# Governance Framework

## Document Control

All controlled documents in this repository must use YAML front matter containing:

```yaml
document_id: unique-identifier
title: Document Title
version: X.Y
status: [proposed|draft|in_review|approved|implementation_ready|superseded|archived]
owner: Owner Name
reviewer: Reviewer Name(s)
approved_by: Approver Name
approved_date: YYYY-MM-DD
next_review: YYYY-MM-DD
supersedes: [document_id if applicable]
authoritative_path: path/to/document.md
```

## Document Status Lifecycle

| Status | Meaning | Authority |
|--------|---------|-----------|
| **proposed** | Initial draft awaiting review and approval | Author |
| **draft** | Under development, not yet ready for review | Author |
| **in_review** | Submitted for feedback; comments accepted | Reviewer |
| **approved** | Accepted and binding company guidance | Designated Approver (typically Kenny) |
| **implementation_ready** | Approved and ready for implementation repository consumption | PMO/Delivery Lead |
| **superseded** | Replaced by newer version; kept for historical reference | Governance Owner |
| **archived** | No longer applicable; retained per retention policy | Governance Owner |

## Approval Authority

- **Company strategy, brand, methodology, service architecture**: Kenny Bush, Principal
- **Product strategy and roadmaps**: Kenny Bush, Principal
- **Market and thought leadership**: Kenny Bush, Principal
- **Operations and standards**: Kenny Bush, Principal
- **Decisions** (ADRs): Kenny Bush, Principal (must be explicitly approved to become binding)

## Repository Boundaries

### This Repository (Company Architecture)
**Authoritative for:**
- Company strategy and vision
- Brand and messaging
- The DataMind Method
- Service architecture
- Client journey design
- Website strategy and page briefs
- Market credibility and thought leadership
- Product roadmap and strategy
- Operating standards
- Architecture and business decisions

**Authority flows outward** from this repository to implementation repositories.

### DataMind Forge (Delivery Governance)
**Authoritative for:**
- Execution governance and PMO
- EWOs (Engagement Work Orders)
- Standards enforcement and compliance
- Delivery evidence and reporting
- Project tracking and resource allocation

### Implementation Repositories
Examples: `datamind-website`, product repositories, accelerator repositories

**Consume approved requirements** from this repository but do not define company strategy.

**Cannot silently redefine** approved strategy without a decision record in this repository.

## Document Management Rules

1. **Single Authoritative Version**: Each document has one authoritative path. No `final-v2` or `backup` copies.
2. **Git History as Changelog**: Use Git commits to track revisions. Previous versions remain in history.
3. **No Silent Redefinition**: Changes to approved strategy require a formal review and update with new version number.
4. **Decision Requests**: When strategic authority or scope is unclear, create a decision request (ADR-draft) rather than guessing.
5. **No AI Attribution**: Do not list Claude or AI systems as document authors or co-authors.

## Decision Records (ADRs)

All architectural and strategic decisions are recorded in `/decisions/` using the template: `ADR-NNNN-decision-title.md`

- ADRs start as `proposed` (not binding)
- Kenny must explicitly approve an ADR for it to become binding
- Once approved, ADRs are the authoritative rationale behind company decisions
- Superseded ADRs remain in Git history

## Change Process

1. Create a feature branch for changes to this repository
2. Author/update documents with YAML front matter
3. Open a draft pull request with:
   - Clear summary of changes
   - List of affected documents
   - Links to supporting ADRs or strategy documents
   - Any assumptions or decisions needed from Kenny
4. Kenny reviews and approves
5. Merge to main

## Implementation Repository Consumption

Implementation repositories (e.g., datamind-website):
- Reference authoritative documents from this repository
- Use version-pinned links or Git commit references
- Request ADRs if they need to diverge from approved strategy
- Report implementation results back to this repository via decision updates

---

**Last Updated**: 2026-07-10  
**Governed By**: Kenny Bush, Principal
