# 05 — Multi-Agent Systems

## Objectives

Study when coordinating specialized agents is useful, how to control workflow state, and how to evaluate the complete system.

## Concepts to understand

- Agent orchestration and workflow graphs
- Specialized agents and supervisor architectures
- Collaboration, shared state, and shared memory
- Workflow control, termination, and failure recovery
- Human-in-the-loop review and multi-agent evaluation

## Planned implementations

- Model a small workflow as explicit states and transitions.
- Compare a single-agent baseline with a supervised multi-agent design.
- Explore specialized roles and shared state with traceable handoffs.
- Add human review to selected workflow steps.
- Evaluate task success, latency, cost, and failure modes.

## Relevant technologies

Python and LangGraph; model/provider APIs and evaluation tools as needed.

## Suggested progression

1. Establish a single-agent baseline for a bounded task.
2. Represent the workflow and transitions explicitly.
3. Add a supervisor and one specialized agent.
4. Add shared state, failure handling, and human review.
5. Compare against the baseline and justify orchestration complexity.
