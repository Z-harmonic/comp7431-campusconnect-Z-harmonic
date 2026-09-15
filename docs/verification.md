# Verification

## Planned commands
- Run: python app.py
- Test: pytest

## Required evidence for the later prototype
- [ ] 5 expected questions pass
- [ ] 2 confusing questions (no matching or ambiguous source) get a safe fallback
- [ ] 2 conflicting questions (two approved sources disagree) are flagged as
      conflicting and routed to a safe handoff, not silently answered from
      one source
- [ ] Source and owner display correctly
- [ ] No private data is required

## Week 1 evidence
- [ ] Every Markdown file opens in VS Code
- [ ] sample_pages.md says the content is synthetic
- [ ] No password, token, API key, or student record appears

## Rule
Fix the app, not the test, unless the expected result is wrong.
