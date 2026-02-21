# AI-Assisted SDLC Flows

This directory contains detailed workflow documentation for AI-assisted software development.

## Available Flows

### 1. [New Application Development Flow](new-app-flow.md)

**Use When:**
- Building applications from scratch
- Starting greenfield projects
- No existing codebase to migrate

**Approach:** Chain of Context (Output of Step n = Input of Step n+1)

**Steps:**
1. Project Initiation & Context Building
2. Requirements Analysis & PRD
3. Architecture & Tech Stack Design
4. POC & Validation
5. Planning & Task Breakdown
6. Implementation & Unit Testing
7. Integration Testing & UAT

---

### 2. [Legacy System Migration Flow](migration-flow.md)

**Use When:**
- Modernizing existing legacy systems
- Missing or outdated documentation
- Need to preserve business logic

**Approach:** Code-to-Requirement (Reverse Engineering)

**Steps:**
1. Code Discovery & Mapping
2. Business Logic Extraction
3. Gap Analysis & Modernized PRD
4. Modern Architecture Design
5. Implementation with Parity Testing

---

### 3. [Additional Requirements Flow](additional-requirements-flow-v1.1A.md)

**Use When:**
- Adding new features to existing applications
- Enhancing functionality of a running system
- Evolving requirements for mature products
- Need to ensure backward compatibility

**Approach:** Analyze Before You Act (Impact Analysis First)

**Steps:**
1. Requirements Intake & Clarification
2. Impact Analysis (Codebase, Dependencies, Risks)
3. Task Breakdown & Planning
4. Design Updates
5. Implementation & Testing (with Regression Focus)

---

## Flow Selection Guide

| Scenario | Recommended Flow | Key Consideration |
|----------|------------------|-------------------|
| New product idea | New App Flow | Start with requirements |
| Legacy PHP → Node.js | Migration Flow | Extract business rules first |
| Monolith → Microservices | Migration Flow | Map existing components |
| Startup MVP | New App Flow | Iterate quickly with POC |
| Compliance-driven rewrite | Migration Flow | Ensure behavior parity |
| New SaaS product | New App Flow | Design-first approach |
| Modernize mainframe | Migration Flow | Document implicit logic |
| Add feature to existing app | Additional Requirements Flow | Impact analysis first |
| Enhance running system | Additional Requirements Flow | Preserve stability |
| Evolving product requirements | Additional Requirements Flow | Regression testing focus |

---

## Skill Recommendations

Both flows use specific skills from the `converted-templates/skills/` directory. Each step lists max 2 recommended skills for focused expertise.

### Skills Coverage

**Development:**
- Architecture & Design
- Implementation & Testing
- Planning & Execution

**Quality:**
- Code Review
- Testing Patterns
- Performance Profiling

**Strategy:**
- Requirements Analysis
- Gap Analysis
- Technical Decision Making

---

## Best Practices

### For New Applications
1. **Never skip Step 1** - PKB is foundation for all subsequent steps
2. **Validate early** - POC catches architecture issues before implementation
3. **Maintain traceability** - Link code back to requirements
4. **Test continuously** - Unit tests in Step 6, integration in Step 7

### For Legacy Migration
1. **Use diagrams** - Process flows provide critical context
2. **Validate with I/O** - Real examples prevent hallucination
3. **Module-by-module** - Don't process entire monolith at once
4. **Parity testing** - Prove new system matches old behavior
5. **Document decisions** - Record why bugs were preserved or fixed

### For Additional Requirements
1. **Impact analysis first** - Understand all affected components before coding
2. **Map dependencies** - Trace direct and indirect impacts
3. **Break down tasks** - Create discrete, estimable work items
4. **Regression testing** - Ensure existing functionality preserved
5. **Update design docs** - Keep SDD and diagrams current

---

## Related Resources

- [Project Context](../PROJECT_CONTEXT.md) - Overview of AI-SDLC framework
- [Converted Templates](../converted-templates/) - Skills, agents, commands, integrations
- [Metadata](../converted-templates/metadata/) - Template discovery and search

---

_Last Updated: February 19, 2026_
