# Lab 6 & 7 Combined Homework Assignment

**Course:** CS-PD-2025 - Product Development for Software Engineers  
**Due Date:** Midnight, November 27th, 2025 (Thursday)  
**Submission:** Push all deliverables to your team's GitHub repository

---

## 📋 Overview

This combined homework integrates technical architecture planning (Lab 6) with Agile sprint planning (Lab 7) to prepare your team for MVP development. You'll document technical decisions, set up analytics infrastructure, create your development roadmap, and plan your first sprint.

**Total Points:** 100  
**Estimated Time:** 6-8 hours (team work)

---

## 🎯 Learning Objectives

By completing this homework, you will:
- ✅ Document system architecture and technical decisions with clear rationale
- ✅ Identify and plan mitigation strategies for technical risks
- ✅ Define analytics events and metrics to track product success
- ✅ Create an 8-week product roadmap aligned with course milestones
- ✅ Map your team's development workflow and ceremonies
- ✅ Plan your first 2-week sprint with specific, estimable tasks

---

## 📂 Repository Structure

Create the following structure in your team repository:

```
/team-[your-team-name]/
├── /03-build/
│   ├── /architecture/
│   │   ├── system-design.md           
│   │   ├── tech-stack.md              
│   │   ├── architecture-diagram.png  
│   │   └── risk-spikes.md             
│   ├── /analytics/
│   │   ├── event-schema.md           
│   │   ├── metrics-definition.md      
│   │   └── platform-setup.md         
│   ├── /roadmap/
│   │   ├── product-roadmap.md         
│   │   └── sprint-1-plan.md           
│   └── /workflow/
│       └── process-map.md            
```

---

## 📝 Part 1: Technical Architecture (35 points)

### Part 1A: System Design Document (10 points)

**File:** `/03-build/architecture/system-design.md`

Document your high-level system architecture using this template:

```markdown
# System Design Document

**Project:** [Your Project Name]  
**Team:** [Your Team Name]  
**Last Updated:** [Date]

---

## Executive Summary

[2-3 sentences describing the overall architecture approach]

---

## System Overview

### Architecture Pattern
[Describe your architectural pattern: Monolithic, Microservices, Client-Server, etc.]

**Why this pattern?**
- [Reason 1]
- [Reason 2]
- [Reason 3]

### High-Level Components

**Frontend:**
- Platform: [Web, Mobile, Desktop]
- Framework: [React, Vue, Flutter, etc.]
- Hosting: [Vercel, Netlify, etc.]

**Backend:**
- Framework: [Express, Django, Flask, etc.]
- API Style: [REST, GraphQL, etc.]
- Hosting: [AWS, Heroku, Railway, etc.]

**Database:**
- Type: [SQL, NoSQL]
- Technology: [PostgreSQL, MongoDB, Firebase, etc.]
- Hosting: [Managed service or self-hosted]

**Third-Party Services:**
- Authentication: [Service name]
- Payment Processing: [If applicable]
- Email/Notifications: [If applicable]
- Other: [List any other services]

---

## Data Flow

### User Authentication Flow
1. [Step 1]
2. [Step 2]
3. [Step 3]

### Core Feature Flow (Your Main Feature)
1. [Step 1]
2. [Step 2]
3. [Step 3]

[Create a simple diagram or detailed description]

---

## Database Schema

### Key Entities

**User Table:**
- id (primary key)
- [other key fields]

**[Your Core Entity]:**
- id (primary key)
- [relationships]
- [key fields]

**[Additional Tables]:**
- [List key tables and relationships]

---

## Scalability Considerations

### Current Scope (MVP)
- Expected users: [X-Y users]
- Expected traffic: [requests per day/hour]
- Data volume: [estimated]

### Future Scaling Plan
- [How you'll scale if needed]
- [What would change at 1000 users?]
- [What would change at 10,000 users?]

---

## Security Considerations

- [ ] User authentication implemented
- [ ] Data encryption (in transit and at rest)
- [ ] Input validation and sanitization
- [ ] API rate limiting
- [ ] Environment variables for sensitive data
- [ ] [Other security measures]
```

**Grading Criteria:**
- **Completeness (4 pts):** All sections filled with meaningful content
- **Clarity (3 pts):** Architecture clearly explained, understandable to team members
- **Appropriateness (3 pts):** Architecture choices match your project scope and team skills

---

### Part 1B: Tech Stack Decisions (10 points)

**File:** `/03-build/architecture/tech-stack.md`

Document WHY you chose each technology using this template:

