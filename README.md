# MarketSignal

A planned stock-forecasting research project built through a clarification-first, orchestrator-led agent workflow.

## Project status

This repository is being specified. The documents describe the intended project and working process; they do not mean that any application, skill, subagent, integration, or test has already been implemented.

The first activity is a requirements conversation with the user, not automatic implementation.

## Intended product

The project may combine:

- Market-price ingestion and validation.
- Time-series feature engineering.
- Machine-learning forecasting and chronological evaluation.
- Experiment tracking and a prediction API.
- Financial-news relevance and sentiment.
- Model lifecycle automation and monitoring.
- Controlled IBKR paper-trading integration.

The exact scope, instruments, prediction target, tools, and acceptance criteria must be confirmed with the user. This project does not promise profitable forecasts or production readiness.

The separate B2B lead-generation idea is not part of this project unless explicitly added.

## Agent architecture

```text
User: vision, requirements, decisions, approval
                         |
                         v
                   Orchestrator
       Clarification, planning, decomposition, delegation,
       workspace skills, review, critique, progress tracking
                         |
             +-----------+-----------+
             |           |           |
             v           v           v
         Subagent 1  Subagent 2  Subagent 3
         Specialist  Specialist  Specialist
             |           |           |
             +-----------+-----------+
                         |
                         v
                Deliverables and evidence
                         |
                         v
               Critique and revision loop
```

The main agent the user chats with is the orchestrator. It does not write application code, tests, or implementation scripts. Specialist subagents do that work. The orchestrator may maintain planning documents, skill instructions, and agent definitions.

Use three specialist roles, with no more than three active specialist subagents at once. The roles are agreed with the user and can be reassigned between the project's two stages. Do not invent agent execution if the environment lacks subagent support.

## Documents

- `PROJECT_GOAL.md`: the user's intended product, workflow, and decision boundaries.
- `AGENTS.md`: operational instructions for agents working in this repository.
- `README.md`: a human-readable introduction and starting procedure.

Planning records, task specifications, skills, and agent definitions will be created after clarification. Their absence at this point is expected.

## Start in VS Code

1. Open the local repository folder.
2. Save these three documents in its top-level directory.
3. Inspect any existing instructions for conflicts before replacing them.
4. Open the Codex extension and start a new project conversation.
5. Paste the following prompt.

```text
Read AGENTS.md and PROJECT_GOAL.md in full.

You are the orchestrator, not an implementation agent.

First:
- Summarize your understanding of my intended outcome.
- Inspect existing project instructions for conflicts.
- Ask focused questions about unresolved requirements.
- Tell me how to provide the two external skills:
  a planning skill and a skill-creation skill.

Do not change application code or launch implementation yet.
Confirm Stage 1 scope, specialist roles, and acceptance criteria with me.
```

## External skills

The user will supply a planning skill and a skill-creation skill. They are not bundled with these documents. The orchestrator must inspect them, check compatibility and safety, and explain how they will be used before installing, adapting, or executing their supporting code.

## Two-stage progression

Stage boundaries and specialist allocation are not yet confirmed. A possible division is core forecasting first, followed by selected news, operations, and paper-trading extensions. Treat this as a discussion proposal, not authorization to build everything.

Before a stage transition, review acceptance evidence, resolve or explicitly defer open issues, preserve handovers, and obtain the user's agreement on the next stage. Retiring a subagent does not mean deleting its deliverables.

## Safety and verification

- Ask before making consequential assumptions.
- Offer options when the user says they do not know.
- Do not expose or commit credentials.
- Do not silently spend, publish, deploy, or perform broker actions.
- Never connect to or execute against a live-money trading account within this scope.
- Report actual tests, measurements, and agent activity, not planned or imagined results.
- Preserve the user's ability to inspect, approve, and stop the workflow.

Installation and execution commands will be added when the implementation and environment are confirmed. Do not treat an untested example command as an established setup procedure.
