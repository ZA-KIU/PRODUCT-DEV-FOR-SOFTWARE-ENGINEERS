# Team Workflow & Development Process

**Team:** [Your Team Name]  
**Date Created:** [Date]  
**Last Updated:** [Date]

---

## Overview

This document defines HOW our team will work together over the next 8 weeks to build our MVP. It's our operating agreement for development.

**Why this matters:**
- Everyone knows what to expect
- Reduces confusion and conflict
- Ensures code quality
- Enables parallel work without blockers

---

## Our Development Methodology

**We are using:** Agile/Scrum (adapted for academic capstone)

**Why Agile?**
[Explain why you chose Agile over Waterfall or Lean for your project]

**Example:** "We're building an MVP with uncertain requirements. Agile lets us iterate based on user feedback every 2 weeks rather than committing to a fixed plan upfront."

**Our Adaptations:**
[How are you adapting Scrum for a 4-person academic team?]

**Example:**
- No formal Scrum Master role—we rotate facilitation
- Daily standups are async (not everyone available same time)
- Sprint reviews include user testing, not just internal demos

---

## Sprint Cadence (2-Week Iterations)

### Sprint Structure

**Duration:** 2 weeks (14 days)

**Sprint Flow:**
```
Day 1 (Monday):
  └─ Sprint Planning (1 hour)
     └─ Commit to stories, assign tasks

Days 2-12 (Tues-Sat):
  └─ Daily Standup (10 min, async)
  └─ Development work
  └─ Midweek Check-in (Wed, 30 min)

Day 13 (Saturday):
  └─ Final testing & polish

Day 14 (Sunday):
  └─ Sprint Review (30 min)
  └─ Sprint Retrospective (30 min)
  └─ Sprint 1 ends, Sprint 2 begins next Monday
```

### Sprint Schedule (8 Weeks)

| Sprint | Dates | Focus | Major Deliverable |
|--------|-------|-------|-------------------|
| Sprint 1 | Nov 10-23 | Foundation + Core Feature #1 | Unified dashboard deployed |
| Midterm | Week of Nov 24 | EXAM WEEK - Reduced capacity | — |
| Sprint 2 | Nov 24-30 (1 week) | Core Feature #2 + Integration | Real-time updates working |
| Sprint 3 | Dec 1-14 | Polish + Analytics + Testing | MVP complete with dashboard |
| Final Prep | Dec 15-Jan 7 | Testing + Presentations | Final demo ready |

---

## Daily Standup Process

### Format
**Async in Slack** (preferred) or **10-min sync call** (if needed)

**Time:** Every day at 9:00 AM

**Where:** #team-standup Slack channel

### What Each Person Posts

```
**Yesterday:**
✅ Completed T-001-3 (TaskDashboard component)
✅ Reviewed PR #42

**Today:**
🚀 Starting T-001-4 (Task filtering logic)
🚀 Will pair with [Name] on authentication

**Blockers:**
🚫 Waiting for design mockup approval
🚫 Need help debugging API endpoint (will reach out to [Name])
```

### Rules

- **Post by 9:00 AM** (flexible on weekends)
- **Be specific:** "Working on dashboard" → "Building TaskDashboard React component (T-001-3)"
- **Flag blockers immediately:** Don't wait until midweek check-in
- **Keep it brief:** 3-5 bullet points max
- **No async standup on weekends** (optional weekend work)

### When We Do Sync Standups

**Only if:**
- Major blocker affecting multiple people
- Critical decision needed
- Team requests it

**How:** 10-min video call, same format

---

## Midweek Check-In

### Schedule
**Every Wednesday at 5:00 PM** (30 minutes)

**Where:** Google Meet / Zoom

**Who:** Full team (required attendance)

### Agenda (30 min)

**1. Sprint Burndown Review (10 min)**
   - How many stories/tasks complete?
   - Are we on track for sprint goal?
   - Burndown chart check

