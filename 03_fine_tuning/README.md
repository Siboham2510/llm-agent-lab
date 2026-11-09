# 03 — LLM Fine-tuning

## Objectives

Learn when model adaptation is appropriate, how to prepare training data, and how to evaluate fine-tuning against a clear baseline.

## Concepts to understand

- Hugging Face Transformers and Datasets
- Instruction data preparation and supervised fine-tuning (SFT)
- LoRA, QLoRA, quantization, and parameter-efficient fine-tuning
- Preference optimization, including Direct Preference Optimization (DPO)
- Training configuration, validation, overfitting, and model evaluation
- Model packaging and deployment considerations

## Planned implementations

- Inspect and validate a small instruction dataset.
- Establish a baseline evaluation before training.
- Prepare a cloud-GPU notebook for a small SFT run.
- Compare full fine-tuning concepts with LoRA/QLoRA workflows where feasible.
- Evaluate outputs consistently and document compute, limits, and reproducibility.

## Relevant technologies

Hugging Face Transformers, Datasets, PEFT, and cloud GPU notebooks (for example, Google Colab). These frameworks are not part of the initial local dependencies.

## Suggested progression

1. Learn dataset formats and evaluation design.
2. Run inference and record a baseline.
3. Use a cloud GPU for a small, bounded SFT exercise.
4. Study LoRA/QLoRA and compare results with the baseline.
5. Explore preference optimization only after understanding supervised workflows.

Do not expect GPU training to run in the local CPU-only environment.
