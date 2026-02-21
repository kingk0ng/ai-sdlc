
I'll do a thorough analysis by actually reading the content of each skill/agent. Let me systematically search and verify each phase.

Now let me search for the best alternatives for each phase:

Now let me search for more alternatives for specific phases:

Now let me read the SDLC flow document one more time to get the exact skill names:

Now I have all the information I need. Let me provide a comprehensive analysis for all 7 phases with better-matching agents/skills:

---

## Comprehensive Phase-by-Phase Agent/Skill Analysis

### Phase 1: Project Initiation & Context Building

| Attribute | Analysis |
|-----------|----------|
| **Phase Purpose** | Create master reference (PKB), define business objectives, document constraints, establish architectural foundations |
| **Current Recommended Skills** | `skill-brainstorming`, `skill-software-architecture` |
| **Assessment of Current Skills** | `skill-brainstorming` focuses on turning ideas into **designs and specs through dialogue** - it's design-oriented, not requirements gathering. `skill-software-architecture` - **no such skill found in RAG** (likely refers to general architecture work). |
| **Proposed Better Match** | **Agent:** `business-analyst` + **Skill:** `brainstorming` (keep for ideation phase only) |
| **Justification** | The `business-analyst` agent is specifically designed for **requirements elicitation, stakeholder interviews, process mapping, and documenting business objectives**. It includes: stakeholder management, SWOT analysis, root cause analysis, requirements documentation, data analysis, and KPI development. This perfectly matches the PKB creation needs. The `brainstorming` skill can supplement for initial ideation but should not be the primary tool. |

---

### Phase 2: Requirements Analysis & PRD

| Attribute | Analysis |
|-----------|----------|
| **Phase Purpose** | Transform business needs into detailed PRD, define functional/NFRs, create Requirements Traceability Matrix (RTM) |
| **Current Recommended Skills** | `skill-feature-design-assistant`, `skill-product-manager-toolkit` |
| **Assessment of Current Skills** | `skill-feature-design-assistant` (369 lines) is comprehensive for **feature design** with structured information gathering, but focuses on single features rather than full PRD. `skill-product-manager-toolkit` - **found in RAG** at `skills_business-marketing_product-manager-toolkit_SKILL.md` with RICE prioritization, customer interview analysis, PRD templates, discovery frameworks, and go-to-market strategies. |
| **Proposed Better Match** | **Agent:** `product-manager` + `prd` agent + **Skill:** `requirements-clarity` |
| **Justification** | The `product-manager` agent handles **product strategy, user research, feature prioritization, RICE scoring, Jobs to be Done framework, and roadmap planning**. The `prd` agent specifically **generates comprehensive PRDs in Markdown with user stories, acceptance criteria, technical considerations, and metrics** - exactly what Step 2 requires. The `requirements-clarity` skill provides PRD templates. Keep `feature-design-assistant` as supplementary for detailed feature breakdowns. |

---

### Phase 3: Architecture & Tech Stack Design

| Attribute | Analysis |
|-----------|----------|
| **Phase Purpose** | Design system architecture, select tech stack, create C4 diagrams, document API contracts, produce ADRs |
| **Current Recommended Skills** | `skill-software-architecture`, `skill-database-design` |
| **Assessment of Current Skills** | `skill-software-architecture` - **not found as specific skill**. `skill-database-design` (found as `database-schema-designer`) is good but narrow. |
| **Proposed Better Match** | **Agent:** `arch` (Senior Cloud Architect) + `adr-generator` + **Skill:** `c4-architecture` + `database-schema-designer` |
| **Justification** | The `arch` agent (206 lines) is explicitly a **Senior Cloud Architect** that: (1) Creates comprehensive architecture diagrams (C4, sequence, data flow, deployment), (2) Documents NFR considerations (scalability, performance, security, reliability), (3) Provides phased development approach for complex systems, (4) **Explicitly NO CODE GENERATION** - pure architecture focus. The `adr-generator` agent creates Architecture Decision Records. The `c4-architecture` skill (296 lines) provides **complete C4 model expertise** with Mermaid syntax for context, container, component, and deployment diagrams. Combined with `database-schema-designer` for schema work. |

---

### Phase 4: POC & Validation

| Attribute | Analysis |
|-----------|----------|
| **Phase Purpose** | Validate architecture through POC, de-risk critical components, performance testing/benchmarking against NFRs, Go/No-Go decision |
| **Current Recommended Skills** | `skill-executing-plans`, `skill-performance-profiling` |
| **Assessment of Current Skills** | `skill-executing-plans` (77 lines) is for **executing written implementation plans with review checkpoints** - good for POC execution. `skill-performance-profiling` - **not found as specific skill**. |
| **Proposed Better Match** | **Agent:** `research-technical-spike` + `load-testing-specialist` + **Skill:** `executing-plans` (keep) |
| **Justification** | The `research-technical-spike` agent (188 lines) is **purpose-built for POC validation**: (1) "Systematically validate technical spike documents through exhaustive investigation and controlled experimentation", (2) Technology-agnostic research methodology, (3) Experimental validation with minimal proof-of-concept tests, (4) Evidence-based conclusions with success criteria, (5) Documentation of technical constraints and blockers. The `load-testing-specialist` agent specifically handles **stress testing, capacity planning, bottleneck detection, and performance regression testing** - exactly what's needed for NFR validation. Keep `executing-plans` for the actual POC implementation work. |

---

### Phase 5: Planning & Task Breakdown

