---
document_id: DIR-MARKET
title: Market Directory
version: 0.1
status: approved
owner: Kenny Bush
reviewer: null
approved_by: Kenny Bush
approved_date: 2026-07-10
next_review: 2026-10-10
supersedes: null
authoritative_path: 06-market/README.md
---

# 06-market/

**Purpose**: Market positioning, competitive differentiation, thought leadership, and market strategy. The authoritative source for "how we position ourselves in the market."

## What Belongs Here

- Competitive differentiation and positioning statements
- Market analysis and opportunity identification
- Target market segments and personas
- Thought leadership and content strategy
- Speaking engagements and conference strategy
- Published articles, blog posts, and research
- Market research and industry insights
- Brand storytelling and narrative arc

## What Does NOT Belong Here

- ❌ Brand guidelines (see 02-brand/)
- ❌ Company strategy (see 01-company/)
- ❌ Service definitions (see 04-services/)
- ❌ Website content (see 05-website/)
- ❌ Product roadmaps (see 07-products/)
- ❌ Methodology (see 03-methodology/)

## Approval Authority

**Kenny Bush** — Principal  
All market positioning and thought leadership require Kenny's approval to ensure consistency with company strategy and brand.

## Document Format

All documents use YAML front matter with document_id, version, status, owner, reviewer, approved_by, approved_date.

See `/templates/document-template.md` for structure.

## Creating Market Documents

1. Use the appropriate template from `/templates/`
2. Fill in YAML front matter
3. Document:
   - Market opportunity or competitive angle
   - How this supports DataMind's positioning
   - Target audience and key messages
4. Mark status as `draft`
5. Create feature branch
6. Open draft PR with clear rationale
7. Kenny approves

## Publishing Approved Content

Once a document (article, research, etc.) is approved:
1. Implement in appropriate channel (blog, LinkedIn, publication)
2. Link back to this repository in publication metadata
3. Update document with publication details and results

## Updating Market Documents

Market positions and thought leadership evolve:
1. Increment version number
2. Mark status as `in_review`
3. Document what changed and why
4. Get Kenny's approval
5. Communicate to relevant teams

## Relationship to Implementation Repositories

Implementation repositories (datamind-website, product repos) should:
- Reference approved market positioning when building features
- Align product messaging with approved thought leadership
- Support market strategy through accelerators and demonstrations

---

**Owner**: Kenny Bush  
**Last Updated**: 2026-07-10
