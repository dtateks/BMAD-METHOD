<!-- Scoped to src/utility/. Read root AGENTS.md and src/AGENTS.md first. -->

# AGENTS.md - Utility Components

> Shared components injected during agent compilation.

## Directory Overview

```
utility/
└── agent-components/            # Templates for compiled agents
    ├── activation-rules.txt     # Agent activation logic
    ├── activation-steps.txt     # Step-by-step activation
    ├── agent-command-header.md  # Standard command header
    ├── agent.customize.template.yaml  # Customization template
    ├── handler-action.txt       # Action command handler
    ├── handler-data.txt         # Data loading handler
    ├── handler-exec.txt         # Exec command handler
    ├── handler-multi.txt        # Multi-command handler
    ├── handler-tmpl.txt         # Template handler
    ├── handler-validate-workflow.txt  # Workflow validation
    ├── handler-workflow.txt     # Workflow execution handler
    └── menu-handlers.txt        # Menu handler dispatcher
```

## Purpose

These components are **injected into compiled agents** during the flattening/compilation process. They provide:

1. **Consistent behavior** across all agents
2. **DRY principle** - shared logic not duplicated
3. **Maintainability** - update once, applies everywhere

## Component Types

### Activation Components

| File | Purpose |
|------|---------|
| `activation-rules.txt` | Rules for when agent activates |
| `activation-steps.txt` | Steps agent follows on activation |

### Command Handlers

| File | Handles | Description |
|------|---------|-------------|
| `handler-workflow.txt` | `workflow:` | Execute YAML workflow |
| `handler-exec.txt` | `exec:` | Execute markdown file |
| `handler-action.txt` | `action:` | Inline action |
| `handler-tmpl.txt` | `tmpl:` | Template processing |
| `handler-data.txt` | `data:` | Load data file |
| `handler-validate-workflow.txt` | `validate-workflow:` | Validate workflow |
| `handler-multi.txt` | Multiple targets | Handle multiple commands |

### Structural Components

| File | Purpose |
|------|---------|
| `agent-command-header.md` | Standard header for commands |
| `menu-handlers.txt` | Dispatcher for menu commands |
| `agent.customize.template.yaml` | User customization template |

## How Compilation Works

1. **Agent YAML** is read (`*.agent.yaml`)
2. **Flattener** processes the agent
3. **Utility components** are injected based on:
   - Menu command types present
   - Agent configuration flags
4. **Compiled markdown** is output to `_bmad/`

## Guidelines For AI Agents

### MUST DO

- Understand injection points before editing
- Test changes with full agent compilation
- Keep handlers minimal and focused
- Maintain backward compatibility

### MUST AVOID

- **DO NOT** add agent-specific logic here
- **DO NOT** break handler signatures
- **DO NOT** remove required components
- **DO NOT** add complex logic (keep simple)

### Testing Changes

```bash
# After modifying utility components:
npm run bundle           # Rebuild web bundles
npm run validate:schemas # Validate all agents

# Test with actual agent compilation
npx bmad-method install  # In a test project
```

### Handler Template Pattern

Handlers follow this pattern:
```
[Condition/Trigger]
[Action to take]
[Expected behavior]
```

Keep handlers:
- **Declarative** - What to do, not how
- **Minimal** - Single responsibility
- **Clear** - Easy to understand intent
