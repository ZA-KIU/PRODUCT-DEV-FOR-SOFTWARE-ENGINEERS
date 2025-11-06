# User Story Writing Guide

**Purpose:** Learn how to write effective user stories that guide development and testing

---

## What Is a User Story?

A **user story** is a short, simple description of a feature told from the perspective of the person who desires the new capability (usually a user or customer).

**Format:**
```
As a [type of user],
I want to [perform some action],
So that [I can achieve some goal/benefit].
```

---

## Why User Stories Matter

**Benefits:**
1. **User-focused:** Keeps team focused on user value, not just technical implementation
2. **Testable:** Clear acceptance criteria make testing straightforward
3. **Negotiable:** Details can be discussed and refined
4. **Small:** Each story completable in 1-5 days
5. **Estimable:** Team can estimate effort required

**Without good user stories:** Teams build features users don't need, miss edge cases, and can't tell when they're "done."

---

## The Three Components

### 1. Role (Who?)

**Bad:**
- "As a user..."  (too vague)

**Good:**
- "As a CS student managing 3 group projects..."
- "As a team leader coordinating 5 teammates..."
- "As a new user signing up for the first time..."

**Tip:** Reference your ICP. Be specific about which user segment.

### 2. Action (What?)

**Bad:**
- "I want a dashboard" (no specific action)
- "I want to use the app" (too vague)

**Good:**
- "I want to see all my assigned tasks on a single page"
- "I want to mark a task as complete with one click"
- "I want to filter tasks by project"

**Tip:** Use verbs. Describe the specific capability.

### 3. Benefit (Why?)

**Bad:**
- "So that it's easier" (vague)
- "So that I can manage tasks" (just restates the action)

**Good:**
- "So that I don't waste time checking WhatsApp, Drive, and GitHub separately"
- "So that my teammates immediately see progress without asking me"
- "So that I can focus on work instead of coordination"

**Tip:** Connect back to your validated pain points from interviews. Use language from your problem statement.

---

## Complete Example

### Bad User Story

```
As a user,
I want a task list,
So that I can see tasks.
```

**Problems:**
- "User" is too generic
- "Task list" doesn't explain what actions are possible
- "See tasks" doesn't explain the value/benefit
- Not testable—how do you know when it's done?

### Good User Story

```
As a CS student working on 3 concurrent group projects,
I want to see all tasks assigned to me across WhatsApp, Google Drive, and GitHub on a single dashboard,
So that I don't waste 20 minutes each morning checking multiple tools to figure out what to work on.
```

**Why it's good:**
- Specific user type with context (CS student, 3 projects)
- Clear action (see all tasks... on single dashboard)
- Quantified benefit (save 20 minutes, validated from interviews)
- Testable (can verify dashboard shows tasks from all three sources)

---

## Writing Acceptance Criteria

**Acceptance criteria** are conditions that must be true for the story to be "done." They're your checklist for testing.

### Format

Use checkboxes for each criterion:

```
- [ ] Criterion 1 (observable, testable)
- [ ] Criterion 2
- [ ] Criterion 3
- [ ] Criterion 4 (analytics/metrics)
```

### Guidelines

**Each criterion should be:**
- **Observable:** You can see/verify it
- **Testable:** Pass/fail, no ambiguity
- **Specific:** No vague language like "works well"

**Typical criteria:**
- **Functional:** Feature does X when user does Y
- **Performance:** Page loads in < 2 seconds
- **Edge cases:** Handles empty states, errors gracefully
- **Analytics:** Event X fires correctly
- **UX:** Works on mobile, accessible, etc.

### Example

**User Story:**
```
As a team leader,
I want to assign a task to a teammate,
So that they know what to work on without me messaging them.
```

**Acceptance Criteria:**
```
- [ ] User can select a task from the task list
- [ ] User can select a teammate from a dropdown
- [ ] Task shows assigned teammate's name after assignment
- [ ] Assigned teammate receives a notification (email or in-app)
- [ ] Task_Assigned event fires with properties: task_id, assigned_to, assigned_by
- [ ] Assignment works on mobile (responsive design)
- [ ] If no teammates available, show helpful message: "Add teammates first"
```

**Why these are good criteria:**
- Each is a clear pass/fail test
- Covers happy path (normal usage)
- Covers edge case (no teammates available)
- Includes analytics requirement
- Includes UX consideration (mobile, helpful messages)

---

## Common Mistakes & Fixes

### Mistake 1: Story is Too Large

**Bad:**
```
As a user,
I want to manage all aspects of my projects,
So that I'm more productive.
```

**Problem:** This is an epic, not a story. It's weeks of work.

**Fix:** Break into smaller stories:
1. "I want to see all my tasks..."
2. "I want to mark tasks as complete..."
3. "I want to filter tasks by project..."
4. "I want to assign tasks to teammates..."

**Rule:** If a story takes >5 days, it's too big. Split it.

---

### Mistake 2: Technical Implementation, Not User Value

**Bad:**
```
As a developer,
I want to set up a PostgreSQL database with migrations,
So that we can store data.
```

**Problem:** This is a technical task, not a user story. Users don't care about PostgreSQL.

**Fix:** Reframe from user perspective:
```
As a CS student,
I want my task list to persist across sessions,
So that I don't lose my progress when I close the app.
```

**Then:** "Set up PostgreSQL" becomes a **technical task** under this story, not a story itself.

**Rule:** User stories describe user-facing value. Technical tasks go inside stories.

---

### Mistake 3: No Clear Benefit

**Bad:**
```
As a user,
I want to click a button,
So that I can interact with the app.
```

**Problem:** Clicking a button isn't a benefit. What does the button *do*?

**Fix:**
```
As a team member,
I want to mark a task as complete with one click,
So that my teammates immediately see progress without me needing to message them.
```

