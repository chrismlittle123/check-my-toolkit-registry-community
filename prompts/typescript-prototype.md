# TypeScript Coding Standards - Prototype

Guidelines for rapid prototyping and experimentation. Focus on speed over polish.

## Security

- Never commit secrets, API keys, or credentials to files. Use environment variables.

## Tooling

- Use `pnpm` for package management.
- Use `package.json` for project configuration.
- Use `.nvmrc` to specify Node.js version.

## Dependencies

- Pin versions with caret in `package.json` (e.g., `"express": "^4.18.0"`).
- Lockfile (`pnpm-lock.yaml`) is optional for prototypes.

## Imports

- Remove obviously unused imports.
- Import organization is flexible during prototyping.

## Type Checking

- Type annotations are optional but encouraged for public APIs.
- Running `tsc --noEmit` is optional but recommended before sharing code.
- Prefer `strict: false` in tsconfig.json for faster iteration.

## Error Handling

- Catch exceptions at main entry points to provide useful error messages.
- Let unexpected errors propagate with full stack traces for debugging.

## Testing

- Testing is optional for prototypes.
