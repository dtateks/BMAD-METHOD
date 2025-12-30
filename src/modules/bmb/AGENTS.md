<!-- Scoped to src/modules/bmb/. Read root AGENTS.md and src/AGENTS.md first. -->

# AGENTS.md - BMad Builder (BMB)

> Module for creating custom agents, workflows, and modules.

## Directory Overview

```
bmb/
├── agents/                      # Builder agents
│   ├── agent-builder.agent.yaml
│   ├── workflow-builder.agent.yaml
│   └── module-builder.agent.yaml
├── workflows/                   # Creation workflows
│   ├── create-agent/           # 11-step agent creation
│   ├── create-workflow/        # Workflow creation
│   ├── create-module/          # Module creation
│   ├── edit-agent/             # Agent modification
│   ├── edit-workflow/          # Workflow modification
│   └── workflow-compliance-check/
├── reference/                   # Example agents
│   ├── agents/simple-examples/
│   └── workflows/
├── docs/                        # Builder documentation
├── workflows-legacy/            # Deprecated workflows
└── module.yaml                  # Module configuration
```

## Agents

| Agent | Purpose |
|-------|---------|
| `agent-builder` | Creates new custom agents |
| `workflow-builder` | Creates new workflows |
| `module-builder` | Creates complete modules |

## Key Workflows

### Create Agent (`create-agent/`)

11-step workflow for agent creation:
1. Requirements gathering
2. Persona definition
3. Menu command design
4. Trigger configuration
5. ... (see workflow for full steps)

**Output**: Valid `*.agent.yaml` file

### Create Workflow (`create-workflow/`)

Workflow for creating step-file or simple workflows:
- Defines workflow structure
- Creates step files
- Sets up data/templates

### Create Module (`create-module/`)

Complete module creation:
- Module configuration (`module.yaml`)
- Agent definitions
- Workflow structure
- Documentation

## Reference Examples (`reference/`)

Example agents for learning:

| Type | Location | Use For |
|------|----------|---------|
| Simple | `agents/simple-examples/` | Basic single-purpose agents |
| Expert | (in create-agent/data) | Complex domain agents |
| Module | (in create-agent/data) | Agents within modules |

## Module Configuration

| Config Key | Purpose |
|------------|---------|
| `bmb_creations_output_folder` | Where generated content is saved |

Default: `{output_folder}/bmb-creations`

## Guidelines For AI Agents

### MUST DO

- Use create-agent workflow for new agents
- Follow agent YAML schema strictly
- Validate with `npm run validate:schemas`
- Reference examples in `reference/` directory

### MUST AVOID

- **DO NOT** skip workflow steps
- **DO NOT** create agents without proper triggers
- **DO NOT** use non-kebab-case triggers
- **DO NOT** duplicate trigger names within agent

### Agent Schema Requirements

```yaml
agent:
  metadata:
    id: "_bmad/{module}/agents/{name}.md"
    name: "Display Name"
    title: "Agent Title"
    icon: "🤖"
    module: bmm  # Required for module agents
  persona:
    role: "..."
    identity: "..."
    communication_style: "..."
    principles: |
      - Principle 1
  menu:
    - trigger: "kebab-case-trigger"
      workflow: "{path}"
      description: "[TRG] Description"
```

### Trigger Rules

- Kebab-case only: `dev-story`, `code-review`
- No spaces, underscores, or camelCase
- Unique within agent
- Non-empty strings
