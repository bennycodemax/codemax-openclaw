# AI Dev Team — Agent Directory
# This file is read by the CTO agent to understand delegation targets.

## Available Agents

### project-manager
**Role:** Project Manager & Scrum Master
**Trigger with:** sessions_send(agentId="project-manager", message="...")
**Best for:** Sprint planning, task tracking, standup summaries, project docs, coordination between agents

### backend-dev
**Role:** Senior Backend Engineer
**Trigger with:** sessions_send(agentId="backend-dev", message="...")
**Best for:** API design, server-side code, database work, backend PR reviews, performance issues

### frontend-dev
**Role:** Senior Frontend Engineer
**Trigger with:** sessions_send(agentId="frontend-dev", message="...")
**Best for:** React components, UI implementation, accessibility, CSS, client-side performance

### qa-tester
**Role:** QA Engineer & Test Lead
**Trigger with:** sessions_send(agentId="qa-tester", message="...")
**Best for:** Test case creation, bug validation, QA reports, sign-off before release

### devops
**Role:** DevOps & Infrastructure Engineer
**Trigger with:** sessions_send(agentId="devops", message="...")
**Best for:** CI/CD, infrastructure changes, deployments, monitoring, incident response

### tech-support
**Role:** Technical Support Specialist
**Trigger with:** sessions_send(agentId="tech-support", message="...")
**Best for:** User issue investigation, documentation, knowledge base, bug escalation from users

## Handoff Protocol
Always include in sessions_send messages:
- from: (your agent id)
- to: (target agent id)
- task_id: (sprint task reference)
- context: (what's been done, what's needed)
- deliver_to: (where to post the result)
- deadline: (urgency level)
