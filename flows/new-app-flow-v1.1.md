# New Application Development Flow

## 🔄 AI-Assisted SDLC: Chain of Context

### Core Principle

**"Output of Step n = Input of Step n+1"** while maintaining Project Context (Step 1) as foundation throughout all steps.

This approach ensures AI maintains "memory" across the development lifecycle, preventing contradictions and ensuring consistency.

---

## Executive Summary

| Attribute | Description |
|-----------|-------------|
| **Document Version** | 1.1 |
| **Last Updated** | February 17, 2026 |
| **Process Owner** | Product Development Team |
| **Target Audience** | Development Teams, Project Managers, Business Stakeholders |
| **Process Scope** | End-to-end application development lifecycle |

---

## Success Metrics & KPIs

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| Requirements Traceability | 100% | All requirements linked to test cases |
| Phase Gate Approval Rate | ≥95% | Stakeholder sign-off per phase |
| Defect Escape Rate | <5% | Bugs found post-UAT vs total bugs |
| On-Time Delivery | ≥90% | Sprint completion rate |
| Documentation Coverage | 100% | All artifacts produced per phase |

---

## Stakeholder RACI Matrix

| Activity | Product Owner | Tech Lead | Dev Team | QA | BA |
|----------|--------------|-----------|----------|----|----|
| Project Initiation | A | C | I | I | R |
| Requirements Analysis | A | C | I | C | R |
| Architecture Design | C | A | R | I | C |
| POC Validation | I | A | R | C | I |
| Planning & Breakdown | A | R | C | C | C |
| Implementation | I | A | R | C | I |
| Integration & UAT | A | C | I | R | C |

**Legend:** R=Responsible, A=Accountable, C=Consulted, I=Informed

---

## Development Steps

### Step 1: Project Initiation & Context Building

**Purpose:** Create the master reference document for the entire project.

**Phase Gate Criteria:**
- [ ] Business objectives documented and approved
- [ ] Stakeholder requirements captured
- [ ] Constraints identified and accepted
- [ ] PKB reviewed and signed off

**Input:**
- Raw ideas and business goals
- Business constraints (budget, timeline, resources)
- Industry standards and regulations
- Stakeholder requirements and expectations

**Key Activities:**
- Define business logic and objectives with measurable outcomes
- Document constraints (technical, regulatory, budgetary)
- Establish coding standards and best practices
- Create architectural foundations
- Conduct initial risk assessment

**Recommended Skills:**
- `skill-brainstorming` - Ideation and requirement gathering
- `skill-software-architecture` - Architectural planning and foundation design

**Output Artifacts:**
| Artifact | Format | Owner |
|----------|--------|-------|
| Project Knowledge Base (PKB) | Markdown/Wiki | Business Analyst |
| Stakeholder Register | RACI Matrix | Project Manager |
| Initial Risk Register | Risk Matrix | Tech Lead |

**Risks & Mitigations:**
| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Unclear requirements | Medium | High | Structured stakeholder interviews |
| Scope creep | High | Medium | Clear scope boundaries in PKB |

---

### Step 2: Requirements Analysis & PRD

**Purpose:** Transform business needs into detailed, traceable product requirements.

**Phase Gate Criteria:**
- [ ] All user stories have acceptance criteria
- [ ] NFRs quantified with measurable thresholds
- [ ] PRD approved by Product Owner
- [ ] Requirements traced to business objectives

**Input:**
- Project Knowledge Base (from Step 1)
- User stories and use cases
- Functional requirements
- Non-functional requirements

**Key Activities:**
- Analyze use cases and user journeys
- Define functional requirements with acceptance criteria
- Specify NFRs (performance: <200ms response, 99.9% uptime, etc.)
- Create comprehensive PRD with user research
- Establish requirements traceability matrix

**Recommended Skills:**
- `skill-feature-design-assistant` - Requirements analysis and feature planning
- `skill-product-manager-toolkit` - PRD creation and product strategy

**Output Artifacts:**
| Artifact | Format | Owner |
|----------|--------|-------|
| Product Requirements Document (PRD) | Markdown | Product Manager |
| Use Case Specifications | UML/Markdown | Business Analyst |
| Requirements Traceability Matrix | Spreadsheet | Business Analyst |

