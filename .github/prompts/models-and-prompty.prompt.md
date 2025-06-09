---
mode: 'agent'
description: 'Converts a prompty file to a GitHub Models prompt file (or vice versa)'
---

Prompty files (`*.prompty`) and GitHub Model prompt files (`*.prompt.yaml` or `*.prompt.yml`) are different ways to store LLM prompts.

**Prompty File**
- A YAML file with a `.prompty` file extension
- The schema is defined in [/docs/prompty-schema.yaml](/docs/prompty-schema.yaml)
- An example Prompty file is found in [/docs/prompty-sample.prompty](/docs/prompty-sample.prompty)

**GitHub Models Prompt File**
- a YAML file with a `.prompt.yaml` or `.prompt.yml` file extension
- An example GitHub Models prompt file is found in [/docs/gh-sample.prompt.yaml](/docs/gh-sample.prompt.yaml)
- A GitHub Models prompt file has two key parts:
  - Runtime information (required)
    - Prompt templates (system, user, etc.) using simple {{variable}} placeholders
  - Development information (optional)
    - Human-readable name and description
    - Model identifier and parameters
    - Sample data for testing and evaluations
    - Data describing the evaluators themselves