```markdown
# Tech Stack Decisions

**Project:** [Your Project Name]  
**Team:** [Your Team Name]  
**Last Updated:** [Date]

---

## Decision Framework

For each technology choice, we considered:
1. **Team expertise:** Do we know this tech, or can we learn it in 2-3 weeks?
2. **Project fit:** Does it match our MVP requirements?
3. **Community & resources:** Is there good documentation and support?
4. **Deployment ease:** Can we deploy and iterate quickly?
5. **Cost:** Is it free/affordable for our MVP?

---

## Frontend Technology

### Choice: [Technology Name]
**Alternatives Considered:** [List 2-3 alternatives]

| Criterion | Score (1-5) | Notes |
|-----------|-------------|-------|
| Team Expertise | [X] | [Brief explanation] |
| Project Fit | [X] | [Brief explanation] |
| Community Support | [X] | [Brief explanation] |
| Deployment Ease | [X] | [Brief explanation] |
| Cost | [X] | [Brief explanation] |
| **TOTAL** | **[X/25]** | |

**Key reasons for choice:**
1. [Reason 1]
2. [Reason 2]
3. [Reason 3]

**Tradeoffs accepted:**
- **Giving up:** [What we lose with this choice]
- **Gaining:** [What we gain with this choice]

---

## Backend Technology

### Choice: [Technology Name]
**Alternatives Considered:** [List 2-3 alternatives]

[Same table and format as Frontend]

---

## Database Technology

### Choice: [Technology Name]
**Alternatives Considered:** [List 2-3 alternatives]

[Same table and format as Frontend]

---

## Deployment & Infrastructure

### Hosting Platform: [Platform Name]
**Why this platform:**
- [Reason 1]
- [Reason 2]

### CI/CD Pipeline
- **Tool:** [GitHub Actions, GitLab CI, etc.]
- **Deployment trigger:** [On merge to main, manual, etc.]

---

## Development Tools

### Version Control
- **Platform:** GitHub
- **Branching strategy:** [Describe your approach]

### Project Management
- **Tool:** [GitHub Projects, Jira, Trello, etc.]
- **Sprint tracking:** [How you'll track tasks]

### Communication
- **Primary:** [Slack, Discord, WhatsApp, etc.]
- **Meetings:** [How often, what format]

---

## Learning Plan

**Technologies we need to learn:**

| Technology | Current Skill Level (1-5) | Learning Resources | Time Needed |
|------------|---------------------------|-------------------|-------------|
| [Tech 1] | [X] | [Links/resources] | [X weeks] |
| [Tech 2] | [X] | [Links/resources] | [X weeks] |

**De-risking strategy:**
- [How you'll minimize learning risk]
- [Backup plans if learning takes too long]
```

**Grading Criteria:**
- **Rationale Quality (4 pts):** Clear reasoning with specific tradeoffs
- **Decision Framework (3 pts):** Systematic evaluation of alternatives
- **Realism (3 pts):** Choices are achievable given team skills and timeline

---

### Part 1C: Architecture Diagram (5 points)

**File:** `/03-build/architecture/architecture-diagram.png`

Create a visual diagram showing your system architecture.

**Requirements:**
- Show all major components (Frontend, Backend, Database, Third-party services)
- Indicate data flow with arrows
- Label key interactions
- Include deployment environment information

