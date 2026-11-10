# Lab09 Multimodal Journey Evidence

Branch: feature/week-9-multimodal-integration

## Journey A — Supported
- Input method used: text
- RAG answer observed:
  > I don't have any information about CampusConnect in front of me, so I can't give you the exact steps for that system. In general, most services have a "Forgot password" or "Reset password" link on the sign-in page that emails you a reset link.
  >
  > If you can tell me a bit more about CampusConnect, like whether it's a school portal or an app, I can try to point you in the right direction.
- Citation or source observed: None. The answer cited no CampusConnect document and gave only generic password-reset advice, so retrieval did not return a grounded source for this question.
- Voice behavior: Not exercised in this run. Input was text only; no voice input or spoken output was triggered.
- Video remained optional: yes

## Journey B — Unsupported
- Question used: Thanksgiving dining hall hours
- Abstention or human next step observed: The assistant abstained (gave no hours) and pointed the user to the school's dining services or student portal as the human next step.
  > I don't have any information about CampusConnect or Thanksgiving dining hall hours available to me, so I can't give you the specific times. Those details are usually posted by the school's dining services or student portal.
  > Is there anything else I can help you with?
- Text fallback worked with video muted/skipped: yes

## Traceability
- Requirement: one optional multimodal CampusConnect journey
- Files changed: `docs/week9/MULTIMODAL_JOURNEY.md` (the only file changed on this branch vs `main`)
- Known limitation: Journey A was not grounded in CampusConnect content (no citation), so the supported path currently behaves like the unsupported one and falls back to generic advice. Voice was not tested in this run.
