<!-- Scoped to src/modules/bmm/. Read root AGENTS.md and src/AGENTS.md first. -->

# AGENTS.md - BMad Method (BMM)

> Primary agile development module with 9 agents and 34+ workflows.

## Directory Overview

```
bmm/
├── agents/                      # 9 specialized agents
├── workflows/                   # 4 phases + special workflows
│   ├── 1-analysis/             # Brainstorming, research
│   ├── 2-plan-workflows/       # PRD, tech-spec, GDD, UX
│   ├── 3-solutioning/          # Architecture, epics/stories
│   ├── 4-implementation/       # Sprint, dev-story, code-review
│   ├── bmad-quick-flow/        # Rapid development track
│   ├── testarch/               # Test architecture workflows
│   └── ...                     # Additional workflows
├── data/                        # Templates and standards
├── docs/                        # Module documentation
├── teams/                       # Team configurations
├── testarch/                    # Test architecture knowledge
├── _module-installer/           # DO NOT EDIT
└── module.yaml                  # Module configuration
```

## Agents

| Agent | File | Role |
|-------|------|------|
| Analyst | `analyst.agent.yaml` | Requirements analysis, research |
| Architect | `architect.agent.yaml` | System architecture design |
| Developer | `dev.agent.yaml` | Story implementation (Amelia) |
| PM | `pm.agent.yaml` | Product management, PRD creation |
| Quick Flow Solo Dev | `quick-flow-solo-dev.agent.yaml` | Rapid development (Barry) |
| Scrum Master | `sm.agent.yaml` | Sprint management |
| Test Architect | `tea.agent.yaml` | QA strategy, test patterns |
| Tech Writer | `tech-writer.agent.yaml` | Documentation |
| UX Designer | `ux-designer.agent.yaml` | UX/UI design |

## Workflow Phases

### Phase 1: Analysis (`1-analysis/`)
- Brainstorming sessions
- Research and exploration
- Product briefs

### Phase 2: Planning (`2-plan-workflows/`)
- PRD (Product Requirements Document)
- Technical specifications
- Game design documents (GDD)
- UX designs

### Phase 3: Solutioning (`3-solutioning/`)
- Architecture design
- Epic and story creation
- Technical approach

### Phase 4: Implementation (`4-implementation/`)
- Sprint planning
- Dev story execution
- Code review
- Retrospectives

### Special Workflows
- `bmad-quick-flow/` - Rapid development for small features
- `testarch/` - Test architecture and QA workflows

## Module Configuration

| Config Key | Purpose |
|------------|---------|
| `project_name` | Project title |
| `user_skill_level` | beginner/intermediate/expert |
| `planning_artifacts` | PRD, architecture output location |
| `implementation_artifacts` | Sprint, story files location |
| `project_knowledge` | Docs, research location |
| `tea_use_mcp_enhancements` | Test Architect MCP features |
| `tea_use_playwright_utils` | Playwright utils integration |

## Guidelines For AI Agents

### MUST DO

- Follow 4-phase methodology for new projects
- Use Quick Flow for small features/fixes
- Keep dev agent lean (coding context only)
- Use step-file architecture for complex workflows

### MUST AVOID

- **DO NOT** skip phases without understanding scope
- **DO NOT** bloat dev agent with documentation
- **DO NOT** edit `_module-installer/`
- **DO NOT** break workflow step sequences

### Agent Design Principles

1. **Single responsibility** - Each agent has one domain
2. **Lean personas** - Dev needs code context, not docs
3. **Clear triggers** - Unambiguous command shortcuts
4. **Workflow-driven** - Complex logic in workflows
