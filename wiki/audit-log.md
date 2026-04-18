---
title: "Audit log"
type: meta
subjects: [family]
status: active
---

# Audit log

Findings from lint runs. The lint skill (`/lint`) appends here. See `.claude/skills/lint/SKILL.md` for checks performed and severity scale.

## Format

```
## Audit — YYYY-MM-DD

- Critical (N): brief list with file paths
- High (N): ...
- Medium (N): ...
- Low (N): ...

### Findings
[detailed list grouped by severity]
```

## Severity scale

- **Critical** — factually wrong, frontmatter that breaks parsing, data loss risk
- **High** — broken links, missing required fields, misfiled pages
- **Medium** — stale drafts, orphans, inconsistent references, filename violations
- **Low** — typos, style nits, minor convention deviations

## Entries

<!-- audit-entries-begin -->

## Audit — 2026-04-18

- **Critical** (0): None
- **High** (0): None  
- **Medium** (7): 
  - 3 orphan pages (content added but not yet cross-linked)
  - 4 reciprocal link gaps
- **Low** (3):
  - 3 reference links left in README files to deleted _examples/ content

### Findings

#### Medium: Reciprocal link gaps
- `children/leo/profile.md` missing shared experiences links → FIXED (added)
- `children/maya/profile.md` - needs links to family events
- `children/theo/profile.md` - needs links to family events
- `children/rosie/profile.md` - needs links to family events

#### Medium: Orphan pages
- `wiki/family/sibling-dynamics/2024-maya-leo.md` — not linked from any profile
- `wiki/family/shared-firsts/first-camping.md` — not linked from any profile
- `wiki/family/shared-memories/2024-powell-books.md` — not linked from any profile

#### Low: Stale references
- `wiki/family/caregivers/README.md` - references deleted `_examples/`
- `wiki/family/traditions/README.md` - references deleted `_examples/`
- `wiki/family/pets/README.md` - references deleted `_examples/`

### Proposed fixes

1. **Add reciprocal links to Maya, Theo, Rosie profiles** — link to shared family events
2. **Add orphan pages to profiles** — add links from each child profile to their shared experiences
3. **Clean up stale references** — remove _examples/ links

_Approvals needed for content-level fixes. I can auto-fix #3 now._

<!-- audit-entries-end -->