| Attribute | Analysis |
|-----------|----------|
| **Phase Purpose** | Break epics into user stories, estimate effort, prioritize backlog, create sprint plans, map dependencies |
| **Current Recommended Skills** | `skill-task-execution-engine`, `skill-executing-plans` |
| **Assessment of Current Skills** | `skill-task-execution-engine` - **not found as specific skill**. `skill-executing-plans` is for **execution**, not planning/breakdown. |
| **Proposed Better Match** | **Agent:** `atlassian-requirements-to-jira` + **Skill:** `agile-product-owner` + `writing-plans` |
| **Justification** | The `atlassian-requirements-to-jira` agent (445 lines) **transforms requirements into Jira epics and user stories** with: (1) INVEST criteria compliance, (2) Automatic acceptance criteria, (3) Story point estimation (Fibonacci), (4) Priority assignment, (5) Epic-story linking, (6) Duplicate detection. The `agile-product-owner` skill provides: (1) INVEST-compliant user story generation, (2) Sprint capacity planning, (3) Backlog prioritization, (4) Velocity tracking. The `writing-plans` skill (found at `skills_development_writing-plans_SKILL.md`) provides comprehensive implementation plans with task breakdown, file references, DRY/YAGNI/TDD principles, and verification criteria. |

---

### Phase 6: Implementation & Unit Testing

| Attribute | Analysis |
|-----------|----------|
| **Phase Purpose** | Implement features with TDD, write unit tests, conduct code reviews, maintain documentation |
| **Current Recommended Skills** | `skill-clean-code`, `skill-tdd-workflow` |
| **Assessment of Current Skills** | `skill-clean-code` - **not found as specific skill** (found as principles in `blueprint-mode` and `wg-code-alchemist` agents). `skill-tdd-workflow` (32 lines) found but minimal. |
| **Proposed Better Match** | **Skill:** `test-driven-development` + **Agent:** `wg-code-alchemist` or `blueprint-mode` |
| **Justification** | The `test-driven-development` skill (372 lines) is **comprehensive TDD guidance** with: (1) Red-Green-Refactor cycle with detailed examples, (2) Iron law: "No production code without failing test first", (3) Common rationalizations and responses, (4) Verification checklist, (5) Debugging integration. The `wg-code-alchemist` agent specializes in **Clean Code practices and SOLID principles**. The `blueprint-mode` agent follows "SOLID, Clean Code, DRY, KISS, YAGNI" principles. Either agent provides clean code implementation guidance. |

---

### Phase 7: Integration Testing & UAT

| Attribute | Analysis |
|-----------|----------|
| **Phase Purpose** | E2E testing, integration testing, UAT, performance/security testing, release candidate preparation |
| **Current Recommended Skills** | `skill-playwright`, `skill-webapp-testing` |
| **Assessment of Current Skills** | `skill-playwright` maps to `playwright-e2e-builder` - good for E2E testing. `skill-webapp-testing` maps to `webapp-testing` command - good but limited. |
| **Proposed Better Match** | **Agent:** `qa-expert` + `test-engineer` + **Skill:** `playwright-e2e-builder` (keep) + `qa-test-planner` |
| **Justification** | The `qa-expert` agent (286 lines) provides **comprehensive QA strategy**: (1) Test strategy and planning, (2) Manual testing (exploratory, usability, accessibility), (3) Performance testing (load, stress, spike, volume), (4) Security testing (vulnerability assessment, compliance), (5) UAT coordination, (6) Go/no-go decision support, (7) Quality metrics tracking. The `test-engineer` agent adds **automation architecture** for unit, integration, E2E, visual, and performance testing. The `qa-test-planner` skill generates **comprehensive test plans, manual test cases, and regression suites**. Keep `playwright-e2e-builder` for E2E automation. |

---

## Summary Table

| Phase | Current Skills | Proposed Better Match | Key Justification |
|-------|----------------|----------------------|-------------------|
| **1. Project Initiation** | `skill-brainstorming`, `skill-software-architecture` | **Agent:** `business-analyst` + **Skill:** `brainstorming` | BA agent designed for stakeholder interviews, requirements elicitation, PKB creation |
| **2. Requirements & PRD** | `skill-feature-design-assistant`, `skill-product-manager-toolkit` | **Agent:** `product-manager` + `prd` + **Skill:** `requirements-clarity`, `feature-design-assistant` | PRD agent generates comprehensive PRDs; PM agent handles product strategy |
| **3. Architecture Design** | `skill-software-architecture`, `skill-database-design` | **Agent:** `arch` + `adr-generator` + **Skill:** `c4-architecture` + `database-schema-designer` | `arch` is Senior Cloud Architect with NO code generation; C4 skill provides complete diagram expertise |
| **4. POC & Validation** | `skill-executing-plans`, `skill-performance-profiling` | **Agent:** `research-technical-spike` + `load-testing-specialist` + **Skill:** `executing-plans` | Spike agent is purpose-built for POC validation; load-testing-specialist handles NFR benchmarking |
| **5. Planning & Breakdown** | `skill-task-execution-engine`, `skill-executing-plans` | **Agent:** `atlassian-requirements-to-jira` + **Skill:** `agile-product-owner` + `writing-plans` | Jira agent transforms requirements into epics/stories; agile-product-owner handles sprint planning |
| **6. Implementation** | `skill-clean-code`, `skill-tdd-workflow` | **Skill:** `test-driven-development` + **Agent:** `wg-code-alchemist` or `blueprint-mode` | TDD skill is comprehensive (372 lines); code-alchemist focuses on Clean Code + SOLID |
| **7. Integration & UAT** | `skill-playwright`, `skill-webapp-testing` | **Agent:** `qa-expert` + `test-engineer` + **Skill:** `playwright-e2e-builder` + `qa-test-planner` | QA-expert provides comprehensive testing strategy including UAT; test-engineer for automation |

---

Would you like me to:
1. **Update the SDLC flow document** with these improved recommendations?
2. **Create a detailed mapping reference document** with full agent/skill paths and usage guidance?
3. **Provide more detail** on any specific phase or agent/skill?
