# AI-Assisted SDLC Project Context

## 📋 Project Overview

This project provides a comprehensive framework for AI-assisted Software Development Life Cycle (SDLC) with two primary workflows:

1. **New Application Development Flow** - Building applications from scratch using AI assistance
2. **Legacy System Migration Flow** - Modernizing existing systems through reverse engineering

The project includes a rich library of **converted templates** containing:
- **Agents**: Specialized AI agents for different domains (AI specialists, development teams, DevOps, etc.)
- **Commands**: Executable commands for automation, deployment, testing, and utilities
- **Integrations**: MCP (Model Context Protocol) integrations for external services
- **Skills**: Reusable knowledge modules covering development, AI research, security, etc.

---

## 🔄 AI-Assisted SDLC Flows

### Flow 1: New Application Development (new-app-flow.md)

**Purpose**: Create new applications from scratch using a "Chain of Context" approach where each step builds on the previous one.

#### Core Principle
**"Output of Step n = Input of Step n+1"** while maintaining Project Context (Step 1) as foundation throughout.

#### Development Steps

| Step | Output | Next Use | Key Activities |
|------|--------|----------|----------------|
| **1. Project Initiation** | Project Knowledge Base (PKB) | All subsequent steps | Create master reference: business logic, constraints, standards |
| **2. Requirements & PRD** | Product Requirements Document | Architecture design, planning, UAT | Analyze use cases, define functional/non-functional requirements |
| **3. Architecture Design** | System Design Document (SDD) | POC, task breakdown, implementation | Design system architecture, select tech stack, create DB schema |
| **4. POC & Validation** | Validation Results | Planning confirmation | Build proof-of-concept for riskiest components |
| **5. Planning & Breakdown** | Project Backlog | Implementation | Break epics into stories, create WBS, prioritize tasks |
| **6. Implementation** | Feature Code + Tests | Integration testing | Code features with unit tests following standards |
| **7. Integration & UAT** | Tested Product | Production | End-to-end testing, user acceptance testing |

**Key Benefit**: AI maintains "memory" across steps, preventing contradictions and ensuring consistency.

---

### Flow 2: Legacy System Migration (migration-flow.md)

**Purpose**: Modernize legacy systems through reverse engineering when documentation is missing.

#### Core Principle
**"Code-to-Requirement"** - Extract business logic from existing code before modernization.

#### Migration Steps

| Step | Input | Output | AI Role |
|------|-------|--------|---------|
| **1. Code Discovery** | Legacy Source Code + Structure | System Map & Component Catalog | Analyze code structure, identify entry points, map technologies |
| **2. Logic Extraction** | System Map + Module Code | Extracted Business Rules (EBR) | Convert code to human-readable business logic |
| **3. Gap Analysis** | EBR + New Requirements | Modernized PRD | Create target requirements identifying as-is vs to-be |
| **4. Architecture Design** | Modernized PRD + Old Schema | New System Design + Migration Scripts | Design modern architecture and data migration plan |
| **5. Implementation** | New Design + Old System | Modernized System | Implement with parity tests to ensure consistency |

#### Critical Enhancements

**Using Process Flow Diagrams:**
- **Step 1**: Provide as "map" for AI to understand system structure
- Enables accurate module grouping by business function

**Using Input/Output Examples:**
- **Step 2**: Validate extracted logic against real data
- **Step 6**: Create automated parity tests (new system = old system results)
- Reduces hallucination, ensures accuracy

**Critical Considerations:**
- **Code Volume**: Process module-by-module for large monoliths
- **Hidden Bugs**: Decide whether to preserve or fix legacy bugs
- **Testing**: Use I/O examples as ground truth for regression testing

---

## 📁 Converted Templates Structure

The `converted-templates/` directory contains 600+ templates organized by type:

### 1. Agents (`agents/`)

Specialized AI agents for specific development tasks and domains:

- **AI Specialists**: Prompt engineers for LLM optimization, model evaluators for benchmarking, AI ethics advisors
- **Development Teams**: Test generators for comprehensive test cases, test runners for failure diagnosis, code reviewers
- **DevOps & Infrastructure**: MCP developers for Model Context Protocol servers, deployment specialists
- **Expert Advisors**: Architecture advisors, security penetration testers, QA experts for quality strategy
- **Business & UX**: UX researchers for user behavior analysis, product strategists
- **Specialized Teams**: Game development, media processing, workflow automation