**Risks & Mitigations:**
| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Missing requirements | Medium | High | Multiple elicitation techniques |
| Conflicting stakeholder needs | Medium | Medium | Prioritization workshops |

---

### Step 3: Architecture & Tech Stack Design

**Purpose:** Design system architecture and select appropriate technologies aligned with requirements.

**Phase Gate Criteria:**
- [ ] Architecture addresses all NFRs
- [ ] Tech stack approved by Tech Lead
- [ ] All diagrams reviewed and validated
- [ ] Security architecture documented

**Input:**
- Product Requirements Document (from Step 2)
- Project Knowledge Base (from Step 1) for constraints
- Technology landscape assessment
- Security requirements

**Key Activities:**
- Design system architecture (microservices, monolith, serverless)
- Select tech stack based on requirements and team capability
- Design database schema and data models
- Create architecture diagrams (C4 model, sequence, ER diagrams)
- Document API contracts and integration points

**Recommended Skills:**
- `skill-software-architecture` - System design and architectural patterns
- `skill-database-design` - Schema design and data modeling

**Output Artifacts:**
| Artifact | Format | Owner |
|----------|--------|-------|
| System Design Document (SDD) | Markdown | Tech Lead |
| Architecture Diagrams | Mermaid/Draw.io | Tech Lead |
| Database Schema | ERD | Database Architect |
| API Specifications | OpenAPI/Swagger | Tech Lead |

**Risks & Mitigations:**
| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Over-engineering | Medium | Medium | Start simple, iterate based on needs |
| Technology mismatch | Low | High | POC validation in Step 4 |

---

### Step 4: POC & Validation

**Purpose:** Validate architecture decisions and de-risk critical components.

**Phase Gate Criteria:**
- [ ] Critical components validated
- [ ] Performance benchmarks met
- [ ] Go/No-Go decision documented
- [ ] Technical debt identified and accepted

**Input:**
- System Design Document (from Step 3)
- Riskiest/most critical components identified
- Performance requirements from PRD

**Key Activities:**
- Build proof-of-concept for critical/risky components
- Validate tech stack can handle expected load (load testing)
- Performance testing and benchmarking against NFRs
- Identify potential bottlenecks and technical debt
- Document lessons learned and architecture refinements

**Recommended Skills:**
- `skill-executing-plans` - POC implementation and execution
- `skill-performance-profiling` - Performance validation and optimization

**Output Artifacts:**
| Artifact | Format | Owner |
|----------|--------|-------|
| POC Code | Repository | Tech Lead |
| Validation Report | Markdown | Tech Lead |
| Go/No-Go Decision | Sign-off Document | Product Owner |

**Risks & Mitigations:**
| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| POC scope creep | High | Medium | Time-boxed validation sprints |
| False positive results | Medium | High | Realistic test data and scenarios |

---

### Step 5: Planning & Task Breakdown

**Purpose:** Break down work into manageable, prioritized tasks with clear estimates.

**Phase Gate Criteria:**
- [ ] All epics broken into user stories
- [ ] Story points estimated
- [ ] Sprint capacity planned
- [ ] Dependencies mapped

**Input:**
- Product Requirements Document (from Step 2)
- System Design Document (from Step 3)
- POC Validation Results (from Step 4)

**Key Activities:**
- Break epics into user stories with acceptance criteria
- Create Work Breakdown Structure (WBS)
- Estimate task complexity and effort (story points)
- Prioritize backlog items using MoSCoW or WSJF
- Identify and document dependencies

**Recommended Skills:**
- `skill-task-execution-engine` - Task decomposition and workflow planning
- `skill-executing-plans` - Sprint planning and execution strategy

**Output Artifacts:**
| Artifact | Format | Owner |
|----------|--------|-------|
| Project Backlog | Jira/GitHub Issues | Product Owner |
| Sprint Plans | Markdown | Scrum Master |
| Dependency Map | Diagram | Tech Lead |

**Risks & Mitigations:**
| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Underestimation | High | Medium | Include buffer, use historical data |
| Missing dependencies | Medium | High | Cross-team dependency reviews |

