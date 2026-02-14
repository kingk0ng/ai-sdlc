# Legacy System Migration Flow

## 🔄 Legacy-Driven AI-Assisted SDLC

### Core Principle

**"Code-to-Requirement"** - Extract business logic from existing code before modernization.

This reverse engineering approach transforms legacy systems into modern applications while preserving critical business logic.

---

## Migration Steps

### Step 1: Code Discovery & Mapping

**Purpose:** Analyze legacy system structure and create comprehensive system map.

**Input:**
- Legacy source code (all modules)
- Folder and file structure
- Database schema (existing)
- Process flow diagrams (if available)
- System documentation (if available)

**Key Activities:**
- Map project structure and dependencies
- Identify entry points (API endpoints, UI routes, batch jobs)
- Catalog technologies and frameworks used
- Document data flow between components
- Create component catalog

**Recommended Skills:**
- `skill-code-reviewer` - Code analysis and structure understanding
- `skill-production-code-audit` - System-wide code quality assessment

**Output:** 📄 **System Map** + **Component Catalog**

---

### Step 2: Business Logic Extraction

**Purpose:** Extract business rules from code into human-readable documentation.

**Input:**
- System Map (from Step 1)
- Source code per module
- Input/Output examples (if available)
- Business process flows

**Key Activities:**
- Convert code logic to plain language business rules
- Document validation rules and constraints
- Identify data transformations
- Map business workflows
- Validate extracted logic against I/O examples

**Recommended Skills:**
- `skill-api-documentation-generator` - Document existing APIs and logic
- `skill-database-schema-designer` - Understand data models and relationships

**Output:** 📄 **Extracted Business Rules (EBR)**

---

### Step 3: Gap Analysis & Modernized PRD

**Purpose:** Define target requirements bridging legacy to modern system.

**Input:**
- Extracted Business Rules (from Step 2)
- New business requirements
- Pain points from legacy system
- Modern technology capabilities

**Key Activities:**
- Identify logic to preserve (As-is)
- Define improvements and new features (To-be)
- Document breaking changes
- Prioritize modernization opportunities
- Create comprehensive PRD for new system

**Recommended Skills:**
- `skill-senior-architect` - Strategic technical decisions
- `skill-feature-design-assistant` - Requirements analysis and planning

**Output:** 📄 **Modernized PRD** (As-is + To-be sections)

---

### Step 4: Modern Architecture Design

**Purpose:** Design modern system architecture and data migration strategy.

**Input:**
- Modernized PRD (from Step 3)
- Legacy database schema
- System constraints and requirements
- Technology landscape assessment

**Key Activities:**
- Design modern architecture (microservices, cloud-native, etc.)
- Select modern tech stack
- Design new database schema
- Plan data migration strategy
- Create migration scripts and ETL processes
- Design API modernization (REST/GraphQL)

**Recommended Skills:**
- `skill-software-architecture` - Modern architecture patterns
- `skill-api-patterns` - API design decisions (REST vs GraphQL vs tRPC)

**Output:** 📄 **New System Design (SDD)** + **Migration Plan** + **Migration Scripts**

---

### Step 5: Implementation with Parity Testing

**Purpose:** Implement modernized system with tests ensuring legacy behavior preservation.

**Input:**
- New System Design (from Step 4)
- Extracted Business Rules (from Step 2)
- Legacy system I/O examples
- Migration scripts

**Key Activities:**
- Implement features in modern tech stack
- Create parity tests (new system = old system results)
- Validate business logic preservation
- Systematic debugging and issue resolution
- Progressive migration and validation

**Recommended Skills:**
- `skill-clean-code` - Implementation following best practices
- `skill-testing-patterns` - Comprehensive test strategy including parity tests

**Output:** 📦 **Modernized System** + **Parity Test Suite** + **Migration Validation**

---

## Data Flow Summary

| Step | Input | Output | AI Role |
|------|-------|--------|---------|
| **1. Discovery** | Legacy Source Code + Structure | System Map & Component Catalog | Analyze code structure, identify entry points, map technologies |
| **2. Extraction** | System Map + Module Code | Extracted Business Rules (EBR) | Convert code to human-readable business logic |
| **3. Gap Analysis** | EBR + New Requirements | Modernized PRD | Create target requirements (as-is vs to-be) |
| **4. Architecture** | Modernized PRD + Old Schema | New System Design + Migration Plan | Design modern architecture and data migration |
| **5. Implementation** | New Design + Old System | Modernized System + Parity Tests | Implement with tests ensuring consistency |

---

## Critical Enhancements

### Using Process Flow Diagrams

**When to Use:** Step 1 (Code Discovery)

**Purpose:** Provide "map" for AI to understand system structure

**Benefits:**
- Accurate module grouping by business function
- Better understanding of data flow
- Identifies critical paths and dependencies

**How to Use:**
- Attach flow diagrams with Step 1 prompt
- Ask AI to map code modules to diagram components
- Validate AI's understanding of business processes

---

### Using Input/Output Examples

**When to Use:** Step 2 (Logic Extraction) and Step 5 (Implementation)

**Purpose:** 
- **Step 2:** Validate extracted logic against real data
- **Step 5:** Create automated parity tests

**Benefits:**
- Reduces hallucination
- Ensures accuracy of extracted logic
- Provides ground truth for regression testing
- Validates new system behavior matches old system

**How to Use:**
- **Step 2:** "Use this I/O example to verify your extracted logic is correct"
- **Step 5:** "Create unit tests using these I/O examples as expected behavior"

---

## Critical Considerations

### 1. Code Volume
**Challenge:** Large monolithic codebases cannot be processed all at once

**Solution:** Process module-by-module or domain-by-domain
- Break system into logical modules
- Process each module through Steps 1-2 independently
- Synthesize results in Step 3

---

### 2. Hidden Bugs
**Challenge:** Legacy code may contain bugs users have accepted

**Decision Points:**
- Preserve bug for backward compatibility?
- Fix bug as part of modernization?
- Document as known limitation?

**Recommendation:** Use I/O examples to identify unexpected behaviors, then decide consciously

---

### 3. Testing Strategy
**Challenge:** Ensuring new system doesn't break existing functionality

**Solution:** Comprehensive parity testing
- Use I/O examples as test cases
- Create regression test suite
- Validate business logic preservation
- Progressive rollout with comparison testing

---

## Migration Patterns

### Pattern 1: Strangler Fig
Gradually replace legacy system components while both systems run in parallel.

**Best For:** Large monoliths, mission-critical systems

---

### Pattern 2: Big Bang
Complete rewrite and cutover in single deployment.

**Best For:** Smaller systems, non-critical applications, clean breaks

---

### Pattern 3: Database First
Migrate and modernize database, then applications.

**Best For:** Multiple applications sharing one database

---

## Key Benefits

1. **Logic Preservation:** Business rules extracted and documented
2. **Validation:** Parity tests ensure behavioral consistency
3. **Modernization:** Leverage modern tech stack and patterns
4. **Documentation:** Create documentation that never existed
5. **Quality Improvement:** Fix technical debt while preserving business logic

---

_Last Updated: February 14, 2026_
