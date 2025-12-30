<!-- Scoped to src/core/. Read root AGENTS.md and src/AGENTS.md first. -->

# AGENTS.md - BMad Core

> Foundation framework always installed with any BMad module.

## Directory Overview

```
core/
├── agents/                      # Core agents
│   └── bmad-master.agent.yaml  # Master orchestrator agent
├── resources/                   # Shared resources
│   └── excalidraw/             # Diagram templates and helpers
├── tasks/                       # Task definitions (XML)
│   ├── advanced-elicitation.xml
│   ├── index-docs.xml
│   ├── review-adversarial-general.xml
│   ├── validate-workflow.xml
│   └── workflow.xml
├── tools/                       # Tool definitions
│   └── shard-doc.xml           # Document sharding tool
├── workflows/                   # Core workflows
│   ├── brainstorming/          # Brainstorming session workflow
│   └── party-mode/             # Multi-agent party mode
├── _module-installer/           # DO NOT EDIT - Installation scripts
└── module.yaml                  # Core configuration prompts
```

## Core Configuration (`module.yaml`)

Defines installation prompts for all BMad installations:

| Config Key | Purpose | Default |
|------------|---------|---------|
| `user_name` | What agents call the user | `BMad` |
| `communication_language` | Chat language/style | `English` |
| `document_output_language` | Document output language | `English` |
| `output_folder` | Default output location | `_bmad-output` |

## Core Agent

**bmad-master.agent.yaml** - Master orchestrator that:
- Coordinates between specialized agents
- Routes requests to appropriate agents
- Handles cross-module interactions

## Core Tasks (XML)

| Task | Purpose |
|------|---------|
| `advanced-elicitation.xml` | Advanced questioning techniques |
| `index-docs.xml` | Document indexing |
| `review-adversarial-general.xml` | Adversarial review patterns |
| `validate-workflow.xml` | Workflow structure validation |
| `workflow.xml` | Core workflow execution logic |

## Core Workflows

### Brainstorming (`workflows/brainstorming/`)

Step-file workflow for guided brainstorming sessions:
- `brain-methods.csv` - Available brainstorming methods
- `template.md` - Session output template
- `steps/` - Sequential step files

### Party Mode (`workflows/party-mode/`)

Multi-agent collaboration workflow:
- Coordinates multiple agents working together
- Agent loading and handoff patterns

## Coding Conventions

- **XML for tasks/tools**: Define reusable logic
- **YAML for workflows**: Step-file architecture
- **Markdown for steps**: Step content with frontmatter

## Guidelines For AI Agents

### MUST DO

- Preserve core config variables when editing `module.yaml`
- Follow XML schema for tasks/tools
- Use step-file architecture for workflows
- Test changes with `npm run validate:schemas`

### MUST AVOID

- **DO NOT** edit `_module-installer/` directory
- **DO NOT** remove core config prompts
- **DO NOT** break path variable resolution
- **DO NOT** modify bmad-master without understanding orchestration

### Path Variables (Defined Here)

| Variable | Set In | Resolves To |
|----------|--------|-------------|
| `{project-root}` | installer | User's project root |
| `{output_folder}` | core config | Default output location |
| `{user_name}` | core config | User's display name |
| `{communication_language}` | core config | Chat language |
| `{document_output_language}` | core config | Document language |
