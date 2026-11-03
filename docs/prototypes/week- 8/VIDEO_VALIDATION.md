# Week 8 AI Presenter Prototype and Validation
Student: Eric Wei
Date: 11/02/2026
Branch: feature/week-8-avatar-prototype
HeyGen project: CampusConnect IT Help Introduction
## Prototype hypothesis
A short AI presenter will help a new user understand the supported
IT topics, privacy boundary, and human fallback.
## Shared video
AI-generated presenter - not a live staff member.
This is a prerecorded introduction. It does not answer questions.
[Watch the CampusConnect presenter](https://app.heygen.com/videos/campusconnect-it-help-introduction-9e93ced9864b44709c6bc7544a7db5af)
## Transcript
Hello. I am an AI-generated CampusConnect presenter, not a live staff member. You can use CampusConnect
for approved campus IT help.
Ask about password resets, secure campus Wi-Fi, or the IT Service Desk. Please do not share passwords,
recovery codes, student records, or other private information.
If the chatbot cannot support an answer from its approved guide, it will direct you to a human. This video is a
prerecorded introduction. You can read the same script in our GitHub project.
## Five checks
1. AI disclosure, IT topics, privacy, and fallback: OBSERVED; PASS
2. Full script and video duration: 30 SECONDS; OBSERVED; PASS
3. Captions on and readable: OBSERVED; PASS
4. Muted video and GitHub transcript: OBSERVED; PASS
5. Share link works without HeyGen sign-in: OBSERVED; PASS
## Design decision
Decision: KEEP

Reason based on my checks: Meet all the check points
One improvement for later: Upload a customized voice
## Engineering and AI Use Log
AI tool used: HeyGen
What HeyGen generated: A quick video about CampusConnect IT Help Introduction

What I verified myself: I watched the full 30-second video with captions on and again muted, confirmed the spoken script matches the GitHub transcript word for word, and opened the share link in a private browser window to confirm it plays without a HeyGen sign-in.

Remaining limitation: The presenter is a prerecorded, one-way introduction that cannot answer follow-up questions, and it uses a stock HeyGen voice instead of a customized one.
