# Necromancer AI

**Persistent Goal Execution Engine**

> Bring goals to life — and keep them alive until real progress happens.

---

## Overview

**Necromancer AI** is a meta-agent system that accepts a real-world objective and continuously works toward it.

Instead of answering prompts or completing one-time tasks, the system **designs a workflow, executes it, verifies outcomes, adapts strategy, and repeats** until measurable progress occurs.

The user does not micromanage instructions.
The user delegates responsibility.

---

## What Makes It Different

Traditional AI:

* responds to messages
* stops when the conversation stops

Typical agents:

* execute a sequence once
* cannot reliably recover from failure

**Necromancer AI:**

* runs for days or weeks
* monitors real outcomes
* modifies its own plan
* continues operating in the background

It is not a chatbot.

It is an **autonomous execution system**.

---

## Core Idea

The LLM is **not the application**.

The LLM is a reasoning component inside a persistent control loop.

The real system is:

```
Goal → Plan → Execute → Verify → Adapt → Repeat
```

The AI thinks.
The platform remembers.
The workflow runs.

---

## System Architecture

The platform uses **one LLM operating in structured roles** rather than many independent chatting agents.

### 1) Necromancer (Supervisor)

The central controller.

Responsibilities:

* maintain goal state
* choose next action
* detect stagnation
* change strategies
* summon workers

This is the meta-agent.

---

### 2) Architect (Planner)

Converts a vague request into an operational objective.

Produces:

* milestones
* measurable success criteria
* structured workflow plan

It never executes actions.

---

### 3) Capability Builder

Creates reusable abilities (“rituals”).

Examples:

* web monitoring
* lead extraction
* document generation
* outreach workflows

It composes tools instead of writing arbitrary software.

---

### 4) Workers (Constructs)

Short-lived executors.

They:

* browse
* extract data
* write messages
* interact with services

They exist only for a task and are destroyed afterward.

---

### 5) Verifier (Judge)

Checks **reality**, not messages.

It determines:

* success
* failure
* partial progress

Examples:

* reply received
* meeting scheduled
* metric changed

This prevents hallucinated completion.

---

## Persistent Workflow

The workflow does **not** live in the LLM.

It is stored in the backend as structured state.

The agent proposes workflows.
The system runs them.

A workflow contains:

* goal definition
* stages
* current step
* history
* evidence
* metrics
* strategy version

This allows execution across restarts and long time periods.

---

## Execution Loop

1. User submits a goal
2. Architect creates plan
3. Workflow is saved
4. Supervisor schedules tasks
5. Workers act
6. Verifier checks outcomes
7. Supervisor adapts strategy
8. Repeat until goal condition is satisfied

---

## Experience Memory (Learning)

Completed workflows are saved as **experience**.

When a similar goal appears:

* past solutions are retrieved
* strategies are adapted
* success improves over time

The system learns *how problems are solved*, not personal data.

---

## Example Use Cases

* Job search automation
* Lead generation
* Research monitoring
* Learning plans
* Outreach campaigns
* Content publishing workflows

---

## Tech Stack (Suggested)

**Backend**

* Python + FastAPI

**LLM Provider**

* OpenAI compatible API

**Persistence**

* PostgreSQL — workflow state
* Redis — task queue
* Vector database — workflow experience retrieval

**Execution**

* Background workers (Celery / RQ / workers)
* Scheduler for periodic actions

---

## Design Principles

* Workflows are persistent
* Agents are temporary
* Evidence determines success
* Strategy can change
* The system must resume after interruption

---

## What This Is Not

* Not a chatbot
* Not a role-play multi-agent conversation
* Not a code-generating autonomous programmer
* Not a single-step automation script

It is a **self-adjusting operational system**.

---

## Project Goal

Build software that you can hand a real objective to and trust that progress will continue without constant supervision.

Necromancer AI does not assist.

It **operates**.

---

## Status

Early architecture and prototype phase.

Primary focus:

* reliability
* persistence
* verifiable outcomes
* adaptive workflows

---

## License

TBD
