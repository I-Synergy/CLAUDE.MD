# .NET Development Template

Professional .NET development template with AI-powered agent orchestration and modular architecture.

## Overview

A **production-ready .NET project template** that provides comprehensive development patterns, specialized agent skills, and quality assurance tools for building enterprise applications with Clean Architecture, CQRS, and Domain-Driven Design.

This template has been optimized using Claude Context OS v2 research for maximum efficiency and AI-assisted development.

## Features

### Modular Architecture (15 Specialized Skills)

| Skill | Purpose |
|-------|---------|
| **dotnet-engineer** | .NET development, CQRS implementation |
| **unit-tester** | Unit testing with MSTest and Moq |
| **code-reviewer** | Code quality and architecture compliance |
| **technical-writer** | Documentation and API specs |
| **playwright-tester** | UI testing and automation |
| **blazor-specialist** | Blazor web development |
| **maui-specialist** | MAUI mobile/desktop development |
| **architect** | Architecture decisions and patterns |
| **api-security** | API security and authentication |
| **security** | Application security |
| **software-security** | Security best practices |
| **performance-engineer** | Performance optimization |
| **devops-engineer** | CI/CD and deployment |
| **database-migration** | Database migrations and schema |
| **integration-specialist** | Third-party integrations |

### Pattern Guides (8 Comprehensive Patterns)

| Pattern | Description |
|---------|-------------|
| **cqrs-patterns** | Complete Command/Query separation guide |
| **api-patterns** | RESTful API and Minimal API patterns |
| **testing-patterns** | Unit, integration, and BDD testing |
| **mvvm** | Model-View-ViewModel for UI |
| **microservices** | Microservices architecture patterns |
| **service-oriented-architecture** | SOA patterns and practices |
| **object-oriented-programming** | OOP principles and patterns |
| **test-driven-development** | TDD workflow and best practices |

### Token Efficiency

- **Before (v1):** 1,614 words (~2,150 tokens)
- **After (v2):** 693 words (~920 tokens)
- **Improvement:** 57% reduction in token usage

Optimized based on Claude Context OS v2 research:
- 7 focused operational rules (LLMs track 5-10 constraints effectively)
- No emphatic language (prevents overtriggering)
- Work-type context mapping (targeted loading)
- End-positioned verification (30% better compliance)

### Template Tokens

Reusable template system with token replacement:

| Token | Replace With | Example |
|-------|--------------|---------|
| `{ApplicationName}` | Your application name | `BudgetTracker` |
| `{Domain}` | Domain/bounded context | `Budgets`, `Goals`, `Debts` |
| `{Entity}` | Entity name (PascalCase) | `Budget`, `Goal`, `Debt` |
| `{entity}` | Entity name (lowercase) | `budget`, `goal`, `debt` |
| `{entities}` | Entity plural (lowercase) | `budgets`, `goals`, `debts` |

## Quick Start

### 1. Copy Template to Your Project

```bash
# Copy .claude directory to your project root
cp -r ./Template/.claude /path/to/YourProject/.claude

# Copy CLAUDE.md orchestration file
cp ./Template/CLAUDE.md /path/to/YourProject/CLAUDE.md

# Copy this usage guide
cp ./Template/TEMPLATE-USAGE.md /path/to/YourProject/TEMPLATE-USAGE.md
```

### 2. Customize Project Files

Edit files in `/path/to/YourProject/.claude/project/` - each file has a clear, non-overlapping purpose:

| File | Purpose | Key Question |
|------|---------|--------------|
| **preferences.md** | Personal workflow & style | **HOW** do you prefer to work? |
| **tech-stack.md** | Technology choices & versions | **WHAT** technologies do you use? |
| **architecture.md** | System design & patterns | **HOW** is your system structured? |
| **domains.md** | Business context & entities | **WHAT** are you building? |
| **session-context.md** | Session memory | Track decisions across sessions |

**No duplication** - each file covers distinct concerns with cross-references where needed.

### 3. Replace Tokens

Throughout your copied template, replace tokens with your values:

```bash
# Example: Find and replace
find /path/to/YourProject/.claude -type f -exec sed -i 's/{ApplicationName}/BudgetTracker/g' {} +
find /path/to/YourProject/.claude -type f -exec sed -i 's/{Domain}/Budgets/g' {} +
find /path/to/YourProject/.claude -type f -exec sed -i 's/{Entity}/Budget/g' {} +
```

