<!-- Scoped to src/modules/bmgd/. Read root AGENTS.md and src/AGENTS.md first. -->

# AGENTS.md - BMad Game Development (BMGD)

> Game development module with specialized agents for game creation workflows.

## Directory Overview

```
bmgd/
├── agents/                      # 6 game dev agents
│   ├── game-architect.agent.yaml
│   ├── game-designer.agent.yaml
│   ├── game-dev.agent.yaml
│   ├── game-qa.agent.yaml
│   ├── game-scrum-master.agent.yaml
│   └── game-solo-dev.agent.yaml
├── workflows/                   # Game dev workflows
│   ├── 1-preproduction/        # Concept, planning
│   ├── 2-design/               # GDD, mechanics
│   ├── 3-technical/            # Architecture, systems
│   ├── 4-production/           # Implementation
│   ├── bmgd-quick-flow/        # Rapid game dev
│   ├── gametest/               # QA workflows
│   └── workflow-status/        # Progress tracking
├── gametest/                    # Game QA knowledge base
│   └── knowledge/              # QA patterns and guides
├── teams/                       # Team configurations
├── docs/                        # Module documentation
├── _module-installer/           # DO NOT EDIT
└── module.yaml                  # Module configuration
```

## Agents

| Agent | Role |
|-------|------|
| `game-architect` | Game system architecture, technical design |
| `game-designer` | Game mechanics, GDD, balance |
| `game-dev` | Game implementation, coding |
| `game-qa` | Game testing, QA strategy |
| `game-scrum-master` | Sprint management for game dev |
| `game-solo-dev` | All-in-one rapid game development |

## Workflow Phases

### Phase 1: Preproduction (`1-preproduction/`)
- Game concept development
- Market research
- Core loop definition

### Phase 2: Design (`2-design/`)
- Game Design Document (GDD)
- Mechanics design
- Narrative design

### Phase 3: Technical (`3-technical/`)
- Game architecture
- System design
- Technical specifications

### Phase 4: Production (`4-production/`)
- Sprint implementation
- Feature development
- Asset integration

### Special Workflows
- `bmgd-quick-flow/` - Rapid prototyping
- `gametest/` - QA and testing workflows

## Module Configuration

| Config Key | Purpose | Options |
|------------|---------|---------|
| `project_name` | Game project name | - |
| `game_dev_experience` | Skill level | beginner/intermediate/expert |
| `planning_artifacts` | GDD, design docs location | - |
| `implementation_artifacts` | Sprint files location | - |
| `primary_platform` | Game engine/framework | unity, unreal, godot, other |

## Supported Platforms

Multi-select during installation:
- **Unity** - C#, Unity Engine
- **Unreal Engine** - C++, Blueprints
- **Godot** - GDScript, C#
- **Other** - Custom frameworks

## Guidelines For AI Agents

### MUST DO

- Follow game dev phases for new projects
- Use appropriate agent for each task
- Consider target platform in technical decisions
- Use gametest knowledge for QA patterns

### MUST AVOID

- **DO NOT** skip GDD for complex games
- **DO NOT** mix platform-specific code patterns
- **DO NOT** ignore performance considerations
- **DO NOT** edit `_module-installer/`

### Game-Specific Considerations

- **Performance**: Games have strict frame budgets
- **Platform**: Engine-specific patterns matter
- **Assets**: Consider asset pipeline in architecture
- **Testing**: Game testing differs from app testing
