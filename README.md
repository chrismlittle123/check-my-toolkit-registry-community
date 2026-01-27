# Standards Community Registry

Community standards for [@standards-kit/conform](https://github.com/chrismlittle123/standards-kit).

## Structure

```
├── prompts/           # Coding guidelines (markdown)
│   ├── python-prototype.md
│   ├── python-internal.md
│   ├── python-production.md
│   ├── typescript-prototype.md
│   ├── typescript-internal.md
│   └── typescript-production.md
│
├── rulesets/          # check.toml configs
│   ├── python-prototype.toml
│   ├── python-internal.toml
│   ├── python-production.toml
│   ├── typescript-prototype.toml
│   ├── typescript-internal.toml
│   └── typescript-production.toml
│
└── README.md
```

## Tiers

| Tier | Purpose |
|------|---------|
| **prototype** | Rapid prototyping, experiments |
| **internal** | Internal tools, team projects |
| **production** | Customer-facing, production code |

## Prompts

Markdown coding standards for humans and AI assistants.

## Rulesets

`check.toml` configurations for @standards-kit/conform. Copy or reference these in your project.

Example `check.toml`:
```toml
# Copy the contents of rulesets/python-production.toml
# or use extends when supported:
# [extends]
# base = "github:chrismlittle123/standards-community/rulesets/python-production.toml"
```

## Contributing

Add new standards following the `{language}-{tier}` naming convention.
