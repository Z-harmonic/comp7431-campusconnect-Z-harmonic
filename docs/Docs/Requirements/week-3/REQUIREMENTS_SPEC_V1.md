# CampusConnect Requirements Specification v1
Status: Draft — Week 3
Student: Eric Wei
Branch: docs/week-3-requirements-ai
## 1. Problem statement
Students who need IT Support information need a reliable way to find the correct
next step because the current experience may be scattered, difficult to search, or
hard to verify as current.
## 2. Evidence carried forward from Week 2
- E-01: An advisor reported that students assume he controls the process "because I am the person they can reach," although he does not own the underlying policy or system.
- E-02: When two official pages gave conflicting information, the advisor stopped before replying and privately verified with a colleague; this verification was invisible to the student and had to be repeated each time.
- A-01: We assume a student who receives a safe-failure response plus a next step will follow it rather than escalating to a person. This was not observed before.
## 3. One user journey inside the MVP
A student asks one typed IT Support question. CampusConnect searches only approved
IT Support material, returns a short answer with a visible source, or says the
available sources do not support an answer.
## 4. Four requirements
- FR-01 — The system shall accept one typed IT Support question.
- GR-01 — Every factual answer shall identify the approved source used.
- SF-01 — If approved sources are insufficient, the system shall not invent an
answer and shall provide a helpful IT Support next step.
- NFR-01 — A keyboard user shall be able to submit a question and read the result.
## 5. MVP boundary
IN: one typed question, approved IT Support material, one grounded answer, visible
source, safe failure, and helpful next step.
OUT: password resets, ticket creation, personal student records, voice, automatic
actions, and answers from unapproved material.
## 6. AI critique and human decision
- ChatGPT suggestion: SF-01
  - ASSUMPTION — “helpful IT Support next step” is not defined enough to be consistently testable. Without defining what qualifies as a next step, reviewers cannot reliably determine whether safe-failure behavior passes.
  - Smallest testable revision: Add: “The response shall provide a specific next step that directs the student to an approved IT Support resource or contact.”
- Claude suggestion: SF-01
  - "Insufficient" and "helpful" are undefined, so no one can write a pass/fail test, and nothing says what happens when two approved sources conflict, which is the situation E-02 actually observed.
  - Safe failure is the MVP's core trust behavior. If it can't be tested, the system could confidently cite one of two conflicting approved pages, repeating the hidden-verification problem in E-02 (ASSUMPTION: the current wording would not treat conflicting sources as "insufficient").
  - "If no approved source answers the question, or two approved sources give conflicting answers, the system shall return no factual answer and shall display [named IT Support contact channel — to be confirmed with IT Support]; test: submit a question covered by two conflicting approved pages and verify that no answer appears and the contact channel is shown."
- My decision: Revised
- My reason: 
  - I accepted Claude's structure and rejected the scope of its
  trigger condition. ChatGPT's revision defines only the output of a safe
  failure; it leaves "insufficient" undefined, so a question covered by two
  conflicting approved pages would still return a confident, sourced answer.
  That is exactly the situation E-02 documented, and E-01 explains why it is
  costly: the student treats the visible interface as the authority even when
  it does not own the underlying policy. Claude's version defines both the
  trigger and the behavior and supplies a pass/fail test, which makes SF-01
  reviewable rather than aspirational. Two human changes: (1) I folded
  ChatGPT's wording "an approved IT Support resource or contact" into the
  behavior clause because it is more specific and stays inside the Section 5
  boundary (no ticket creation, no action taken for the student); (2) I did
  not accept semantic conflict detection into v1 — for v1, "conflicting" is
  limited to approved sources carrying different last-updated dates for the
  same question, which is detectable without interpreting page meaning.
  Open dependency: the named contact channel must be confirmed with IT
  Support before SF-01 can be tested. This revision makes SF-01 testable but
  does not validate A-01, which still requires observing whether a student
  follows the next step instead of escalating.
