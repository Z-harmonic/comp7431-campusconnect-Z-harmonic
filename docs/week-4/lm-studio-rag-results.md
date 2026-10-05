# Week 4 LM Studio RAG Results 

Name: Eric Wei 
Model: IBM Granite 4.0 H Tiny Q4_K_M 
Documents: campusconnect password help.txt, campusconnect wifi help.txt

## Supported question 

Result: PASS
Observation: Totally referred to the txt file and give proper answer.

## Unsupported question 

Result: PASS
Observation: The model didn't speculate by it's own, and pass the question to the IT help desk.

## Action request 

Result: PASS
Observation: Totally refered to the txt file and give each steps to solve the problem.

## Architecture lesson 

The local LLM route worked well when given abundant references. 
It needs human help when additional action is needed.
