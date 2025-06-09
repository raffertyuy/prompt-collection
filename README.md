# Prompt Collection: GitHub Models Format

This repository contains my personal collection of prompts for Large Language Models (LLMs), all stored in the standardized GitHub Models prompt file format (`*.prompt.yaml`).

## About the Collection

- Prompts are organized by use case and domain (e.g., chat, completion, persona-systemprompts).
- All prompts follow the GitHub Models schema for clarity, reusability, and compatibility with modern LLM workflows.
- The collection includes prompts sourced from open-source projects, community contributions, and original work.

## File Structure

- **chat/**: Prompts for conversational agents across various industries.
- **completion/**: Prompts for text generation, summarization, extraction, and more.
- **persona-systemprompts/**: System and persona prompts for role-based LLM behavior.
- **docs/**: Example prompt files and schema references.

## Prompt File Format

All prompts use the `.prompt.yaml` extension and conform to the GitHub Models prompt schema, which includes:

- **Runtime information**: Prompt templates (system, user, etc.) with `{{variable}}` placeholders.
- **Development information** (optional): Name, description, model parameters, sample data, and evaluation metadata.

See `docs/gh-sample.prompt.yaml` for a detailed example.

## Contributing

Contributions are welcome! Please ensure new prompts follow the GitHub Models format and include clear descriptions and sample data where possible.

## License

See [LICENSE](LICENSE) for details.