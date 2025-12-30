# AGENTS.md - BMad Source Directory

> AI agent instructions for `src/` directory. This is where all BMad content lives.

## Directory Overview

```
src/
├── core/                    # BMad Core framework (always installed)
├── modules/                 # Official modules (user-selectable)
│   ├── bmm/                # BMad Method - Agile development (main module)
│   ├── bmb/                # BMad Builder - Create custom agents/workflows
│   ├── bmgd/               # BMad Game Dev - Game development
│   └── cis/                # Creative Intelligence Suite
└── utility/                 # Shared components for agent compilation
```

## Core (`src/core/`)

Foundation framework - always installed with any module.

| Directory | Purpose |
|-----------|---------|
| `agents/` | Core agents (`bmad-master.agent.yaml` - orchestrator) |
| `resources/` | Shared resources (excalidraw templates) |
| `tasks/` | Task definitions (XML: validation, workflow, shard-doc) |
| `workflows/` | Core workflows (brainstorming, party-mode, advanced-elicitation) |
| `_module-installer/` | **DO NOT EDIT** - Installation scripts |
| `module.yaml` | Core config prompts (user_name, language, output_folder) |

> **Note**: `core/tools/` deprecated - `shard-doc.xml` moved to `tasks/`. Advanced elicitation moved from `tasks/` to `workflows/advanced-elicitation/`.

## Modules (`src/modules/`)

### BMM - BMad Method (`src/modules/bmm/`)

Primary agile development module with 9 agents and 34+ workflows.

**Agents** (`agents/`):

| Agent | Role |
|-------|------|
| `analyst` | Requirements analysis, research |
| `architect` | System architecture design |
| `dev` | Story implementation (Amelia) |
| `pm` | Product management, PRD creation |
| `quick-flow-solo-dev` | Rapid development (Barry) |
| `sm` | Scrum Master, sprint management |
| `tea` | Test Architect, QA strategy |
| `tech-writer` | Documentation |
| `ux-designer` | UX/UI design |

**Workflows** (`workflows/`):

| Phase | Directory | Purpose |
|-------|-----------|---------|
| 1 | `1-analysis/` | Brainstorming, research, product briefs |
| 2 | `2-plan-workflows/` | PRD, tech-spec, GDD, narrative, UX |
| 3 | `3-solutioning/` | Architecture, epics/stories creation |
| 4 | `4-implementation/` | Sprint planning, dev-story, code-review |
| - | `bmad-quick-flow/` | Rapid development track |
| - | `testarch/` | Test architecture workflows |

**Other Directories**:

- `data/` - Templates (project-context, documentation-standards)
- `teams/` - Team configurations
- `docs/` - Module documentation (migrated to website - may be empty)
- `testarch/` - Test architecture knowledge base

### BMB - BMad Builder (`src/modules/bmb/`)

Create custom agents, workflows, and modules.

**Agents**: `agent-builder`, `module-builder`, `workflow-builder`

**Workflows**:

- `create-agent/` - 11-step agent creation
- `create-workflow/` - 12-step workflow creation
- `create-module/` - Module creation
- `edit-agent/`, `edit-workflow/` - Modification workflows
- `workflow-compliance-check/` - Validation

**Reference**: `reference/` - Example agents (simple, expert, module types)

### BMGD - BMad Game Dev (`src/modules/bmgd/`)

Game development module.

**Agents**: `game-architect`, `game-designer`, `game-dev`, `game-qa`, `game-scrum-master`, `game-solo-dev`

### CIS - Creative Intelligence Suite (`src/modules/cis/`)

Innovation and creative workflows.

**Agents**: `brainstorming-coach`, `creative-problem-solver`, `design-thinking-coach`, `innovation-strategist`, `presentation-master`, `storyteller/`

## Utility (`src/utility/`)

Shared components injected during agent compilation.

**`agent-components/`** - Templates injected into compiled agents:

- `activation-rules.txt`, `activation-steps.txt` - Agent activation
- `handler-*.txt` - Menu command handlers (workflow, exec, action, tmpl, data)
- `agent-command-header.md` - Standard agent header
- `agent.customize.template.yaml` - Customization template

## Agent YAML Schema

All agents use `*.agent.yaml` format with strict schema validation.

