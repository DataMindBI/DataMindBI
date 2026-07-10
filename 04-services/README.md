---
document_id: DIR-SERVICES
title: Services Directory
version: 0.1
status: approved
owner: Kenny Bush
reviewer: null
approved_by: Kenny Bush
approved_date: 2026-07-10
next_review: 2026-10-10
supersedes: null
authoritative_path: 04-services/README.md
---

# 04-services/

**Purpose**: Service architecture and definitions. What we offer to clients and how we package delivery. The authoritative source for "what we sell."

## What Belongs Here

- Service catalog and definitions (Business Intelligence, Data Engineering, AI/ML, etc.)
- Service tiers and packaging options
- Service-level agreements (SLAs) and guarantees
- Delivery models (embedded, managed services, etc.)
- Pricing structure and commercial model
- Success criteria and delivery expectations
- Prerequisites and assumptions for each service
- Client onboarding and kickoff standards

## What Does NOT Belong Here

- ❌ Methodology (see 03-methodology/) — How we deliver, not what we deliver
- ❌ Company strategy (see 01-company/)
- ❌ Brand guidelines (see 02-brand/)
- ❌ Product roadmaps (see 07-products/)
- ❌ Website content (see 05-website/)
- ❌ Operating processes (see 08-operations/)

## Approval Authority

**Kenny Bush** — Principal  
All service definitions require Kenny's explicit approval, especially:
- New services or service tiers
- Changes to SLAs or delivery expectations
- Pricing model changes
- Commercial terms

## Document Format

All documents use YAML front matter with document_id, version, status, owner, reviewer, approved_by, approved_date.

See `/templates/document-template.md` for structure.

## Key Distinction: Services vs. Methodology

- **Services** ("what we deliver") — Service catalog, tiers, SLAs, pricing, commercial terms
- **Methodology** ("how we work") — See 03-methodology/ for delivery approach and quality standards

Example:
- Service: "We offer Business Intelligence Development, Data Engineering, and AI/ML Services" (what)
- Methodology: "We use semantic modeling, agile delivery, and human-in-the-loop validation" (how)

## Creating Service Definitions

1. Use `/templates/document-template.md`
2. Clearly define:
   - What the service includes and excludes
   - Success criteria and delivery expectations
   - Prerequisites and assumptions
   - Engagement timeline
   - Commercial terms (if applicable)
3. Mark status as `draft`
4. Create feature branch
5. Open draft PR with business case and competitive positioning
6. Kenny approves

## Updating Service Definitions

When services evolve:
1. Increment version number
2. Mark status as `in_review`
3. Document what changed and why
4. Get Kenny's approval
5. Communicate changes to sales and delivery teams

## Using Service Definitions

**For DataMind Forge**: Use approved service definitions when:
- Scoping client engagements
- Creating EWOs (Engagement Work Orders)
- Setting pricing and commercial terms

**For implementation repositories**: Reference service definitions when:
- Building demos or accelerators
- Creating documentation
- Setting expectations

---

**Owner**: Kenny Bush  
**Last Updated**: 2026-07-10
