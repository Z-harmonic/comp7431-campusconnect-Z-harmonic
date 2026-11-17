# Week 10 MVP Test, CI, and Freeze

Student: Eric Wei
Date: 11/16/2026
Branch: release/week-10-rc1  
Local URL: http://127.0.0.1:7860  
Environment: Chrome on macOS

## 1. Six-test MVP record

| # | Quality area | Action and expected result | Observed evidence | Result |
|---|---|---|---|---|
| 1 | Supported retrieval | Ask: "How do I reset my CampusConnect password?" The answer uses the approved password-reset passage. | IT-01, Password Reset | PASS |
| 2 | Citation support | Open the displayed source from Test 1. At least one important answer claim is directly supported by the source passage. | The agent is using the elevenlab knowledge base info | PASS |
| 3 | Unsupported query | Ask: "What are the Thanksgiving dining hall hours?" The system states its IT-support limit and does not invent hours, a source, phone number, or office. | Source: IT-03, IT Service Desk. | PASS |
| 4 | Voice and text fallback | Use the supported answer. If voice works, its meaning matches the visible grounded answer. If voice is unavailable, the text, source, and a clear Continue in text or retry path remain. | Ask questions about Secure Campus Wi-Fi | PASS |
| 5 | Video accessibility | Mute the tab and skip the video. AI disclosure and transcript remain visible, and the chatbot is reachable by keyboard. | Tested pass. | PASS |
| 6 | Latency and recovery | Time one supported question. Class target: grounded text in 5 seconds or less. If slower, the question is preserved and progress, retry, or text fallback is clear. | Agents respond in 5 seconds. | PASS |

## 2. Lighthouse and manual accessibility evidence

Performance score: 94 
Accessibility score: 96
One important Lighthouse finding or "none listed": Requests are blocking the page's initial render, which may delay LCP.
Keyboard plus muted-video result: Using tab to switch each buttons and space to confirm(press).

## 3. Defect decision and retest

Highest-severity finding: Reduce unused CSS.
Severity: MINOR
Smallest repair made: No repair required
Focused retest result: 

## 4. Release gate

Release decision: GO
Decision reason: Further optimazation will be made and for now it is good to go.
GitHub Actions run: Pending
Release tag if GO: v0.9.0-rc1

## 5. Engineering and AI Use Log

What I tested myself: 
What remained human-reviewed rather than automated: 
Known limitation carried into Week 11 Red Teaming: 
