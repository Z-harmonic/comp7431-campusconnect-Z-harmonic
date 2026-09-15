# Spec: CampusConnect guidance

## User story
As Maya, I want a trustworthy next step so I can act before a deadline.

## Acceptance criteria
- Shows source and owner
- Flags conflicting guidance
- Offers handoff when confidence is low

## Design concerns
- Accessibility
- Privacy
- Outdated content
- Human escalation

## Human confirmation needed
- Which offices own each source? **Status: unresolved.** No office ownership
  has been invented or assumed for any source. This blocks the
  release_checklist.md "Source owner is visible" gate — release cannot
  proceed until a content owner names the responsible office for every
  source in data/sample_pages.md.
- How often must each source be reviewed? **Status: unresolved.** Blocks
  content-freshness tracking described in docs/intent.md.

Owner of this decision: content owner (see docs/intent.md next-intent
section). Needed before the next slice's data can be loaded, since
data/sample_pages.md entries require a real owner field, not a placeholder.
