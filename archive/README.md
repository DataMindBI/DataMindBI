---
document_id: DIR-ARCHIVE
title: Archive Directory
version: 0.1
status: approved
owner: Kenny Bush
reviewer: null
approved_by: Kenny Bush
approved_date: 2026-07-10
next_review: 2026-10-10
supersedes: null
authoritative_path: archive/README.md
---

# archive/

**Purpose**: Superseded, deprecated, and archived documents. Kept for historical reference and audit trail.

## What Belongs Here

- Documents with status `superseded` (replaced by newer versions)
- Deprecated policies or procedures
- Historical decisions no longer active
- Archived initiatives or projects
- Old strategy documents replaced by new ones

## What Does NOT Belong Here

- ❌ Active, approved documents (those stay in their original directories)
- ❌ Documents still in draft (keep those in active directories)
- ❌ Temporary files or work-in-progress

## Archival Process

When a document becomes obsolete:

1. **Mark status as `superseded`** in the document's YAML front matter
2. **Add `supersedes` field** pointing to what this replaced (if applicable)
3. **Increment version number** one final time
4. **Move to archive/** with the same filename
5. **Update the original directory's README** to reflect the supersession
6. **Keep in Git history** — do not delete

**Example**:
- Active document: `01-company/strategic-blueprint-v1.md` (status: approved)
- New version: `01-company/strategic-blueprint-v2.md` (status: approved)
- Archived: `archive/strategic-blueprint-v1.md` (status: superseded)

## Keeping Historical Records

Archives are important for:
- **Audit trail**: Showing what decisions were made and when
- **Learning**: Understanding why past decisions were revisited
- **Traceability**: Linking current decisions to their origins
- **Regulatory**: Maintaining records for compliance

**Never delete archived documents** — keep them for institutional memory.

## Related Decisions

See [ADR-0001](../decisions/ADR-0001-company-repository-boundaries.md) for governance principles that support maintaining historical records.

---

**Owner**: Kenny Bush  
**Last Updated**: 2026-07-10

## Current Archive Contents

*None yet — all documents are currently active*
