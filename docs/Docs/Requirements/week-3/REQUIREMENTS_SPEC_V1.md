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
- ChatGPT suggestion: <ADD ONE SHORT SUGGESTION>
- Claude suggestion: <ADD ONE SHORT SUGGESTION>
- My decision: Accepted / Revised / Rejected
- My reason: <EXPLAIN USING WEEK 2 EVIDENCE, SCOPE, OR TESTABILITY>
