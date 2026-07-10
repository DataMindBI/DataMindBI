# DataMind BI — Business Architecture Repository

<div align="center">

## The Authoritative Source for DataMind Strategy, Brand, and Operating Standards

**Repository**: https://github.com/datamindbi/datamindbi  
**Phase**: Foundation (v0.1)  
**Governed by**: Kenny Bush, Principal

</div>

---

## What This Repository Is

**DataMind BI** is the single authoritative repository for:
- Company strategy and vision
- Brand and messaging
- The DataMind Method
- Service architecture and definitions
- Client journey design
- Website strategy
- Market positioning and thought leadership
- Product roadmaps and strategy
- Operating standards and governance
- Architecture and business decisions (ADRs)

This is **NOT** an application repository. It does not contain source code, application infrastructure, or product deployment configurations.

---

## What This Repository Is NOT

- ❌ Application source code
- ❌ Product repositories (those are separate: datamind-website, datamind-powerbi-analytics, etc.)
- ❌ Project management or PMO (that's DataMind Forge)
- ❌ Deployment infrastructure
- ❌ CI/CD pipelines for products

Implementation repositories **consume approved requirements** from this repository but remain independent for delivery.

---

## Repository Structure

```
datamindbi/
├── README.md                          ← You are here
├── GOVERNANCE.md                      ← Document control framework
├── STATUS.md                          ← Executive status and blockers
├── CLAUDE.md                          ← Instructions for Claude sessions
├── CHANGELOG.md                       ← What changed and when
│
├── 00-governance/                     ← Governance framework and policies
├── 01-company/                        ← Company strategy and vision
├── 02-brand/                          ← Brand guidelines and messaging
├── 03-methodology/                    ← The DataMind Method
├── 04-services/                       ← Service definitions and architecture
├── 05-website/                        ← Website strategy
│   └── page-briefs/                   ← Approved page briefs for datamind-website
├── 06-market/                         ← Market positioning and thought leadership
├── 07-products/                       ← Product strategy and roadmaps
├── 08-operations/                     ← Operating standards and how we work
│
├── decisions/                         ← Architecture Decision Records (ADRs)
│   └── ADR-0001-company-repository-boundaries.md
├── templates/                         ← Document templates for consistent structure
│   ├── document-template.md
│   ├── decision-record-template.md
│   ├── initiative-template.md
│   └── review-template.md
│
└── archive/                           ← Superseded and archived documents
```

---

## How Documents Are Controlled

Every strategic document in this repository must have **YAML front matter** specifying:
- `document_id` — Unique identifier
- `title` — Document name
- `version` — Version number (semantic: 0.1, 0.2, 1.0, etc.)
- `status` — One of: proposed, draft, in_review, approved, implementation_ready, superseded, archived
- `owner` — Document owner
- `reviewer` — Who reviewed it
- `approved_by` — Who approved it (usually Kenny)
- `approved_date` — When it was approved
- `next_review` — When it should be reviewed again

**Only `approved` status documents represent binding company guidance.**

See [GOVERNANCE.md](./GOVERNANCE.md) for complete details.

---

## Directory Guide

### [00-governance/](./00-governance/)
**Governance framework, policies, compliance, standards.**  
Approval Authority: Kenny Bush  
Who modifies: Governance owner (established in directory README)

### [01-company/](./01-company/)
**Company strategy, vision, market positioning, strategic blueprint.**  
Approval Authority: Kenny Bush  
Who modifies: Strategy owner

### [02-brand/](./02-brand/)
**Brand guidelines, visual identity, messaging framework, tone.**  
Approval Authority: Kenny Bush  
Who modifies: Brand owner

### [03-methodology/](./03-methodology/)
**The DataMind Method — repeatable delivery standards, quality gates, service delivery framework.**  
Approval Authority: Kenny Bush  
Who modifies: Methodology owner

### [04-services/](./04-services/)
**Service definitions, tiers, pricing model, delivery models, SLAs.**  
Approval Authority: Kenny Bush  
Who modifies: Service architecture owner

### [05-website/](./05-website/)
**Website strategy, site architecture, approved content briefs.**  
Approval Authority: Kenny Bush  
Who modifies: Website strategy owner  
**Note**: datamind-website repository implements this strategy.

### [06-market/](./06-market/)
**Market positioning, competitive differentiation, thought leadership, content strategy.**  
Approval Authority: Kenny Bush  
Who modifies: Market strategy owner

### [07-products/](./07-products/)
**Product strategy, roadmap, accelerator portfolio, feature prioritization.**  
Approval Authority: Kenny Bush  
Who modifies: Product strategy owner

### [08-operations/](./08-operations/)
**Operating standards, how we work, what we value, internal processes.**  
Approval Authority: Kenny Bush  
Who modifies: Operations owner

### [decisions/](./decisions/)
**Architecture Decision Records (ADRs).** Every strategic decision is recorded here with rationale, alternatives considered, and approval status.  
**Naming**: ADR-NNNN-decision-title.md  
**Approval Authority**: Kenny Bush  
**Process**: Start as `proposed`, get reviewed, become `approved`

### [templates/](./templates/)
**Document templates** for consistency across the repository. Use these when creating new documents.  
Use: Copy the appropriate template, fill in YAML, write content.

### [archive/](./archive/)
**Superseded and archived documents.** Kept for historical reference.

---

## Working with This Repository

### Read First
Before making changes to this repository, read:
1. [GOVERNANCE.md](./GOVERNANCE.md) — Document control and approval process
2. [STATUS.md](./STATUS.md) — Current phase and blockers
3. [decisions/](./decisions/) — All approved ADRs

### To Create a New Document
1. Choose the correct directory (01-company/, 02-brand/, etc.)
2. Use the appropriate template from `/templates/`
3. Fill in YAML front matter completely
4. Mark status as `draft` or `proposed` (not `approved`)
5. Create via feature branch; open draft PR
6. Link related ADRs in the PR description

### To Update an Approved Document
1. Increment version number
2. Mark status as `in_review`
3. Update content
4. Open draft PR with justification
5. Kenny reviews and approves before merge

### For Decisions
Use [decisions/ADR-NNNN-decision-record-template.md](./templates/decision-record-template.md):
1. Number sequentially (ADR-0001, ADR-0002, etc.)
2. Start with status `proposed`
3. Open draft PR
4. Only mark `approved` after Kenny approves

### For Implementation Repositories
Implementation repositories (datamind-website, product repos) should:
- **Reference** approved documents from this repository with version-pinned links
- **Request ADRs** if they discover missing or conflicting strategy
- **Report results** back to strategy documents via ADR updates

---

## Current Status

See [STATUS.md](./STATUS.md) for:
- Current phase and overall status
- Active blockers and decisions awaiting approval
- Implementation-ready items
- Recently approved documents
- Next checkpoint

---

## Authority and Governance

### Approval Chain
- **Company strategy, brand, methodology, services, products, operations**: Kenny Bush, Principal
- **Architecture decisions** (ADRs): Kenny Bush, Principal
- **Implementation**: Delegated to implementation repository owners

### Escalation
If authority or scope is unclear:
1. Document the question
2. Stop making changes
3. Open a draft PR for discussion
4. Ask Kenny for clarification

### Repository Boundaries
See [decisions/ADR-0001-company-repository-boundaries.md](./decisions/ADR-0001-company-repository-boundaries.md) for the complete decision on:
- What this repository is authoritative for
- What DataMind Forge is responsible for
- What implementation repositories own

---

## Git Workflow

### Branches
- Feature branches: `foundation/description`, `feature/description`, or `fix/description`
- All changes go through feature branches, never direct commits to `main`

### Pull Requests
- Open as **draft PR** with full description
- Include change summary, affected documents, assumptions
- Link related ADRs or strategy documents
- Keep in draft until review is complete

### Commits
- Clear, descriptive messages
- Format: `category: description`
- Example: `docs: add ADR-0001 company repository boundaries (proposed)`

### No History Rewriting
- Never use `git reset --hard` on main
- No squashing or rebasing on main
- Keep full history for audit trail

---

## Implementation Repositories

These repositories implement approved strategy from this repository:

| Repository | What It Does | Consumes From |
|------------|-------------|---------------|
| [datamind-website](https://github.com/datamindbi/datamind-website) | Company website | `05-website/page-briefs/`, brand guidelines |
| [datamind-powerbi-analytics](https://github.com/datamindbi/datamind-powerbi-analytics) | Reference analytics demo | Service definitions, methodology |
| [datamind-consulting-cli](https://github.com/datamindbi/datamind-consulting-cli) | Back-office automation demo | Operations standards, methodology |
| [datamind-ai-agents](https://github.com/datamindbi/datamind-ai-agents) | AI/MCP demo | Service architecture, methodology |
| [datamind-fieldservice-suite](https://github.com/datamindbi/datamind-fieldservice-suite) | Field service demo | Service definitions, brand |

---

## Contact & Governance

- **Repository Owner**: Kenny Bush, Principal
- **Governance Framework**: See [GOVERNANCE.md](./GOVERNANCE.md)
- **All Questions**: Escalate via draft PR or open a decision request (ADR)

---

## Quick Start for Claude Sessions

1. Read [CLAUDE.md](./CLAUDE.md) — Session instructions
2. Read [GOVERNANCE.md](./GOVERNANCE.md) — Document control rules
3. Read [STATUS.md](./STATUS.md) — Current phase and blockers
4. Read all approved ADRs in `decisions/`
5. Never invent strategy — stop and ask if unclear
6. Create decision requests (ADRs) for missing decisions

---

**Last Updated**: 2026-07-10  
**Current Phase**: Foundation (v0.1)  
**Status**: Awaiting strategic blueprint and ADR-0001 approval

---

<div align="center">

**DataMind BI Repository** — Authoritative business architecture and strategy for DataMind Consulting  
Service-Disabled Veteran-Owned Small Business (SDVOSB) · U.S. Navy Veteran-owned

</div>
