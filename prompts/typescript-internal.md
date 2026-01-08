# TypeScript Coding Standards - Internal

Standards for internal tools, services, and team-facing applications.

## Tooling

- Use `pnpm` for package management.
- Use `eslint` for linting.
- Use `tsc --noEmit` for type checking.

## Imports

- Remove all unused imports.
- Sort imports: external dependencies, then internal modules.
- Use ES module imports (`import`/`export`), not CommonJS.

## Type Checking

- Run `tsc --noEmit` to verify type correctness.
- Add type annotations to all function signatures.
- Enable `strict: true` in tsconfig.json.
- Avoid `any` - prefer `unknown` with type guards.
- Avoid free strings, use enums or union types where appropriate.
- Avoid loose object types, use interfaces or type aliases for all object shapes.
- Use Zod schemas for runtime validation of external data.

## Error Handling

- Handle errors explicitly. Never swallow errors silently.
- Prefer `unknown` over `any` in catch clauses.

## Testing

- Every new feature must include unit tests and integration tests.