**Tools you can use:**
- [Excalidraw](https://excalidraw.com/) (recommended - simple and free)
- [Draw.io](https://app.diagrams.net/)
- [Lucidchart](https://www.lucidchart.com/)
- Figma
- Hand-drawn (photo) - must be clear and legible

**Include a brief README in system-design.md:**
```markdown
## Architecture Diagram

See: [architecture-diagram.png](./architecture-diagram.png)

### Component Descriptions:
- **Frontend:** [Brief description]
- **Backend:** [Brief description]
- **Database:** [Brief description]
- **[Service X]:** [Brief description]
```

**Grading Criteria:**
- **Completeness (2 pts):** All major components shown
- **Clarity (2 pts):** Diagram is readable and well-organized
- **Accuracy (1 pt):** Correctly represents your intended architecture

---

### Part 1D: Risk Spikes (10 points)

**File:** `/03-build/architecture/risk-spikes.md`

Identify technical risks and plan "spike" investigations to mitigate them.

> **What's a Risk Spike?** A time-boxed investigation (4-8 hours) to explore an uncertain technical area and de-risk your project.

```markdown
# Technical Risk Spikes

**Project:** [Your Project Name]  
**Team:** [Your Team Name]  
**Last Updated:** [Date]

---

## Risk Identification

### High-Risk Technical Areas

We've identified the following areas of technical uncertainty:

1. **[Risk Name]** - Severity: [High/Medium/Low]
2. **[Risk Name]** - Severity: [High/Medium/Low]
3. **[Risk Name]** - Severity: [High/Medium/Low]

---

## Spike 1: [Risk Name]

### Risk Description
[What's the technical uncertainty? Why is this risky?]

**Impact if not addressed:**
- [Consequence 1]
- [Consequence 2]

### Spike Investigation Plan

**Time Box:** [4-8 hours]  
**Owner:** [Team member name]  
**Due Date:** [Date - should be within Sprint 1]

**Investigation Questions:**
1. [Question 1]
2. [Question 2]
3. [Question 3]

**Acceptance Criteria (Done when):**
- [ ] [Criterion 1]
- [ ] [Criterion 2]
- [ ] [Criterion 3]

**Resources:**
- [Documentation link]
- [Tutorial link]
- [Example project link]

### Outcome (Fill after spike)

**Findings:**
- [Key finding 1]
- [Key finding 2]

**Decision:**
[What did you decide to do based on the spike?]

**Next Steps:**
- [Action item 1]
- [Action item 2]

---

## Spike 2: [Risk Name]

[Same format as Spike 1]

---

## Spike 3: [Risk Name]

[Same format as Spike 1]

---

## Additional Risks (Lower Priority)

**Risks we're aware of but not spiking yet:**
1. [Risk] - We'll address this in Sprint 2/3 if needed
2. [Risk] - Acceptable risk for MVP

---

## Risk Management Strategy

**How we'll handle new risks:**
1. [Strategy 1]
2. [Strategy 2]

**Weekly risk review:**
- [When and how you'll review risks as a team]
```

**Grading Criteria:**
- **Risk Identification (3 pts):** Identified 3+ genuine technical risks
- **Spike Plans (4 pts):** Clear investigation plans with questions and acceptance criteria
- **Realism (3 pts):** Spikes are scoped appropriately and assigned to team members

---

## 📊 Part 2: Analytics Foundation (25 points)

### Part 2A: Event Schema (10 points)

**File:** `/03-build/analytics/event-schema.md`

Define 6-10 core events you'll track in your MVP.

```markdown
# Analytics Event Schema

**Project:** [Your Project Name]  
**Team:** [Your Team Name]  
**Last Updated:** [Date]

---

## Event Naming Convention

**Format:** `[Object]_[Action]`

**Examples:**
- `user_signed_up`
- `task_created`
- `report_exported`

---

## Core Events

### Event 1: user_signed_up

**Trigger:** When a new user completes registration

**Properties:**
```json
{
  "user_id": "string (UUID)",
  "email": "string",
  "signup_method": "email | google | facebook",
  "referral_source": "string (optional)",
  "timestamp": "ISO 8601 datetime",
  "user_agent": "string"
}
```

**Why we're tracking this:**
[Explanation of what insight this gives you]

**Related to North Star Metric:** [Yes/No - explain]

---

### Event 2: [event_name]

**Trigger:** [When this event fires]

**Properties:**
```json
{
  "[property_1]": "[type] - [description]",
  "[property_2]": "[type] - [description]",
  "timestamp": "ISO 8601 datetime"
}
```

**Why we're tracking this:**
[Explanation]

**Related to North Star Metric:** [Yes/No - explain]

---

[Continue for all 6-10 events]

---

## Event Taxonomy

### User Lifecycle Events
- [ ] User signs up
- [ ] User verifies email (if applicable)
- [ ] User completes onboarding
- [ ] User invites another user (if applicable)

### Core Feature Events
- [ ] [Key action 1]
- [ ] [Key action 2]
- [ ] [Key action 3]

### Engagement Events
- [ ] User logs in
- [ ] User performs [important action]
- [ ] User shares/exports content (if applicable)

---

## Implementation Notes

**Analytics Platform:** [Mixpanel, Amplitude, PostHog, Google Analytics 4, etc.]  
**Implementation Approach:** [Client-side, Server-side, or Hybrid]

**Code Example (Placeholder):**
```javascript
// Example for Task Created event
analytics.track('task_created', {
  task_id: newTask.id,
  priority: newTask.priority,
  assigned_to: newTask.assignedUser,
  due_date: newTask.dueDate,
  timestamp: new Date().toISOString()
});
```

---

## Data Privacy & Compliance

**PII (Personally Identifiable Information) Policy:**
- [ ] Email addresses: [How you'll handle]
- [ ] IP addresses: [How you'll handle]
- [ ] Names: [How you'll handle]

**User consent:**
- [ ] How users will be informed about tracking
- [ ] Opt-out mechanism (if required)
```

**Grading Criteria:**
- **Event Quality (4 pts):** 6-10 well-defined events with clear triggers and properties
- **Relevance (3 pts):** Events align with product's core value proposition
- **Completeness (3 pts):** All events have proper schema and tracking rationale

---

### Part 2B: Metrics Definition (10 points)

**File:** `/03-build/analytics/metrics-definition.md`

Define your North Star Metric and key supporting metrics.

```markdown
# Metrics Definition

**Project:** [Your Project Name]  
**Team:** [Your Team Name]  
**Last Updated:** [Date]

---

## North Star Metric (NSM)

**Our North Star Metric is:**  
**[Metric Name]**

### Definition
[Precisely define how this metric is calculated]

**Formula:**  
`[Metric] = [Calculation]`

**Example:**  
If we have 100 weekly active users and 60 complete [key action] at least once per week, our NSM = 60%.

### Why This Metric?

**Reflects core value:**
- [How this metric shows users getting value from your product]

**Measures success:**
- [How improvement in this metric = product success]

**Influences key decisions:**
- [How this metric will guide your product decisions]

### NSM Targets

**Current (Week 7-8):** [Target value]  
**Sprint 2 (Week 9-10):** [Target value]  
**Sprint 3 (Week 11-12):** [Target value]  
**Sprint 4 (Week 13-14):** [Target value]

---

## Activation Metric

**What counts as an "activated" user?**

[Define the specific action(s) that indicate a user has experienced value]

**Our activation criteria:**
A user is activated when they:
1. [Action 1]
2. [Action 2] (within X days/weeks)

**Why this definition:**
[Explain why this action indicates value]

**Activation Target:**
- Week 7-8: [X%] of new signups activated
- Week 9-10: [X%] of new signups activated

---

## AARRR Metrics Framework

### Acquisition
**How we'll measure it:**  
- Metric: [Signups per week]
- Target (Sprint 1): [X signups]
- Tracking: Event `user_signed_up`

**Acquisition channels:**
- [ ] Direct (URL sharing)
- [ ] Referral (if applicable)
- [ ] [Channel 3]

---

### Activation
**How we'll measure it:**  
- Metric: [% of users who complete key action]
- Target (Sprint 1): [X%]
- Tracking: Event `[your_activation_event]`

---

### Retention
**How we'll measure it:**  
- Metric: [% of users who return in Week 2]
- Target (Sprint 2): [X%]
- Tracking: Compare `user_logged_in` events over time

---

### Referral
**How we'll measure it:**  
- Metric: [If applicable - % of users who share/invite]
- Target: [If applicable]
- Tracking: Event `[referral_event]`

---

### Revenue
**How we'll measure it:**  
- Metric: [If applicable - for free MVPs, note "N/A - Free MVP"]
- Note: [Your monetization hypothesis if applicable]

---

## Supporting Metrics

### Engagement Metrics
| Metric | Definition | Target (Sprint 1) |
|--------|------------|-------------------|
| Daily Active Users (DAU) | Unique users per day | [X users] |
| Weekly Active Users (WAU) | Unique users per week | [X users] |
| Sessions per user | Avg sessions per user per week | [X sessions] |

### Feature-Specific Metrics
| Feature | Metric | Target |
|---------|--------|--------|
| [Feature 1] | [Usage metric] | [X per week] |
| [Feature 2] | [Usage metric] | [X per week] |

---

## Metric Review Cadence

**Sprint Planning (Every 2 weeks):**
- Review all metrics
- Adjust targets based on learnings
- Identify metric-driven experiments

**Weekly Standup (Every Friday):**
- Quick check on NSM
- Note any significant changes
- Flag issues needing attention

---

## Analytics Dashboard Plan

**Dashboard Tool:** [Google Data Studio, Metabase, platform's native dashboard]

**Dashboard Sections:**
1. **Overview**
   - North Star Metric (week over week)
   - Activation rate
   - User growth

2. **User Journey**
   - Funnel: Signup → Activation → Retention
   - Drop-off points

3. **Feature Usage**
   - [Feature 1 usage]
   - [Feature 2 usage]

**Dashboard URL:** [Add after setup]
```

**Grading Criteria:**
- **NSM Quality (4 pts):** Well-chosen North Star Metric with clear rationale
- **AARRR Framework (3 pts):** All relevant AARRR metrics defined
- **Targets (3 pts):** Realistic targets set for each sprint

---

### Part 2C: Platform Setup Documentation (5 points)

**File:** `/03-build/analytics/platform-setup.md`

Document your analytics platform setup.

```markdown
# Analytics Platform Setup

**Project:** [Your Project Name]  
**Platform:** [Mixpanel, Amplitude, PostHog, GA4, etc.]  
**Setup Date:** [Date]

---

## Platform Selection

**Chosen Platform:** [Platform Name]

**Why we chose this:**
1. [Reason 1]
2. [Reason 2]
3. [Reason 3]

**Free tier limits:**
- [Limit 1]
- [Limit 2]
- Sufficient for our MVP: [Yes/No - explain]

---

## Account Setup

**Team Account Details:**
- [ ] Account created
- [ ] All team members invited
- [ ] Project created: [Project name]
- [ ] Environment: [Production, Development, or both]

**Access:**
- Account owner: [Name]
- Admin access: [Names]
- Viewer access: [Names if different]

---

## Integration Plan

### SDK/Library Installation

**For [Frontend/Backend]:**
```bash
# Installation command
npm install [package-name]
```

**Configuration:**
```javascript
// Example initialization code
import analytics from '[package]';

analytics.init('[YOUR-API-KEY]', {
  // config options
});
```

### Event Implementation Timeline

**Sprint 1 (Week 7-8):**
- [ ] Platform SDK integrated
- [ ] Core 6 events implemented
- [ ] Testing and validation complete

**Sprint 2 (Week 9-10):**
- [ ] Additional events added
- [ ] Dashboard configured
- [ ] Team trained on dashboard use

---

## Testing & Validation

**How we'll verify events are working:**
1. [Test method 1 - e.g., use platform's debugger]
2. [Test method 2 - e.g., trigger events in dev environment]
3. [Test method 3 - e.g., check real-time dashboard]

**Validation Checklist:**
- [ ] Events fire on correct triggers
- [ ] Properties captured correctly
- [ ] User identification working
- [ ] No PII leaked inappropriately

---

## Documentation for Team

**Where to find analytics:**
- Dashboard URL: [URL after setup]
- Login credentials: [How team accesses - use password manager]

**How to track new events:**
```javascript
// Template for adding new events
analytics.track('[event_name]', {
  // properties object
});
```

**Resources:**
- Platform docs: [Link]
- Our event schema: [Link to event-schema.md]
```

**Grading Criteria:**
- **Setup Complete (2 pts):** Platform account created and configured
- **Integration Plan (2 pts):** Clear implementation plan with timeline
- **Documentation (1 pt):** Team can use the platform based on docs

---

## 🚀 Part 3: Agile Sprint Planning (40 points)

### Part 3A: Product Roadmap (15 points)

**File:** `/03-build/roadmap/product-roadmap.md`

Create an 8-week product roadmap breaking your capstone into 4 two-week sprints.

```markdown
# Product Roadmap (8-Week MVP)

**Project:** [Your Project Name]  
**Team:** [Your Team Name]  
**Timeline:** Week 7-14 (November - December 2025)  
**Last Updated:** [Date]

---

## Vision & Goals

### Product Vision
[One paragraph: What are you building and why?]

### Success Criteria (End of Week 14)
1. [Measurable criterion 1]
2. [Measurable criterion 2]
3. [Measurable criterion 3]

---

## Sprint Overview

| Sprint | Weeks | Theme | Key Deliverable |
|--------|-------|-------|-----------------|
| Sprint 1 | 7-8 | [Theme] | [Deliverable] |
| Sprint 2 | 9-10 | [Theme] | [Deliverable] |
| Sprint 3 | 11-12 | [Theme] | [Deliverable] |
| Sprint 4 | 13-14 | [Theme] | [Deliverable] |

---

## Sprint 1: [Sprint Theme]
**Dates:** Week 7-8 (Nov 6-21, 2025)  
**Goal:** [One sentence sprint goal]

### What We'll Build
1. **[Feature 1]**
   - User Story: As a [user], I want [feature] so that [benefit]
   - Acceptance Criteria:
     - [ ] [Criterion 1]
     - [ ] [Criterion 2]

2. **[Feature 2]**
   - User Story: As a [user], I want [feature] so that [benefit]
   - Acceptance Criteria:
     - [ ] [Criterion 1]
     - [ ] [Criterion 2]

3. **[Feature 3]**
   - User Story: As a [user], I want [feature] so that [benefit]
   - Acceptance Criteria:
     - [ ] [Criterion 1]
     - [ ] [Criterion 2]

### Technical Work
- [ ] [Technical task 1 - e.g., set up database]
- [ ] [Technical task 2 - e.g., implement authentication]
- [ ] [Technical task 3 - e.g., deploy to staging]

### Success Metrics
- [Metric 1]: Target [X]
- [Metric 2]: Target [X]

### Dependencies & Risks
- **Dependencies:** [What we need from others or external factors]
- **Risks:** [What could prevent sprint success]

---

## Sprint 2: [Sprint Theme]
**Dates:** Week 9-10 (Nov 22 - Dec 5, 2025)  
**Goal:** [One sentence sprint goal]

[Same format as Sprint 1]

---

## Sprint 3: [Sprint Theme]
**Dates:** Week 11-12 (Dec 6-19, 2025)  
**Goal:** [One sentence sprint goal]

[Same format as Sprint 1]

---

## Sprint 4: [Sprint Theme]
**Dates:** Week 13-14 (Dec 20, 2025 - Jan 2, 2026)  
**Goal:** [One sentence sprint goal]

[Same format as Sprint 1]

---

## Feature Prioritization

### MoSCoW Method

**Must Have (Sprint 1-2):**
- [Feature/Capability 1]
- [Feature/Capability 2]
- [Feature/Capability 3]

**Should Have (Sprint 2-3):**
- [Feature/Capability 1]
- [Feature/Capability 2]

**Could Have (Sprint 3-4):**
- [Feature/Capability 1]
- [Feature/Capability 2]

**Won't Have (Out of scope for MVP):**
- [Feature 1 - explain why not]
- [Feature 2 - explain why not]

---

## Roadmap Assumptions

**Assumptions we're making:**
1. [Assumption 1 - e.g., "We can deploy to production by Week 8"]
2. [Assumption 2 - e.g., "Each team member commits 10-12 hours/week"]
3. [Assumption 3 - e.g., "No major technical blockers"]

**If these assumptions are wrong:**
- [Mitigation plan]

---

## Alignment with Course Milestones

| Week | Course Milestone | Our Deliverable |
|------|------------------|-----------------|
| Week 9 | Midterm Exam | [How we'll balance] |
| Week 11 | [Course requirement] | [Our plan] |
| Week 14 | Final Demo Day | [Final MVP state] |

---

## Progress Tracking

**How we'll track progress:**
- [Tool: GitHub Projects, Jira, etc.]
- [Update frequency: Daily, Weekly]

**Definition of Done (Sprint):**
- [ ] All planned features delivered
- [ ] Code reviewed and merged
- [ ] Deployed to staging/production
- [ ] Documentation updated
- [ ] Demo-ready

**Velocity tracking:**
- Sprint 1: [Target story points]
- Adjust in Sprint 2 based on actual velocity
```

**Grading Criteria:**
- **Roadmap Structure (5 pts):** Clear 4-sprint breakdown with themes and goals
- **Feature Details (5 pts):** Features have user stories and acceptance criteria
- **Realism (5 pts):** Roadmap is achievable given team capacity and skills

---

### Part 3B: Process Map (10 points)

**File:** `/03-build/workflow/process-map.md`

Document your team's development workflow from idea to deployment.

```markdown
# Team Development Process Map

**Project:** [Your Project Name]  
**Team:** [Your Team Name]  
**Last Updated:** [Date]

---

## Workflow Overview

**Our development process:**
Idea → Planning → Development → Review → Testing → Deployment → Monitor

---

## Phase 1: Idea & Planning

### Input
- New feature request
- Bug report
- User feedback
- Team brainstorm

### Activities
1. **Capture:** Log idea/request in [Tool]
2. **Discuss:** Brief team discussion (async or in meeting)
3. **Estimate:** Assign story points (Planning Poker)
4. **Prioritize:** Add to backlog with priority label
5. **Refine:** Break down into smaller tasks if needed

### Output
- Backlog item with:
  - User story
  - Acceptance criteria
  - Story point estimate
  - Priority label

### Tools
- [GitHub Issues, Jira, Trello, etc.]

---

## Phase 2: Development

### Trigger
- Sprint planning: Task assigned to developer
- Developer pulls task from "Ready" column

### Activities
1. **Create branch:** `git checkout -b feature/[task-name]`
2. **Implement:** Write code following team standards
3. **Self-test:** Test locally before pushing
4. **Commit:** Clear, descriptive commit messages
5. **Push:** Push branch to GitHub

### Coding Standards
```markdown
**Branch naming:**
- feature/[feature-name]
- bugfix/[bug-name]
- hotfix/[critical-fix]

**Commit messages:**
- Format: [type]: [description]
- Examples:
  - feat: add user authentication
  - fix: resolve login redirect bug
  - docs: update README with setup instructions

**Code style:**
- [Linting tool if using]
- [Formatting tool if using]
- [Indentation, naming conventions]
```

### Output
- Feature branch with working code
- Local tests passed

---

## Phase 3: Code Review

### Trigger
- Developer opens Pull Request (PR)

### Activities
1. **Create PR:**
   - Descriptive title and description
   - Link to related issue
   - Screenshots/demo if UI changes
   - Reviewer(s) assigned

2. **Review process:**
   - Reviewer checks:
     - [ ] Code quality
     - [ ] Follows team standards
     - [ ] Tests included (if applicable)
     - [ ] No obvious bugs
     - [ ] Matches acceptance criteria
   
3. **Feedback:**
   - Reviewer leaves comments
   - Developer addresses feedback
   - Repeat until approved

4. **Approval:**
   - At least [1-2] approvals required
   - All comments resolved

### PR Template
```markdown
## Description
[What does this PR do?]

## Related Issue
Closes #[issue number]

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## How Has This Been Tested?
[Describe testing approach]

## Screenshots (if applicable)
[Add screenshots]

## Checklist
- [ ] Code follows team style guidelines
- [ ] Self-reviewed code
- [ ] Commented complex code
- [ ] Updated documentation
- [ ] No new warnings
- [ ] Tested locally
```

### Output
- Approved PR ready to merge

---

## Phase 4: Testing

### Pre-Merge Testing
**Who:** Developer + Reviewer  
**When:** Before PR approval  
**What:**
- [ ] Feature works as expected
- [ ] No regression (existing features still work)
- [ ] Edge cases tested
- [ ] Mobile responsive (if web app)

### Post-Merge Testing
**Who:** QA person or full team  
**When:** After merge to main/staging  
**What:**
- [ ] Deploy to staging environment
- [ ] Smoke test: Core flows work
- [ ] Integration test: New feature + existing features
- [ ] Performance check: No major slowdowns

### Testing Tools
- Manual testing: [Checklist]
- Automated tests: [If you have them - Jest, Pytest, etc.]
- Staging environment: [URL]

---

## Phase 5: Deployment

### Deployment Strategy
**Environment setup:**
- **Development:** Local machines
- **Staging:** [Staging URL] - for testing
- **Production:** [Production URL] - live users

### Deployment Process

**Automatic deployment:**
- Trigger: Merge to `main` branch
- Tool: [GitHub Actions, Vercel auto-deploy, etc.]
- Time: [~X minutes]

**Manual deployment (if not automated):**
1. [Step 1]
2. [Step 2]
3. [Step 3]

### Deployment Checklist
- [ ] All tests passed
- [ ] Staging tested successfully
- [ ] Database migrations run (if needed)
- [ ] Environment variables updated
- [ ] Rollback plan ready

### Rollback Plan
**If deployment breaks production:**
1. [Immediate action]
2. [How to revert]
3. [Communication plan]

---

## Phase 6: Monitoring & Iteration

### Post-Deployment Monitoring

**Immediately after deploy (First 30 mins):**
- [ ] Check logs for errors
- [ ] Test critical user flows
- [ ] Monitor analytics (if available)
- [ ] Verify performance metrics

**First 24 hours:**
- [ ] Watch for bug reports
- [ ] Monitor user behavior in analytics
- [ ] Check system performance
- [ ] Review error logs

**First week:**
- [ ] Gather user feedback
- [ ] Check metrics against targets
- [ ] Identify issues or improvements
- [ ] Plan next iteration

### Feedback Loops
**How we gather feedback:**
1. [Direct user conversations]
2. [In-app feedback form]
3. [Usage analytics]
4. [Team retrospectives]

**How feedback becomes tasks:**
1. Log in [Tool]
2. Prioritize in backlog grooming
3. Schedule for future sprint

---

## Agile Ceremonies

### Sprint Planning (Every 2 weeks - Monday)
**Duration:** 1-2 hours  
**Participants:** Full team  
**Agenda:**
1. Review sprint goal
2. Review backlog
3. Estimate stories (Planning Poker)
4. Commit to sprint scope
5. Break down tasks
6. Assign initial work

**Output:** Sprint backlog with assigned tasks

---

### Daily Standups (Every day - 15 min)
**Time:** [Your chosen time]  
**Format:** [In-person, Slack, voice call]  
**Each person shares:**
1. What I did yesterday
2. What I'm doing today
3. Any blockers

**Output:** Team alignment, blockers identified

---

### Sprint Review (End of sprint - Friday)
**Duration:** 30-60 minutes  
**Participants:** Full team (+ instructor if presenting)  
**Agenda:**
1. Demo completed work
2. Review sprint metrics
3. Gather feedback
4. Discuss what didn't get done

**Output:** Feedback for next sprint

---

### Sprint Retrospective (End of sprint - Friday)
**Duration:** 30-45 minutes  
**Participants:** Full team  
**Agenda:**
1. What went well?
2. What didn't go well?
3. What will we improve?
4. Action items for next sprint

**Format:** [Your chosen retro format - Start/Stop/Continue, etc.]

**Output:** Action items to improve process

---

### Backlog Grooming (Mid-sprint - Optional)
**Duration:** 30 minutes  
**Participants:** Full team or subset  
**Agenda:**
1. Review upcoming backlog items
2. Add details and acceptance criteria
3. Rough estimation
4. Prioritize

**Output:** Well-prepared backlog for next sprint planning

---

## Team Communication

### Communication Channels

**Slack/Discord channels:**
- `#general` - Team chat, non-urgent
- `#standup` - Daily updates
- `#bugs` - Bug reports and tracking
- `#random` - Off-topic, fun stuff

**GitHub:**
- Issues - Feature requests, bugs
- PRs - Code review discussions
- Discussions - Design decisions, questions

**Video calls:**
- Tool: [Zoom, Google Meet, Discord]
- Sprint ceremonies
- Pair programming sessions
- Emergency discussions

### Response Time Expectations
- **Urgent (blocking work):** 1-2 hours
- **Important:** Same day
- **Normal:** Within 24 hours
- **Low priority:** Within 48 hours

### Availability
**Team member availability:**
- [Member 1]: [Days/times available]
- [Member 2]: [Days/times available]
- [Member 3]: [Days/times available]
- [Member 4]: [Days/times available]

---

## Decision Log

**How we make and document decisions:**

### Decision Template
```markdown
## Decision: [Title]
**Date:** [Date]
**Decision makers:** [Names]

**Context:**
[What problem are we solving?]

**Options considered:**
1. [Option A] - [Pros/Cons]
2. [Option B] - [Pros/Cons]

**Decision:**
[What we chose and why]

**Consequences:**
[What changes because of this decision]
```

**Where we log decisions:**
- [Location: Wiki, Docs folder, etc.]

---

## Continuous Improvement

**How we'll evolve this process:**
1. Sprint retrospectives identify process issues
2. Team agrees on improvements
3. Try improvement for one sprint
4. Assess and keep or drop

**Process review schedule:**
- After Sprint 1: Major review
- After each sprint: Minor adjustments
```

**Grading Criteria:**
- **Workflow Completeness (4 pts):** All phases from idea to monitoring documented
- **Ceremonies (3 pts):** Scrum ceremonies defined with clear cadence
- **Realism (3 pts):** Process fits team's capacity and working style

---

### Part 3C: First Sprint Plan (15 points)

**File:** `/03-build/roadmap/sprint-1-plan.md`

Detailed plan for your first 2-week sprint (Week 7-8).

```markdown
# Sprint 1 Plan (Week 7-8)

**Sprint Dates:** November 6-21, 2025  
**Sprint Goal:** [One clear sentence - what will be true at the end of this sprint?]  
**Team Capacity:** [Total story points team can commit to]

---

## Sprint Backlog

### User Stories

#### Story 1: [Story Title]
**Priority:** High  
**Story Points:** [X]  
**Assigned to:** [Name]

**User Story:**  
As a [type of user], I want [goal] so that [reason/benefit].

**Acceptance Criteria:**
- [ ] [Specific, testable criterion 1]
- [ ] [Specific, testable criterion 2]
- [ ] [Specific, testable criterion 3]

**Tasks:** (Break down into sub-tasks if needed)
- [ ] [Task 1] - [Estimated hours: X]
- [ ] [Task 2] - [Estimated hours: X]
- [ ] [Task 3] - [Estimated hours: X]

**Definition of Done:**
- [ ] Code complete and working locally
- [ ] Code reviewed and approved
- [ ] Merged to main branch
- [ ] Deployed to staging
- [ ] Tested by another team member
- [ ] Documentation updated (if needed)

---

#### Story 2: [Story Title]
[Same format as Story 1]

---

#### Story 3: [Story Title]
[Same format as Story 1]

---

[Include 4-6 user stories total]

---

## Technical Tasks (Not user-facing)

### Task 1: [Technical Task]
**Assigned to:** [Name]  
**Story Points:** [X]

**Description:**  
[What needs to be done]

**Why it's needed:**  
[Explanation of necessity]

**Tasks:**
- [ ] [Subtask 1] - [Est. hours: X]
- [ ] [Subtask 2] - [Est. hours: X]

**Definition of Done:**
- [ ] [Criterion 1]
- [ ] [Criterion 2]

---

[Include 2-3 technical tasks]

---

## Sprint Metrics & Goals

### Velocity Target
**Target story points to complete:** [X points]  
(This is a guess for Sprint 1 - we'll refine based on actual velocity)

### Success Metrics
| Metric | Target | How We'll Measure |
|--------|--------|-------------------|
| [Metric 1] | [X] | [Method] |
| [Metric 2] | [X] | [Method] |
| Stories completed | [X/Y stories] | Sprint board |
| Velocity achieved | [X points] | Burndown chart |

---

## Sprint Schedule

### Week 1 (Nov 6-14)
**Monday Nov 6 - Sprint Planning**
- 1-2 hours: Full team sprint planning meeting
- Output: Sprint backlog finalized

**Daily: Nov 7-14**
- Daily standup at [time]
- Development work
- Code reviews

**Friday Nov 8 - Mid-Sprint Check**
- 30 min: Quick sync on progress
- Adjust if needed

---

### Week 2 (Nov 15-21)
**Daily: Nov 15-20**
- Daily standup at [time]
- Development work
- Code reviews
- Testing

**Thursday Nov 21 - Sprint Review & Retro**
- 30 min: Demo completed work
- 30 min: Retrospective
- Plan for Sprint 2

---

## Risk Management

### Known Risks
1. **[Risk 1]**
   - Impact: [High/Medium/Low]
   - Mitigation: [Plan]

2. **[Risk 2]**
   - Impact: [High/Medium/Low]
   - Mitigation: [Plan]

### Dependencies
- [ ] [External dependency 1]
- [ ] [External dependency 2]

### Blockers (Will update during sprint)
- None identified yet

---

## Team Agreements for Sprint 1

### Working Hours
- [Member 1]: [Available times]
- [Member 2]: [Available times]
- [Member 3]: [Available times]
- [Member 4]: [Available times]

### Communication
- Daily standups: [Time and format]
- Urgent issues: [How to escalate]
- Response time: [Expectation]

### Code Review
- PRs reviewed within: [X hours]
- Minimum reviewers: [X people]

---

## Planning Poker Results

### Story Point Scale
- 1 point = ~2 hours work
- 2 points = ~4 hours work
- 3 points = ~6 hours work
- 5 points = ~10 hours work
- 8 points = ~16 hours work (consider breaking down)

### Estimation Session Notes
[Notes from your team's Planning Poker session]

---

## Burndown Tracking

**How we'll track:**
- [GitHub Projects, Jira burndown, spreadsheet, etc.]

**Update frequency:**
- Daily during standup

**Chart location:**
- [Link or location]

---

## Sprint Board

**Columns:**
1. To Do
2. In Progress
3. Code Review
4. Testing
5. Done

**Card movement rules:**
- Only pull from "To Do" when ready to start
- "In Progress" limit: 2 cards per person max
- Can't skip columns
- "Done" requires all DoD criteria met

**Board location:**
- [GitHub Projects board URL]
```

**Grading Criteria:**
- **Story Quality (6 pts):** 4-6 well-written user stories with clear acceptance criteria
- **Task Breakdown (4 pts):** Stories broken into estimable tasks
- **Estimation (3 pts):** Realistic story points assigned using Planning Poker
- **Completeness (2 pts):** Sprint includes schedule, risks, and team agreements

---

## 📤 Submission Instructions

### Deadline
**All files must be committed and pushed to your team's GitHub repository by:**  
**Thursday, November 27th, 2025 at 11:59 PM (Midnight)**

---

### Submission Checklist

Before submitting, verify your repository has all required files:

**Part 1: Technical Architecture (35 pts)**
- [ ] `/03-build/architecture/system-design.md`
- [ ] `/03-build/architecture/tech-stack.md`
- [ ] `/03-build/architecture/architecture-diagram.png` (or .jpg, .pdf)
- [ ] `/03-build/architecture/risk-spikes.md`

**Part 2: Analytics Foundation (25 pts)**
- [ ] `/03-build/analytics/event-schema.md`
- [ ] `/03-build/analytics/metrics-definition.md`
- [ ] `/03-build/analytics/platform-setup.md`

**Part 3: Agile Sprint Planning (40 pts)**
- [ ] `/03-build/roadmap/product-roadmap.md`
- [ ] `/03-build/workflow/process-map.md`
- [ ] `/03-build/roadmap/sprint-1-plan.md`

**Formatting & Quality**
- [ ] All files are properly formatted Markdown
- [ ] No placeholder text like "[Insert here]" left in documents
- [ ] Links work (internal repo links and external resources)
- [ ] Images/diagrams are clear and visible
- [ ] Commit messages are descriptive

---

### How to Submit

1. **Ensure all team members have committed their work**
```bash
git add .
git commit -m "Add Lab 6-7 homework: Technical architecture and sprint planning"
git push origin main
```

2. **Verify on GitHub**
   - Go to your repository on GitHub
   - Check that all files are present
   - Click on files to verify content displays correctly

3. **Submit repository link** (if required by instructor)
   - Submit your repository URL via [submission platform]
   - Format: `https://github.com/[your-team]/[your-repo]`

---

## 🤔 FAQs

**Q: Can we use tools other than Markdown?**  
A: Markdown is required for text documents, but architecture diagrams can be PNG/JPG/PDF. If you want to embed additional materials (Figma links, etc.), that's fine as supplements.

**Q: What if we haven't chosen our tech stack yet?**  
A: You must make technology decisions as part of this homework. Use the decision framework in Part 1B to evaluate options and commit to choices. You can adjust later if absolutely necessary, but making decisions now is part of the learning.

**Q: Do we need to actually sign up for an analytics platform?**  
A: Yes, signing up is required (all major platforms have free tiers). You don't need to implement tracking code yet, but you must document the setup for implementation in Sprint 1.

**Q: How detailed should user stories be?**  
A: Each user story should have clear acceptance criteria (3-5 criteria) and be broken into estimated tasks. If you can't estimate it, it's not detailed enough.

**Q: What if our sprint plan changes?**  
A: That's expected! This is your initial plan. You'll update it during Sprint Planning and throughout the sprint. Document changes in your sprint retrospective.

**Q: Can we work on this separately or must we meet?**  
A: Some sections (like architecture and roadmap) require team discussion and consensus. Others (like writing up documentation) can be divided. We recommend at least 2 team meetings: one for technical decisions and one for sprint planning.

**Q: How long should each document be?**  
A: Quality over quantity. A concise, well-thought-out document is better than a long, vague one. Most documents should be 2-5 pages when printed. The process map might be longer due to ceremony descriptions.

**Q: What if we identify more than 3 risk spikes?**  
A: Document all significant risks, but prioritize 3 for investigation in Sprint 1. You can tackle others in later sprints.

---

## 💡 Tips for Success

### Time Management
- **Don't leave this for the last day!** This is 6-8 hours of work.
- Start with architecture decisions (Part 1) - everything else builds on this
- Allocate time:
  - Part 1 (Architecture): 2-3 hours
  - Part 2 (Analytics): 2 hours
  - Part 3 (Sprint Planning): 2-3 hours

### Team Collaboration
- Hold a team meeting for architecture decisions - don't decide individually
- Use Planning Poker for story point estimation (builds team calibration)
- Divide documentation writing, but review together before submitting

### Quality Over Quantity
- Specific, realistic plans beat vague, ambitious ones
- If you're copying templates without customization, stop and think
- Your documents should reflect YOUR project and YOUR team

### Resources
- Review lecture slides from Weeks 6-7
- Check lab materials for templates and examples
- Ask questions in office hours or Slack #lab-help
- Look at sample architecture diagrams from well-known projects

---

## 🎯 Grading Summary

| Section | Points | Files |
|---------|--------|-------|
| **Part 1: Technical Architecture** | **35** | |
| 1A: System Design | 10 | system-design.md |
| 1B: Tech Stack Decisions | 10 | tech-stack.md |
| 1C: Architecture Diagram | 5 | architecture-diagram.png |
| 1D: Risk Spikes | 10 | risk-spikes.md |
| **Part 2: Analytics Foundation** | **25** | |
| 2A: Event Schema | 10 | event-schema.md |
| 2B: Metrics Definition | 10 | metrics-definition.md |
| 2C: Platform Setup | 5 | platform-setup.md |
| **Part 3: Agile Sprint Planning** | **40** | |
| 3A: Product Roadmap | 15 | product-roadmap.md |
| 3B: Process Map | 10 | process-map.md |
| 3C: First Sprint Plan | 15 | sprint-1-plan.md |
| **TOTAL** | **100** | **10 files** |

---

## 📚 Additional Resources

### Architecture & Technical Decisions
- [The C4 Model for Software Architecture](https://c4model.com/)
- [Architecture Decision Records](https://adr.github.io/)
- [AWS Architecture Center](https://aws.amazon.com/architecture/)

### Analytics & Metrics
- [Mixpanel Guide to Product Analytics](https://mixpanel.com/topics/)
- [Amplitude's Analytics Playbook](https://amplitude.com/books/product-analytics-playbook)
- [Lean Analytics (Book)](https://leananalyticsbook.com/)

### Agile & Scrum
- [The Scrum Guide](https://scrumguides.org/)
- [Planning Poker Guide](https://www.mountaingoatsoftware.com/agile/planning-poker)
- [User Story Template](https://www.atlassian.com/agile/project-management/user-stories)

### Tools
- **Diagramming:** Excalidraw, Draw.io, Lucidchart, Miro
- **Analytics:** Mixpanel, Amplitude, PostHog, Google Analytics 4
- **Project Management:** GitHub Projects, Jira, Linear, Trello

---

**Good luck with your planning! Remember: A good plan executed well beats a perfect plan that's too complex to follow. Start simple, iterate, and adjust as you learn.** 🚀

---

**Questions?** Post in Slack #lab-help or come to office hours: Tuesday & Thursday 2-4 PM, Room K-305
