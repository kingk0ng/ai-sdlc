Usage notes:

Prompt:
Use skill .github/skills-templates/skills/development/skill-brainstorming.md
analyze docs/tenant_management.md and produce a PRDs.

Feedback:
many confirmation questions to be answered.

Prompt: 
Use .github/skills-templates/skills/development/skill-software-architecture.md analyze docs/plans/2026-02-14-tenant-management-prd.md and correct design.

Feedback: 
Good enough



Use .github/skills-templates/agents/ai-specialists/agent-task-decomposition-expert.md, create tasks breakdown file from: 
docs/plans/2026-02-14-tenant-management-prd.md
and docs/plans/2026-02-14-tenant-management-prd-DESIGN-CORRECTIONS.md.

Feedback: 
Good enough


Use .github/skills-templates/skills/development/skill-clean-code.md
Implement Phase4 of the feature: docs/implementation-tasks/2026-02-14-tenant-management-dashboard.md
Feedback: 
Good enough
Not mark checkbox when completed tasks


Test Phase4 with: .github/skills-templates/skills/development/skill-playwright.md
Test Phase1 to 4 with: .github/skills-templates/skills/development/skill-playwright.md
I perform manual tests and found many features notworking. Create Cypress UI testing and test them.


Use .github/agents/devops-infrastructure/agent-deployment-engineer.md
Review and deploy the updates.
Feedback: 
Good enough


The RAG search found several relevant results. The top matches for review deployment are:

Rank	File	Score	Type
1	skill-deployment-procedures.md	0.99	Skill
2	agent-deployment-engineer.md	0.82	Agent
3	agent-code-reviewer.md	0.87	Agent
4	command-pr-review.md	0.83	Command
5	command-deployment-monitoring-observability.md	0.88	Command
Best matches for your use case:

skill-deployment-procedures — Pre-deployment checklist (tests passing, code reviewed, production build, env vars, migrations, rollback plan, monitoring).
agent-deployment-engineer — Senior deployment engineer agent for CI/CD pipelines, deployment automation, release orchestration, zero-downtime deployments, and automated rollbacks.
command-pr-review (Task 5: DevOps Review) — Evaluates build/deploy/monitoring integration for PRs, validates CI/CD pipeline compatibility, and checks infrastructure needs.
For a review before deploying your app, I'd recommend combining:

agent-deployment-engineer — to orchestrate and validate the deployment itself
skill-deployment-procedures — as the checklist/procedure to follow
command-pr-review — if you're reviewing a PR before merging and deploying