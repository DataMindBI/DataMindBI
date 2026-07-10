---
document_id: DOC-XXXX
title: Document Title
version: 0.1
status: draft
owner: Author Name
reviewer: Reviewer Name
approved_by: Kenny Bush (or null if not approved)
approved_date: null (set when approved)
next_review: YYYY-MM-DD
supersedes: null (reference prior version if updating)
authoritative_path: category/document-name.md
---

# Document Title

## Overview
One paragraph explaining what this document covers and why it matters.

## Scope
Define what is and is not covered by this document.

---

## Section 1: Core Concept

Explain the main idea or standard being documented.

### Subsection 1.1
Provide supporting detail, guidelines, or examples.

### Subsection 1.2
Additional context or variations.

---

## Section 2: Application

Describe how this applies to DataMind work:
- Who follows this guidance?
- When does it apply?
- What are the exceptions?

### Examples
Provide concrete examples or use cases.

---

## Section 3: Responsibilities

| Role | Responsibility |
|------|-----------------|
| Owner | Maintains this document and requests updates |
| Reviewer | Reviews changes before approval |
| Implementers | Apply this guidance in their work |

---

## Related Documents
- [Document Name](path/to/document.md)
- [ADR-NNNN](../decisions/ADR-NNNN-title.md)

---

## Approval
- **Draft completed by**: [Author] on [date]
- **Ready for review**: [Yes/No]
- **Reviewed by**: [Reviewer] on [date]
- **Approved by**: Kenny Bush on [date] (leave empty until approved)

---

## Revision History
| Version | Date | Author | Change |
|---------|------|--------|--------|
| 0.1 | YYYY-MM-DD | Author Name | Initial draft |

---

**Status**: `{{ status }}` — Last updated {{ approved_date or "draft" }}
