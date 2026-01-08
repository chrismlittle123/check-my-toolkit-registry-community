# Python Coding Standards - Production

Strict standards for production-grade, customer-facing code.

## Tooling

- Use `uv` for package management and virtual environments.
- Use `pyproject.toml` for project configuration.
- Use `ruff` for linting and formatting.

## Dependencies

- Pin versions exactly in `pyproject.toml` (e.g., `requests==2.31.0`).
- Commit `uv.lock` to ensure deterministic builds.
- Use `uv sync --frozen` in CI/CD to fail if lockfile is out of date.

## Containers

- Use Docker for all production deployments.
- Use `uv sync --frozen` in Dockerfile for reproducible builds.
- Pin Python version explicitly in Dockerfile base image.

## Imports

- Remove all unused imports.
- Sort imports: standard library, third-party, local.
- Use absolute imports over relative imports.
- Group imports with blank lines between groups.

## Types

- Add type hints to ALL function signatures (public and private).
- Use built-in generics (`list[str]`, `dict[str, int]`) instead of `typing.List`, `typing.Dict`.
- Avoid free strings, use enums where appropriate.
- Avoid free dictionaries, use pydantic models for structured data.

## Error Handling

- Be specific with exception types. NEVER use bare `except:` clauses.
- Use context managers (`with` statements) for resource management.

## Security

- Never log sensitive data (passwords, tokens, PII).
- Validate all external inputs.
- Use parameterized queries for database operations.
- Avoid `eval()`, `exec()`, and dynamic code execution.

## Testing

- Every new feature must include unit tests and integration tests.
