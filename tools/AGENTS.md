<!-- Scoped to tools/ directory. Read root AGENTS.md first. -->

# AGENTS.md - Tools Directory

> Build tools, CLI installer, validation, and development utilities for BMad Method.

## Directory Overview

```
tools/
├── cli/                          # BMad CLI installer
│   ├── bmad-cli.js              # Main CLI entry point
│   └── bundlers/                # Web bundle builders
├── flattener/                    # File flattening utilities
│   └── main.js                  # Flatten agent/workflow files
├── schema/                       # Schema validation
│   └── agent.js                 # Zod-based agent YAML validator
├── lib/                          # Shared utilities
├── maintainer/                   # Internal maintenance scripts
├── build-docs.js                # Documentation builder
├── validate-agent-schema.js     # CLI wrapper for schema validation
└── bmad-npx-wrapper.js          # NPX entry point
```

## Build & Run Commands

```bash
# Schema validation
npm run validate:schemas          # Validate all *.agent.yaml files
node tools/validate-agent-schema.js

# Web bundles
npm run bundle                    # Build all web bundles
npm run rebundle                  # Rebuild existing bundles

# Documentation
npm run docs:build                # Build docs with Docusaurus
npm run docs:dev                  # Start docs dev server

# File flattening
npm run flatten                   # Run flattener utility

# Format workflow markdown
node tools/format-workflow-md.js <file>
```

## Key Components

### CLI Installer (`cli/`)

Main BMad installation tool invoked via `npx bmad-method install`.

- **bmad-cli.js**: Commander-based CLI with install commands
- **bundlers/**: Web bundle generation for ChatGPT/Claude/Gemini

### Schema Validation (`schema/`)

Zod-based validation for `*.agent.yaml` files.

- **agent.js**: Complete agent schema with validation rules
- Validates: metadata, persona, menu, triggers, commands, prompts
- Enforces: kebab-case triggers, required fields, module paths

### Flattener (`flattener/`)

Compiles agent YAML into single markdown files for IDE consumption.

- Resolves file references and paths
- Injects utility components from `src/utility/`
- Handles variable substitution (`{project-root}`, etc.)

## Coding Style & Conventions

**From ESLint config**:

- CommonJS patterns allowed (`unicorn/prefer-module: off`)
- Console logging allowed (CLI tool)
- No `no-unused-vars` errors (internal scripts)
- Process exit allowed (`n/no-process-exit: off`)

**File patterns**:

- Scripts: `*.js` (CommonJS for Node compatibility)
- Config: `*.yaml` (never `.yml`)

## Common Tasks

| Task | Command/File |
|------|--------------|
| Add new CLI command | Edit `cli/bmad-cli.js` |
| Add schema rule | Edit `schema/agent.js` |
| Add web bundle | Edit `cli/bundlers/bundle-web.js` |
| Add utility script | Create in `tools/` root |
| Update platform codes | Edit `platform-codes.yaml` |

## Guidelines For AI Agents

### MUST DO

- Test schema changes: `npm run validate:schemas`
- Keep CLI output user-friendly with chalk/ora
- Handle errors gracefully with clear messages
- Follow CommonJS patterns for Node compatibility

### MUST AVOID

- **DO NOT** break existing CLI commands
- **DO NOT** change schema without updating tests
- **DO NOT** hardcode absolute paths
- **DO NOT** add dependencies without checking package.json

### Schema Validation Rules

Agent triggers must be:
- Kebab-case only (`dev-story`, not `devStory`)
- Unique within agent (no duplicates)
- Non-empty strings

Command targets (one required):
- `workflow`, `exec`, `action`, `tmpl`, `data`, `validate-workflow`
