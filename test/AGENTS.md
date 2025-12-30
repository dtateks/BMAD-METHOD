<!-- Scoped to test/ directory. Read root AGENTS.md first. -->

# AGENTS.md - Test Directory

> Test infrastructure for BMad Method agent schema validation and installation components.

## Directory Overview

```
test/
├── fixtures/                     # Test fixture files
│   └── agent-schema/            # Agent schema test cases
│       ├── valid/               # 18 fixtures that should pass
│       │   ├── top-level/       # Basic structure tests
│       │   ├── metadata/        # Metadata field tests
│       │   ├── persona/         # Persona validation tests
│       │   ├── menu/            # Menu structure tests
│       │   ├── menu-commands/   # Command target tests
│       │   ├── menu-triggers/   # Trigger format tests
│       │   ├── critical-actions/ # Optional field tests
│       │   └── prompts/         # Prompts field tests
│       └── invalid/             # 32 fixtures that should fail
│           ├── top-level/       # Structure errors
│           ├── metadata/        # Metadata errors
│           ├── persona/         # Persona errors
│           ├── menu/            # Menu errors
│           ├── menu-commands/   # Command errors
│           ├── menu-triggers/   # Trigger format errors
│           ├── critical-actions/ # Action errors
│           ├── prompts/         # Prompt errors
│           └── yaml-errors/     # YAML parsing errors
├── test-agent-schema.js         # Main schema test runner
├── test-installation-components.js # Installation tests
├── test-cli-integration.sh      # CLI integration tests (bash)
├── unit-test-schema.js          # Unit tests for schema
└── README.md                    # Comprehensive test docs
```

## Test Commands

```bash
# Full test suite
npm test                          # Run all tests + lint + format

# Individual test runners
npm run test:schemas              # Agent YAML schema tests
npm run test:install              # Installation component tests
npm run test:coverage             # Schema tests with coverage

# CLI integration (bash)
./test/test-cli-integration.sh    # Test CLI exit codes

# Direct runners
node test/test-agent-schema.js    # Schema test runner
node test/unit-test-schema.js     # Unit tests
```

## Test Coverage

| Metric | Coverage |
|--------|----------|
| Statements | 100% |
| Branches | 100% |
| Functions | 100% |
| Lines | 100% |

**Fixtures**: 50 total (18 valid, 32 invalid)

## Fixture Format

Test fixtures use YAML comment metadata:

```yaml
# Test: Description of what this tests
# Expected: PASS (or FAIL - error description)
# Path context: src/modules/bmm/agents/test.agent.yaml
agent:
  metadata:
    # ... test content
```

## Coding Style & Conventions

**From ESLint config**:

- CommonJS patterns allowed
- Console logging allowed
- `no-unused-vars` disabled for test scripts
- Fixtures excluded from linting (`test/fixtures/**`)

## Common Tasks

| Task | Command/Location |
|------|------------------|
| Add valid test case | Create in `fixtures/agent-schema/valid/{category}/` |
| Add invalid test case | Create in `fixtures/agent-schema/invalid/{category}/` |
| Run single test file | `node test/test-agent-schema.js` |
| View coverage report | Open `coverage/index.html` after `npm run test:coverage` |
| Debug test failure | Check fixture's `# Expected:` comment |

## Guidelines For AI Agents

### MUST DO

- Include `# Test:` and `# Expected:` comments in new fixtures
- Place valid fixtures in `valid/`, invalid in `invalid/`
- Run `npm test` to verify all tests pass
- Match fixture category to validation rule being tested

### MUST AVOID

- **DO NOT** modify existing fixtures without understanding their purpose
- **DO NOT** add fixtures without proper comment metadata
- **DO NOT** skip running tests after changes
- **DO NOT** edit `test/fixtures/**/*.yaml` for ESLint (excluded)

### Test Categories

| Category | Tests |
|----------|-------|
| top-level | Root `agent` key structure |
| metadata | id, name, title, icon, module |
| persona | role, identity, communication_style, principles |
| menu | Required menu array, menu items |
| menu-commands | workflow, exec, action, tmpl, data targets |
| menu-triggers | Kebab-case, no duplicates, no asterisks |
| critical-actions | Optional array, non-empty strings |
| prompts | Optional, id + content required |
| yaml-errors | Malformed YAML, bad indentation |
