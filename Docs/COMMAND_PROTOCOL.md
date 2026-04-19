# COMMAND PROTOCOL

## Purpose
This project uses a command hierarchy for structured multi-agent execution.

The hierarchy is:
User -> Leader Agent -> Specialist Agent -> Report -> Leader Agent -> User

## Core Rules
1. The user gives mission-level instructions only.
2. The Leader Agent translates missions into structured tasks.
3. Each specialist agent receives only a narrow, clearly bounded task.
4. Every specialist must return a structured report.
5. No specialist may expand scope beyond the assigned task.
6. No task is considered complete until verified.
7. The Leader Agent consolidates specialist reports into a final decision report.

## Leader Responsibilities
- Interpret the user's intent accurately
- Break missions into sub-tasks
- Assign the correct specialist
- Enforce scope boundaries
- Collect reports
- Identify blockers and risks
- Produce a final report for the user

## Specialist Responsibilities
- Execute only the assigned task
- State assumptions explicitly
- Report risks honestly
- Avoid system-wide changes unless explicitly authorized
- Return results in the required report format

## Completion Logic
A task is only complete when:
- the required deliverables exist
- the definition of done is satisfied
- risks are documented
- verification is documented

## Escalation Logic
A specialist must escalate to the Leader Agent if:
- a dependency is missing
- a scope conflict appears
- the task requires architectural change
- the task is not technically feasible as assigned