# BMAD METHOD - COMPLETE WORKFLOW SYSTEM
**Comprehensive LLM Context Documentation**

---

## TABLE OF CONTENTS

1. [System Overview](#system-overview)
2. [Core Framework](#core-framework)
3. [BMM Module - Agile Development](#bmm-module---agile-development)
4. [BMB Module - Builder](#bmb-module---builder)
5. [BMGD Module - Game Development](#bmgd-module---game-development)
6. [CIS Module - Creative Intelligence](#cis-module---creative-intelligence)
7. [Workflow Architecture](#workflow-architecture)
8. [Interconnection Map](#interconnection-map)
9. [Best Practices](#best-practices)
10. [Path Variables & Configuration](#path-variables--configuration)

---

## SYSTEM OVERVIEW

BMAD Method is an AI-driven agile development framework consisting of:

| Component | Workflows | Step Files | Technique Libraries | Purpose |
|-----------|-----------|------------|---------------------|---------|
| **Core** | 3 | 11 | 62 creativity techniques | Foundation framework, always installed |
| **BMM** | 34+ | 66 | - | Primary agile development (software) |
| **BMB** | 6 | 45 | - | Build custom agents/workflows/modules |
| **BMGD** | 23 | 54+ | 24 game types | Game development workflows |
| **CIS** | 4 | 35 | 115 creative methods | Creative & strategic innovation |
| **TOTAL** | ~70 | ~211 | 201+ methods | Complete development ecosystem |

### Directory Structure

```
src/
├── core/                    # Core framework (always installed)
│   ├── agents/             # bmad-master.agent.yaml
│   ├── workflows/          # brainstorming, party-mode, advanced-elicitation
│   ├── resources/          # Shared resources (excalidraw)
│   └── tasks/              # Task definitions (validation, workflow, shard-doc)
├── modules/
│   ├── bmm/               # BMad Method - Agile development
│   ├── bmb/               # BMad Builder - Create agents/workflows
│   ├── bmgd/              # BMad Game Dev - Game development
│   └── cis/               # Creative Intelligence Suite
└── utility/                # Shared components
    └── agent-components/   # Agent compilation templates
```

---

## CORE FRAMEWORK

### Purpose
Foundation framework - always installed with any module. Provides base agents, workflows, and resources.

### Core Agents

| Agent | Purpose |
|-------|---------|
| `bmad-master` | Orchestrator for all BMAD operations |

### Core Workflows

#### 1. Brainstorming Workflow

**Location:** `core/workflows/brainstorming/`

**Purpose:** Facilitate interactive brainstorming sessions using 62+ diverse creativity techniques across 10 categories.

**Architecture:**
- Micro-file architecture: Each step is self-contained
- State tracking: Frontmatter in output document tracks progress
- JIT loading: Only current step loaded in memory
- Data-driven: Techniques loaded on-demand from CSV

**Technique Categories (62 total):**

| Category | Count | Examples |
|----------|-------|----------|
| collaborative | 5 | Yes And, Brain Writing, Role Playing |
| creative | 11 | What If, Analogical, Reversal, First Principles |
| deep | 8 | Five Whys, Morphological, Provocation |
| introspective_delight | 6 | Inner Child, Shadow Work, Values Archaeology |
| structured | 7 | SCAMPER, Six Thinking Hats, Mind Mapping |
| theatrical | 6 | Time Travel, Alien Anthropologist, Dream Fusion |
| wild | 8 | Chaos Engineering, Pirate Code, Quantum Superposition |
| biomimetic | 3 | Nature's Solutions, Ecosystem, Evolutionary |
| quantum | 3 | Observer Effect, Entanglement, Superposition |
| cultural | 4 | Indigenous, Fusion Cuisine, Ritual, Mythic |

**Step-by-Step Flow:**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-session-setup.md` | Initialize workflow, detect continuation, present 4 selection modes |
| 1b | `step-01b-continue.md` | Handle session resumption |
| 2a | `step-02a-user-selected.md` | Browse full technique library manually |
| 2b | `step-02b-ai-recommended.md` | AI matches techniques to session goals |
| 2c | `step-02c-random-selection.md` | Serendipitous discovery |
| 2d | `step-02d-progressive-flow.md` | Systematic divergent → convergent journey |
| 3 | `step-03-technique-execution.md` | Interactive coaching and facilitation |
| 4 | `step-04-idea-organization.md` | Synthesize ideas into actionable outcomes |

**4 Selection Modes:**

1. **User-Selected** - Browse full library, multi-technique selection
2. **AI-Recommended** - Goal-matched suggestions (3-phase sequence)
3. **Random Selection** - Serendipitous discovery with [Shuffle] option
4. **Progressive Flow** - 4-phase systematic journey:
   - Expansive Exploration (divergent, wild)
   - Pattern Recognition (analytical)
   - Idea Development (refining)
   - Action Planning (milestone-setting)

**Coaching Principles:**
- One element at a time for deep exploration
- Dynamic response to user insights
- Back-and-forth coaching not Q&A sequences
- User control: "next technique" or "move on" at any time
- Organic documentation as insights emerge

**Output:** Comprehensive session documentation with themes, priorities, and action plan

---

#### 2. Party Mode Workflow

**Location:** `core/workflows/party-mode/`

**Purpose:** Orchestrate group discussions between all installed BMAD agents, enabling natural multi-agent conversations with character consistency.

**Step-by-Step Flow:**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-agent-loading.md` | Load agent manifest, build complete roster, merge personalities |
| 2 | `step-02-discussion-orchestration.md` | Multi-agent conversation management |
| 3 | `step-03-graceful-exit.md` | Satisfying session conclusion |

**Agent Selection Logic:**
- **Primary:** Best expertise match for topic
- **Secondary:** Complementary perspective
- **Tertiary:** Cross-domain or devil's advocate

**Features:**
- Natural cross-talk ("As [Agent] mentioned...")
- Respectful disagreements
- Question handling protocol (pause for user, allow inter-agent)
- Rotation for inclusive participation
- TTS integration for each agent response

**Exit Triggers:** `*exit`, `goodbye`, `end party`, `quit`

**Output:** Session highlights with characteristic agent farewells

---

#### 3. Advanced Elicitation Workflow

**Location:** `core/workflows/advanced-elicitation/`

**Purpose:** Deep questioning techniques to extract comprehensive information when standard conversation isn't sufficient.

**Files:**
- `workflow.xml` - XML-based workflow definition
- `methods.csv` - Elicitation technique library

**Key Features:**
- Multiple elicitation techniques (Socratic, Devil's Advocate, etc.)
- Integrates with other workflows via A/P/C menu
- Supports `communication_language` for multilingual sessions

---

## BMM MODULE - AGILE DEVELOPMENT

### Purpose
Primary agile development module with 9 agents and 34+ workflows for software development from bug fixes to enterprise platforms.

### BMM Agents

| Agent | Role | Primary Workflows |
|-------|------|-------------------|
| `analyst` | Requirements analysis, research | research, create-product-brief |
| `architect` | System architecture design | create-architecture |
| `dev` | Story implementation (Amelia) | dev-story |
| `pm` | Product management, PRD creation | prd |
| `quick-flow-solo-dev` | Rapid development (Barry) | quick-dev |
| `sm` | Scrum Master, sprint management | sprint-planning, retrospective |
| `tea` | Test Architect, QA strategy | testarch workflows |
| `tech-writer` | Documentation | document-project |
| `ux-designer` | UX/UI design | create-ux-design |

### Workflow Organization

BMM workflows are organized into 4 development phases plus 6 specialized utility workflow groups:

```
┌────── PHASE 1: ANALYSIS ──────────────────────────────┐
│ - research (market/domain/technical)                │
│ - create-product-brief (6 steps)                     │
└──────────────────────────┬───────────────────────────┘
                           ↓
┌────── PHASE 2: PLANNING ─────────────────────────────┐
│ - prd (11 steps) ←─ product-brief                    │
│ - create-ux-design (14 steps) [parallel recommended] │
└──────────────────────────┬───────────────────────────┘
                           ↓
┌────── PHASE 3: SOLUTIONING ──────────────────────────┐
│ - create-architecture (8 steps)                      │
│ - create-epics-and-stories (4 steps)                 │
│ - check-implementation-readiness (6 steps)          │
└──────────────────────────┬───────────────────────────┘
                           ↓
┌────── PHASE 4: IMPLEMENTATION ──────────────────────┐
│ - sprint-planning → sprint-status.yaml              │
│ - create-story → dev-story → code-review             │
│ - retrospective                                      │
│ - correct-course                                     │
└──────────────────────────────────────────────────────┘

┌────── PARALLEL: QUICK FLOW ─────────────────────────┐
│ - create-tech-spec (4 steps)                         │
│ - quick-dev (6 steps) [escalates to full BMM]       │
└──────────────────────────────────────────────────────┘

┌────── CROSS-CUTTING: TESTARCH ───────────────────────┐
│ 8 QA workflows throughout phases                     │
│ (atdd, framework, test-design, automate, ci, etc.)   │
└──────────────────────────────────────────────────────┘

┌────── UTILITY: AS NEEDED ────────────────────────────┐
│ - document-project (brownfield)                     │
│ - generate-project-context                           │
│ - workflow-status (master router)                    │
│ - excalidraw-diagrams (4 types)                      │
└──────────────────────────────────────────────────────┘
```

---

### PHASE 1: ANALYSIS

#### 1.1 Research Workflow

**Location:** `modules/bmm/workflows/1-analysis/research/workflow.md`

**Purpose:** Conduct comprehensive research across multiple domains using current web data and verified sources.

**Research Types (Routing-Based):**

| Type | Focus |
|------|-------|
| Market Research | Market size, growth, competition, customer insights |
| Domain Research | Industry analysis, regulations, technology trends |
| Technical Research | Technology evaluation, architecture decisions |

**Key Features:**
- Web search REQUIRED (aborts if unavailable)
- Anti-hallucination protocol with source verification
- Multiple sources required for critical claims
- Confidence levels (High/Medium/Low)

**Output:** `{planning_artifacts}/research/{type}-{topic}-research-{date}.md`

---

#### 1.2 Create Product Brief Workflow

**Location:** `modules/bmm/workflows/1-analysis/create-product-brief/`

**Purpose:** Create comprehensive product briefs through collaborative step-by-step discovery.

**Step-by-Step Flow (6 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-init.md` | Initialize workflow, detect continuation, discover input documents |
| 1b | `step-01b-continue.md` | Handle workflow continuation |
| 2 | `step-02-vision.md` | Product vision discovery: problem, solution, differentiators |
| 3 | `step-03-users.md` | Target users: personas, user journeys |
| 4 | `step-04-metrics.md` | Success metrics: user success, business objectives, KPIs |
| 5 | `step-05-scope.md` | MVP scope: core features, out-of-scope, future vision |
| 6 | `step-06-complete.md` | Complete workflow, suggest next steps |

**Key Features:**
- Collaborative Business Analyst role
- A/P/C menu at each step (Advanced Elicitation, Party Mode, Continue)
- Discovers brainstorming/research documents automatically
- State tracking via frontmatter `stepsCompleted`

**Output:** `{planning_artifacts}/product-brief-{project_name}-{date}.md`

---

### PHASE 2: PLANNING

#### 2.1 PRD (Product Requirements Document) Workflow

**Location:** `modules/bmm/workflows/2-plan-workflows/prd/`

**Purpose:** Create comprehensive PRDs through collaborative step-by-step discovery between PM peers.

**Step-by-Step Flow (11 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-init.md` | Initialize, load product brief and context |
| 1b | `step-01b-continue.md` | Handle continuation |
| 2 | `step-02-discovery.md` | Deep product discovery |
| 3 | `step-03-success.md` | Define success criteria |
| 4 | `step-04-journeys.md` | User journey mapping |
| 5 | `step-05-domain.md` | Domain analysis |
| 6 | `step-06-innovation.md` | Innovation opportunities |
| 7 | `step-07-project-type.md` | Project type classification |
| 8 | `step-08-scoping.md` | Scope definition |
| 9 | `step-09-functional.md` | Functional requirements |
| 10 | `step-10-nonfunctional.md` | Non-functional requirements |
| 11 | `step-11-complete.md` | Finalize PRD |

**Output:** `{planning_artifacts}/prd-{project_name}-{date}.md`

---

#### 2.2 Create UX Design Workflow

**Location:** `modules/bmm/workflows/2-plan-workflows/create-ux-design/`

**Purpose:** Create comprehensive UX design specifications through visual exploration.

**Step-by-Step Flow (14 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-init.md` | Initialize |
| 1b | `step-01b-continue.md` | Continuation handler |
| 2 | `step-02-discovery.md` | UX discovery |
| 3 | `step-03-core-experience.md` | Core experience definition |
| 4 | `step-04-emotional-response.md` | Emotional design |
| 5 | `step-05-inspiration.md` | Design inspiration |
| 6 | `step-06-design-system.md` | Design system |
| 7 | `step-07-defining-experience.md` | Experience definition |
| 8 | `step-08-visual-foundation.md` | Visual foundation |
| 9 | `step-09-design-directions.md` | Design directions |
| 10 | `step-10-user-journeys.md` | User journeys |
| 11 | `step-11-component-strategy.md` | Component strategy |
| 12 | `step-12-ux-patterns.md` | UX patterns |
| 13 | `step-13-responsive-accessibility.md` | Responsive & accessibility |
| 14 | `step-14-complete.md` | Complete |

**Output:** `{planning_artifacts}/ux-design-specification.md`

---

### PHASE 3: SOLUTIONING

#### 3.1 Create Architecture Workflow

**Location:** `modules/bmm/workflows/3-solutioning/create-architecture/`

**Purpose:** Create comprehensive architecture decisions through collaborative discovery for AI agent implementation consistency.

**Step-by-Step Flow (8 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-init.md` | Initialize |
| 1b | `step-01b-continue.md` | Continuation |
| 2 | `step-02-context.md` | Context gathering |
| 3 | `step-03-starter.md` | Starter architecture |
| 4 | `step-04-decisions.md` | Architecture decisions |
| 5 | `step-05-patterns.md` | Design patterns |
| 6 | `step-06-structure.md` | Project structure |
| 7 | `step-07-validation.md` | Validation |
| 8 | `step-08-complete.md` | Complete |

**Data Files:**
- `data/project-types.csv` - Project type classification
- `data/domain-complexity.csv` - Domain complexity assessment

**Output:** Architecture document in `{planning_artifacts}/`

---

#### 3.2 Create Epics and Stories Workflow

**Location:** `modules/bmm/workflows/3-solutioning/create-epics-and-stories/`

**Purpose:** Transform PRD requirements and Architecture decisions into implementable stories.

**Prerequisites:** PRD + Architecture documents (UX recommended if UI exists)

**Step-by-Step Flow (4 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-validate-prerequisites.md` | Validate required documents exist |
| 2 | `step-02-design-epics.md` | Design epic structure |
| 3 | `step-03-create-stories.md` | Create user stories with ACs |
| 4 | `step-04-final-validation.md` | Final validation |

**Templates:**
- `templates/epics-template.md` - Epic breakdown template

**Output:** `{planning_artifacts}/epics.md`

---

#### 3.3 Check Implementation Readiness Workflow

**Location:** `modules/bmm/workflows/3-solutioning/check-implementation-readiness/`

**Purpose:** Validate PRD, Architecture, and Epics & Stories for completeness before Phase 4.

**Step-by-Step Flow (6 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-document-discovery.md` | Discover documents |
| 2 | `step-02-prd-analysis.md` | Analyze PRD |
| 3 | `step-03-epic-coverage-validation.md` | Validate epic coverage |
| 4 | `step-04-ux-alignment.md` | UX alignment check |
| 5 | `step-05-epic-quality-review.md` | Epic quality review |
| 6 | `step-06-final-assessment.md` | Final assessment |

**Templates:**
- `templates/readiness-report-template.md`

---

### PHASE 4: IMPLEMENTATION

#### 4.1 Sprint Planning Workflow

**Location:** `modules/bmm/workflows/4-implementation/sprint-planning/`

**Purpose:** Generate and manage sprint status tracking file.

**Inputs:**
- All epic files from `{planning_artifacts}`
- Pattern: `epic*.md`

**Output:** `{implementation_artifacts}/sprint-status.yaml`

---

#### 4.2 Create Story Workflow

**Location:** `modules/bmm/workflows/4-implementation/create-story/`

**Purpose:** Create the next user story from epics with enhanced context analysis.

**Input Files:**
- `sprint-status.yaml` (primary source)
- `epics.md` (enhanced with BDD and source hints)
- Fallbacks: PRD, Architecture, UX

**Output:** `{implementation_artifacts}/{story_key}.md`

---

#### 4.3 Dev Story Workflow

**Location:** `modules/bmm/workflows/4-implementation/dev-story/`

**Purpose:** Execute a story by implementing tasks/subtasks, writing tests, validating.

**Input Files:**
- Story file
- Sprint status
- Project context

**Key Features:**
- Auto-discovers story file if not specified
- Updates story status on completion

---

#### 4.4 Code Review Workflow

**Location:** `modules/bmm/workflows/4-implementation/code-review/`

**Purpose:** ADVERSARIAL Senior Developer code review.

**Review Focus:**
- Code quality
- Test coverage
- Architecture compliance
- Security
- Performance

**Key Feature:** Must find minimum 3-10 specific problems. Never accepts "looks good".

---

#### 4.5 Sprint Status Workflow

**Location:** `modules/bmm/workflows/4-implementation/sprint-status/`

**Purpose:** Summarize sprint status, surface risks, route to right workflow.

---

#### 4.6 Retrospective Workflow

**Location:** `modules/bmm/workflows/4-implementation/retrospective/`

**Purpose:** Review epic completion, extract lessons learned, explore impacts.

---

#### 4.7 Correct Course Workflow

**Location:** `modules/bmm/workflows/4-implementation/correct-course/`

**Purpose:** Navigate significant changes during sprint execution.

**Output:** `{planning_artifacts}/sprint-change-proposal-{date}.md`

---

### BMAD QUICK-FLOW (Rapid Development Track)

#### Quick Dev Workflow

**Location:** `modules/bmm/workflows/bmad-quick-flow/quick-dev/`

**Purpose:** Flexible rapid development - execute tech-specs OR direct instructions.

**Step-by-Step Flow (6 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-mode-detection.md` | Detect Mode A (tech-spec) or Mode B (direct), capture git baseline, handle escalation |
| 2 | `step-02-context-gathering.md` | Quick context for direct mode (files, patterns, dependencies) |
| 3 | `step-03-execute.md` | Execute implementation - iterate through tasks |
| 4 | `step-04-self-check.md` | Self-audit against tasks, tests, AC, patterns |
| 5 | `step-05-adversarial-review.md` | Construct diff, invoke adversarial review task |
| 6 | `step-06-resolve-findings.md` | Handle review findings (walk-through, auto-fix, skip) |

**State Variables:**
- `{baseline_commit}` - Git HEAD at start
- `{execution_mode}` - "tech-spec" or "direct"
- `{tech_spec_path}` - Path if Mode A

**Escalation Levels:**
- Level 0-2: Focused feature → tech-spec recommended
- Level 3+: Platform/system work → BMad Method recommended

---

#### Create Tech-Spec Workflow

**Location:** `modules/bmm/workflows/bmad-quick-flow/create-tech-spec/`

**Purpose:** Conversational spec engineering - ask questions, investigate code, produce implementation-ready tech-spec.

**Step-by-Step Flow (4 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-understand.md` | Analyze requirement delta, quick orient scan, informed questions |
| 2 | `step-02-investigate.md` | Map technical constraints and anchor points |
| 3 | `step-03-generate.md` | Generate the spec |
| 4 | `step-04-review.md` | Review and finalize |

**Ready for Development Standard:**
- Actionable: Every task has clear file path and specific action
- Logical: Tasks ordered by dependency
- Testable: All ACs follow Given/When/Then
- Complete: No placeholders or "TBD"
- Self-Contained: Fresh agent can implement without history

**Output:** `{implementation_artifacts}/tech-spec-{slug}.md`

---

### TEST ARCHITECTURE (TEA - 8 Workflows)

**Location:** `modules/bmm/workflows/testarch/`

**Purpose:** Comprehensive testing strategy throughout development lifecycle.

| Workflow | Purpose | Phase |
|----------|---------|-------|
| `atdd/workflow.yaml` | Generate failing acceptance tests before implementation (TDD red-green-refactor) | Phase 3/4 |
| `framework/workflow.yaml` | Initialize production-ready test framework (Playwright or Cypress) | Phase 1 |
| `test-design/workflow.yaml` | Dual-mode: System-level testability (Phase 3) OR Epic-level test planning (Phase 4) | Phase 3/4 |
| `automate/workflow.yaml` | Expand test automation coverage after implementation | Phase 4 |
| `ci/workflow.yaml` | Scaffold CI/CD quality pipeline | Any phase |
| `test-review/workflow.yaml` | Review test quality using knowledge base and best practices | Phase 4 |
| `nfr-assess/workflow.yaml` | Assess non-functional requirements (performance, security, reliability) | Phase 3/4 |
| `trace/workflow.yaml` | Generate requirements-to-tests traceability matrix + quality gate decision | Phase 4 |

**Gate Decision Types:** PASS, CONCERNS, FAIL, WAIVED

---

### UTILITY WORKFLOWS

#### Document Project Workflow

**Location:** `modules/bmm/workflows/document-project/`

**Purpose:** Analyze and document brownfield projects for AI-assisted development.

**Workflow Modes:**
1. **Initial Scan** - No existing docs, full project scan
2. **Full Rescan** - Update all documentation
3. **Deep Dive** - Detailed docs for specific area

**Templates:**
| Template | Purpose |
|----------|---------|
| `templates/index-template.md` | Documentation index |
| `templates/project-overview-template.md` | Executive summary |
| `templates/source-tree-template.md` | Directory structure |
| `templates/deep-dive-template.md` | Deep dive analysis |
| `templates/project-scan-report-schema.json` | State tracking |

**Output:** `{project_knowledge}/` directory with multiple files

---

#### Generate Project Context Workflow

**Location:** `modules/bmm/workflows/generate-project-context/`

**Purpose:** Create concise `project-context.md` with critical rules for AI agents.

**Step-by-Step Flow (3 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-discover.md` | Discover technology stack, patterns, configurations |
| 2 | `step-02-generate.md` | Generate context rules by category |
| 3 | `step-03-complete.md` | Finalize |

**Rule Categories Generated:**
1. Technology Stack & Versions
2. Language-Specific Rules
3. Framework-Specific Rules
4. Testing Rules
5. Code Quality & Style Rules
6. Development Workflow Rules
7. Critical Don't-Miss Rules

**Output:** `{output_folder}/project-context.md`

---

#### Workflow Status Workflow

**Location:** `modules/bmm/workflows/workflow-status/`

**Purpose:** Master router and status tracker - answers "what should I do now?"

**Operating Modes:**
| Mode | Purpose |
|------|---------|
| `interactive` (default) | Normal status check flow |
| `validate` | Check if calling workflow should proceed |
| `data` | Extract specific information |
| `init-check` | Simple existence check |
| `update` | Centralized status file updates |

**Sub-workflow:** `init/workflow.yaml` - Initialize workflow tracking for new projects

**Output:** Reads/updates `{planning_artifacts}/bmm-workflow-status.yaml`

---

#### Excalidraw Diagrams Workflow

**Location:** `modules/bmm/workflows/excalidraw-diagrams/`

**Purpose:** Create technical diagrams using Excalidraw format.

| Workflow | Purpose | Output |
|----------|---------|--------|
| `create-diagram/workflow.yaml` | General technical diagrams (architecture, ERD, UML) | `diagram-{timestamp}.excalidraw` |
| `create-flowchart/workflow.yaml` | Process/pipeline/logic flows | `flowchart-{timestamp}.excalidraw` |
| `create-wireframe/workflow.yaml` | Website/app wireframes | `wireframe-{timestamp}.excalidraw` |
| `create-dataflow/workflow.yaml` | Data flow diagrams (DFD) | `dataflow-{timestamp}.excalidraw` |

**Shared Resources:**
- `_shared/excalidraw-templates.yaml`
- `_shared/excalidraw-library.json`
- Core helpers from `core/resources/excalidraw/`

---

## BMB MODULE - BUILDER

### Purpose
Create custom agents, workflows, and modules for BMAD framework.

### BMB Agents

| Agent | Role |
|-------|------|
| `agent-builder` | Create and edit BMAD agents |
| `workflow-builder` | Create and edit workflows |
| `module-builder` | Create complete modules |

### BMB Workflows

| Workflow | Purpose | Steps | Web Bundle |
|----------|----------|-------|------------|
| `create-agent` | Create agent BMAD compliant | 8 steps | Yes |
| `create-workflow` | Create workflow new | 9 steps | Yes |
| `create-module` | Create module complete | 11 steps | Yes |
| `edit-agent` | Edit existing agent | 5 steps | No |
| `edit-workflow` | Edit existing workflow | 5 steps | Yes |
| `workflow-compliance-check` | Check compliance to standards | 8 steps | No |

---

#### Create Agent Workflow

**Location:** `modules/bmb/workflows/create-agent/`

**Purpose:** Create agent BMAD compliant through guided discovery, persona development, and command structure building.

**Step-by-Step Flow (8 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-brainstorm.md` | Optional Brainstorming - explore agent ideas |
| 2 | `step-02-discover.md` | Discover Purpose & Type (Simple/Expert/Module) |
| 3 | `step-03-persona.md` | Shape Personality (role, identity, communication_style, principles) |
| 4 | `step-04-commands.md` | Build Capabilities - convert to YAML command structure |
| 5 | `step-05-name.md` | Agent Naming - name, title, icon, filename |
| 6 | `step-06-build.md` | Generate YAML - complete YAML file and sidecar content |
| 7 | `step-07-validate.md` | Quality Check - validation conversation with technical checks |
| 8 | `step-08-celebrate.md` | Celebration & Next Steps - activation guidance |

**Agent Types Supported:**

1. **Simple Agent** - Self-contained in YAML, stateless, no persistent memory
2. **Expert Agent** - Has sidecar files, persistent memory, domain-restricted knowledge
3. **Module Agent** - Full module-level agent with complex integrations

**Templates Used:**
- `templates/simple-agent.template.md` - Simple Agent architecture guide
- `templates/expert-agent.template.md` - Expert Agent architecture guide
- `templates/agent-plan.template.md` - Agent planning document template

**Reference Materials:**
- `/data/reference/agents/simple-examples/commit-poet.agent.yaml` - Simple Agent example
- `/data/reference/agents/expert-examples/journal-keeper/` - Expert Agent example with sidecar
- `/data/reference/agents/module-examples/` - Module Agents examples (trend-analyst, security-engineer)
- `/data/communication-presets.csv` - 13 categories communication styles
- `/data/agent-validation-checklist.md` - Validation checklist

---

#### Create Workflow Workflow

**Location:** `modules/bmb/workflows/create-workflow/`

**Purpose:** Create structured standalone workflows using markdown-based step architecture.

**Step-by-Step Flow (9 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-init.md` | Initialization - workflow name, uniqueness check, folder creation |
| 2 | `step-02-gather.md` | Requirements Gathering - comprehensive requirements via conversation |
| 3 | `step-03-tools-configuration.md` | Tools Configuration - core tools, LLM features, memory, external integrations |
| 4 | `step-04-plan-review.md` | Plan Review - review complete plan, check if workflow produces documents |
| 5 | `step-05-output-format-design.md` | Output Format Design - Strict/Structured/Semi-structured/Free-form |
| 6 | `step-06-design.md` | Workflow Structure Design - step sequence, interaction patterns, file structure |
| 7 | `step-07-build.md` | File Generation - workflow.md, step files, templates |
| 8 | `step-08-review.md` | Review & Validation - review generated files, validation checks |
| 9 | `step-09-complete.md` | Completion - final summary, usage guidance, next steps |

**Workflow Types Supported:**
| Type | Description |
|------|-------------|
| **Document** | Generates documents (PRDs, specs, plans) |
| **Action** | Performs actions (refactoring, orchestration) |
| **Interactive** | Guided sessions (brainstorming, coaching) |
| **Autonomous** | Runs without human input (batch processing) |
| **Meta-Workflow** | Coordinates other workflows |

**Instruction Styles:**
- **Intent-Based** (Recommended) - Steps describe goals/principles, AI adapts conversation naturally
- **Prescriptive** - Steps provide exact instructions, controlled/predictable

**Output Format Spectrum:**
1. **Strictly Structured** - Government forms, legal docs
2. **Structured** - Project reports, business proposals
3. **Semi-structured** - Character sheets, lesson plans
4. **Free-form** - Creative stories, blog posts

---

#### Create Module Workflow

**Location:** `modules/bmb/workflows/create-module/`

**Purpose:** Create complete BMAD modules with agents, workflows, and installation infrastructure.

**Step-by-Step Flow (11 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-init.md` | Initialization - module name, existing work check, module plan creation |
| 1b | `step-01b-continue.md` | Continuation - resume previous session |
| 2 | `step-02-concept.md` | Define Concept & Scope - module vision, identity, boundaries |
| 3 | `step-03-components.md` | Plan Components - agent/workflow/task architecture |
| 4 | `step-04-structure.md` | Create Structure - directory structure and module complexity type |
| 5 | `step-05-config.md` | Configuration - create module.yaml with config prompts |
| 6 | `step-06-agents.md` | Create Agents - generate agent files from plan |
| 7 | `step-07-workflows.md` | Create Workflow Plans - generate workflow plan documents |
| 8 | `step-08-installer.md` | Installation Configuration - setup installer.js if needed |
| 9 | `step-09-documentation.md` | Documentation - create README, TODO, guides |
| 10 | `step-10-roadmap.md` | Development Roadmap - plan future development phases |
| 11 | `step-11-validate.md` | Validation - final validation against checklist |

**Module Complexity Types:**
| Type | Criteria |
|------|----------|
| **Simple** | 1-2 agents (Simple type), 1-3 workflows, no complex integrations |
| **Standard** | 2-4 agents (mixed types), 3-8 workflows, some shared resources |
| **Complex** | 4+ agents or Module-type, 8+ workflows, complex interdependencies |

**Module Structure Created:**
```
{module_code}/
├── agents/                    # Agent definitions
├── workflows/                 # Workflow folders
├── tasks/                     # Task files
├── templates/                 # Shared templates
├── data/                      # Module data
├── _module-installer/         # Installation config
│   └── installer.js
├── module.yaml                # Module configuration
└── README.md                  # Documentation
```

**Templates Used:**
- `templates/module-plan.template.md` - Module planning document
- `templates/module.template.yaml` - module.yaml structure
- `templates/agent.template.md` - Agent file template
- `templates/workflow-plan-template.md` - Workflow plan template
- `templates/installer.template.js` - Custom installer template

---

#### Edit Agent Workflow

**Location:** `modules/bmb/workflows/edit-agent/`

**Purpose:** Edit existing BMAD agents with best practices and targeted analysis.

**Step-by-Step Flow (5 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-discover-intent.md` | Discover Intent - get agent path and user editing goals |
| 2 | `step-02-analyze-agent.md` | Analyze Agent - load agent, relevant docs, identify issues |
| 3 | `step-03-propose-changes.md` | Propose Changes - present changes one-by-one with before/after |
| 4 | `step-04-apply-changes.md` | Apply Changes - apply approved changes using Edit tool |
| 5 | `step-05-validate.md` | Validate - validate changes meet BMAD standards |

**Key Features:**
- JIT Documentation Loading - only load docs relevant to user goals
- One-by-one Approval - user approves each change before apply
- Targeted Analysis - focus on user's stated issues, not everything

**Documentation References (loaded JIT):**
- `understanding-agent-types.md`
- `agent-compilation.md`
- `simple-agent-architecture.md`
- `expert-agent-architecture.md`
- `agent-menu-patterns.md`
- `communication-presets.csv`

---

#### Edit Workflow Workflow

**Location:** `modules/bmb/workflows/edit-workflow/`

**Purpose:** Edit and improve existing workflows with best practices compliance.

**Step-by-Step Flow (5 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-analyze.md` | Workflow Analysis - load target workflow, understand structure |
| 2 | `step-02-discover.md` | Discover Improvement Goals - understand user needs collaboratively |
| 3 | `step-03-improve.md` | Collaborative Improvement - address each improvement iteratively |
| 4 | `step-04-validate.md` | Validation & Completion - validate improvements, prepare summary |
| 5 | `step-05-compliance-check.md` | Compliance Validation - run workflow-compliance-check |

**Templates Used:**
- `templates/workflow-analysis.md` - Analysis findings
- `templates/improvement-goals.md` - User goals documentation
- `templates/improvement-log.md` - Track all changes
- `templates/validation-results.md` - Validation findings
- `templates/completion-summary.md` - Final summary

**Improvement Categories:**
- **CRITICAL** - Blocking successful runs
- **IMPORTANT** - Enhancing user experience
- **NICE-TO-HAVE** - Polish and refinements

---

#### Workflow Compliance Check Workflow

**Location:** `modules/bmb/workflows/workflow-compliance-check/`

**Purpose:** Systematic validation of workflows against BMAD standards with adversarial analysis and detailed reporting.

**Step-by-Step Flow (8 phases):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-validate-goal.md` | Goal Confirmation - confirm workflow path and validation scope |
| 2 | `step-02-workflow-validation.md` | workflow.md Validation - against workflow-template.md standards |
| 3 | `step-03-step-validation.md` | Step-by-Step Validation - each step against step-template.md |
| 4 | `step-04-file-validation.md` | File Validation - file sizes, markdown formatting, CSV standards |
| 5 | `step-05-intent-spectrum-validation.md` | Intent Spectrum Validation - Intent vs Prescriptive positioning |
| 6 | `step-06-web-subprocess-validation.md` | Web/Subprocess Optimization - web search and subprocess efficiency |
| 7 | `step-07-holistic-analysis.md` | Holistic Analysis - flow validation, goal alignment, meta-workflow failures |
| 8 | `step-08-generate-report.md` | Generate Report - comprehensive compliance report |

**Validation Areas:**

| Phase | Focus |
|-------|-------|
| **Phase 1** | Frontmatter, Role Description, Architecture, Initialization |
| **Phase 2** | MANDATORY EXECUTION RULES, Task References, Menu Patterns |
| **Phase 3** | File sizes (≤5K optimal, >15K action required), Markdown formatting, CSV data files |
| **Phase 4** | Intent vs Prescriptive spectrum assessment |
| **Phase 5** | Web search necessity, subprocess optimization |
| **Phase 6** | Flow validation, goal alignment, meta-workflow failures |
| **Phase 7** | Severity-ranked recommendations, automated fix options |

**Severity Rankings:**
- **Critical** - Must fix for workflow to function
- **Major** - Significantly impacts quality/maintainability
- **Minor** - Standards compliance improvements

**File Size Guidelines:**

| Size | Rating |
|------|--------|
| ≤5K | Optimal |
| 5K-7K | Good |
| 7K-10K | Acceptable |
| 10K-12K | Concern |
| >15K | Action Required |

---

## BMGD MODULE - GAME DEVELOPMENT

### Purpose
Game development module with specialized workflows for game design, architecture, and QA.

### BMGD Agents

| Agent | Role |
|-------|------|
| `game-architect` | Game system architecture |
| `game-designer` | Game design documentation |
| `game-dev` | Game implementation |
| `game-qa` | Game testing and quality |
| `game-scrum-master` | Agile game development |
| `game-solo-dev` | Rapid game prototyping |

### BMGD Workflow Organization

```
┌────── PHASE 0: PRE-PRODUCTION ────────────────────┐
│ - brainstorm-game (4 steps, 26 techniques)       │
│ - game-brief (8 steps)                           │
└──────────────────────────┬────────────────────────┘
                           ↓
┌────── PHASE 1: DESIGN ───────────────────────────┐
│ - gdd (14 steps, 24 game type guides)            │
│ - narrative (11 steps) [for story-driven games]  │
└──────────────────────────┬────────────────────────┘
                           ↓
┌────── PHASE 2: TECHNICAL ────────────────────────┐
│ - game-architecture (9 steps)                    │
│ - generate-project-context (3 steps)             │
└──────────────────────────┬────────────────────────┘
                           ↓
┌────── PHASE 3: PRODUCTION ───────────────────────┐
│ - Same as BMM Phase 4 + game-specific            │
│ - 60fps, feel, platform considerations           │
└───────────────────────────────────────────────────┘

┌────── PARALLEL: QUICK FLOW ──────────────────────┐
│ - quick-prototype (4 steps)                      │
│ - quick-dev (6 steps)                            │
│ - create-tech-spec (4 steps)                     │
└───────────────────────────────────────────────────┘

┌────── GAMETEST (6 workflows) ────────────────────┐
│ - test-framework, test-design, playtest-plan     │
│ - performance (60fps target), automate, review   │
└───────────────────────────────────────────────────┘
```

---

### PHASE 0: PRE-PRODUCTION (Optional)

#### Brainstorm Game Workflow

**Location:** `modules/bmgd/workflows/1-preproduction/brainstorm-game/`

**Purpose:** Game idea ideation with game-specific techniques.

**Step-by-Step Flow (4 steps):**
1. Game concept generation
2. Core mechanics exploration
3. Player fantasy mining
4. Viability assessment

**Key Data Files:**
- `game-brain-methods.csv` - 26 game-specific techniques including:
  - MDA Framework Exploration
  - Core Loop Brainstorming
  - Player Fantasy Mining
  - Genre Mashup
  - Verbs Before Nouns
  - Failure State Design
- `game-context.md` - Domain-specific context

---

#### Game Brief Workflow

**Location:** `modules/bmgd/workflows/1-preproduction/game-brief/`

**Purpose:** Define game vision before detailed design.

**Step-by-Step Flow (8 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-init.md` | Initialize, load context |
| 2 | `step-02-vision.md` | Game vision, concept |
| 3 | `step-03-platforms.md` | Target platforms |
| 4 | `step-04-audience.md` | Target audience |
| 5 | `step-05-core-gameplay.md` | Core gameplay loop |
| 6 | `step-06-unique-selling-points.md` | USPs |
| 7 | `step-07-success-metrics.md` | Success criteria |
| 8 | `step-08-complete.md` | Complete brief |

**Templates:** `game-brief-template.md`

---

### PHASE 1: DESIGN

#### GDD (Game Design Document) Workflow

**Location:** `modules/bmgd/workflows/2-design/gdd/`

**Purpose:** Create comprehensive game design documentation.

**Step-by-Step Flow (14 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-init.md` | Initialize, load game brief |
| 2 | `step-02-context.md` | Game context analysis |
| 3 | `step-03-platforms.md` | Platform-specific design |
| 4 | `step-04-vision.md` | Game vision statement |
| 5 | `step-05-core-gameplay.md` | Core gameplay mechanics |
| 6 | `step-06-mechanics.md` | Detailed mechanics |
| 7 | `step-07-game-type-specific.md` | Game type-specific sections |
| 8 | `step-08-progression.md` | Progression systems |
| 9 | `step-09-levels-content.md` | Level and content design |
| 10 | `step-10-art-audio.md` | Art and audio direction |
| 11 | `step-11-technical.md` | Technical specifications |
| 12 | `step-12-epics.md` | Epic breakdown |
| 13 | `step-13-metrics.md` | Analytics and metrics |
| 14 | `step-14-complete.md` | Complete GDD |

**Key Data Files:**
- `gdd-template.md` - GDD structure template
- `game-types.csv` - 24 game types with guides

**24 Game Type Guides:**
- Action Platformer, Puzzle, RPG, Strategy, Shooter
- Adventure, Simulation, Roguelike, MOBA, Fighting
- Racing, Sports, Survival, Horror, Idle/Incremental
- Card Game, Tower Defense, Metroidvania, Visual Novel
- Rhythm, Turn-Based Tactics, Sandbox, Text-Based, Party Game

**Each game type has specialized guide covering:**
- Core mechanics
- Progression systems
- Content design patterns
- Technical considerations
- Common pitfalls

---

#### Narrative Workflow

**Location:** `modules/bmgd/workflows/2-design/narrative/`

**Purpose:** Narrative design for story-driven games.

**Step-by-Step Flow (11 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-init.md` | Initialize, assess narrative needs |
| 2 | `step-02-story-structure.md` | Story structure framework |
| 3 | `step-03-characters.md` | Character development |
| 4 | `step-04-world-building.md` | World and lore |
| 5 | `step-05-plot-points.md` | Major plot points |
| 6 | `step-06-branching.md` | Branching narrative design |
| 7 | `step-07-dialogue.md` | Dialogue writing |
| 8 | `step-08-cinematics.md` | Cinematic moments |
| 9 | `step-09-quest-structure.md` | Quest and mission design |
| 10 | `step-10-integration.md` | Narrative integration with gameplay |
| 11 | `step-11-complete.md` | Complete narrative doc |

**Templates:**
- `narrative-template.md`
- `checklist.md`

---

### PHASE 2: TECHNICAL

#### Game Architecture Workflow

**Location:** `modules/bmgd/workflows/3-technical/game-architecture/`

**Purpose:** Game architecture covering engine, systems, and networking.

**Step-by-Step Flow (9 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-init.md` | Initialize, load GDD and context |
| 2 | `step-02-context.md` | Context analysis |
| 3 | `step-03-starter.md` | Starter template/engine discovery |
| 4 | `step-04-decisions.md` | Architectural decisions (rendering, physics, networking) |
| 5 | `step-05-patterns.md` | Design patterns |
| 6 | `step-06-cross-cutting.md` | Cross-cutting concerns |
| 7 | `step-07-structure.md` | Project structure |
| 8 | `step-08-validation.md` | Validation |
| 9 | `step-09-complete.md` | Complete architecture |

**Key Data Files:**
- `architecture-template.md`
- `decision-catalog.yaml` - Common game architecture decisions
- `architecture-patterns.yaml` - Game-specific patterns
- `pattern-categories.csv` - Pattern classification

---

#### Generate Project Context Workflow

**Location:** `modules/bmgd/workflows/3-technical/generate-project-context/`

**Purpose:** Create project-context.md for AI agents (similar to BMM but game-specific).

**Step-by-Step Flow (3 steps):**
1. Discover game technology stack (Unity/Unreal/Godot)
2. Generate context rules (game-specific patterns, 60fps, feel)
3. Complete and save

**Templates:** `project-context-template.md`

---

### PHASE 3: PRODUCTION

Production workflows mirror BMM Phase 4 with game-specific considerations:

| Workflow | Game-Specific Focus |
|----------|-------------------|
| `sprint-planning` | Game development sprint planning |
| `sprint-status` | Game development progress tracking |
| `create-story` | Game feature stories |
| `dev-story` | Game feature implementation |
| `code-review` | Game-specific review (60fps, feel, platform) |
| `retrospective` | Game development retrospectives |
| `correct-course` | Game development course corrections |

**Game-Specific Code Review Criteria:**
- Frame rate performance (60fps target)
- Game feel and responsiveness
- Platform-specific optimizations
- Memory usage patterns
- Asset loading strategies
- Input handling consistency

---

### BMGD QUICK FLOW

#### Quick Prototype Workflow

**Location:** `modules/bmgd/workflows/bmgd-quick-flow/quick-prototype/`

**Purpose:** Rapid game prototyping for quick validation.

**Step-by-Step Flow (4 steps):**

| Step | File | Purpose |
|------|------|---------|
| 1 | `step-01-define.md` | Define what to prototype (Mechanic/Feature/Visual/System) |
| 2 | `step-02-criteria.md` | Define success criteria |
| 3 | `step-03-implement.md` | Rapid implementation |
| 4 | `step-04-playtest.md` | Playtest and evaluate |

**Focus:** Playable outcomes over completeness

---

#### Quick Dev Workflow

**Location:** `modules/bmgd/workflows/bmgd-quick-flow/quick-dev/`

**Purpose:** Flexible game development - execute tech-specs or implement features directly.

**Similar to BMM quick-dev** with game-specific context loading.

---

#### Create Tech-Spec Workflow

**Location:** `modules/bmgd/workflows/bmgd-quick-flow/create-tech-spec/`

**Purpose:** Conversational spec engineering for game features.

**Similar to BMM create-tech-spec** with game-specific considerations:
- Engine-specific patterns (Unity/Unreal/Godot)
- Performance implications
- Asset integration
- Platform-specific constraints

---

### GAMETEST (Game QA Workflows)

**Location:** `modules/bmgd/workflows/gametest/`

**Purpose:** Comprehensive game testing strategy.

| Workflow | Purpose | Variables |
|----------|---------|-----------|
| `test-framework/workflow.yaml` | Initialize test framework for Unity/Unreal/Godot | `game_engine: auto`, `test_framework: auto` |
| `test-design/workflow.yaml` | Create game test scenarios | `design_level: full/targeted/minimal`, `focus_area: auto/gameplay/progression/multiplayer/performance` |
| `test-review/workflow.yaml` | Review test quality and coverage | `review_scope: full/targeted/quick` |
| `playtest-plan/workflow.yaml` | Create structured playtesting sessions | `playtest_type: internal/external/focused`, `session_duration`, `participant_count` |
| `performance/workflow.yaml` | Performance testing strategy | `target_fps: 60`, `target_platform: auto/pc/console/mobile` |
| `automate/workflow.yaml` | Generate automated game tests | `coverage_target: critical-paths/comprehensive/selective` |

**Game-Specific Testing Areas:**
- 60fps performance validation
- Input latency and responsiveness
- Cross-platform compatibility
- Asset streaming and loading
- Multiplayer synchronization
- Save/load systems
- Progression systems

---

### WORKFLOW STATUS (Progress Tracking)

**Location:** `modules/bmgd/workflows/workflow-status/`

**Purpose:** Master router - "what should I do now?" with game development paths.

**Operating Modes:** Same as BMM workflow-status

**Path Definitions:**
- `gamedev-greenfield.yaml` - Full game dev methodology
- `gamedev-brownfield.yaml` - Existing project extension
- `quickflow-greenfield.yaml` - Rapid prototyping
- `quickflow-brownfield.yaml` - Quick fixes to existing

**Project Levels:**

| Level | Title | Stories | Documentation |
|-------|-------|---------|---------------|
| 0 | Game Jam/Prototype | 1-5 | Minimal - quick GDD notes |
| 1 | Mini Game | 5-15 | Game Brief + Light GDD |
| 2 | Indie Game | 15-40 | Game Brief + GDD + Architecture |
| 3 | AA Game | 40-100 | Full GDD + Architecture + Narrative |
| 4 | AAA Game | 100+ | Full documentation suite |

---

### BMGD vs BMM Key Differences

| Aspect | BMGD (Game Dev) | BMM (Agile Method) |
|--------|-----------------|-------------------|
| **Primary document** | GDD (Game Design Document) | PRD (Product Requirements Document) |
| **Design phase** | GDD + Narrative Design | PRD + UX Design |
| **Technical phase** | game-architecture | architecture |
| **Game type guides** | 24 game type specific guides | N/A |
| **Testing workflows** | gametest (6 workflows) | testarch (8 workflows) |
| **Special focus** | 60fps, feel, platform | General software quality |
| **Brainstorming** | game-brain-methods.csv (26 techniques) | brain-methods.csv (62 techniques) |
| **Quick flow** | quick-prototype, quick-dev, create-tech-spec | bmad-quick-flow |
| **Project levels** | 0-4 (Game Jam → AAA) | 0-4 (Micro → Enterprise) |

**Game-Specific Additions in BMGD:**
1. **MDA Framework** (Mechanics-Dynamics-Aesthetics)
2. **Core Loop Design**
3. **Player Fantasy Mining**
4. **Game Feel considerations**
5. **Platform-specific (Unity, Unreal, Godot)**
6. **Playtesting workflows**
7. **Narrative Design integration**
8. **Performance testing (60fps target)**

---

## CIS MODULE - CREATIVE INTELLIGENCE

### Purpose
Creative Intelligence Suite - 4 interactive workflows facilitating creative and strategic processes through curated technique libraries and structured AI facilitation.

### CIS Agents

| Agent | Role |
|-------|------|
| `design-thinking-coach` | Guide design thinking processes |
| `innovation-strategist` | Strategic innovation planning |
| `creative-problem-solver` | Systematic problem solving |
| `presentation-master` | Presentation design and delivery |
| `storyteller` (2 variants) | Narrative crafting and storytelling |
| `brainstorming-coach` | Facilitate brainstorming sessions |

### CIS Workflows

| Workflow | Files | Steps | Methods Library |
|----------|-------|-------|-----------------|
| **Design Thinking** | 5 files | 7 steps | 30 design methods |
| **Innovation Strategy** | 5 files | 9 steps | 30 innovation frameworks |
| **Problem Solving** | 5 files | 9 steps | 30 solving methods |
| **Storytelling** | 6 files | 10 steps | 25 story frameworks |

---

### Design Thinking Workflow

**Location:** `modules/cis/workflows/design-thinking/`

**Purpose:** Guide human-centered design processes using empathy-driven methodologies.

**Process:** Empathize → Define → Ideate → Prototype → Test

**Files:**
- `workflow.yaml` - Configuration, paths, variables
- `instructions.md` - 7-step facilitation guide
- `design-methods.csv` - 30 design methods across 6 phases
- `template.md` - Structured output format
- `README.md` - Documentation

**Step-by-Step Flow (7 steps):**

| Step | Goal | Key Activities | Outputs |
|------|------|----------------|---------|
| **1** | Define design challenge | Problem/opportunity exploration, user identification, constraints, success criteria | `design_challenge`, `challenge_statement` |
| **2** | EMPATHIZE - Build user understanding | User interviews, empathy mapping, journey mapping, shadowing | `user_insights`, `key_observations`, `empathy_map` |
| **3** | DEFINE - Frame the problem | POV statements, "How Might We" questions, affinity clustering | `pov_statement`, `hmw_questions`, `problem_insights` |
| **4** | IDEATE - Generate solutions | Brainstorming, Crazy 8s, SCAMPER, 15-30 ideas minimum | `ideation_methods`, `generated_ideas`, `top_concepts` |
| **5** | PROTOTYPE - Make ideas tangible | Paper prototyping, storyboarding, Wizard of Oz, role playing | `prototype_approach`, `prototype_description`, `features_to_test` |
| **6** | TEST - Validate with users | Usability testing, feedback capture, A/B testing | `testing_plan`, `user_feedback`, `key_learnings` |
| **7** | Plan next iteration | Refinements, action items, success metrics | `refinements`, `action_items`, `success_metrics` |

**Design Methods Library (30 methods across 6 phases):**

**Empathize Phase:**
- User Interviews, Empathy Mapping, Shadowing, Journey Mapping, Diary Studies

**Define Phase:**
- Problem Framing, How Might We, Point of View Statement, Affinity Clustering, Jobs to be Done

**Ideate Phase:**
- Brainstorming, Crazy 8s, SCAMPER Design, Provotype Sketching, Analogous Inspiration

**Prototype Phase:**
- Paper Prototyping, Role Playing, Wizard of Oz, Storyboarding, Physical Mockups

**Test Phase:**
- Usability Testing, Feedback Capture Grid, A/B Testing, Assumption Testing, Iterate and Refine

**Implement Phase:**
- Pilot Programs, Service Blueprinting, Design System Creation, Stakeholder Alignment, Measurement Framework

---

### Innovation Strategy Workflow

**Location:** `modules/cis/workflows/innovation-strategy/`

**Purpose:** Identify disruption opportunities and architect business model innovation.

**Focus:** Sustainable competitive advantage over features.

**Files:**
- `workflow.yaml` - Configuration, paths, variables
- `instructions.md` - 9-step strategic facilitation guide
- `innovation-frameworks.csv` - 30 innovation frameworks across 6 categories
- `template.md` - Strategic output format
- `README.md` - Documentation

**Step-by-Step Flow (9 steps):**

| Step | Goal | Key Activities | Outputs |
|------|------|----------------|---------|
| **1** | Establish strategic context | Company analysis, strategic drivers, constraints, success definition | `company_name`, `strategic_focus`, `current_situation`, `strategic_challenge` |
| **2** | Analyze market landscape | TAM/SAM/SOM, Five Forces, competitive mapping | `market_landscape`, `competitive_dynamics`, `market_opportunities`, `market_insights` |
| **3** | Analyze current business model | Business Model Canvas, Value Proposition Canvas, vulnerability assessment | `current_business_model`, `value_proposition`, `revenue_cost_structure`, `model_weaknesses` |
| **4** | Identify disruption opportunities | Disruptive Innovation, Jobs to be Done, Blue Ocean Strategy | `disruption_vectors`, `unmet_jobs`, `technology_enablers`, `strategic_whitespace` |
| **5** | Generate innovation opportunities | Three Horizons, Value Chain Analysis, 5-10 specific innovations | `innovation_initiatives`, `business_model_innovation`, `value_chain_opportunities`, `partnership_opportunities` |
| **6** | Develop and evaluate strategic options | 3 distinct strategic options with pros/cons | `option_a/b/c_name`, `option_a/b/c_description`, `option_a/b/c_pros`, `option_a/b/c_cons` |
| **7** | Recommend strategic direction | Bold recommendation with rationale and hypotheses | `recommended_strategy`, `key_hypotheses`, `success_factors` |
| **8** | Build execution roadmap | 3-phase implementation plan with milestones | `phase_1`, `phase_2`, `phase_3` |
| **9** | Define metrics and risk mitigation | Leading/lagging indicators, decision gates, risk mitigation | `leading_indicators`, `lagging_indicators`, `decision_gates`, `key_risks`, `risk_mitigation` |

**Innovation Frameworks Library (30 frameworks across 6 categories):**

**Disruption:**
- Disruptive Innovation Theory, Jobs to be Done, Blue Ocean Strategy, Crossing the Chasm, Platform Revolution

**Business Model:**
- Business Model Canvas, Value Proposition Canvas, Business Model Patterns, Revenue Model Innovation, Cost Structure Innovation

**Market Analysis:**
- TAM SAM SOM Analysis, Five Forces Analysis, PESTLE Analysis, Market Timing Assessment, Competitive Positioning Map

**Strategic:**
- Three Horizons Framework, Lean Startup Methodology, Innovation Ambition Matrix, Strategic Intent Development, Scenario Planning

**Value Chain:**
- Value Chain Analysis, Unbundling Analysis, Platform Ecosystem Design, Make vs Buy Analysis, Partnership Strategy

**Technology:**
- Technology Adoption Lifecycle, S-Curve Analysis, Technology Roadmapping, Open Innovation Strategy, Digital Transformation Framework

---

### Problem Solving Workflow

**Location:** `modules/cis/workflows/problem-solving/`

**Purpose:** Apply systematic problem-solving methodologies to crack complex challenges.

**Approach:** Detective-style puzzle solving with root cause focus.

**Files:**
- `workflow.yaml` - Configuration, paths, variables
- `instructions.md` - 9-step systematic facilitation guide
- `solving-methods.csv` - 30 solving methods across 6 categories
- `template.md` - Problem analysis output format
- `README.md` - Documentation

**Step-by-Step Flow (9 steps):**

| Step | Goal | Key Activities | Outputs |
|------|------|----------------|---------|
| **1** | Define and refine the problem | Problem statement refinement, context gathering | `problem_title`, `problem_category`, `initial_problem`, `refined_problem_statement`, `problem_context`, `success_criteria` |
| **2** | Diagnose and bound the problem | Is/Is Not Analysis, pattern identification | `problem_boundaries` |
| **3** | Conduct root cause analysis | Five Whys, Fishbone Diagram, Systems Thinking | `root_cause_analysis`, `contributing_factors`, `system_dynamics` |
| **4** | Analyze forces and constraints | Force Field Analysis, Constraint Identification | `driving_forces`, `restraining_forces`, `constraints`, `key_insights` |
| **5** | Generate solution options | TRIZ, Lateral Thinking, Morphological Analysis, 10-15 ideas | `solution_methods`, `generated_solutions`, `creative_alternatives` |
| **6** | Evaluate and select solution | Decision Matrix, Cost Benefit Analysis, Risk Assessment | `evaluation_criteria`, `solution_analysis`, `recommended_solution`, `solution_rationale` |
| **7** | Plan implementation | PDCA Cycle, action steps, timeline, resources | `implementation_approach`, `action_steps`, `timeline`, `resources_needed`, `responsible_parties` |
| **8** | Establish monitoring and validation | Success metrics, validation plan, risk mitigation | `success_metrics`, `validation_plan`, `risk_mitigation`, `adjustment_triggers` |
| **9** | Capture lessons learned (optional) | Reflection on process and insights | `key_learnings`, `what_worked`, `what_to_avoid` |

**Solving Methods Library (30 methods across 6 categories):**

**Diagnosis:**
- Five Whys Root Cause, Fishbone Diagram, Problem Statement Refinement, Is/Is Not Analysis, Systems Thinking

**Analysis:**
- Force Field Analysis, Pareto Analysis, Gap Analysis, Constraint Identification, Failure Mode Analysis

**Synthesis:**
- TRIZ Contradiction Matrix, Lateral Thinking Techniques, Morphological Analysis, Biomimicry Problem Solving, Synectics Method

**Evaluation:**
- Decision Matrix, Cost Benefit Analysis, Risk Assessment Matrix, Pilot Testing Protocol, Feasibility Study

**Implementation:**
- PDCA Cycle, Gantt Chart Planning, Stakeholder Mapping, Change Management Protocol, Monitoring Dashboard

**Creative:**
- Assumption Busting, Random Word Association, Reverse Brainstorming, Six Thinking Hats, SCAMPER for Problems

---

### Storytelling Workflow

**Location:** `modules/cis/workflows/storytelling/`

**Purpose:** Craft compelling narratives using proven story frameworks and techniques.

**Style:** Whimsical master storyteller facilitation.

**Files:**
- `workflow.yaml` - Configuration, paths, variables
- `instructions.md` - 10-step narrative development guide
- `story-types.csv` - 25 story frameworks across 5 categories
- `template.md` - Story output format with variations
- `README.md` - Documentation

**Step-by-Step Flow (10 steps):**

| Step | Goal | Key Activities | Outputs |
|------|------|----------------|---------|
| **1** | Story Context Setup | Purpose, audience, key messages, constraints | `story_purpose`, `target_audience`, `key_messages` |
| **2** | Select Story Framework | Framework recommendation from 10 options | `story_type`, `framework_name` |
| **3** | Gather Story Elements | Framework-specific element gathering (Hero's Journey, Pixar Spine, Brand Story, etc.) | `story_beats`, `character_voice`, `conflict_tension`, `transformation` |
| **4** | Craft Emotional Arc | Beginning/middle/end emotions, peaks and valleys | `emotional_arc`, `emotional_touchpoints` |
| **5** | Develop Opening Hook | Surprising facts, intriguing opening, immediate relatability | `opening_hook` |
| **6** | Write Core Narrative | User drafts OR AI writes OR co-creation | `complete_story`, `core_narrative` |
| **7** | Create Story Variations | Short (1-3 sentences), Medium (1-2 paragraphs), Extended (full) | `short_version`, `medium_version`, `extended_version` |
| **8** | Usage Guidelines | Channel recommendations, audience adaptations, tone notes | `best_channels`, `audience_considerations`, `tone_notes`, `adaptation_suggestions` |
| **9** | Refinement and Next Steps | Strengths, areas to improve, additional versions needed | `resolution`, `refinement_opportunities`, `additional_versions`, `feedback_plan` |
| **10** | Generate Final Output | Compile all components, write to file | Final story document |

**Story Frameworks Library (25 frameworks across 5 categories):**

**Transformation:**
- Hero's Journey, Pixar Story Spine, Customer Journey, Challenge Overcome, Character Arc

**Strategic:**
- Brand Story, Vision Narrative, Origin Story, Positioning Story, Culture Story

**Persuasive:**
- Pitch Narrative, Sales Story, Change Story, Fundraising Story, Advocacy Story

**Analytical:**
- Data Storytelling, Case Study, Research Narrative, Insight Narrative, Process Story

**Emotional:**
- Hook Driven, Conflict Resolution, Empathy Story, Human Interest, Vulnerable Story

---

### Common Features Across All CIS Workflows

1. **Interactive Facilitation** - AI guides through questions, not generation
2. **Technique Libraries** - CSV databases of proven methods for each domain
3. **Context Integration** - Optional `--data` input for domain relevance
4. **Structured Output** - Comprehensive markdown reports with templates
5. **Energy Checkpoints** - Adaptive pacing based on user engagement
6. **Checkpoint Protocol** - Save progress after each section

---

## WORKFLOW ARCHITECTURE

### Step-File Architecture

All complex workflows in BMAD use **step-file architecture**:

```
workflow-name/
├── workflow.yaml              # Configuration
├── workflow.md                # Instructions (or workflow.yaml contains instructions)
├── steps/
│   ├── step-01-init.md
│   ├── step-01b-continue.md   # Resume support
│   ├── step-02-xxx.md
│   └── step-NN-xxx.md
├── templates/                 # Output templates
├── checklist.md              # Validation checklist (optional)
└── data/                      # Reference data (CSV, YAML)
    └── *.csv, *.yaml
```

### Core Principles

**1. Micro-file Design**
- Each step is self-contained with embedded rules
- Steps define goals and how to achieve them
- No external dependencies within step files

**2. Just-In-Time Loading**
- Only current step loaded in memory
- Reduces context load
- Enables large workflow systems

**3. Sequential Enforcement**
- No skipping steps
- Progress tracked via frontmatter `stepsCompleted` array
- Continuation support via `step-01b-continue.md`

**4. State Tracking**
```yaml
---
stepsCompleted: [1, 2, 3]
session_topic: 'Project X'
selected_approach: 'user-selected'
techniques_used: ['brainstorming', 'scamper']
ideas_generated: ['Idea 1', 'Idea 2']
workflow_completed: true
---
```

**5. Append-Only Building**
- Documents built by appending content
- No rewriting existing sections
- Maintains audit trail

### Universal Rules (Every Step)

```markdown
- 🛑 NEVER generate content without user input
- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 📋 YOU ARE A FACILITATOR, not a content generator
- 💾 Update frontmatter before loading next step
- 🚫 Forbidden to skip steps
```

### Standard Menu Pattern

```markdown
**Select an Option:**
[A] Advanced Elicitation
[P] Party Mode
[C] Continue

#### Menu Handling Logic:
- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save content, update frontmatter, then load next step
```

### File Size Guidelines

| Size | Rating | Action |
|------|--------|--------|
| ≤5K | Optimal | No action needed |
| 5K-7K | Good | No action needed |
| 7K-10K | Acceptable | Monitor |
| 10K-12K | Concern | Consider refactoring |
| >15K | Action Required | Split into smaller steps |

---

## INTERCONNECTION MAP

### BMM Development Flow

```
┌────── PHASE 1: ANALYSIS ─────────────────────────┐
│                                                     │
│  brainstorm (Core)                                 │
│     ↓                                               │
│  research (Market/Domain/Technical)                │
│     ↓                                               │
│  create-product-brief (6 steps)                   │
│     ↓                                               │
│  workflow-status (check progress)                 │
│                                                     │
└──────────────────────────┬────────────────────────┘
                           │
                           ▼
┌────── PHASE 2: PLANNING ──────────────────────────┐
│                                                     │
│  prd (11 steps) ←─ product-brief                   │
│  ├─→ success criteria                             │
│  ├─→ user journeys                               │
│  ├─→ functional requirements                      │
│  └─→ non-functional requirements                  │
│                                                     │
│  create-ux-design (14 steps) [parallel]           │
│  ├─→ core experience                              │
│  ├─→ design system                                │
│  ├─→ user journeys                                │
│  └─→ responsive & accessibility                   │
│                                                     │
│  workflow-status (check progress)                 │
│                                                     │
└──────────────────────────┬────────────────────────┘
                           │
                           ▼
┌────── PHASE 3: SOLUTIONING ───────────────────────┐
│                                                     │
│  create-architecture (8 steps)                    │
│  ├─→ context analysis                             │
│  ├─→ starter architecture                         │
│  ├─→ architectural decisions                     │
│  ├─→ design patterns                              │
│  └─→ project structure                           │
│                                                     │
│  create-epics-and-stories (4 steps)              │
│  ├─→ validate prerequisites                      │
│  ├─→ design epics                                 │
│  ├─→ create stories with ACs                     │
│  └─→ final validation                            │
│                                                     │
│  check-implementation-readiness (6 steps)         │
│  ├─→ document discovery                           │
│  ├─→ PRD analysis                                │
│  ├─→ epic coverage validation                    │
│  └─→ final assessment                            │
│                                                     │
│  testarch: test-design (Phase 3)                 │
│                                                     │
└──────────────────────────┬────────────────────────┘
                           │
                           ▼
┌────── PHASE 4: IMPLEMENTATION ──────────────────────┐
│                                                     │
│  sprint-planning → sprint-status.yaml             │
│                                                     │
│  create-story → dev-story → code-review           │
│     │           │              ↓                   │
│     │           │         (3-10 issues)           │
│     │           │                                   │
│     │           ↓                                   │
│     │      (implementation + tests)               │
│     │                                             │
│     └──────────────────────────┐                  │
│                                ↓                  │
│  retrospective (per epic)      │                  │
│     └──────────────────────────┘                  │
│                                                     │
│  correct-course (if changes needed)               │
│                                                     │
│  testarch: atdd, automate, nfr-assess, trace       │
│                                                     │
└─────────────────────────────────────────────────────┘
```

### BMGD Game Development Flow

```
┌────── PHASE 0: PRE-PRODUCTION ────────────────────┐
│                                                     │
│  brainstorm-game (4 steps)                        │
│  └─→ 26 game-specific techniques                  │
│                                                     │
│  game-brief (8 steps)                              │
│  └─→ game vision, platforms, audience, USPs        │
│                                                     │
└──────────────────────────┬────────────────────────┘
                           │
                           ▼
┌────── PHASE 1: DESIGN ─────────────────────────────┐
│                                                     │
│  gdd (14 steps) ←─ game-brief                     │
│  ├─→ context & platforms                          │
│  ├─→ vision & core gameplay                       │
│  ├─→ mechanics                                    │
│  ├─→ game-type-specific sections                  │
│  ├─→ progression & levels                         │
│  ├─→ art & audio direction                        │
│  └─→ epics & metrics                             │
│                                                     │
│  narrative (11 steps) [if story-driven]           │
│  ├─→ story structure                              │
│  ├─→ characters & world                           │
│  ├─→ plot points                                  │
│  ├─→ branching narrative                           │
│  └─→ dialogue & cinematics                        │
│                                                     │
└──────────────────────────┬────────────────────────┘
                           │
                           ▼
┌────── PHASE 2: TECHNICAL ─────────────────────────┐
│                                                     │
│  game-architecture (9 steps)                      │
│  ├─→ context analysis                             │
│  ├─→ starter template/engine                      │
│  ├─→ architectural decisions                       │
│  ├─→ design patterns                              │
│  └─→ project structure                            │
│                                                     │
│  generate-project-context (game-specific)        │
│                                                     │
└──────────────────────────┬────────────────────────┘
                           │
                           ▼
┌────── PHASE 3: PRODUCTION ─────────────────────────┐
│                                                     │
│  [Same as BMM Phase 4 with game-specific focus]   │
│                                                     │
│  Game-specific code review:                         │
│  - 60fps performance validation                    │
│  - Game feel and responsiveness                   │
│  - Platform-specific optimizations                │
│                                                     │
│  gametest workflows:                               │
│  - playtest-plan                                  │
│  - performance testing                            │
│  - game-specific test automation                  │
│                                                     │
└─────────────────────────────────────────────────────┘
```

### Quick Flow Tracks

```
┌────── BMM QUICK FLOW ──────────────────────────────┐
│                                                     │
│  create-tech-spec (4 steps)                         │
│  ├─→ understand requirements                       │
│  ├─→ investigate code                              │
│  ├─→ generate spec                                 │
│  └─→ review & finalize                            │
│                                                     │
│  quick-dev (6 steps)                               │
│  ├─→ mode detection (tech-spec/direct)            │
│  ├─→ context gathering                            │
│  ├─→ execute implementation                       │
│  ├─→ self-check                                   │
│  ├─→ adversarial review                           │
│  └─→ resolve findings                             │
│                                                     │
│  Escalation:                                       │
│  Level 0-2 → tech-spec recommended                │
│  Level 3+ → full BMad Method                      │
│                                                     │
└─────────────────────────────────────────────────────┘

┌────── BMGD QUICK FLOW ─────────────────────────────┐
│                                                     │
│  quick-prototype (4 steps)                          │
│  ├─→ define prototype scope                       │
│  ├─→ success criteria                             │
│  ├─→ rapid implementation                         │
│  └─→ playtest & evaluate                          │
│                                                     │
│  quick-dev (6 steps)                               │
│  [Similar to BMM with game-specific context]      │
│                                                     │
│  create-tech-spec (game-specific)                  │
│  [Engine-specific patterns: Unity/Unreal/Godot]   │
│                                                     │
└─────────────────────────────────────────────────────┘
```

### CIS Workflows Integration

```
┌────── CIS WORKFLOWS ───────────────────────────────┐
│                                                     │
│  Design Thinking (7 steps)                          │
│  └─→ Empathize → Define → Ideate → Prototype →   │
│       Test → Plan iteration                       │
│                                                     │
│  Innovation Strategy (9 steps)                      │
│  └─→ Context → Market → Business Model →         │
│       Disruption → Innovations → Options →        │
│       Recommendation → Roadmap → Metrics           │
│                                                     │
│  Problem Solving (9 steps)                         │
│  └─→ Define → Diagnose → Root Cause → Forces →   │
│       Solutions → Evaluate → Plan → Monitor      │
│                                                     │
│  Storytelling (10 steps)                            │
│  └─→ Context → Framework → Elements → Arc →       │
│       Hook → Narrative → Variations → Guidelines │
│       → Refinement → Output                       │
│                                                     │
│  Integration Points:                               │
│  ├─ Design Thinking ↔ BMM UX workflows            │
│  ├─ Innovation Strategy ↔ BMM Architecture       │
│  ├─ Problem Solving ↔ BMM Dev workflows          │
│  └─ Storytelling ↔ Tech Writer narratives         │
│                                                     │
└─────────────────────────────────────────────────────┘
```

---

## BEST PRACTICES

### For Creating Workflows

1. **Use Step-File Architecture** for complex workflows (>3 steps)
2. **Keep Steps Focused** - Each step should have single clear purpose
3. **Include Continuation Support** - Always add `step-01b-continue.md`
4. **Use Standard Menu Pattern** - A/P/C options for user control
5. **Track Progress** - Update frontmatter before loading next step
6. **Load Templates** - Use `workflow-template.md` and `step-template.md` standards
7. **Validate with Compliance Check** - Run workflow-compliance-check before finalizing

### For Running Workflows

1. **Read Complete Step File** - Never skip reading full step content
2. **Don't Generate Without Input** - Always get user input first
3. **Be a Facilitator** - Guide users through process, don't generate for them
4. **Update Frontmatter** - Save progress before loading next step
5. **Handle Continuations** - Check for existing workflow documents
6. **Use Menu System** - Present options clearly, honor user choice
7. **Validate Prerequisites** - Check required documents exist before proceeding

### For Agent Development

1. **Keep Personas Lean** - Dev agents need coding context, not extensive docs
2. **Use Clear Triggers** - Kebab-case only, unambiguous commands
3. **Build Capabilities as Commands** - Each trigger maps to workflow or action
4. **Follow Agent YAML Schema** - All fields required
5. **Test with Schema Validation** - Run `npm run validate:schemas`
6. **Use Appropriate Agent Type** - Simple vs Expert vs Module

### For Module Development

1. **Determine Complexity Level** - Simple, Standard, or Complex
2. **Create Module Structure** - Follow standard directory layout
3. **Configure module.yaml** - Define installation prompts
4. **Create Agents** - Use agent-builder workflow
5. **Create Workflows** - Use workflow-builder workflow
6. **Write Documentation** - README.md with usage examples
7. **Create Installer** - If custom installation needed

### For Testing Strategy

1. **Phase 1:** Set up test framework (testarch/framework)
2. **Phase 3:** Design system-level tests (testarch/test-design)
3. **Phase 4:**
   - Write acceptance tests first (testarch/atdd) - TDD approach
   - Implement story (dev-story)
   - Expand automation (testarch/automate)
   - Run adversarial review (code-review)
4. **Pre-release:**
   - Assess non-functional requirements (testarch/nfr-assess)
   - Generate traceability matrix (testarch/trace)
   - Review test quality (testarch/test-review)

### For Code Quality

1. **Always Run Adversarial Review** - Must find 3-10 issues
2. **Never Accept "Looks Good"** - Push for specific problems
3. **Review Multiple Dimensions:**
   - Code quality
   - Test coverage
   - Architecture compliance
   - Security
   - Performance
4. **Fix All Critical Issues** - Before marking review complete
5. **Track Findings** - Document resolution process

---

## PATH VARIABLES & CONFIGURATION

### Global Path Variables

| Variable | Purpose | Example |
|----------|---------|---------|
| `{project-root}` | User's project root directory | `/Users/dev/my-project` |
| `{output_folder}` | Configured output folder | `project-planning-artifacts` |
| `{planning_artifacts}` | Full path to planning docs | `{project-root}/{output_folder}` |
| `{implementation_artifacts}` | Implementation docs location | `{project-root}/{output_folder}` |
| `{user_name}` | User's configured name | `John` |
| `{communication_language}` | Chat language | `Vietnamese` |
| `{document_output_language}` | Document language | `English` |

### BMM Configuration (module.yaml)

Located at `modules/bmm/module.yaml`

```yaml
project_name:
  prompt: "What is the title of your project?"
  default: "{directory_name}"
  result: "{value}"

planning_artifacts:
  prompt: "Where should artifacts be stored?"
  default: "{output_folder}/project-planning-artifacts"
  result: "{project-root}/{value}"

implementation_artifacts:
  prompt: "Where should implementation docs be stored?"
  default: "{output_folder}/implementation-artifacts"
  result: "{project-root}/{value}"

user_name:
  prompt: "What should I call you?"
  default: "Developer"
  result: "{value}"

communication_language:
  prompt: "What language should I communicate in?"
  default: "Vietnamese"
  result: "{value}"

document_output_language:
  prompt: "What language should documents be written in?"
  default: "English"
  result: "{value}"

user_skill_level:
  prompt: "What is your skill level?"
  default: "intermediate"
  result: "{value}"
```

### Workflow Status Configuration

Located at `workflows/workflow-status/`

**Operating Modes:**
- `interactive` (default) - Normal status check flow
- `validate` - Check if calling workflow should proceed
- `data` - Extract specific information
- `init-check` - Simple existence check
- `update` - Centralized status file updates

**Path Definitions:**
- `paths/gamedev-greenfield.yaml` - Full game dev methodology
- `paths/gamedev-brownfield.yaml` - Existing project extension
- `paths/quickflow-greenfield.yaml` - Rapid prototyping
- `paths/quickflow-brownfield.yaml` - Quick fixes to existing

### Input File Discovery Patterns

**Smart patterns for sharded vs whole documents:**

```yaml
load_strategies:
  FULL_LOAD:
    pattern: "*prd*.md"
    priority: 1

  SELECTIVE_LOAD:
    pattern: "*prd*/index.md"
    priority: 2

  INDEX_GUIDED:
    pattern: "*prd*/"
    requires: "index.md"
    priority: 3
```

**Priority:**
1. Check for whole file first: `*prd*.md`
2. Then check sharded: `*prd*/index.md`
3. Index-guided: Load index, then selective loading

---

## SUMMARY

The BMAD Method provides a comprehensive AI-driven development framework across **5 modules** with **~69 workflows** organized through **~211 step files** and **201+ creative methods**.

**Key Strengths:**

1. **Structured Methodology** - Phase-based approach from analysis to implementation
2. **Flexibility** - Quick Flow for rapid development, full methodology for complex projects
3. **Quality Assurance** - Adversarial code reviews, test architecture workflows
4. **Extensibility** - Builder module (BMB) for custom agents/workflows/modules
5. **Domain Specialization** - Game Dev (BMGD) and Creative Intelligence (CIS) modules
6. **Interactive Facilitation** - AI guides users through processes, doesn't generate without input

**Recommended Usage:**

| Project Type | Recommended Path |
|--------------|------------------|
| Bug fixes, small features | Quick Flow (create-tech-spec → quick-dev) |
| Medium features | BMM Quick Flow or Phase 3-4 directly |
| New products/features | Full BMM Method (Phases 1-4) |
| New games | Full BMGD Method (Phases 0-3) |
| Game prototypes | BMGD Quick Flow |
| Creative challenges | CIS workflows |
| Custom needs | Use BMB to create agents/workflows |

**Quality Gates:**

- Schema validation: `npm run validate:schemas`
- Linting: `npm run lint`
- Code review: Always adversarial (3-10 issues min)
- Test coverage: TestArch workflows throughout
- Compliance: workflow-compliance-check for workflows

---

**End of BMAD Method Complete Workflow Documentation**
