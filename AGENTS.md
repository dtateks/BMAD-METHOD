# AGENTS.md - BMad Method Repository

> AI agent instructions for the BMad Method monorepo. Read this file first, then sub-directory AGENTS.md files.

## Project Overview

**BMad Method** (Build More, Architect Dreams) - AI-Driven Agile Development framework built on **BMad Core** (Collaboration Optimized Reflection Engine).

| Attribute | Value |
|-----------|-------|
| Language | JavaScript (Node.js ≥20.0.0) |
| Package Manager | npm |
| Version | 6.0.0-alpha (see package.json) |
| License | MIT |

**Core Purpose**: 21 specialized AI agents across 4 modules, 50+ guided workflows for agile development from bug fixes to enterprise platforms.

## File Coordination

- **Root AGENTS.md** (this file): Applies to entire repository
- **src/AGENTS.md**: BMad content authoring (agents, workflows, modules)
- **tools/AGENTS.md**: CLI tools, build scripts, validation
- **test/AGENTS.md**: Testing infrastructure and fixtures
- **Rule**: Nearest AGENTS.md wins for local context; always read root first

## Build & Run Commands

```bash
# Installation
npm install                          # Install dependencies
npx bmad-method@alpha install        # Install BMad to a project

# Development
npm run lint                         # ESLint (JS, YAML)
npm run lint:fix                     # Auto-fix lint issues
npm run lint:md                      # Markdownlint
npm run format:check                 # Prettier check
npm run format:fix                   # Auto-format

# Build
npm run bundle                       # Build web bundles
npm run docs:build                   # Build documentation
npm run docs:dev                     # Dev server for docs
```

## Test & Quality Commands

```bash
# Full test suite (runs all below)
npm test

# Individual test commands
npm run test:schemas                 # Agent YAML schema tests
npm run test:install                 # Installation component tests
npm run validate:schemas             # Validate all agent YAML files
npm run test:coverage                # Run with coverage report
```

## Architecture & Code Structure

```
├── src/                             # BMad content (see src/AGENTS.md)
│   ├── core/                        # Core framework (always installed)
│   ├── modules/                     # Official modules (bmm, bmb, bmgd, cis)
│   └── utility/                     # Shared agent components
├── tools/                           # Build & CLI tools (see tools/AGENTS.md)
│   ├── cli/                         # BMad CLI installer
│   ├── flattener/                   # File flattening utilities
│   └── schema/                      # Agent schema validation
├── test/                            # Test suite (see test/AGENTS.md)
│   └── fixtures/                    # Test fixtures
├── docs/                            # User documentation (markdown)
├── samples/                         # Custom module examples
└── website/                         # Docusaurus site (generated)
```

## Coding Style & Conventions

**From ESLint config (`eslint.config.mjs`)**:

- Use `.yaml` extension (never `.yml`)
- Double quotes in YAML (`yml/quotes: prefer: double`)
- CommonJS allowed in `tools/**`, `test/**`, `_module-installer/**`
- Console logging allowed (CLI tool)
- Kebab-case for file names

**Agent YAML Schema**:

- All agents: `*.agent.yaml` format
- Triggers: kebab-case only (`dev-story`, not `devStory`)
- Validate before commit: `npm run validate:schemas`

## Environment & Secrets

- No environment variables required for development
- Node.js ≥20.0.0 required (see `.nvmrc`)
- Husky git hooks enabled (runs lint-staged on commit)

## Workflow & Common Tasks

| Task | Command/Action |
|------|----------------|
| Add new agent | Create `src/modules/{module}/agents/{name}.agent.yaml` |
| Add workflow | Create `src/modules/{module}/workflows/{category}/{name}/` |
| Validate changes | `npm run validate:schemas && npm run lint` |
| Format code | `npm run format:fix` |
| Run full CI | `npm test` |
| Build web bundles | `npm run bundle` |

**PR Workflow**: Submit to `main` for critical fixes only. See CONTRIBUTING.md for guidelines.

## Guidelines For AI Agents

### MUST DO

- Read `src/AGENTS.md` before editing any content in `src/`
- Run `npm run validate:schemas` after editing agent YAML files
- Follow existing file naming (kebab-case, `.yaml` not `.yml`)
- Keep agent personas lean and focused
- Use step-file architecture for complex workflows

### MUST AVOID

- **DO NOT** edit `_module-installer/` directories
- **DO NOT** use `.yml` extension for YAML files
- **DO NOT** add duplicate triggers within an agent
- **DO NOT** skip required agent schema fields
- **DO NOT** commit without running validation

### Path Variables in BMad Content

| Variable | Resolves To |
|----------|-------------|
| `{project-root}` | User's project root |
| `{output_folder}` | Configured output folder |
| `{user_name}` | User's configured name |

### Quick Validation Checklist

```bash
npm run validate:schemas   # Agent YAML structure
npm run lint               # Code style (JS + YAML)
npm run lint:md            # Markdown formatting
npm run format:check       # Prettier formatting
```
