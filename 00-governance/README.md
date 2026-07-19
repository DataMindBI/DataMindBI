---
document_id: DIR-GOVERNANCE
title: Governance Directory
version: 0.1
status: approved
owner: Kenny Bush
reviewer: null
approved_by: Kenny Bush
approved_date: 2026-07-10
next_review: 2026-10-10
supersedes: null
authoritative_path: 00-governance/README.md
---

# 00-governance/

**Purpose**: Company governance framework, policies, compliance standards, and internal operating rules.

## What Belongs Here

- Governance policies (document control, approval authority, decision processes)
- Compliance and risk frameworks
- Data governance and security policies
- Privacy and data classification standards
- Internal process standards
- Budget and resource allocation policies
- HR and team standards

## What Does NOT Belong Here

- ❌ Brand guidelines (see 02-brand/)
- ❌ Service definitions (see 04-services/)
- ❌ Company strategy (see 01-company/)
- ❌ Methodology and delivery standards (see 03-methodology/)
- ❌ Website strategy (see 05-website/)

## Approval Authority

**Kenny Bush** — Principal  
All governance documents require Kenny's explicit approval before becoming binding.

## Document Format

All documents in this directory must follow the template structure:
- YAML front matter with document_id, version, status, owner, reviewer, approved_by, approved_date
- Clear sections explaining policy, scope, who it applies to, exceptions
- Explicit approval timestamp

See `/templates/document-template.md` for the standard structure.

## Related Documents

- [GOVERNANCE.md](../GOVERNANCE.md) — Document control framework
- [CLAUDE.md](../CLAUDE.md) — Instructions for Claude sessions (references governance)
- [ADR-0001](../decisions/ADR-0001-company-repository-boundaries.md) — Repository boundaries decision

## Relationship to Other Repositories

DataMind Forge may enforce governance policies documented here (e.g., checking that work follows approved standards).

Implementation repositories must comply with governance policies in this directory.

---

**Owner**: Kenny Bush  
**Last Updated**: 2026-07-10
