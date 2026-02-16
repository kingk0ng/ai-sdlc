# New Application Development Flow

## 🔄 AI-Assisted SDLC: Chain of Context

### Core Principle

**"Output of Step n = Input of Step n+1"** while maintaining Project Context (Step 1) as foundation throughout all steps.

This approach ensures AI maintains "memory" across the development lifecycle, preventing contradictions and ensuring consistency.

---

## Development Steps

### Step 1: Project Initiation & Context Building

**Purpose:** Create the master reference document for the entire project.

**Input:**
- Raw ideas and business goals
- Business constraints
- Industry standards and regulations
- Stakeholder requirements

**Key Activities:**
- Define business logic and objectives
- Document constraints (technical, regulatory, budgetary)
- Establish coding standards and best practices
- Create architectural foundations

**Recommended Skills:**
- `skill-brainstorming` - Ideation and requirement gathering
- `skill-software-architecture` - Architectural planning and foundation design

**Output:** 📄 **Project Knowledge Base (PKB)**

---

### Step 2: Requirements Analysis & PRD

**Purpose:** Transform business needs into detailed product requirements.

**Input:**
- Project Knowledge Base (from Step 1)
- User stories and use cases
- Functional requirements
- Non-functional requirements

**Key Activities:**
- Analyze use cases and user journeys
- Define functional requirements
- Specify non-functional requirements (performance, security, scalability)
- Create comprehensive PRD with user research

**Recommended Skills:**
- `skill-feature-design-assistant` - Requirements analysis and feature planning
- `skill-product-manager-toolkit` - PRD creation and product strategy

**Output:** 📄 **Product Requirements Document (PRD)** + **Use Cases**

---

### Step 3: Architecture & Tech Stack Design

**Purpose:** Design system architecture and select appropriate technologies.

**Input:**
- Product Requirements Document (from Step 2)
- Project Knowledge Base (from Step 1) for constraints
- Technology landscape assessment

**Key Activities:**
- Design system architecture (microservices, monolith, serverless)
- Select tech stack based on requirements
- Design database schema and data models
- Create architecture diagrams (component, sequence, ER diagrams)

**Recommended Skills:**
- `skill-software-architecture` - System design and architectural patterns
- `skill-database-design` - Schema design and data modeling

**Output:** 📄 **System Design Document (SDD)** + **Tech Stack** + **Diagrams**

---

### Step 4: POC & Validation

**Purpose:** Validate architecture decisions through proof-of-concept implementation.

**Input:**
- System Design Document (from Step 3)
- Riskiest/most critical components identified

**Key Activities:**
- Build proof-of-concept for critical components
- Validate tech stack can handle expected load
- Performance testing and benchmarking
- Identify potential bottlenecks

**Recommended Skills:**
- `skill-executing-plans` - POC implementation and execution
- `skill-performance-profiling` - Performance validation and optimization

**Output:** 💻 **POC Code** + 📊 **Validation Results**

---

### Step 5: Planning & Task Breakdown

**Purpose:** Break down work into manageable, prioritized tasks.

**Input:**
- Product Requirements Document (from Step 2)
- System Design Document (from Step 3)
- POC Validation Results (from Step 4)

**Key Activities:**
- Break epics into user stories
- Create Work Breakdown Structure (WBS)
- Estimate task complexity and effort
- Prioritize backlog items

**Recommended Skills:**
- `agent-task-decomposition-expert` - Task decomposition and workflow planning
- `skill-executing-plans` - Sprint planning and execution strategy

**Output:** 📋 **Project Backlog** + **Sprint Plans**

---

### Step 6: Implementation & Unit Testing

**Purpose:** Implement features with comprehensive testing.

**Input:**
- Prioritized backlog tasks (from Step 5)
- Product Requirements Document (from Step 2)
- Coding standards (from PKB Step 1)

**Key Activities:**
- Implement features following design patterns
- Write unit tests alongside code
- Follow TDD workflow
- Code reviews and quality checks

**Recommended Skills:**
- `skill-clean-code` - Implementation following best practices
- `skill-tdd-workflow` - Test-driven development approach

**Output:** 📦 **Feature Code** + **Unit Tests** + **Test Reports**

---

### Step 7: Integration Testing & UAT

**Purpose:** Validate complete system through end-to-end testing.

**Input:**
- Feature code (from Step 6)
- Product Requirements Document (from Step 2)
- Use cases for validation

**Key Activities:**
- End-to-end testing across all features
- Integration testing between components
- User acceptance testing (UAT)
- Performance and security testing

**Recommended Skills:**
- `skill-playwright` - E2E testing automation
- `skill-webapp-testing` - Comprehensive web application testing

**Output:** ✅ **Tested Product** + **UAT Documentation** + **Release Candidate**

---

## Data Flow Summary

| Step | Output | Used By (Next Steps) |
|------|--------|---------------------|
| **1. Project Initiation** | Project Knowledge Base (PKB) | All subsequent steps (foundation) |
| **2. Requirements & PRD** | Product Requirements Document | Steps 3 (design), 5 (planning), 7 (UAT) |
| **3. Architecture Design** | System Design Document (SDD) | Steps 4 (POC), 5 (breakdown), 6 (implementation) |
| **4. POC & Validation** | Validation Results | Step 5 (confirms feasibility) |
| **5. Planning & Breakdown** | Project Backlog | Step 6 (implementation tasks) |
| **6. Implementation** | Feature Code + Tests | Step 7 (integration testing) |
| **7. Integration & UAT** | Tested Product | Production deployment |

---

## Key Benefits

1. **Consistency:** Each step builds on verified outputs from previous steps
2. **Traceability:** Clear lineage from requirements to implementation
3. **Quality:** Testing integrated at every level
4. **Context Preservation:** AI maintains understanding across all phases
5. **Reduced Hallucination:** Concrete artifacts serve as ground truth

---

_Last Updated: February 14, 2026_
