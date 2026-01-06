# Frontend Sandbox UI

## Role
The Sandbox UI is the user-facing interface for the platform. Users can submit video ideas, review scripts, approve scene breakdowns, select preferred AI tools, and monitor production progress. The UI also allows download of the final assembled video.

---

## Inputs
- User video idea / concept  
- Target duration  
- Tone / style preferences  
- Audience type  
- Budget constraints (optional)  
- Tool preferences (optional)  

---

## Outputs
- Displays generated narration script from Script Agent  
- Displays scene breakdown from Scene Planner Agent  
- Displays recommended AI tools per scene from Tool Selector Agent  
- Displays cost validation from Cost Guard Agent  
- Displays production progress from Execution Orchestrator  
- Displays final video download link from QA & Assembly Agent  

---

## Rules (VERY IMPORTANT)
- Must only send approved requests to Execution Orchestrator  
- Must prevent user from approving projects that exceed budget limits  
- Must refresh progress in real time or on refresh request  
- Must display clear error messages from any agent (Script, Scene Planner, Cost Guard, Tool Selector, Execution Orchestrator, QA & Assembly)  

---

## Failure Conditions
- Missing or invalid user input → ERROR: INVALID INPUT  
- User attempts to approve a project exceeding budget → ERROR: BUDGET EXCEEDED  
- UI cannot connect to backend agents → ERROR: CONNECTION FAILED
