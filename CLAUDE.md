# Claude Instructions for DataMind BI Repository

This file instructs Claude sessions interacting with the DataMind BI business-architecture repository.

---

## Before You Begin

Read in this order:
1. [README.md](./README.md) — Repository purpose and identity
2. [GOVERNANCE.md](./GOVERNANCE.md) — Document control and approval authority
3. [STATUS.md](./STATUS.md) — Current phase and blockers
4. [decisions/](./decisions/) — All approved ADRs (architecture decision records)

This context is authoritative. When in doubt, refer to it rather than inferring from task description.

---

## Core Principles

### Never Invent Company Strategy
- Do not create strategy documents, brand guidelines, service definitions, or product roadmaps without explicit approval.
- If strategic content is missing, create a **decision request** (ADR-draft) rather than filling the gap yourself.
- Stop and document the gap instead of guessing.

### Treat Authoritative Documents as Immutable
- Do not rewrite approved documents without explicit approval and version increment.
- Do not duplicate authoritative content (no "final-v2", "backup", or "working copy" versions).
- Use Git history for revisions — previous versions remain in Git, not as separate files.

### Follow Document Control Strictly
- Every controlled document must have YAML front matter with: document_id, title, version, status, owner, reviewer, approved_by, approved_date, next_review.
- Allowed statuses: proposed, draft, in_review, approved, implementation_ready, superseded, archived.
- Document status reflects its authority: only "approved" documents are binding company guidance.

### Respect Repository Boundaries
- **This repository** is authoritative for company strategy, brand, methodology, service architecture, and business decisions.
- **DataMind Forge** is authoritative for execution governance, PMO, EWOs, standards enforcement, and delivery.
- **Implementation repositories** (datamind-website, product repos) consume approved requirements from here but do not redefine strategy.
- If an implementation repository needs to diverge from approved strategy, request an ADR decision in this repository first.

### Authority Escalation
- Most decisions require **Kenny Bush** (Principal) approval.
- If scope or authority is unclear, stop and document the question before proceeding.
- Do not make assumptions about what Kenny would approve.

---

## Working with Documents

### Creating a New Document
1. Use the appropriate template from `/templates/`:
   - `document-template.md` for policy, standard, or guidance
   - `decision-record-template.md` for architectural/strategic decisions
   - `initiative-template.md` for projects or initiatives
   - `review-template.md` for periodic reviews

2. Populate YAML front matter completely (no empty fields).

3. Mark status as `draft` or `proposed` (not `approved`).

4. Create via feature branch; open draft PR with full change description.

### Updating an Existing Document
1. Read the current version first (understand its status and version number).
2. If the document is `approved`, increment version (e.g., 0.1 → 0.2) and mark as `in_review`.
3. Document the change rationale in Git commit message.
4. Open draft PR; include justification for changes.

### Publishing a Document
- Only `approved` status documents are binding.
- All substantive changes require draft PR → Kenny review → explicit approval before merge.
- No silent edits to approved documents.

---

## Using Decision Records (ADRs)

All strategic or architectural decisions belong in `/decisions/ADR-NNNN-title.md`.

**Creating an ADR:**
1. Use `templates/decision-record-template.md`.
2. Number sequentially (ADR-0001, ADR-0002, etc.).
3. Start with status `proposed`.
4. Open draft PR for Kenny review.
5. **Only after Kenny approves** should you mark it `approved`.

**Example scenarios for ADRs:**
- "Should we change the service pricing model?" → ADR
- "What is the boundary between this repo and DataMind Forge?" → ADR
- "Which website framework should we use?" → ADR (belongs in this repo so implementation repo can consume it)

---

## Git Workflow

### Branch Naming
- Feature branches: `foundation/description` or `feature/description`
- Do not commit directly to `main`

### Commits
- Use clear, descriptive messages
- Example: `docs: add ADR-0001 company repository boundaries (proposed)`
- Format: `category: description`

### Do NOT
- Rewrite Git history (no `git reset --hard`, `git rebase -i` on main)
- Add Claude or AI systems as document authors or co-authors
- Add AI attribution trailers (e.g., "Co-Authored-By: Claude") to commits
- Create merge commits on main with AI co-author labels

---

## When You Get Stuck

1. **Missing strategic content?** → Create a decision request (ADR-draft).
2. **Unclear authority?** → Stop and document the question.
3. **Conflicting requirements?** → Document the conflict instead of guessing.
4. **Implementation repo diverging from strategy?** → Request an ADR in this repo before proceeding.

### Escalation
If you encounter a situation not covered by this guidance:
1. Document the situation and question clearly.
2. Stop making changes.
3. Report to Kenny with full context.

---

## Relationship to Implementation Repositories

Implementation repositories (e.g., `datamind-website`) should:
- Reference approved documents from this repository
- Use version-pinned links or Git commit references
- Request new ADRs if they discover a strategic decision gap
- Report results back to this repository via updates to related ADRs

**Do not:** Silently diverge from approved strategy or redefine requirements without an ADR.

---

## Helpful Context

- **Repository Purpose**: Authoritative business architecture and strategy for DataMind Consulting.
- **Phase**: Foundation (v0.1) — establishing governance framework.
- **Current Blockers**: See [STATUS.md](./STATUS.md)
- **Approval Authority**: See [GOVERNANCE.md](./GOVERNANCE.md)
- **Owner**: Kenny Bush, Principal

---

**Last Updated**: 2026-07-10  
**Applies To**: All Claude sessions in this repository
