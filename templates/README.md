---
document_id: DIR-TEMPLATES
title: Templates Directory
version: 0.1
status: approved
owner: Kenny Bush
reviewer: null
approved_by: Kenny Bush
approved_date: 2026-07-10
next_review: 2026-10-10
supersedes: null
authoritative_path: templates/README.md
---

# templates/

**Purpose**: Standard document templates for consistent structure and YAML front matter across the repository.

## Available Templates

### document-template.md
**Use for**: Policies, standards, guidance, brand guidelines, service definitions, anything that isn't a decision, initiative, or review.

**Contains**:
- YAML front matter structure
- Section headers for typical document content
- Approval and revision history tracking

**When to use**:
- Governance policies
- Brand guidelines
- Service definitions
- Methodology documents
- Operating standards
- General guidance

### decision-record-template.md
**Use for**: Architecture Decision Records (ADRs) documenting significant company or technical decisions.

**Contains**:
- YAML front matter for ADRs
- Context section (why this decision matters)
- Decision section (the choice)
- Rationale section (why it's better than alternatives)
- Consequences section (impact)
- Alternatives considered section
- Approval tracking

**When to use**:
- Any strategic decision (service offerings, pricing, market positioning)
- Architectural decisions (technology stack, repository boundaries)
- Organizational decisions (team structure, approval authority)
- Process decisions (how we work, governance)

### initiative-template.md
**Use for**: Initiatives, projects, and major efforts with specific timelines and deliverables.

**Contains**:
- YAML front matter
- Business case (problem, opportunity, success metrics)
- Scope (what's included, excluded, dependencies)
- Timeline with phases and owners
- Resources required
- Risks and mitigations
- Implementation notes

**When to use**:
- New product or accelerator initiatives
- Major company projects
- Market initiatives or campaigns
- Technology platform shifts

### review-template.md
**Use for**: Periodic reviews (quarterly, annual) of strategy, products, market position, performance.

**Contains**:
- Executive summary
- Key findings with status (on track, at risk, blocked)
- Metrics and performance data
- Decisions needed
- Recommendations
- Escalation items
- Next steps

**When to use**:
- Quarterly or annual strategy reviews
- Product performance reviews
- Market position reviews
- Initiative check-ins

---

## How to Use Templates

1. **Choose the right template** for your document type (see guidance above)
2. **Copy the template file**:
   ```bash
   cp templates/document-template.md 01-company/my-new-document.md
   ```
3. **Fill in YAML front matter**:
   - `document_id`: Unique ID (e.g., STRAT-001, ADR-0002, PB-001)
   - `title`: Document name
   - `version`: Start with 0.1
   - `status`: Start with `draft` or `proposed`
   - `owner`: Who owns this document
   - `reviewer`: Who should review it
   - `approved_by`: Leave null until approved
   - `approved_date`: Leave null until approved
   - `next_review`: When should this be reviewed again
   - `authoritative_path`: Where the document lives

4. **Write your content** in the sections provided

5. **Respect the template structure** — templates are designed for consistency across the repository

6. **Do not skip YAML front matter** — it's required for all controlled documents

---

## Document ID Conventions

Choose an ID based on document type and directory:

| Directory | ID Pattern | Example |
|-----------|-----------|---------|
| 01-company/ | STRAT-XXX | STRAT-001 |
| 02-brand/ | BRAND-XXX | BRAND-001 |
| 03-methodology/ | METHOD-XXX | METHOD-001 |
| 04-services/ | SRVDEF-XXX | SRVDEF-001 |
| 05-website/ | WEB-XXX or PB-XXX | WEB-001 or PB-001 (page brief) |
| 06-market/ | MARKET-XXX | MARKET-001 |
| 07-products/ | PROD-XXX | PROD-001 |
| 08-operations/ | OPS-XXX | OPS-001 |
| decisions/ | ADR-NNNN | ADR-0001 |

---

## YAML Front Matter Reference

```yaml
---
document_id: UNIQUE-ID     # Required: Use ID convention above
title: Document Title      # Required: Clear, descriptive title
version: 0.1              # Required: Semantic version (0.1, 0.2, 1.0, etc.)
status: draft             # Required: proposed|draft|in_review|approved|implementation_ready|superseded|archived
owner: Author Name        # Required: Who owns this document
reviewer: Reviewer Name   # Optional: Who reviewed it (can be comma-separated)
approved_by: Kenny Bush   # Optional: Who approved it (leave null if not approved)
approved_date: null       # Optional: YYYY-MM-DD (leave null if not approved)
next_review: YYYY-MM-DD   # Optional: When should this be reviewed again
supersedes: null          # Optional: ID of prior version if updating
authoritative_path: path/to/document.md  # Required: Where this document lives
---
```

---

## Adding New Templates

If a new document type needs a template:
1. Create the template in this directory
2. Document its purpose in this README
3. Create a draft PR with the new template
4. Get Kenny's approval

---

**Owner**: Kenny Bush  
**Last Updated**: 2026-07-10
