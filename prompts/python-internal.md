# Python Coding Standards - Internal

Standards for internal tools, services, and team-facing applications.

## Tooling

- Use `uv` for package management and virtual environments.
- Use `pyproject.toml` for project configuration.
- Use `ruff` for linting and formatting.

## Dependencies

- Pin versions compatibly in `pyproject.toml` (e.g., `requests~=2.28`).
- Commit `uv.lock` to ensure reproducible installs across the team.
- Use `uv sync` to install dependencies from lockfile.

## Imports

- Remove all unused imports.
- Sort imports: standard library, third-party, local.
- Use absolute imports over relative imports.

## Types

- Add type hints to all function signatures.
- Avoid free strings, use enums where appropriate.
- Avoid free dictionaries, use pydantic models for structured data.

## Error Handling

- Be specific with exception types. Avoid bare `except:` clauses.
- Use context managers (`with` statements) for resource management.

## Testing

- Every new feature must include unit tests and integration tests.