**Format**: Each agent defines use cases with examples, invocation contexts, and specific expertise boundaries.

### 2. Commands (`commands/`)

Executable automation commands with specific argument hints and capabilities:

- **Automation**: Husky CI pre-commit checks, workflow orchestration, CI/CD pipeline management
- **Deployment**: Blue-green deployment strategies, containerization, release preparation with validation
- **Testing**: Test automation orchestration (parallel/sequential/conditional), E2E setup, mutation testing, test changelog automation
- **Performance**: Bundle size optimization with webpack-bundle-analyzer, performance audits with Lighthouse, caching strategies
- **Security**: Authentication system implementation (OAuth/JWT/MFA), penetration testing, secrets scanning, security hardening
- **Database**: Supabase schema sync via MCP integration, migration assistance, type generation
- **Game Development**: Game testing framework automation with CI integration
- **Utilities**: Code quality review, systematic debugging, architecture scenario exploration
- **Project Management**: PAC (Product as Code) tools for epic/ticket management, changelog automation

**Format**: Each command specifies allowed tools, argument hints, complexity level, and estimated token usage.

### 3. Integrations (`integrations/`)

Model Context Protocol (MCP) server integrations for AI-to-service connectivity:

- **Database**: 
  - PostgreSQL, MySQL - Direct database access for queries and management within Claude Code
  - MongoDB - NoSQL document database integration
  - Supabase MCP - Schema synchronization, migration management, real-time monitoring
  - Neon - Serverless Postgres with Management API integration for branching and SQL execution
- **DevTools**: 
  - GitHub - Repository management, issue tracking, pull requests
  - Chrome DevTools - Browser automation, debugging, performance analysis via MCP
  - Playwright - Browser automation with accessibility snapshots for testing
  - Railway - Deployment platform integration for project and infrastructure management
  - Context7 - Up-to-date library/framework documentation fetching
- **Web**: 
  - Web Reader MCP - Full-page content extraction and structured data retrieval
  - Web Search Prime - Real-time information retrieval and web search via Z.AI
  - Fetch - Web content fetching and external API integration
- **Productivity**: 
  - Notion API - Workspace integration for documentation and knowledge management
  - Monday.com API - Work OS integration for agent workflow operations
- **Browser Automation**: 
  - Browserbase - Cloud browser automation with Stagehand for web interactions
  - Browser Server - AI agent-controlled web browsing via browser-use
  - Playwright variants - Multiple implementations for different automation needs
- **Marketing**: 
  - Google Ads, Facebook Ads - MCP servers for programmatic ad management
- **Audio**: 
  - ElevenLabs - Text-to-speech, voice cloning, audio processing, transcription

**Format**: Each integration specifies MCP server configuration, environment variables, capabilities, and use cases.

### 4. Skills (`skills/`)

Reusable knowledge modules with complexity levels and capability definitions:

- **AI Research**: 
  - Agent development (tool building, memory systems, autonomous patterns)
  - LLM fine-tuning with Axolotl (LoRA/QLoRA, DPO/KTO)
  - Prompt engineering and LLM application patterns (RAG pipelines, agent architectures)
  - Computer use agents for desktop automation
  - CrewAI for role-based multi-agent collaboration
- **Development**: 
  - API design patterns - REST vs GraphQL vs tRPC decision-making, versioning, pagination
  - API integration specialist - Third-party API integration with OAuth, rate limiting, retry logic
  - Backend/Frontend patterns - Server-side best practices for Node.js, Express, Next.js
  - Senior roles - Fullstack, backend, frontend development comprehensive guides
  - Architecture patterns - Software architecture, database design
- **Web Development**: 
  - React patterns and UI patterns for state management and component design
  - Next.js best practices and Vercel deployment strategies
  - Svelte development including Storybook integration and testing
  - GraphQL schema design with DataLoader for N+1 prevention
- **Database**: 
  - Schema design and optimization for PostgreSQL, MySQL
  - Supabase best practices including RLS, auth, and real-time features
  - Database migration strategies and query optimization
  - Using Neon for serverless Postgres with branching
- **Security**: 
  - API security best practices (authentication, authorization, input validation)
  - Ethical hacking methodology and penetration testing
  - Security compliance and vulnerability assessment
- **Testing**: 
  - Test-driven development workflow and testing patterns
  - Playwright for E2E testing and web application testing
  - Test automation with comprehensive coverage strategies