---

### Step 6: Implementation & Unit Testing

**Purpose:** Implement features with comprehensive testing following TDD practices.

**Phase Gate Criteria:**
- [ ] Code coverage ≥80%
- [ ] All unit tests passing
- [ ] Code review completed
- [ ] Documentation updated

**Input:**
- Prioritized backlog tasks (from Step 5)
- Product Requirements Document (from Step 2)
- Coding standards (from PKB Step 1)

**Key Activities:**
- Implement features following design patterns
- Write unit tests alongside code (TDD)
- Conduct code reviews and quality checks
- Update technical documentation
- Maintain consistent commit practices

**Recommended Skills:**
- `skill-clean-code` - Implementation following best practices
- `skill-tdd-workflow` - Test-driven development approach

**Output Artifacts:**
| Artifact | Format | Owner |
|----------|--------|-------|
| Feature Code | Repository | Dev Team |
| Unit Tests | Test Suite | Dev Team |
| Test Coverage Report | HTML/Markdown | Dev Team |
| Code Review Records | PR Comments | Tech Lead |

**Risks & Mitigations:**
| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Technical debt accumulation | Medium | High | Regular refactoring sprints |
| Integration issues | Medium | Medium | Continuous integration pipeline |

---

### Step 7: Integration Testing & UAT

**Purpose:** Validate complete system through comprehensive end-to-end testing.

**Phase Gate Criteria:**
- [ ] All E2E tests passing
- [ ] UAT sign-off obtained
- [ ] Performance tests passed
- [ ] Security scan completed

**Input:**
- Feature code (from Step 6)
- Product Requirements Document (from Step 2)
- Use cases for validation

**Key Activities:**
- End-to-end testing across all features
- Integration testing between components
- User acceptance testing (UAT) with stakeholders
- Performance and security testing
- Regression testing

**Recommended Skills:**
- `skill-playwright` - E2E testing automation
- `skill-webapp-testing` - Comprehensive web application testing

**Output Artifacts:**
| Artifact | Format | Owner |
|----------|--------|-------|
| E2E Test Suite | Test Repository | QA Team |
| UAT Sign-off | Document | Product Owner |
| Release Candidate | Deployable Package | DevOps |
| Test Summary Report | Markdown | QA Team |

**Risks & Mitigations:**
| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| UAT delays | Medium | High | Early stakeholder involvement |
| Environment issues | Medium | Medium | Production-like staging environment |

---

## Data Flow Summary

| Step | Output | Used By (Next Steps) | Owner |
|------|--------|---------------------|-------|
| **1. Project Initiation** | Project Knowledge Base (PKB) | All subsequent steps | BA |
| **2. Requirements & PRD** | Product Requirements Document | Steps 3, 5, 7 | PM |
| **3. Architecture Design** | System Design Document (SDD) | Steps 4, 5, 6 | Tech Lead |
| **4. POC & Validation** | Validation Results | Step 5 | Tech Lead |
| **5. Planning & Breakdown** | Project Backlog | Step 6 | PO |
| **6. Implementation** | Feature Code + Tests | Step 7 | Dev Team |
| **7. Integration & UAT** | Tested Product | Production | QA Team |

---

## Key Benefits

1. **Consistency:** Each step builds on verified outputs from previous steps
2. **Traceability:** Clear lineage from requirements to implementation with RTM
3. **Quality:** Testing integrated at every level with measurable coverage
4. **Context Preservation:** AI maintains understanding across all phases
5. **Reduced Hallucination:** Concrete artifacts serve as ground truth
6. **Accountability:** Clear RACI ownership for each phase and artifact
7. **Risk Management:** Proactive risk identification and mitigation per phase
8. **Measurable Outcomes:** KPIs defined for process success tracking

---

## Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | Feb 14, 2026 | Original | Initial document |
| 1.1 | Feb 17, 2026 | BA Review | Added: Executive Summary, Success Metrics & KPIs, RACI Matrix, Phase Gate Criteria, Output Artifacts tables, Risk & Mitigation tables, Change Log. Enhanced: Stakeholder ownership, measurable acceptance criteria, artifact formats |

---

_Last Updated: February 17, 2026_