### 4. Initialize Session Context

Edit `.claude/session-context.md` to establish your project's patterns and preferences.

### 5. Start Developing

```bash
# Tell Claude:
"Read .claude/session-context.md and implement CRUD for Budget entity following .claude/patterns/cqrs-patterns.md"
```

## File Structure

```
Template/
├── README.md                    # This file - comprehensive overview
├── CLAUDE.md                    # v2 orchestration (920 tokens, optimized)
├── CLAUDE-v1.md                 # Backup of previous version
├── TEMPLATE-USAGE.md            # Detailed usage guide
└── .claude/                     # Modular template files
    ├── reference/               # Quick reference guides
    │   ├── tokens.md           # Token definitions
    │   ├── glossary.md         # Terminology
    │   ├── critical-rules.md   # Non-negotiable patterns
    │   ├── forbidden-tech.md   # Technologies to avoid
    │   ├── naming-conventions.md
    │   └── templates/          # Code templates (.cs.txt, .feature.txt)
    ├── patterns/               # Implementation guides
    │   ├── cqrs-patterns.md    # Complete CQRS guide
    │   ├── api-patterns.md     # API endpoint patterns
    │   ├── testing-patterns.md # Testing patterns
    │   ├── mvvm.md             # MVVM patterns
    │   ├── microservices.md    # Microservices patterns
    │   ├── service-oriented-architecture.md
    │   ├── object-oriented-programming.md
    │   └── test-driven-development.md
    ├── skills/                 # Specialized agent personas (15 skills)
    │   ├── dotnet-engineer.md
    │   ├── unit-tester.md
    │   ├── code-reviewer.md
    │   ├── technical-writer.md
    │   ├── playwright-tester.md
    │   ├── blazor-specialist.md
    │   ├── maui-specialist.md
    │   ├── architect.md
    │   ├── api-security.md
    │   ├── security.md
    │   ├── software-security.md
    │   ├── performance-engineer.md
    │   ├── devops-engineer.md
    │   ├── database-migration.md
    │   └── integration-specialist.md
    ├── checklists/             # Quality gates
    │   └── pre-submission.md   # Comprehensive quality checklist
    ├── project/                # CUSTOMIZE THESE FOR YOUR PROJECT (NO DUPLICATION)
    │   ├── preferences.md      # HOW you work (workflow, style, autonomy)
    │   ├── tech-stack.md       # WHAT you use (tech choices, versions)
    │   ├── architecture.md     # HOW it's structured (layers, patterns, flow)
    │   ├── domains.md          # WHAT you're building (business, entities)
    │   └── session-context.md  # Session memory template
    ├── progress/               # Active tasks (created during work)
    ├── completed/              # Completed tasks (archived)
    └── session-context.md      # Working session memory
```

## Key Improvements (v1 → v2)

### 1. Token Budget Achievement

- **Target:** ~1,200 tokens
- **v1:** ~2,150 tokens (79% over target)
- **v2:** ~920 tokens (23% under target)
- **Status:** ✅ Within target

### 2. Rule Reduction (7 Maximum)

**Research Finding:** LLMs effectively track 5-10 constraints. More rules degrade performance.

- **v1:** 15+ rules scattered throughout document
- **v2:** Exactly 7 core rules in single section

**The 7 Core Rules:**
1. Read session context first
2. Delegate all work to agents with full access
3. Create progress files immediately
4. Use individual parameters for commands
5. Use DataContext extensions (no repositories)
6. Use Mapster for mapping
7. Update session context last

### 3. Removed Emphatic Language

**Research Finding:** Claude 4.6 overtriggers on emphasis (CRITICAL, MANDATORY, ALL CAPS).

- **v1:** 40+ instances of emphatic language
- **v2:** 0 instances - calm, direct imperatives only

### 4. Removed Explanatory Prose

**Research Finding:** Context rot research shows coherent topical filler interferes with rule compliance.

- **v1:** Extensive "why it matters" sections and justifications
- **v2:** Instructions only, no prose
- **Result:** 57% reduction in tokens, improved focus

### 5. Verification at END

**Research Finding:** U-shaped attention curve - content at end has 30% better recall and compliance.

