<!-- Scoped to src/modules/cis/. Read root AGENTS.md and src/AGENTS.md first. -->

# AGENTS.md - Creative Intelligence Suite (CIS)

> Innovation and creative problem-solving workflows.

## Directory Overview

```
cis/
├── agents/                      # 6 creative agents
│   ├── brainstorming-coach.agent.yaml
│   ├── creative-problem-solver.agent.yaml
│   ├── design-thinking-coach.agent.yaml
│   ├── innovation-strategist.agent.yaml
│   ├── presentation-master.agent.yaml
│   └── storyteller/            # Storyteller agent (directory)
│       └── storyteller.agent.yaml
├── workflows/                   # Creative workflows
│   ├── design-thinking/        # Design thinking process
│   ├── innovation-strategy/    # Innovation planning
│   ├── problem-solving/        # Creative problem solving
│   ├── storytelling/           # Narrative development
│   └── README.md               # Workflow overview
├── teams/                       # Team configurations
│   ├── creative-squad.yaml
│   └── default-party.csv
├── docs/                        # Module documentation
├── _module-installer/           # DO NOT EDIT
└── module.yaml                  # Module configuration
```

## Agents

| Agent | Purpose |
|-------|---------|
| `brainstorming-coach` | Facilitates brainstorming sessions |
| `creative-problem-solver` | Tackles complex problems creatively |
| `design-thinking-coach` | Guides design thinking process |
| `innovation-strategist` | Strategic innovation planning |
| `presentation-master` | Presentation creation and coaching |
| `storyteller` | Narrative and story development |

## Workflows

### Design Thinking (`design-thinking/`)
5-phase design thinking process:
1. Empathize
2. Define
3. Ideate
4. Prototype
5. Test

### Innovation Strategy (`innovation-strategy/`)
Strategic innovation planning:
- Opportunity identification
- Innovation roadmap
- Implementation strategy

### Problem Solving (`problem-solving/`)
Creative problem-solving frameworks:
- Root cause analysis
- Solution generation
- Evaluation and selection

### Storytelling (`storytelling/`)
Narrative development:
- Story structure
- Character development
- Message crafting

## Module Configuration

CIS uses Core settings only:
- `user_name`
- `communication_language`
- `document_output_language`
- `output_folder`

No custom configuration required.

## Team Configurations

| Team | Purpose |
|------|---------|
| `creative-squad.yaml` | Full creative team |
| `default-party.csv` | Default agent party |

## Guidelines For AI Agents

### MUST DO

- Use appropriate creative framework for the task
- Follow workflow steps sequentially
- Encourage divergent thinking before convergence
- Document creative outputs properly

### MUST AVOID

- **DO NOT** rush creative processes
- **DO NOT** skip empathy/research phases
- **DO NOT** converge too early in ideation
- **DO NOT** edit `_module-installer/`

### Creative Process Principles

1. **Diverge before converge** - Generate many ideas first
2. **Defer judgment** - No criticism during ideation
3. **Build on ideas** - Yes, and... not no, but...
4. **Quantity breeds quality** - More ideas = better ideas
5. **Embrace ambiguity** - Comfort with uncertainty