**Rule:** The benefit should tie back to a validated pain point from your interviews.

---

### Mistake 4: Vague Acceptance Criteria

**Bad:**
- [ ] Dashboard works well
- [ ] User is happy
- [ ] No bugs

**Problem:** Not testable. What does "works well" mean? How do you measure "happy"?

**Fix:**
- [ ] Dashboard loads in < 2 seconds with 50 tasks
- [ ] User survey shows 4+/5 satisfaction after testing
- [ ] Zero P0 bugs; all P1 bugs documented

**Rule:** If you can't test it, it's not a good criterion.

---

## Advanced: INVEST Criteria

Good user stories follow **INVEST**:

**I - Independent**
- Story can be developed without depending on other stories
- Enables parallel work

**N - Negotiable**
- Details can be discussed and refined
- Not a fixed contract

**V - Valuable**
- Delivers value to the user
- Solves a real problem

**E - Estimable**
- Team can estimate effort (story points or hours)
- Not too vague or uncertain

**S - Small**
- Completable in 1-5 days
- If bigger, split it

**T - Testable**
- Clear acceptance criteria
- Can verify when "done"

**Use INVEST as a checklist:** Does your story meet all six?

---

## Story Size Estimation

### T-Shirt Sizing

**XS (1-2 hours):** Simple UI tweak, button color change  
**S (3-6 hours):** Simple feature, one new API endpoint  
**M (1-2 days):** Moderate feature, new React component with state  
**L (2-4 days):** Complex feature, integration with third-party API  
**XL (5+ days):** Too big! Split it.

### Story Points (Fibonacci)

**1 point:** Trivial (1-2 hours)  
**2 points:** Simple (3-4 hours)  
**3 points:** Moderate (1 day)  
**5 points:** Complex (2-3 days)  
**8 points:** Very complex (3-5 days)  
**13 points:** Epic-level (too big, split it)

**Rule:** Story points are relative, not absolute hours. A "3" is roughly 3x the effort of a "1".

---

## Connecting Stories to Evidence

**Every story should cite interview evidence.** This keeps you honest—are you building what users actually need?

**Format:**
```
**User Story:**
As a CS student,
I want to see real-time status updates when teammates complete tasks,
So that I don't need to ask "Are you done yet?" multiple times per day.

**Evidence:**
- Interview #3: "I waste so much time just checking if people finished their parts."
- Interview #7: "I end up messaging 'any updates?' 5 times a day."
- 7 out of 10 interviewees (70%) mentioned real-time updates as a critical need
```

**Why this matters:**
- Validates the story solves a real problem
- Reminds team of user pain when prioritizing
- Provides quotes for final presentation

---

## Story Template (Copy This)

```markdown
### Story ID: US-XXX

**Epic:** [Epic Name]  
**Priority:** Must Have / Should Have / Could Have  
**Sprint:** Sprint 1 / Sprint 2 / Sprint 3  
**Status:** Not Started / In Progress / In Review / Done  
**Assigned To:** [Team Member(s)]  

#### User Story

As a [type of user],
I want to [perform some action],
So that [I can achieve some goal/benefit].

#### Why This Matters (Evidence)

[Cite interview evidence: which pain point does this address? How many interviewees mentioned this? Include quotes.]

#### Acceptance Criteria

- [ ] **Criteria 1:** [Specific, testable condition]
- [ ] **Criteria 2:** [Specific, testable condition]
- [ ] **Criteria 3:** [Specific, testable condition]
- [ ] **Criteria 4 (Analytics):** [Event tracked correctly]

#### Estimated Effort

**Story Points:** [1, 2, 3, 5, 8, 13] or **Hours:** [X hours]

#### Dependencies

- [ ] [Technical dependency, e.g., "User authentication must work"]
- [ ] [Design dependency, e.g., "Dashboard mockup approved"]

#### Analytics Events

- `[Event_Name]` - Fires when [trigger condition]
- `[Event_Name]` - Fires when [trigger condition]

#### Notes / Questions

[Any open questions, technical concerns, or clarifications needed]
```

---

## Practice Exercise

**Your Problem Statement:**
"CS students waste 2-4 hours/week coordinating across disconnected tools because there's no single source of truth for task status."

**Write 3 user stories that address this problem.**

**Example Story 1:**
```
As a CS student working on multiple group projects,
I want to see all my tasks from WhatsApp, Google Drive, and GitHub in one place,
So that I don't waste 20 minutes each morning checking three separate tools.
```

**Now you try:**

**Story 2:** [Write a story about filtering or searching tasks]

**Story 3:** [Write a story about notifications or status updates]

---

## Checklist: Is Your Story Good?

Before adding a story to your backlog, verify:

- [ ] **Format:** Uses "As a... I want... So that..." structure
- [ ] **Specific user:** Not just "user", but which type of user?
- [ ] **Clear action:** Describes what the user can do
- [ ] **Measurable benefit:** Ties to validated pain point
- [ ] **Acceptance criteria:** 3-5 testable conditions
- [ ] **Estimable:** Team can estimate effort (1-5 days)
- [ ] **Independent:** Can be built without depending on other stories
- [ ] **Evidence:** Cites interview data supporting this story
- [ ] **Analytics:** Includes event tracking requirement (if applicable)

---

## Resources

**Further Reading:**
- "User Stories Applied" by Mike Cohn
- "Agile Estimating and Planning" by Mike Cohn
- Mountain Goat Software blog (Mike Cohn's site)

**Tools:**
- GitHub Issues (use labels for epics, sprints)
- Trello/Jira (kanban boards)
- Miro (for collaborative story mapping)

---

**Questions?** Review your interview logs. The best user stories come directly from user pain points.