**2. Blocker Resolution (10 min)**
   - What's blocking progress?
   - Who can help unblock?
   - Decision: Do we need to descope?

**3. Plan Adjustment (10 min)**
   - Do we need to reprioritize tasks?
   - Any stories at risk of not completing?
   - Action items for next 3 days

### Output
- Updated task assignments (if needed)
- Blocker resolution plan
- Go/no-go decision on sprint scope

---

## Sprint Planning (Start of Each Sprint)

### Schedule
**First Monday of sprint at 9:00 AM** (1 hour)

**Where:** In person (if possible) or Google Meet

**Who:** Full team (required)

### Agenda (60 min)

**1. Sprint Goal Review (5 min)**
   - What's the ONE thing we must accomplish?
   - Read sprint goal aloud and confirm commitment

**2. Story Walkthrough (30 min)**
   - Review each user story in sprint
   - Clarify acceptance criteria
   - Break stories into technical tasks
   - Estimate task hours

**3. Capacity Planning (15 min)**
   - Confirm each person's availability (hours/week)
   - Assign task owners
   - Verify total hours ≤ team capacity

**4. Dependencies & Risks (10 min)**
   - Identify blockers
   - Agree on mitigation strategies
   - Assign risk owners

### Output
- Sprint plan document complete
- All tasks assigned
- Team commits to sprint

---

## Sprint Review (End of Each Sprint)

### Schedule
**Last Sunday of sprint at 4:00 PM** (30 minutes)

**Where:** Google Meet

**Who:** Full team

### Agenda (30 min)

**1. Demo Completed Stories (20 min)**
   - Each person demos their work
   - Show working feature in staging environment
   - Walk through acceptance criteria (all met?)

**2. Incomplete Work Discussion (5 min)**
   - What didn't get done?
   - Why not?
   - Move to next sprint or cut?

**3. User Feedback (5 min)**
   - Share results from user testing
   - Quotes, observations, metrics
   - Decisions: What to adjust?

### Output
- List of completed stories
- List of incomplete stories (with plan)
- User feedback documented

---

## Sprint Retrospective (After Sprint Review)

### Schedule
**Last Sunday of sprint at 4:30 PM** (30 minutes)

**Where:** Google Meet

**Who:** Full team

### Agenda (30 min)

**1. What Went Well? (10 min)**
   - Team brainstorms positive observations
   - Use sticky notes (Miro) or Slack thread
   - Examples: "Daily standups were helpful", "Pair programming on API was efficient"

**2. What Didn't Go Well? (10 min)**
   - Team brainstorms challenges/frustrations
   - No blame, focus on process not people
   - Examples: "Estimates were too optimistic", "Too many meetings"

**3. Action Items (10 min)**
   - Pick top 3 issues from "didn't go well"
   - For each, define ONE action item
   - Assign owner and due date

### Output
- 3-5 action items for next sprint
- Documented in retrospective notes
- Owner assigned for each action

### Example Action Items

❌ **Bad:** "Communicate better"  
✅ **Good:** "Add 'blocked?' label to all tasks in GitHub by [Name], starting Sprint 2"

❌ **Bad:** "Improve code quality"  
✅ **Good:** "Require 2 reviewers for PRs >200 lines, enforced by [Name] as Tech Lead"

---

## GitHub Workflow

### Branch Strategy

**Main Branch:**
- `main` = production-ready code
- Always deployable
- Protected (no direct commits)

**Feature Branches:**
- One branch per task or story
- Naming: `feature/task-dashboard` or `feature/US-001`
- Created from `main`, merged back to `main` via PR

**Bugfix Branches:**
- Naming: `bugfix/fix-api-error` or `bugfix/issue-42`

### Branch Lifecycle

