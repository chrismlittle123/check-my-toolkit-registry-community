# Check My Toolkit Registry - Community

A community registry of coding standards, linting rulesets, and prompts for consistent development practices across projects.

## Structure

```
├── code/
│   └── rulesets/          # Linting configurations
│       ├── prototype/     # Relaxed rules for rapid prototyping
│       ├── internal/      # Moderate rules for internal tools
│       └── production/    # Strict rules for production code
└── stack/
    └── prompts/           # Coding standards for AI assistants
        ├── prototype/     # Relaxed guidelines
        ├── internal/      # Moderate guidelines
        └── production/    # Strict guidelines
```

## Tiers

Each resource is organized into three tiers based on strictness:

| Tier | Purpose | Use Case |
|------|---------|----------|
| **prototype** | Relaxed rules | Rapid prototyping, experiments, POCs |
| **internal** | Moderate rules | Internal tools, services, team projects |
| **production** | Strict rules | Customer-facing, production-grade code |

## Supported Languages

### Python 3.12
- **Rulesets**: ruff configurations
- **Prompts**: Coding standards

### TypeScript 5.5
- **Rulesets**: ESLint and tsc configurations (Node.js 20)
- **Prompts**: Coding standards

## Usage

Resources are versioned and referenced via manifest files:
- `code/rulesets/rulesets.json` - Ruleset manifest
- `stack/prompts/prompts.json` - Prompts manifest

Each manifest includes version tracking with a `latest` pointer for easy reference.

## Contributing

When adding new resources:
1. Follow the existing directory structure: `{tier}/{language}/{version}/`
2. Use semantic versioning for new versions
3. Update the corresponding manifest file
4. Ensure file names use kebab-case
