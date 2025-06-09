**GitHub Models Prompt File**
- a YAML file with a `.prompt.yaml` or `.prompt.yml` file extension
- An example GitHub Models prompt file is found in [/docs/gh-sample.prompt.yml](/docs/gh-sample.prompt.yml)
- A GitHub Models prompt file has two key parts:
  - Runtime information (required)
    - Prompt templates (system, user, etc.) using simple {{variable}} placeholders
  - Development information (optional)
    - Human-readable name and description
    - Model identifier and parameters
    - Sample data for testing and evaluations
    - Data describing the evaluators themselves

Sample Prompt File (`text-extractor.prompt.yml`):
```yaml
name: Text Summarizer
description: Summarizes any input text concisely with a standardized "Summary -" prefix format.
model: gpt-4o-mini
modelParameters:
  temperature: 0.5
messages:
  - role: system
    content: You are a text summarizer. Your only job is to summarize text given to you.
  - role: user
    content: |
      Summarize the given text, beginning with "Summary -":
      <text>
      {{input}}
      </text>
testData:
  - input: |
      The quick brown fox jumped over the lazy dog.
      The dog was too tired to react.
    expected: Summary - A fox jumped over a lazy, unresponsive dog.
evaluators:
  - name: Output should start with 'Summary -'
    string:
      startsWith: 'Summary -'
```