```
1. Create branch from main
   $ git checkout main
   $ git pull origin main
   $ git checkout -b feature/task-dashboard

2. Work on branch, commit often
   $ git add .
   $ git commit -m "feat: add TaskDashboard component"
   $ git push origin feature/task-dashboard

3. When done, create Pull Request (PR)
   - Go to GitHub
   - Click "New Pull Request"
   - Base: main, Compare: feature/task-dashboard
   - Fill in PR template

4. Code review by teammate(s)
   - At least 1 approval required
   - Address feedback, push new commits

5. Merge to main
   - Squash and merge (keeps history clean)
   - Delete feature branch after merge

6. Pull latest main
   $ git checkout main
   $ git pull origin main
```

### Pull Request (PR) Template

**Every PR must include:**

```markdown
## Description
[What does this PR do? 1-2 sentences]

## Related Story/Task
- Story: US-001
- Task: T-001-3

## Changes Made
- [Change 1]
- [Change 2]
- [Change 3]

## Testing Done
- [ ] Unit tests added/updated
- [ ] Manual testing completed
- [ ] Works on mobile (if applicable)

## Screenshots (if UI change)
[Add screenshots or GIFs]

## Checklist
- [ ] Code follows team style guide
- [ ] No console errors
- [ ] Analytics events tested (if applicable)
- [ ] Documentation updated (if needed)
```

### Code Review Process

**Reviewers must check:**
- [ ] Code is readable and follows conventions
- [ ] No obvious bugs or security issues
- [ ] Tests are included
- [ ] Acceptance criteria met (if final PR for story)

**Review within:** 24 hours (48 hours on weekends)

**Approval required:** 1 teammate (2 for complex/risky changes)

### Commit Message Format

**Format:** `<type>: <short description>`

**Types:**
- `feat:` New feature
- `fix:` Bug fix
- `refactor:` Code change that doesn't add feature or fix bug
- `test:` Add or update tests
- `docs:` Documentation changes
- `style:` Formatting, missing semicolons, etc.

**Examples:**
- ✅ `feat: add TaskDashboard component`
- ✅ `fix: resolve API endpoint 500 error`
- ✅ `refactor: extract task filtering logic`
- ❌ `updated stuff` (too vague)
- ❌ `fixed bug` (which bug?)

---

## Communication Channels

### Primary: Slack

**Channels:**
- `#team-general` - General team chat, non-urgent
- `#team-standup` - Daily standups only
- `#team-dev` - Technical discussions, code questions
- `#team-blockers` - Flag urgent issues

**Response Time:**
- **Urgent blockers:** 2 hours (use @channel)
- **Code review requests:** 24 hours
- **General questions:** 48 hours

### Secondary: WhatsApp Group

**Use for:**
- Urgent notifications outside work hours
- Quick "I'm running late" messages
- Social/team bonding

