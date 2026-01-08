# Python Coding Standards - Prototype

Guidelines for rapid prototyping and experimentation. Focus on speed over polish.

## Security

- Never commit secrets, API keys, or credentials to files. Use environment variables.

## Tooling

- Use `uv` for package management and virtual environments.
- Use `pyproject.toml` for project configuration.
- Use `ruff` for linting.

## Dependencies

- Pin versions loosely in `pyproject.toml` (e.g., `requests>=2.28`).
- Lockfile (`uv.lock`) is optional for prototypes.

## Imports

- Remove obviously unused imports.
- Import organization is flexible during prototyping.

## Types

- Type hints are optional but encouraged for public APIs.

## Error Handling

- Catch exceptions at main entry points to provide useful error messages.
- Let unexpected errors propagate with full stack traces for debugging.
- Use context managers for resource management (files, connections).

## Testing

- Testing is optional for prototypes.
