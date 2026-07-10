---
document_id: DIR-PAGEbriefs
title: Page Briefs Subdirectory
version: 0.1
status: approved
owner: Kenny Bush
reviewer: null
approved_by: Kenny Bush
approved_date: 2026-07-10
next_review: 2026-10-10
supersedes: null
authoritative_path: 05-website/page-briefs/README.md
---

# 05-website/page-briefs/

**Purpose**: Approved content briefs for each page on datamindbi.com. Each brief defines page purpose, key messages, content sections, and calls-to-action.

## What Belongs Here

- Homepage brief
- Services page briefs (one per major service)
- About/Company briefs
- Case studies or portfolio pages
- Blog or resource center strategy
- Thought leadership or research pages
- Contact or engagement briefs
- Pricing or commercial information pages

**Naming Convention**: `{page-name}-brief.md` (e.g., `homepage-brief.md`, `services-brief.md`, `about-brief.md`)

## What Does NOT Belong Here

- ❌ Actual HTML/CSS/JavaScript (that's in datamind-website repository)
- ❌ Website code or implementation details
- ❌ Brand guidelines (see 02-brand/)
- ❌ Marketing or thought leadership content (see 06-market/)
- ❌ Pricing details not specific to a page

## Approval Authority

**Kenny Bush** — Principal  
All page briefs require explicit approval before datamind-website can implement them.

## Page Brief Structure

Each brief should include (using `/templates/document-template.md`):

```yaml
---
document_id: PB-XXX
title: [Page Name] Brief
version: 0.1
status: draft
owner: Kenny Bush
reviewer: [Reviewer]
approved_by: null
approved_date: null
next_review: 2026-MM-DD
authoritative_path: 05-website/page-briefs/[page-name]-brief.md
---

# [Page Name] Brief

## Page Purpose
One sentence: What is the page for? Who is it for? What action do we want them to take?

## Key Messages
- Message 1: [Key differentiator or value proposition]
- Message 2: [Solution to a client problem]
- Message 3: [Why DataMind is different]

## Content Sections
Define each section (H1, H2, copy, visual requirements):

### Section 1: Hero/Introduction
- Copy: [Brief, compelling opening]
- Visual: [Image, video, or interactive element]
- CTA: [Call-to-action button or link]

### Section 2: [Topic]
- Copy: [Explanation, benefits, details]
- Visual: [Supporting image or graphic]
- CTA: [Secondary CTA if appropriate]

## Calls-to-Action
- Primary CTA: [Button text and link]
- Secondary CTAs: [Other engagement options]

## Success Metrics
- [What we'll measure to know if this page succeeds]

## Visual Requirements
- [Layout style, imagery, interactive elements, animations]

## SEO & Discovery
- Target keywords: [List of keywords this page ranks for]
- Meta description: [Page meta description]
```

## Creating a New Page Brief

1. Copy `/templates/document-template.md`
2. Fill in page-specific details
3. Mark status as `draft`
4. Create feature branch
5. Open draft PR with:
   - Clear page purpose and audience
   - Aligned key messages
   - Competitive differentiation
6. Kenny approves

## Updating Page Briefs

When a page strategy changes:
1. Increment version number
2. Mark status as `in_review`
3. Document what changed and why
4. Link to any related ADRs or strategy changes
5. Get Kenny's approval
6. Notify datamind-website team before implementing

## Relationship to datamind-website Repository

The datamind-website repository:
- Implements these approved briefs
- Uses version-pinned references to this directory
- Reports user engagement and conversion metrics
- Requests updates if the brief is incomplete or unclear

---

**Owner**: Kenny Bush  
**Last Updated**: 2026-07-10

## Current Page Briefs

*None yet — awaiting page strategy definition and Kenny approval*