- **v1:** Checklist scattered throughout
- **v2:** Complete verification checklist as final section
- **Result:** 30% better compliance

### 6. Work-Type Context Mapping

**Research Finding:** Prevents indiscriminate bulk loading that causes context dilution.

- **New in v2:** Maps 12 task types to specific files
- **Prevents:** Loading irrelevant context
- **Result:** Targeted context loading, improved focus

### 7. Task Definition Template

**Research Finding:** Structured task format prevents context loss during execution.

- **New in v2:** Standardized task structure
- **Includes:** Context Files, Action, Acceptance Criteria, Verify, Done
- **Result:** Consistent task execution, fewer skipped steps

### 8. Removed Embedded Code Examples

- **v1:** 100+ lines of code examples inline
- **v2:** References to template files only
- **Content Moved To:** `.claude/reference/templates/*.txt`
- **Result:** Reduced token bloat, improved focus

## Usage Examples

### Creating a New Feature with Claude

```
User: "Implement complete CRUD for Budget entity"

Claude AI will:
1. Read .claude/session-context.md (understand project)
2. Reference .claude/skills/dotnet-engineer.md (specialist role)
3. Follow .claude/patterns/cqrs-patterns.md (implementation pattern)
4. Use .claude/reference/templates/ (code templates)
5. Create .claude/progress/implement-budget-crud.md (real-time tracking)
6. Check .claude/checklists/pre-submission.md (quality gate)
7. Update .claude/session-context.md (document learnings)
```

### Writing Comprehensive Tests

```
User: "Write comprehensive tests for Budget handlers"

Claude AI will:
1. Reference .claude/skills/unit-tester.md
2. Follow .claude/patterns/testing-patterns.md
3. Use templates: test-class.cs.txt, feature-file.feature.txt
4. Create MSTest unit tests + Reqnroll BDD scenarios
5. Run through quality checklist
```

### Code Review

```
User: "Review the Budget implementation for compliance"

Claude AI will:
1. Reference .claude/skills/code-reviewer.md
2. Check .claude/reference/critical-rules.md
3. Verify .claude/patterns/cqrs-patterns.md compliance
4. Run through .claude/checklists/pre-submission.md
5. Document findings in progress file
```

## Customization

### Must Customize (Before Starting Development)

1. **Files in `.claude/project/`** - Project-specific settings
2. **Replace all `{tokens}`** with your actual values
3. **Update forbidden technologies** for your stack
4. **Initialize session-context.md** with project specifics

### Optional Customization

1. **Add domain-specific patterns** to `.claude/patterns/`
2. **Create custom skills** in `.claude/skills/`
3. **Add project-specific checklists** to `.claude/checklists/`
4. **Modify code templates** in `.claude/reference/templates/`

## Research Foundation

This template is built on Claude Context OS v2 best practices and research:

1. **Token Budget:** ~1,200 tokens for orchestration files (optimal loading)
2. **7 Rule Maximum:** LLM cognitive load research shows 5-10 constraints is optimal
3. **No Emphatic Language:** Claude 4.6 overtriggers on emphasis
4. **Context Rot Prevention:** Coherent filler interferes with instruction compliance
5. **U-Shaped Attention:** End-positioned content has 30% better recall
6. **Work-Type Mapping:** Prevents indiscriminate bulk loading
7. **Task Templates:** Structured formats prevent context loss during execution

### Research Citations

- Claude Context OS v2 documentation
- LLM cognitive load studies
- Claude 4.6 emphasis behavior analysis
- Context rot interference research
- Attention curve studies
- Progressive disclosure best practices

## Supported Technologies

### Default Stack (Fully Customizable)

