---
document_id: DIR-PRODUCTS
title: Products Directory
version: 0.1
status: approved
owner: Kenny Bush
reviewer: null
approved_by: Kenny Bush
approved_date: 2026-07-10
next_review: 2026-10-10
supersedes: null
authoritative_path: 07-products/README.md
---

# 07-products/

**Purpose**: Product strategy, roadmaps, and portfolio decisions. The authoritative source for "what products and accelerators we build."

## What Belongs Here

- Product strategy and vision
- Product portfolio decisions
- Accelerator and reference implementation strategy
- Feature roadmaps and prioritization
- Product-market positioning
- Product success metrics and KPIs
- Release planning and versioning strategy
- Product deprecation and sunset policies

## What Does NOT Belong Here

- ❌ Product source code (that's in product repositories like datamind-powerbi-analytics)
- ❌ Service definitions (see 04-services/)
- ❌ Company strategy (see 01-company/)
- ❌ Brand guidelines (see 02-brand/)
- ❌ Methodology (see 03-methodology/)

## Approval Authority

**Kenny Bush** — Principal  
All product strategy and major roadmap decisions require Kenny's explicit approval.

## Document Format

All documents use YAML front matter with document_id, version, status, owner, reviewer, approved_by, approved_date.

See `/templates/document-template.md` for strategy documents and `/templates/initiative-template.md` for product initiatives.

## Product Categories

**Reference Implementations & Demos**:
- datamind-powerbi-analytics — Power BI semantic model and DAX library
- datamind-consulting-cli — CLI automation and back-office tooling
- datamind-ai-agents — Multi-agent orchestration and MCP server
- datamind-fieldservice-suite — Field service and mobile solution

**Accelerators & Frameworks**:
- Frameworks for specific industry verticals
- Technology stacks and deployment patterns
- Customer quick-start packages

## Creating Product Strategies

1. Use `/templates/document-template.md` for strategy or `/templates/initiative-template.md` for new product initiatives
2. Define:
   - Product purpose and target user
   - Strategic fit with DataMind positioning
   - Competitive advantages
   - Success metrics
3. Mark status as `draft`
4. Create feature branch
5. Open draft PR with business case
6. Kenny approves

## Product Roadmaps

Product roadmaps should:
1. Reference approved company strategy
2. Align with market positioning (see 06-market/)
3. Support service definitions (see 04-services/)
4. Follow the DataMind methodology (see 03-methodology/)

## Relationship to Product Repositories

Product repositories (e.g., datamind-powerbi-analytics):
- Implement approved product strategy
- Use version-pinned references to this directory
- Report results and usage back to product strategy documents
- Request product decisions if strategy is unclear

If a product repository needs to diverge from approved strategy:
1. Create a draft PR updating the strategy in this repository
2. Link to the implementation issue
3. Request Kenny's approval before proceeding

---

**Owner**: Kenny Bush  
**Last Updated**: 2026-07-10
