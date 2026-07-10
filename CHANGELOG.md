# Changelog

All significant changes to this repository are documented here. This changelog tracks:
- New documents and frameworks
- Major updates to approved documents
- New decisions (ADRs)
- Approved initiatives
- Process changes

The format is based on [Keep a Changelog](https://keepachangelog.com/), and this project adheres to [Semantic Versioning](https://semver.org/).

---

## [0.1.0] — 2026-07-10 — Foundation Phase

### Added
- Repository structure and governance framework
- **Documents**:
  - README.md — Repository overview and guidance
  - GOVERNANCE.md — Document control and approval framework
  - STATUS.md — Executive status and current blockers
  - CLAUDE.md — Instructions for Claude sessions
  - CHANGELOG.md — This file
  
- **Directory Structure** (all with purpose README files):
  - 00-governance/ — Governance policies
  - 01-company/ — Company strategy and vision
  - 02-brand/ — Brand guidelines and messaging
  - 03-methodology/ — The DataMind Method
  - 04-services/ — Service definitions
  - 05-website/ — Website strategy and page briefs
  - 06-market/ — Market positioning and thought leadership
  - 07-products/ — Product strategy and roadmaps
  - 08-operations/ — Operating standards
  - decisions/ — Architecture Decision Records
  - templates/ — Document templates
  - archive/ — Superseded documents

- **Templates**:
  - document-template.md — For policies, guidelines, definitions
  - decision-record-template.md — For architecture decisions (ADRs)
  - initiative-template.md — For projects and initiatives
  - review-template.md — For periodic reviews

- **Initial Decisions**:
  - ADR-0001 (proposed) — Company Repository Boundaries

### Blockers
- ✋ ADR-0001 awaits Kenny Bush approval (decision not yet binding)
- ✋ DataMind BI 2.0 Strategic Blueprint content not yet pasted (01-company/strategic-blueprint.md is placeholder)

### Next Steps
1. Kenny reviews and approves ADR-0001
2. Strategic blueprint content supplied and added
3. Pull request reviewed and merged
4. Claude sessions load governance context automatically

---

## Version History

| Version | Date | Phase | Status |
|---------|------|-------|--------|
| 0.1.0 | 2026-07-10 | Foundation | In Progress |

---

## How to Contribute to This Changelog

- Add new entries under the latest version heading as changes are made
- Use these categories:
  - **Added**: New documents, frameworks, or processes
  - **Changed**: Updates to existing approved documents
  - **Deprecated**: Documents or processes being phased out
  - **Removed**: Documents or processes no longer used
  - **Fixed**: Corrections to existing documents
  - **Security**: Changes to security policies or controls
- Include dates and related ADR numbers
- Keep entries clear and brief

---

**Last Updated**: 2026-07-10  
**Maintained By**: Kenny Bush, Principal