- **Workflow Automation**: 
  - n8n workflow patterns for webhook processing, API integration, database operations
  - Task orchestration and execution engines
  - CI/CD automation strategies
- **Analytics & Media**: 
  - Data processing with metrics tracking
  - Video processing (Remotion, Manim, Motion Canvas)
  - Audio generation with AudioCraft

**Format**: Each skill includes description, complexity level (basic/medium/advanced), keywords for discovery, required capabilities, estimated token usage, and may reference supporting materials.

---

## 🎯 Skill Matching Framework for SDLC Steps

### Matching Skills to New App Development

| SDLC Step | Recommended Skills | Purpose |
|-----------|-------------------|---------|
| **1. Project Initiation** | `skill-brainstorming`, `skill-create-plan`, `skill-architecture`, `skill-software-architecture` | Ideation, planning, and architectural foundations |
| **2. Requirements & PRD** | `skill-feature-design-assistant`, `skill-senior-architect`, `skill-api-patterns`, `skill-feature-design-assistant` | Requirements analysis and API design decisions |
| **3. Architecture Design** | `skill-software-architecture`, `skill-database-design`, `skill-api-patterns`, `skill-backend-patterns`, `skill-graphql` | System design with REST vs GraphQL decisions, database schema design |
| **4. POC & Validation** | `skill-executing-plans`, `skill-systematic-debugging`, `skill-performance-profiling`, `skill-production-code-audit` | Proof of concept implementation and performance validation |
| **5. Planning & Breakdown** | `skill-task-execution-engine`, `skill-executing-plans`, `skill-writing-plans`, `skill-agile-workflow` | Task decomposition and sprint planning |
| **6. Implementation** | `skill-clean-code`, `skill-testing-patterns`, `skill-tdd-workflow`, `skill-typescript-expert`, `skill-react-dev`, `skill-backend-dev-guidelines` | Code implementation with test-driven development |
| **7. Integration & UAT** | `skill-webapp-testing`, `skill-playwright`, `skill-web-quality-audit`, `skill-test-automation-orchestrator` | End-to-end testing and quality assurance |

### Matching Skills to Legacy Migration

| Migration Step | Recommended Skills | Purpose |
|----------------|-------------------|---------|
| **1. Code Discovery** | `skill-code-reviewer`, `skill-production-code-audit`, `skill-architecture`, `skill-api-documentation-generator` | Analyze legacy code structure and generate system maps |
| **2. Logic Extraction** | `skill-codex-review`, `skill-code-review-checklist`, `skill-api-documentation-generator`, `skill-api-patterns` | Extract business rules from code, document existing API patterns |
| **3. Gap Analysis** | `skill-senior-architect`, `skill-feature-design-assistant`, `skill-software-architecture`, `skill-api-patterns` | Define modern requirements bridging legacy to new system |
| **4. Architecture Design** | `skill-software-architecture`, `skill-database-schema-designer`, `skill-api-patterns`, `skill-graphql`, `skill-backend-patterns` | Design modern architecture with API modernization (REST/GraphQL) |
| **5. Implementation** | `skill-clean-code`, `skill-test-driven-development`, `skill-systematic-debugging`, `skill-testing-patterns`, `skill-parity-testing` | Implement with parity tests ensuring legacy behavior preservation |

### Cross-Cutting Skills (All Phases)

- **Version Control**: `skill-git-commit-helper`, `skill-git-pushing`, `skill-gh-fix-ci`, `skill-github-workflow-automation`
- **Security**: `skill-security-review`, `skill-security-compliance`, `skill-api-security-best-practices`, `skill-ethical-hacking-methodology`
- **Performance**: `skill-performance`, `skill-performance-profiling`, `skill-core-web-vitals`, `skill-bundle-optimization`
- **DevOps**: `skill-devops-iac-engineer`, `skill-docker-expert`, `skill-github-workflow-automation`, `skill-cicd-pipeline`
- **Testing**: `skill-test-automation`, `skill-playwright`, `skill-mutation-testing`, `skill-property-based-testing`
- **AI Integration**: `skill-agent-development`, `skill-mcp-builder`, `skill-prompt-engineering`, `skill-llm-app-patterns`

---

## 📊 Metadata Organization

The `metadata/` directory provides structured information:

- **categories.json**: Templates organized by category (command, integration, skill, agent)
- **index.json**: Complete searchable index of all templates
- **tags.json**: Tag-based classification for easier discovery
- **use-cases.json**: Templates mapped to specific use cases
- **stats.json**: Usage statistics and popularity metrics
- **conversion-log.json**: Template conversion history