```yaml
agent:
  metadata:
    id: "_bmad/{module}/agents/{name}.md"  # Compiled output path
    name: "Display Name"
    title: "Agent Title"
    icon: "🤖"
    module: bmm  # Required for module agents, omit for core

  persona:
    role: "Role description"
    identity: "Who the agent is"
    communication_style: "How it communicates"
    principles: |
      - Principle 1
      - Principle 2

  critical_actions:  # Optional - actions on activation
    - "Load config file..."
    - "Remember user name..."

  menu:  # Required - at least one entry
    - trigger: "DS or dev-story or fuzzy match on dev story"
      workflow: "{project-root}/_bmad/bmm/workflows/..."
      description: "[DS] Description"

  webskip: true  # Optional - skip in web bundles
  discussion: true  # Optional - enable conversational mode
```

**Trigger Format**: kebab-case only (`dev-story`, `code-review`)

**Command Types**:

| Type | Use |
|------|-----|
| `workflow` | Execute YAML workflow |
| `exec` | Execute markdown file |
| `action` | Inline action description |
| `tmpl` | Template processing |
| `data` | Load data file |
| `validate-workflow` | Validate workflow structure |

## Workflow Structure

**Step-file architecture** for complex workflows:

```
workflow-name/
├── workflow.yaml          # Main workflow definition
├── steps/
│   ├── step-01-init.md
│   ├── step-02-analyze.md
│   └── ...
├── data/                  # Reference data
└── templates/             # Output templates
```

**Simple workflows**: Single `workflow.md` or `workflow.yaml` file.

## File Naming Conventions

| Type | Pattern | Example |
|------|---------|---------|
| Agent | `{name}.agent.yaml` | `dev.agent.yaml` |
| Workflow (YAML) | `workflow.yaml` | `workflow.yaml` |
| Workflow (MD) | `workflow.md` | `workflow.md` |
| Step file | `step-{NN}-{name}.md` | `step-01-init.md` |
| Task | `{name}.xml` | `validate-workflow.xml` |
| Tool | `{name}.xml` | `shard-doc.xml` |
| Data | `{name}.md/.csv/.yaml` | `project-context-template.md` |

## Module Configuration

Each module has `module.yaml` defining installation prompts:

```yaml
code: bmm
name: "BMM: BMad Method"
default_selected: true

# Config prompts
project_name:
  prompt: "What is the title of your project?"
  default: "{directory_name}"
  result: "{value}"

planning_artifacts:
  prompt: "Where should artifacts be stored?"
  default: "{output_folder}/project-planning-artifacts"
  result: "{project-root}/{value}"
```

## Editing Guidelines

### MUST DO

- Follow existing agent YAML schema exactly
- Use kebab-case for all file names
- Keep agent personas lean and focused
- Test with schema validation after changes
- Follow step-file architecture for complex workflows

### MUST AVOID

- **DO NOT** edit `_module-installer/` directories
- **DO NOT** use `.yml` extension (use `.yaml`)
- **DO NOT** add duplicate triggers within an agent
- **DO NOT** skip required schema fields
- **DO NOT** break existing workflow step sequences

### Agent Design Principles

1. **Single responsibility** - Each agent has one primary domain
2. **Lean personas** - Dev agents need context for coding, not docs
3. **Clear triggers** - Unambiguous command shortcuts
4. **Workflow-driven** - Complex logic in workflows, not agent persona

### Workflow Design Principles

1. **Step-file for complexity** - Break large workflows into steps
2. **JIT loading** - Only current step in memory
3. **Sequential enforcement** - No skipping steps
4. **State tracking** - Progress in frontmatter

## Path Variables

Used in agent/workflow definitions:

| Variable | Resolves To |
|----------|-------------|
| `{project-root}` | User's project root |
| `{output_folder}` | Configured output folder |
| `{user_name}` | User's configured name |
| `{communication_language}` | Chat language |
| `{document_output_language}` | Document language |

## Validation

Before committing changes to `src/`:

```bash
# From repo root
npm run validate:schemas   # Validate all agent YAML files
npm run test:schemas       # Run schema test suite
npm run lint               # ESLint (includes YAML)
npm run format:check       # Prettier check
```

## Quick Reference

| Task | Location |
|------|----------|
| Add new agent to BMM | `src/modules/bmm/agents/{name}.agent.yaml` |
| Add new workflow to BMM | `src/modules/bmm/workflows/{category}/{name}/` |
| Add core workflow | `src/core/workflows/{name}/` |
| Add shared task | `src/core/tasks/{name}.xml` |
| Modify agent template | `src/utility/agent-components/` |
| Create custom module | Use BMB `create-module` workflow |
