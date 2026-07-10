---
document_id: DIR-WEBSITE
title: Website Directory
version: 0.1
status: approved
owner: Kenny Bush
reviewer: null
approved_by: Kenny Bush
approved_date: 2026-07-10
next_review: 2026-10-10
supersedes: null
authoritative_path: 05-website/README.md
---

# 05-website/

**Purpose**: Website strategy, architecture, and approved page briefs. Strategy flows from this directory to the datamind-website implementation repository.

## What Belongs Here

- Website strategy and positioning
- Site architecture and navigation
- Approved page briefs (content outlines, sections, calls-to-action)
- Page-level copy guidelines
- User journey and conversion strategy
- SEO strategy and keywords
- Content calendar and publishing plan
- Analytics and measurement strategy

## What Does NOT Belong Here

- ❌ HTML/CSS/JavaScript (that's in datamind-website repository)
- ❌ Actual website code (implementation repository)
- ❌ Brand guidelines (see 02-brand/)
- ❌ Marketing content (see 06-market/)
- ❌ Company strategy (see 01-company/)

## Approval Authority

**Kenny Bush** — Principal  
All page briefs and website strategy require Kenny's approval.

## Subdirectories

### page-briefs/
Approved briefs for each page on datamind-website. Each brief outlines:
- Page purpose and audience
- Key messages and calls-to-action
- Content sections and structure
- Visual and interactive elements
- Success metrics

**Files**: One Markdown file per page (e.g., `homepage-brief.md`, `services-brief.md`)

## Document Format

- Page briefs use `/templates/document-template.md`
- YAML front matter with document_id, version, status, approved_by, approved_date
- Clear sections explaining page purpose, content, and CTA

## Creating Page Briefs

1. Define the page purpose and audience
2. Create brief using `/templates/document-template.md`
3. Include:
   - Page purpose
   - Key messages
   - Content sections (H1, H2, copy)
   - Calls-to-action
   - Visual/interactive requirements
4. Mark status as `draft`
5. Open draft PR for Kenny review
6. Kenny approves before implementation

## Updating Page Briefs

When page strategy changes:
1. Increment version number
2. Mark status as `in_review`
3. Document changes and rationale
4. Get Kenny's approval
5. Notify datamind-website team

## Relationship to datamind-website

The datamind-website repository:
- Consumes approved page briefs from here
- Implements briefs using the approved framework
- References this directory with version-pinned links
- Reports analytics back to related page brief documents

If datamind-website discovers that a brief is incomplete or conflicting, it should:
1. Create a draft PR against this repository updating the brief
2. Reference the implementation issue or blocker
3. Request Kenny's approval before proceeding

---

**Owner**: Kenny Bush  
**Last Updated**: 2026-07-10