---

## 🔍 How to Find the Right Skill

### By SDLC Phase

```javascript
// Example: Finding skills for architecture design
categories.skills.development -> filter by keywords: ["architecture", "design", "patterns"]
```

### By Technology

```javascript
// Example: Finding React-specific skills
categories.skills["web-development"] -> filter by keywords: ["react", "nextjs"]
```

### By Complexity

```javascript
// Complexity levels: basic, medium, advanced
// Match to team experience level
```

---

## 🚀 Next Steps: Skill Analysis Plan

### Phase 1: Automated Matching
1. Parse all skill files and extract metadata
2. Create keyword mapping for each SDLC step
3. Build recommendation engine based on:
   - Step requirements
   - Technology stack
   - Team expertise level
   - Project complexity

### Phase 2: Enhancement
1. Add "recommended skills" section to each SDLC step
2. Create skill dependency graphs
3. Build skill progression paths (basic → advanced)

### Phase 3: Integration
1. Create CLI tool for skill recommendation
2. Build interactive skill selector
3. Generate custom SDLC plans with matched skills

---

## 📝 Usage Examples

### Example 1: Starting a New Next.js + Supabase Project

**SDLC Steps + Matched Resources:**

```markdown
Step 1: Project Initiation
- Skills: skill-nextjs-best-practices, skill-brainstorming, skill-create-plan
- Agents: agent-senior-fullstack, agent-architecture-advisor

Step 2: Requirements & API Design
- Skills: skill-feature-design-assistant, skill-api-patterns, skill-graphql
- Commands: command-create-product-requirements-document
- Agents: agent-api-designer

Step 3: Architecture & Database
- Skills: skill-nextjs-best-practices, skill-supabase-postgres-best-practices, skill-database-design
- Commands: command-design-database-schema, command-implement-graphql-api
- Integrations: integration-supabase (MCP for schema sync)

Step 4: POC Implementation
- Skills: skill-nextjs-supabase-auth, skill-clerk-auth, skill-typescript-expert
- Commands: command-setup-development-environment
- Agents: agent-fullstack-developer

Steps 5-7: Development through UAT
- Skills: skill-react-dev, skill-typescript-expert, skill-testing-patterns, skill-playwright
- Commands: command-generate-tests, command-e2e-setup, command-vercel-deploy
- Integrations: integration-playwright-server (for E2E testing)
- Agents: agent-test-generator, agent-test-runner, agent-qa-expert
```

### Example 2: Migrating Legacy PHP + MySQL to Node.js + PostgreSQL

**Migration Steps + Matched Resources:**

```markdown
Step 1: Code Discovery & Mapping
- Skills: skill-code-reviewer, skill-production-code-audit, skill-api-patterns
- Commands: command-analyze-and-explain-code-functionality, command-directory-deep-dive
- Agents: agent-php-pro (for legacy understanding), agent-senior-backend
- Integrations: integration-mysql (MCP for current database access)
- Output: System map identifying all endpoints, database tables, business logic modules

Step 2: Business Logic Extraction
- Skills: skill-api-documentation-generator, skill-database-schema-designer
- Commands: command-code-quality-review, command-api-documentation-generator
- Agents: agent-api-designer, agent-database-specialist
- Integrations: integration-mysql (query and understand existing schema)
- Output: Extracted Business Rules (EBR) document in plain language

Step 3: Gap Analysis & Modern PRD
- Skills: skill-senior-architect, skill-api-patterns (REST vs GraphQL decision)
- Commands: command-create-product-requirements-document
- Agents: agent-architecture-advisor, agent-api-designer
- Output: Modernized PRD with as-is (preserving) vs to-be (improving) sections

Step 4: Modern Architecture Design
- Skills: skill-nodejs-best-practices, skill-typescript-expert, skill-graphql, skill-neon-postgres
- Commands: command-design-rest-api or command-implement-graphql-api, command-design-database-schema
- Integrations: integration-neon or integration-postgresql (MCP setup for new DB)
- Agents: agent-nestjs-expert, agent-database-specialist
- Output: New System Design + Data Migration Scripts

Step 5: Implementation with Parity Testing
- Skills: skill-test-driven-development, skill-systematic-debugging, skill-testing-patterns
- Commands: command-generate-test-cases, command-create-database-migrations
- Integrations: integration-mysql (old DB), integration-postgresql (new DB) for parallel testing
- Agents: agent-test-generator (create parity tests), agent-test-automator (framework setup)
- Output: Modernized system with automated tests proving legacy behavior preservation
```