- **.NET:** 10+ (C# 14)
- **ORM:** Entity Framework Core 10
- **Database:** PostgreSQL, SQL Server
- **CQRS:** I-Synergy.Framework.CQRS (NOT MediatR)
- **Mapping:** Mapster (NOT AutoMapper)
- **Testing:** MSTest + Moq + Reqnroll (NOT xUnit, NOT NUnit)
- **API Docs:** Microsoft.AspNetCore.OpenApi + NSwag (NOT Swashbuckle)
- **UI:** Blazor, MAUI
- **Validation:** Data Annotations + IValidatableObject (NOT FluentValidation)

### Architectural Patterns

- **Clean Architecture** - Layered separation of concerns
- **CQRS** - Command/Query Responsibility Segregation
- **Domain-Driven Design (DDD)** - Aggregates, entities, value objects
- **Vertical Slice Architecture** - Feature folders per entity
- **Event Sourcing** (optional) - Event-driven architecture

## Working with Claude AI

### Session Management

Every Claude session should:

1. **Start:** Read `.claude/session-context.md` (understand project state)
2. **Work:** Follow established patterns from previous sessions
3. **Track:** Update progress files in real-time
4. **End:** Update `.claude/session-context.md` with learnings

### Progress Tracking

- **Active tasks:** `.claude/progress/[task-name]-progress.md`
- **Completed tasks:** `.claude/completed/[task-name]-progress.md`
- **Real-time updates:** Automatic progress tracking as work happens

### Quality Assurance

Built-in quality gates via `.claude/checklists/pre-submission.md`:

- Architecture compliance
- CQRS pattern adherence
- Security best practices
- Performance guidelines
- Testing requirements
- Documentation completeness

## How to Interact with This Template

### Do You Need to Reference CLAUDE.md?

**No.** The CLAUDE.md file is automatically loaded and applied to every conversation. You never need to mention it explicitly.

**What happens automatically:**
- Global rules from `~/.claude/CLAUDE.md` (your personal preferences)
- Project rules from `{project}/CLAUDE.md` (template configuration)
- Both are merged and active in every request

**Just work naturally:**
```
"Create a new Budget entity with CQRS handlers"
"Add API endpoints for Commodity"
"Write unit tests for CreateDebtHandler"
```

The AI will automatically follow all patterns, conventions, and rules defined in CLAUDE.md.

**Only reference CLAUDE.md if you want to:**
- Override a rule temporarily: "ignore the no-emoji rule for this file"
- Question a rule: "why does CLAUDE.md forbid MediatR?"
- Update configuration: "add a new pattern to CLAUDE.md"

### How Chat Commands Work

You can interact with the template using **slash commands** or **natural language**:

#### Slash Commands (Skills)

Invoke specialized skills directly:

```
/dotnet-engineer     - .NET/C# development tasks
/unit-tester         - Write MSTest unit tests
/code-reviewer       - Review code for quality and architecture
/architect           - System design and architecture decisions
/blazor-specialist   - Blazor UI development
/maui-specialist     - MAUI mobile app development
/playwright-tester   - E2E and UI testing
/database-migration  - EF Core migrations and database work
/integration-specialist - External API integrations
/performance-engineer   - Performance optimization
/security            - Security architecture and compliance
/api-security        - API security implementation
/software-security   - Application security practices
/technical-writer    - Documentation creation
```

#### Natural Language

Just describe what you want:

```
"Implement CQRS commands and queries for the Budget entity"
"Add API endpoints for Budget management"
"Write unit tests for CreateBudgetHandler"
"Review the current domain structure"
"Optimize database queries in the Budgets domain"
"Create E2E tests for the login flow"
```

The AI automatically:
- Recognizes the work type
- Loads relevant context files from `.claude/`
- Invokes appropriate skills
- Spawns agents if needed
- Follows all patterns and conventions

#### Structured Task Requests

For complex work, provide structured details:

```
Implement Budget Domain

Requirements:
- Create entity, model, domain layer
- Implement CQRS commands (Create, Update, Delete)
- Implement queries (GetById, GetList)
- Add API endpoints
- Write unit tests

Domain: Budgets
Entity: Budget
Properties: Name, Amount, StartDate, EndDate
```

### Are Agents Created Automatically?

**Yes.** Agents are spawned automatically when needed. You don't need to request them explicitly.

**When agents are spawned automatically:**

- **Complex exploration** - "Find all usages of Budget entity across the codebase"
  - → Spawns `Explore` agent

- **Multi-step implementations** - "Implement complete CQRS for Budget domain"
  - → Spawns `general-purpose` agent

- **Parallel work** - "Review code AND run tests AND update docs"
  - → Spawns multiple agents in parallel

- **Large refactoring** - "Refactor all handlers in the Budgets domain"
  - → Spawns task-specific agents

- **Research tasks** - "How is authentication currently implemented?"
  - → Spawns `Explore` agent

**What you'll see:**

The AI will transparently inform you when spawning agents:

```
"I'll use an Explore agent to search the codebase for Budget entity usages..."
"Spawning a general-purpose agent to implement the CQRS handlers..."
"Creating parallel agents to handle testing and documentation..."
```

**Progress tracking:**

All agents automatically:
- Write progress to `.claude/progress/[task-name]-progress.md`
- Report structured results
- Move completed work to `.claude/completed/`

**You control the process:**
- Request specific approaches: "Search for this manually without agents"
- Ask for parallel work: "Run tests and build in parallel"
- Request agent usage: "Use an agent to explore the authentication flow"

**Bottom line:** Focus on **what you want done**, not **how** it gets done. The AI handles orchestration.

### How Does the AI Choose Which Skill to Use?

Three systems work together automatically:

#### 1. Skills (Specialized Prompts)

**Skills are invoked when:**

**User explicitly requests:**
```
/dotnet-engineer
/unit-tester
/code-reviewer
```

**User's request matches skill description:**
```
You: "Review this code for SOLID principles"
AI: [Recognizes code review → invokes code-reviewer skill]

You: "Write unit tests for CreateBudgetHandler"
AI: [Recognizes testing → invokes unit-tester skill]

You: "Implement CQRS handlers for Budget"
AI: [Recognizes .NET development → invokes dotnet-engineer skill]
```

**Matching logic:**
- **Keywords**: "review", "test", "implement", "optimize", "secure"
- **Context**: Code review vs. development vs. testing
- **Scope**: Architecture vs. implementation vs. documentation

#### 2. Agents (Autonomous Workers)

**Agents are spawned via Task tool for:**
- **Complex exploration** → `Explore` agent
- **Multi-step tasks** → `general-purpose` agent
- **Planning work** → `Plan` agent
- **Git operations** → `Bash` agent

These are different from skills—they're autonomous workers for complex tasks.

#### 3. Context Files (Automatic Loading)

**Context files from `.claude/` are loaded based on Work-Type Context Mapping:**

```
Your request: "Implement CQRS for Budget"

AI automatically loads:
- .claude/skills/dotnet-engineer.md
- .claude/patterns/cqrs-patterns.md
- .claude/reference/critical-rules.md
- .claude/reference/templates/command-handler.cs.txt
```

#### Complete Decision Flow Example

```
You: "Add Budget entity with CQRS handlers and unit tests"

AI process:
1. Recognize work type: CQRS Implementation + Testing

2. Load context files automatically:
   - .claude/skills/dotnet-engineer.md
   - .claude/patterns/cqrs-patterns.md
   - .claude/skills/unit-tester.md
   - .claude/patterns/testing-patterns.md

3. Decide if skills needed:
   - Implementation work → May invoke dotnet-engineer skill
   - Testing work → May invoke unit-tester skill

4. Decide if agents needed:
   - Complex task → May spawn agent for exploration
   - Or handle directly if straightforward

5. Execute work following loaded patterns

6. Write progress to .claude/progress/
```

**You don't need to worry about it.** Just make natural requests, and the AI handles:
- Skill invocation
- Agent spawning
- Context loading
- Pattern following
- Progress tracking

The AI will transparently communicate what's happening:
```
"Loading CQRS patterns and dotnet-engineer context..."
"Invoking unit-tester skill for test generation..."
"Spawning Explore agent to search the codebase..."
```

### Quick Reference: Interaction Patterns

| What You Want | How to Ask | What Happens |
|---------------|------------|--------------|
| **Implement feature** | "Implement CRUD for Budget" | Loads dotnet-engineer skill + CQRS patterns |
| **Write tests** | "Write tests for Budget handlers" | Loads unit-tester skill + testing patterns |
| **Review code** | "Review Budget implementation" | Loads code-reviewer skill + critical rules |
| **Optimize performance** | "Optimize Budget queries" | Loads performance-engineer skill |
| **Find code** | "Find all Budget usages" | Spawns Explore agent |
| **Complex task** | "Refactor entire Budgets domain" | Spawns agent + loads relevant skills |
| **Architecture decision** | "Design payment module architecture" | Loads architect skill + architecture patterns |
| **Security** | "Secure the Budget API" | Loads api-security skill + security patterns |

## How the Template Learns from Usage

The template creates **institutional memory** through structured documentation, enabling continuous improvement across sessions.

### Learning Mechanisms

#### 1. Session Context Memory

[`.claude/session-context.md`](.claude/session-context.md) maintains a living record of project knowledge:

```markdown
# Session Context

## Project Patterns Discovered
- Budget entity uses soft delete pattern (DeletedAt timestamp)
- All monetary amounts use decimal(18,2) precision
- Date ranges validated: EndDate must be > StartDate

## Architectural Decisions
- Decision: Use Redis for caching reference data
  Rationale: Reference data rarely changes, reduces DB load
  Date: 2026-02-15

## Known Issues
- None currently

## Next Session Should Know
- Budget domain is complete reference implementation
- Follow Budget patterns for new domains
```

**Session workflow:**
- **Start** → Read session-context.md (learn from past)
- **Work** → Apply learned patterns
- **End** → Update session-context.md (teach future sessions)

#### 2. Completed Task Archive

Finished tasks in [`.claude/completed/`](.claude/completed/) provide historical context:

```markdown
# Implement Budget Domain - Progress

## What Was Done
- Created Budget entity with soft delete
- Implemented CQRS commands: Create, Update, Delete
- Added validation: EndDate > StartDate

## Patterns Established
- Command parameters: individual values, not model objects
- Soft delete: use DeletedAt, not IsDeleted boolean
- Mapping: Mapster with explicit configuration

## Issues Encountered
- Initial approach used repository pattern
- Refactored to DataContext extensions
- Lesson: Check existing code before creating new patterns
```

**Value for future sessions:**
- Review what patterns worked
- See what issues were encountered
- Understand why decisions were made

#### 3. Progressive Pattern Documentation

As project-specific patterns emerge, they're documented:

```markdown
# .claude/project/domains.md

## Budget Domain

### Validation Rules
- EndDate must be after StartDate
- Amount must be positive
- Name required, max 200 characters

### Business Rules
- Budgets use soft delete (DeletedAt)
- Budget can have multiple Goals
- Goals can have multiple Deposits

### Learned Patterns
- Use decimal(18,2) for all monetary amounts
- Cache budget summaries in Redis (1 hour TTL)
```

#### 4. Decision Records

Architectural decisions create permanent knowledge:

```markdown
# .claude/completed/architecture-decisions.md

## ADR-001: Use Redis for Caching
Date: 2026-02-15
Status: Accepted

Context: Budget API receiving 1000+ req/s for reference data

Decision: Implement Redis caching layer

Consequences:
- Reduced DB load by 80%
- Added Redis dependency
- Cache invalidation strategy needed
```

### What Gets Learned

| Knowledge Type | Storage Location | Update Frequency |
|----------------|------------------|------------------|
| **Patterns discovered** | `session-context.md` | Every session |
| **Architectural decisions** | `completed/` archive | When made |
| **Domain-specific rules** | `.claude/project/domains.md` | As discovered |
| **Common issues** | `session-context.md` | When encountered |
| **Code conventions** | `session-context.md` | As established |
| **Performance optimizations** | `completed/` tasks | After implementation |
| **Testing strategies** | `session-context.md` | As proven effective |
| **Integration patterns** | `.claude/patterns/` | When stabilized |

### Continuous Improvement Example

```
Session 1: Implement Budget Domain
├─ Discovers: Budget uses soft delete pattern
├─ Writes to: session-context.md
│   "Budget domain uses DeletedAt timestamp for soft delete"
└─ Archives: completed/implement-budget-domain-progress.md

Session 2: Implement Goals Domain
├─ Reads: session-context.md (learns soft delete pattern)
├─ Applies: Same soft delete approach to Goals
├─ Discovers: Goals require Budget foreign key validation
├─ Writes to: session-context.md
│   "All child entities validate parent foreign keys exist"
└─ Archives: completed/implement-goals-domain-progress.md

Session 3: Implement Debts Domain
├─ Reads: session-context.md (learns both patterns)
├─ Applies: Soft delete + foreign key validation
├─ Discovers: Debts need additional audit fields
├─ Writes to: session-context.md
│   "Financial entities include audit fields: CreatedBy, ModifiedBy"
└─ Archives: completed/implement-debts-domain-progress.md
```

Each session builds on accumulated knowledge!

### Enhancing the Learning System

#### Create Domain-Specific Patterns

```bash
# Document patterns as they emerge
.claude/patterns/budget-domain-patterns.md
.claude/patterns/authentication-patterns.md
.claude/patterns/caching-strategy.md
```

#### Maintain Decision Log

```markdown
# .claude/project/decisions.md

## All Architectural Decisions

### ADR-001: CQRS with I-Synergy Framework
Date: 2026-02-10
Status: Accepted
Impact: High

### ADR-002: PostgreSQL over SQL Server
Date: 2026-02-12
Status: Accepted
Impact: Medium
```

#### Regular Context Reviews

Consolidate learnings periodically:

```
"Review .claude/session-context.md and consolidate learnings into permanent documentation"
"Extract reusable patterns from Budget implementation into .claude/patterns/"
"Update domains.md with all discovered business rules"
```

#### Pattern Extraction

After major features:

```
"Analyze Budget implementation and extract reusable patterns"
"Document validation approach as a pattern"
"Create caching strategy guide based on Budget implementation"
```

### Learning System Workflow

```
┌─────────────────────────────────────────────────────────┐
│ Session Start                                           │
│ ├─ Read session-context.md                             │
│ ├─ Review completed/ archive                           │
│ └─ Load established patterns                           │
└─────────────────────────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────────┐
│ During Work                                             │
│ ├─ Apply learned patterns                              │
│ ├─ Discover new patterns                               │
│ ├─ Track decisions                                      │
│ └─ Document issues and solutions                       │
└─────────────────────────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────────┐
│ Session End                                             │
│ ├─ Update session-context.md with learnings            │
│ ├─ Archive progress files to completed/                │
│ ├─ Document new patterns                               │
│ └─ Record architectural decisions                      │
└─────────────────────────────────────────────────────────┘
```

### What the Template Does NOT Do

**Limitations:**
- ❌ Train the AI model (no fine-tuning)
- ❌ Persist memory across different projects automatically
- ❌ Share learnings between unrelated projects
- ❌ Automatically detect patterns without guidance
- ❌ Modify its own core rules without explicit instruction

**What it DOES:**
- ✅ Maintain session-to-session context within a project
- ✅ Document discovered patterns explicitly
- ✅ Archive decision history permanently
- ✅ Build institutional knowledge progressively
- ✅ Enable pattern reuse across domains
- ✅ Create searchable knowledge base

### Making the Template Learn Better

**Be explicit about learnings:**

```
"Document this soft delete pattern in session-context.md"
"Add this caching decision to the architecture decisions log"
"Extract this validation approach as a reusable pattern"
"Record this performance optimization for future reference"
```

**Review and consolidate regularly:**

```
"Review session context and move stable patterns to permanent docs"
"Analyze last 5 completed tasks and extract common patterns"
"Update domains.md with all discovered business rules"
"Create a patterns guide for the authentication flow"
```

**Cross-reference learnings:**

```
"Compare Budget and Goals implementations - document common patterns"
"Identify inconsistencies across domains and standardize"
"Extract shared validation logic into documented pattern"
```

### Example: Progressive Learning in Action

**Week 1: Budget Domain**
```markdown
# session-context.md
## Patterns Discovered
- Soft delete with DeletedAt timestamp
- Decimal(18,2) for monetary amounts
```

**Week 2: Goals Domain**
```markdown
# session-context.md
## Patterns Discovered
- Soft delete with DeletedAt timestamp (from Budget)
- Decimal(18,2) for monetary amounts (from Budget)
- Foreign key validation required (new pattern)
- Aggregate totals cached in Redis (new pattern)
```

**Week 3: Debts Domain**
```markdown
# session-context.md
## Patterns Discovered
- Soft delete with DeletedAt timestamp (established)
- Decimal(18,2) for monetary amounts (established)
- Foreign key validation required (established)
- Aggregate totals cached in Redis (established)
- Audit fields: CreatedBy, ModifiedBy (new pattern)
- Financial transactions require idempotency keys (new pattern)
```

**Week 4: Pattern Consolidation**
```markdown
# .claude/patterns/financial-entity-patterns.md

## Financial Entity Standard Pattern

All financial entities must include:
1. Soft delete: DeletedAt timestamp
2. Monetary amounts: decimal(18,2)
3. Foreign key validation
4. Audit fields: CreatedBy, ModifiedBy, CreatedAt, ModifiedAt
5. Redis caching for aggregates (1 hour TTL)
6. Idempotency keys for transactions

Established across: Budget, Goals, Debts domains
Date: 2026-02-16
```

The template transforms from generic patterns to **project-specific institutional knowledge**!

### Benefits of the Learning System

1. **Consistency** - New domains follow established patterns automatically
2. **Efficiency** - Avoid repeating research and decisions
3. **Quality** - Proven patterns reduce bugs and rework
4. **Onboarding** - New team members read session context to understand patterns
5. **Traceability** - Every decision has documented rationale
6. **Evolution** - Patterns improve based on real experience
7. **Knowledge retention** - Nothing is lost between sessions

**Bottom line:** The template creates a **self-improving knowledge base** that makes each session smarter than the last! 📚

## Core Principles

1. **No Shortcuts** - Correct fix is always better than quick fix
2. **Fix Bugs Now** - Don't defer issues unless blocked by infrastructure
3. **Agent Delegation** - All work delegated to specialized agents
4. **Real-Time Progress** - Automatic progress tracking
5. **Session Context** - Read first, update last
6. **Quality First** - Run through checklist before completion
7. **Document Learnings** - Update session context with decisions

## Documentation

- **README.md** (this file) - Comprehensive overview and quick reference
- **CLAUDE.md** - Main orchestration file (v2, optimized)
- **TEMPLATE-USAGE.md** - Detailed usage guide and customization
- **.claude/reference/** - Quick reference guides
- **.claude/patterns/** - Implementation patterns
- **.claude/skills/** - Specialized agent personas

## Examples

### Token Replacement Workflow

```bash
# 1. Copy command handler template
cp .claude/reference/templates/command-handler.cs.txt CreateBudgetCommand.cs

# 2. Replace tokens (example with sed)
sed -i 's/{ApplicationName}/BudgetTracker/g' CreateBudgetCommand.cs
sed -i 's/{Domain}/Budgets/g' CreateBudgetCommand.cs
sed -i 's/{Entity}/Budget/g' CreateBudgetCommand.cs

# 3. Save to correct location
mv CreateBudgetCommand.cs src/BudgetTracker.Domain.Budgets/Features/Budget/Commands/
```

### Quality Check Workflow

```bash
# Before completing task, verify with Claude:
"Review implementation against .claude/checklists/pre-submission.md"

# Claude will check:
# - Agent workflow compliance
# - Architecture patterns
# - Code quality standards
# - Security best practices
# - Testing coverage
# - Documentation completeness
```

## Version History

- **v1 (2026-02-16):** Previous version (1,614 words, ~2,150 tokens)
- **v2 (2026-02-16):** Current version (693 words, ~920 tokens)
  - 57% token reduction
  - 7 focused rules
  - Work-type context mapping
  - End-positioned verification
  - Research-backed optimizations

## Contributing

This template is designed to be:

- **Generic** - Works for any .NET project
- **Modular** - Easy to customize individual components
- **Extensible** - Add your own patterns and skills
- **Maintainable** - Clear separation of concerns
- **Research-Backed** - Based on Claude Context OS v2 best practices

### Improving the Template

1. Keep improvements generic (use tokens)
2. Update modular files (not monolithic CLAUDE.md)
3. Test with fresh project
4. Document in appropriate section
5. Follow v2 principles (no emphatic language, no prose, instructions only)

## Credits

Built with research from:
- Claude Context OS v2 documentation
- LLM cognitive load optimization studies
- Clean Architecture patterns by Robert C. Martin
- Domain-Driven Design by Eric Evans
- CQRS pattern implementations

## License

[Your License Here]

## Support

- **Quick Start:** See Quick Start section above
- **Detailed Guide:** Read `TEMPLATE-USAGE.md`
- **Common Issues:** Check `.claude/reference/critical-rules.md`
- **Implementation Examples:** Review `.claude/patterns/`
- **Quality Checklist:** Follow `.claude/checklists/pre-submission.md`

---

**Remember:** This is a template. Customize the `.claude/project/` files for your specific needs before starting development. All `{tokens}` must be replaced with your actual values.

**Get Started:** Copy the template, customize project files, replace tokens, and start building with AI-assisted development using Claude Code.
