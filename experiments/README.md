# Experiments

## Objectives

Provide a separate space for independent prototypes, benchmarks, comparisons, and ideas that are not yet reusable module implementations.

## Concepts to understand

- Forming a testable hypothesis and choosing a baseline
- Reproducible inputs, configurations, and evaluation measures
- Comparing quality, latency, resource use, and cost
- Recording limitations and deciding when an experiment is ready to graduate into a module

## Planned implementations

- Small, isolated notebooks and prototypes
- Comparative benchmarks for prompts, models, retrieval settings, or agent workflows
- Short experiment notes alongside the relevant code or notebook

## Relevant technologies

Python, Jupyter, and only the libraries required by a specific experiment.

## Suggested progression

1. State the question and expected measurement.
2. Keep the experiment self-contained and use a documented baseline.
3. Record environment, data provenance, configuration, and results.
4. Avoid committing secrets, private datasets, or model weights.
5. Move stable, reusable work into its relevant numbered module.