### Example 3: Setting Up AI Agent with MCP Integrations

**Development Workflow:**

```markdown
Step 1: Define Agent Purpose
- Skills: skill-agent-development, skill-prompt-engineering
- Agents: agent-prompt-engineer

Step 2: Configure MCP Integrations
- Skills: skill-mcp-builder, skill-mcp-integration
- Commands: command-configure-pac-project (if using Product as Code)
- Agents: agent-mcp-developer, agent-mcp-expert
- Integrations needed:
  * integration-github (for repo access)
  * integration-supabase or integration-postgresql (for database)
  * integration-web-reader (for documentation fetching)

Step 3: Build Agent Tools
- Skills: skill-agent-tool-builder, skill-autonomous-agent-patterns
- Agents: agent-mcp-developer (for tool implementation)

Step 4: Test Agent Behavior
- Skills: skill-agent-evaluation, skill-behavioral-modes
- Commands: command-test-automation-orchestrator
- Agents: agent-test-runner, agent-qa-expert

Step 5: Deploy & Monitor
- Commands: command-deployment-monitoring-observability
- Integrations: integration-sentry (error tracking), integration-logfire (OpenTelemetry)
```

---

## 🎯 Project Goals

1. **Reduce AI Hallucination**: Use concrete examples (I/O, diagrams) as ground truth
2. **Maintain Context**: Chain outputs as inputs for consistency
3. **Accelerate Development**: Leverage 600+ templates and skills
4. **Ensure Quality**: Build testing and validation into every step
5. **Enable Knowledge Transfer**: Document everything for team learning

---

## 🤖 Agent Usage Patterns

### Single-Purpose Agents

Use specific agents for focused tasks:

**Testing Workflow:**
- `agent-test-generator` → Analyzes code changes and generates comprehensive test cases by understanding existing test patterns
- `agent-test-runner` → Executes tests, analyzes results, identifies failures, diagnoses root causes, and provides actionable fixes
- `agent-test-automator` → Builds and implements automated test frameworks, creates test scripts, integrates testing into CI/CD pipelines
- `agent-qa-expert` → Develops comprehensive QA strategy addressing test planning, resource allocation, risk assessment across full development lifecycle

**MCP Integration:**
- `agent-mcp-developer` → Builds, debugs, or optimizes Model Context Protocol servers connecting AI systems to external tools and data sources
- `agent-mcp-expert` → Provides MCP configuration guidance, server setup, and integration best practices

**Security:**
- `agent-penetration-tester` → Conducts authorized security penetration tests through active exploitation and validation
- `agent-security-auditor` → Reviews security controls without exploitation, focuses on compliance and policy

### Multi-Agent Patterns

Combine agents for comprehensive analysis:

**Pattern 1: Comprehensive Code Analysis**
```
1. explorer-agent → Map codebase structure
2. security-auditor → Evaluate security posture
3. backend-specialist → Assess API quality
4. frontend-specialist → Review UI/UX patterns
5. test-engineer → Analyze test coverage
6. Synthesize all findings into recommendations
```

**Pattern 2: Feature Development Pipeline**
```
1. feature-design-assistant → Define requirements and design
2. architecture-advisor → Review design decisions
3. senior-fullstack → Implement feature code
4. test-generator → Create comprehensive test suite (parallel)
5. test-runner → Execute and validate tests
6. code-reviewer → Final quality check
```

**Pattern 3: Legacy Migration**
```
1. production-code-audit → Analyze legacy codebase
2. api-designer → Design modern API contracts
3. database-specialist → Plan schema migration
4. mcp-developer → Build integration tools
5. test-automator → Create parity tests
```

---

## 📚 Related Documentation

- [New App Flow](new-app-flow.md) - Detailed new application development process
- [Migration Flow](migration-flow.md) - Legacy system modernization process
- [Converted Templates](converted-templates/) - Browse all available templates
- [Metadata](converted-templates/metadata/) - Structured template information

---

## 🤝 Contributing

To add new skills or improve existing ones:

1. Follow the skill template format
2. Include metadata (keywords, complexity, capabilities)
3. Provide clear usage examples
4. Update metadata files for discoverability

---

_Last Updated: February 14, 2026_
_Project: AI-SDLC Framework_
_Version: 1.0.0_