**Don't use for:**
- Technical discussions (use Slack #team-dev)
- Code reviews (use GitHub)
- Long conversations (use Google Meet)

### Weekly Sync (Beyond Ceremonies)

**Optional:** 1 hour sync call on Fridays at 3:00 PM
- Social check-in
- Show-and-tell of progress
- Pair programming session

---

## Pair Programming Protocol

### When to Pair

**Recommended for:**
- Complex features (>8 hour estimate)
- New technology/framework
- Debugging difficult issues
- Onboarding to unfamiliar codebase

**Not needed for:**
- Simple, well-defined tasks
- CSS/styling tweaks
- Documentation updates

### How to Pair

**Driver-Navigator Model:**
- **Driver:** Types code, focuses on syntax
- **Navigator:** Reviews logic, suggests approach
- **Switch roles every 25 minutes** (Pomodoro)

**Tools:**
- VS Code Live Share (preferred)
- Zoom screen share
- In-person (if available)

**Schedule:**
- Agree on 1-2 hour block
- Both fully focused (no multitasking)
- Take 5-min break every 25 min

---

## Definition of Done (DoD)

### Story-Level DoD

For a user story to be marked "Done":
- [ ] All tasks complete
- [ ] All acceptance criteria met
- [ ] Code reviewed by ≥1 teammate
- [ ] All tests passing (unit + integration)
- [ ] Merged to main branch
- [ ] Deployed to staging environment
- [ ] Analytics events instrumented (if applicable)
- [ ] Tested by ≥1 teammate who didn't write the code
- [ ] No P0 (critical) bugs
- [ ] Documentation updated (README, API docs, etc.)

### Task-Level DoD

For a technical task to be marked "Done":
- [ ] Code written and committed
- [ ] Tests written (if applicable)
- [ ] Self-review completed (no console errors, no obvious bugs)
- [ ] Pushed to feature branch
- [ ] Ready for PR (or already in PR)

---

## Definition of Ready (DoR)

Before a story can be pulled into a sprint:
- [ ] User story written in "As a... I want... So that..." format
- [ ] Acceptance criteria defined (3-5 criteria)
- [ ] Story estimated (story points or hours)
- [ ] Dependencies identified
- [ ] No unresolved questions or ambiguities

If a story doesn't meet DoR, it stays in backlog.

---

## Testing Strategy

### Unit Tests

**Who writes:** Developer who writes the code

**When:** Before submitting PR

**Coverage Target:** >70% for new code

**Framework:** [e.g., Jest for JavaScript, pytest for Python]

### Integration Tests

**Who writes:** Team collaborates

**When:** After major features integrate

**Focus:** API endpoints, database interactions, third-party integrations

### Manual Testing

**Who does:** At least 1 teammate who didn't write the code

**When:** Before story marked "Done"

**Checklist:**
- [ ] Feature works as described in acceptance criteria
- [ ] No console errors
- [ ] Works on mobile (if applicable)
- [ ] Edge cases handled (e.g., empty states, errors)

### User Testing

**Who recruits:** [Team member name] (Discovery Lead)

**When:** End of each sprint (Thursday-Sunday)

**How many users:** 3-5 per sprint

**Process:**
1. Recruit from ICP (use interview contacts)
2. Schedule 15-20 min sessions
3. Prepare test scenarios
4. Observe, take notes (don't help unless stuck)
5. Collect feedback (survey + quotes)

---

## Conflict Resolution Process

### Step 1: Direct Communication (First)
- If you have an issue with a teammate, talk to them directly first
- Use "I" statements: "I felt frustrated when..." not "You always..."
- Focus on behavior, not personality

### Step 2: Team Discussion (If Unresolved)
- Bring issue to team meeting (midweek check-in or retrospective)
- Team discusses and votes (majority rules)
- Tech Lead facilitates, doesn't decide

### Step 3: Role-Based Decision (If Still Deadlocked)
- **Technical decisions:** Tech Lead decides
- **Design decisions:** Frontend Lead decides
- **Analytics decisions:** Analytics Lead decides
- **Process decisions:** Team votes, Program Lead breaks tie

### Step 4: Instructor Escalation (Last Resort)
- Only if Steps 1-3 fail
- Document: What's the conflict? What have you tried?
- Instructor provides guidance or makes final call

---

## Decision-Making Framework

### Consensus Decisions (Preferred)

**Use for:** Sprint goals, roadmap, major technical decisions

**Process:**
1. Discuss options (everyone shares perspective)
2. Propose solution
3. Ask: "Can everyone live with this?"
4. If yes, proceed. If no, discuss concerns and revise.

### Majority Vote

**Use for:** Medium-importance decisions, when consensus fails

**Process:**
1. Each person votes
2. Majority wins (3 out of 4)
3. Losing side "disagrees and commits" (support decision)

### Role-Based Authority

**Use for:** Tactical decisions, time-sensitive choices

**Examples:**
- Tech Lead decides: framework choice, architecture patterns
- Frontend Lead decides: component structure, styling approach
- Backend Lead decides: API design, database schema
- Analytics Lead decides: event naming, dashboard layout

---

## Tools & Platforms

| Purpose | Tool | Owner | Access Required |
|---------|------|-------|-----------------|
| Code repository | GitHub | [Team name org] | All team members |
| Project board | GitHub Projects | [Tech Lead] | All team members |
| Communication | Slack | [Team workspace] | All team members |
| Video calls | Google Meet | [Team calendar] | All team members |
| Design | Figma | [Frontend Lead] | View access for all |
| Database | [e.g., PostgreSQL on Heroku] | [Backend Lead] | Credentials shared securely |
| Hosting | [e.g., Vercel] | [Tech Lead] | Deployment access for leads |
| Analytics | [e.g., Mixpanel] | [Analytics Lead] | View access for all |
| Docs | Google Drive | [Team folder] | Edit access for all |

---

## Team Roles & Backup

**Purpose:** Ensure no single point of failure

| Role | Primary | Backup | Responsibilities |
|------|---------|--------|------------------|
| Tech Lead | [Name] | [Name] | Architecture, code reviews, CI/CD |
| Frontend Lead | [Name] | [Name] | UI/UX, React components, styling |
| Backend Lead | [Name] | [Name] | APIs, database, authentication |
| Analytics Lead | [Name] | [Name] | Event tracking, dashboard, metrics |
| Discovery Lead | [Name] | [Name] | User testing, interview recruiting |
| Program Lead | [Name] | [Name] | Process facilitation, timeline management |

**Note:** Roles are NOT exclusive. Everyone codes. Leads coordinate and make final calls in their domain.

---

## Working Hours & Availability

### Expected Commitment

**Each team member:** 10-15 hours/week
- Sprint 1-2: 15 hours/week (high intensity)
- Sprint 3: 10-12 hours/week (polish phase)

### Core Hours (Everyone Available)

**Best times for sync meetings:**
- [e.g., Weekdays 5:00-7:00 PM]
- [e.g., Weekend mornings 10:00 AM-12:00 PM]

### Individual Availability

| Team Member | Typical Availability | Blackout Times |
|-------------|----------------------|----------------|
| [Name] | Mon-Fri 3-8 PM, Sat 10-2 PM | Tues 4-6 PM (class) |
| [Name] | Mon-Wed-Fri 4-9 PM, Sun 2-6 PM | Thursdays (work) |
| [Name] | Tues-Thurs 2-7 PM, Sat-Sun 9 AM-1 PM | Monday mornings |
| [Name] | Daily 6-9 PM, Weekends flexible | Friday nights |

---

## Emergency Protocol

### If You Can't Meet a Deadline

**Do this:**
1. **Flag early** (don't wait until last minute)
2. Post in #team-blockers: "Need help - can't complete T-001-3 by Thursday"
3. Team decides: Reassign? Extend deadline? Descope?

**Don't do this:**
- Go silent and hope problem resolves itself
- Wait until sprint review to announce incomplete work

### If Life Happens (Sick, Emergency, etc.)

**Do this:**
1. Message team ASAP
2. Estimate when you'll be back
3. Identify critical tasks that need handoff
4. Team reassigns your tasks temporarily

**We understand:** Life happens. Communication is key.

---

## Version History & Updates

| Date | Change | Reason | Updated By |
|------|--------|--------|------------|
| [Date] | Initial workflow created | Lab 6 requirement | [Team] |
| [Date] | Added pair programming protocol | Sprint 1 retro action item | [Name] |
| [Date] | Updated standup time | Team vote | [Name] |

---

## Team Agreement & Sign-Off

**We have read, discussed, and agree to follow this workflow:**

- [ ] [Team Member 1] - [Date] - Signature: ________________
- [ ] [Team Member 2] - [Date] - Signature: ________________
- [ ] [Team Member 3] - [Date] - Signature: ________________
- [ ] [Team Member 4] - [Date] - Signature: ________________

**Next Review:** End of Sprint 1 (during retrospective)

**Instructor Feedback:** [Leave blank]

---

**File Location:** `/03-build/process/team-workflow.md`  
**Created:** [Date]  
**Last Updated:** [Date]  
**Status:** Active
