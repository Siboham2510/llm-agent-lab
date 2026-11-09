# LLM Agent Lab

A practical learning lab for understanding and building with large language models (LLMs), retrieval-augmented generation (RAG), fine-tuning, and AI agents. This repository is a long-term learning project: implementations, experiments, and evaluations will be added progressively as each topic is studied.

The goal is to understand the mathematics and engineering behind these systems—not just to call libraries. Early work emphasizes small, inspectable examples; larger training and inference workloads will use cloud GPUs when needed.

## Motivation and objectives

- Build a solid foundation in language modeling, transformers, attention, tokenization, embeddings, and inference.
- Develop complete RAG pipelines and evaluate retrieval and answer quality.
- Explore supervised fine-tuning and parameter-efficient methods using cloud GPU resources.
- Build reliable, personalized agents with memory, tools, structured outputs, and human approval.
- Study multi-agent orchestration and production-oriented deployment.
- Keep independent prototypes and comparisons separate from reusable module work.

## Learning roadmap

| Module | Focus | Learning outcomes |
| --- | --- | --- |
| [01 — LLM Fundamentals](./01_llm_fundamentals/README.md) | Language models, transformers, attention, tokenization, embeddings, prompting, and inference | Explain core concepts and experiment with generation and model APIs |
| [02 — RAG](./02_rag/README.md) | Ingestion, preprocessing, chunking, embeddings, retrieval, reranking, and evaluation | Build and measure end-to-end retrieval-augmented applications |
| [03 — Fine-tuning](./03_fine_tuning/README.md) | Datasets, SFT, LoRA/QLoRA, quantization, preference optimization, and evaluation | Prepare and evaluate fine-tuning workflows, using cloud GPUs when needed |
| [04 — Personalized AI Agents](./04_ai_agents/README.md) | Conversation context, memory, knowledge, tools, planning, and approvals | Compose useful agents with explicit boundaries and error handling |
| [05 — Multi-Agent Systems](./05_multi_agent_systems/README.md) | Orchestration, supervisors, collaboration, shared state, and human-in-the-loop workflows | Design and evaluate coordinated agent workflows |
| [06 — Deployment](./06_deployment/README.md) | APIs, user interfaces, serving, containers, cloud, monitoring, and security | Package and operate LLM-backed applications responsibly |
| [Experiments](./experiments/README.md) | Independent prototypes, benchmarks, and comparisons | Explore ideas without coupling them to reusable module implementations |

Progress through fundamentals before moving to retrieval, then model adaptation, agents, orchestration, and deployment. Each module README outlines its concepts, planned implementations, technologies, and suggested sequence. Not every topic has an implementation yet.

## Repository structure

```text
llm-agent-lab/
├── .vscode/                 # Shared editor settings
├── 01_llm_fundamentals/     # LLM concepts and foundational exercises
├── 02_rag/                  # Retrieval-augmented generation
├── 03_fine_tuning/          # Fine-tuning and evaluation
├── 04_ai_agents/            # Personalized agents
├── 05_multi_agent_systems/  # Agent orchestration
├── 06_deployment/           # Serving and operations
├── experiments/             # Independent prototypes and benchmarks
├── .env.example             # Blank environment-variable template
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt         # Small initial learning environment
```

Local `.env` files, downloaded datasets, model weights, checkpoints, caches, and generated artifacts are intentionally excluded from Git. Keep private data and credentials out of notebooks, source files, commits, and issue reports.

## Technology stack

The initial environment is intentionally small: Python 3.11, Jupyter, IPython kernel support, `python-dotenv`, pandas, NumPy, and Matplotlib. Later modules may introduce tools such as Hugging Face Transformers and Datasets, vector stores, LangGraph, FastAPI, and Streamlit when an implementation needs them. These larger dependencies are not installed by the initial requirements.

Use CPU-friendly examples for local learning. Plan to use a hosted notebook or another cloud GPU environment for workloads that require GPU acceleration; do not assume a dedicated GPU is available locally.

## Installation on Windows

Open PowerShell in the repository directory. The repository's `.venv` already exists in the current development environment; do not recreate or replace it. For a fresh clone only, create a virtual environment if one is not already present:

```powershell
py -3.11 -m venv .venv
```

Activate the existing environment:

```powershell
.\.venv\Scripts\Activate.ps1
```

If PowerShell blocks activation, follow the [Microsoft guidance for PowerShell execution policies](https://learn.microsoft.com/powershell/module/microsoft.powershell.core/about/about_execution_policies) for your machine or use the VS Code terminal configured to use `.venv\Scripts\python.exe`. Do not change system policy solely for this project without understanding the implications.

Install the starter dependencies:

```powershell
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

In VS Code, select `.venv\Scripts\python.exe` as the Python interpreter and use that environment as the Jupyter notebook kernel.

## Environment variables

Create a local `.env` file from the template, then add a provider key only when a specific exercise requires it:

```powershell
Copy-Item .env.example .env
```

Edit `.env` locally. Keep all values private: `.env` is ignored by Git, while `.env.example` contains empty placeholders and is safe to share. Never commit real API keys.

## Contribution and development workflow

1. Choose a module and read its learning objectives before implementing an exercise.
2. Keep reusable, documented implementations inside the relevant module; put disposable comparisons and prototypes in `experiments/`.
3. Use small, readable Python modules, meaningful names, type hints where useful, and PEP 8 conventions.
4. Include an evaluation or measurement when implementing an ML/LLM component. Record assumptions, limitations, and reproducibility details.
5. Keep credentials, private datasets, and model weights out of the repository. Review `git status` and staged changes before sharing work.
6. Add dependencies only when required by a concrete implementation, and document why they are needed.

## References and learning resources

- [Attention Is All You Need](https://arxiv.org/abs/1706.03762) — the Transformer architecture.
- [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) — visual introduction to attention and Transformers.
- [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course/) — tokenizers, Transformers, datasets, and model workflows.
- [Hugging Face PEFT documentation](https://huggingface.co/docs/peft/index) — parameter-efficient fine-tuning.
- [LangGraph documentation](https://docs.langchain.com/oss/python/langgraph/overview) — stateful agent orchestration.
- [FastAPI documentation](https://fastapi.tiangolo.com/) — Python API development.
- [Python documentation](https://docs.python.org/3.11/) — Python 3.11 language and standard library.

This roadmap is a guide, not a claim that every feature is already implemented. The repository will grow step by step, with an emphasis on understanding, practical work, and measured results.
