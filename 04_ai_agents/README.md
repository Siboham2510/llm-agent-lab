# 04 — Personalized AI Agents

## Objectives

Build agents that can use context, knowledge, and tools reliably while making uncertainty and consequential actions explicit.

## Concepts to understand

- Conversation state, context management, and persistent memory
- Retrieval from a custom knowledge base
- Tool/API calls and controlled Python function execution
- Planning and multi-step task completion
- Structured outputs, validation, retries, and error handling
- Uncertainty, permissions, and human approval for consequential actions

## Planned implementations

- Create a small conversational workflow with explicit state.
- Add persistent memory and knowledge retrieval as separate components.
- Define typed tool inputs and validate structured model outputs.
- Handle tool failures and uncertain answers transparently.
- Gate consequential actions behind a human approval step.

## Relevant technologies

Python, provider APIs or open-weight models, Pydantic-style schema validation, retrieval components, and agent frameworks when they clarify rather than obscure behavior.

## Suggested progression

1. Start with a single-turn model call and explicit input/output types.
2. Add conversation state and tests for context handling.
3. Add one safe, deterministic tool and clear error paths.
4. Introduce memory and knowledge retrieval.
5. Add planning and human approval only with evaluation and safeguards.
