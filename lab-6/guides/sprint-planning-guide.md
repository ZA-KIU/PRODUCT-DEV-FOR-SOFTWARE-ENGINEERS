# Sprint Planning Best Practices

**Purpose:** Learn how to run effective sprint planning sessions and avoid common pitfalls

---

## What Is Sprint Planning?

**Sprint planning** is a ceremony at the start of each sprint where the team:
1. Agrees on the sprint goal
2. Selects user stories from the backlog
3. Breaks stories into tasks
4. Estimates effort
5. Assigns owners
6. Commits to the sprint

**Duration:** 1 hour for a 2-week sprint  
**Attendees:** Full team (required)  
**Output:** Sprint plan document with committed stories and tasks

---

## The Sprint Planning Agenda (60 Minutes)

### Part 1: Sprint Goal (10 minutes)

**What:** Define the ONE thing this sprint must accomplish

**Bad Sprint Goal:**
- "Complete US-001, US-002, US-003, US-004" (just a list of stories)
- "Work on the dashboard" (too vague)

**Good Sprint Goal:**
- "By end of Sprint 1, users can view all their tasks from multiple sources on a unified dashboard"
- "By end of Sprint 2, users receive real-time notifications when teammates update tasks"

**How to Create:**
1. Look at sprint stories
2. Ask: "What user capability do these stories collectively enable?"
3. Write it in one sentence
4. Read aloud, ensure team understands

**Why It Matters:**
- Gives team clarity on what success looks like
- Helps with prioritization during sprint if things go wrong
- Makes sprint review more focused

---

### Part 2: Story Walkthrough (30 minutes)

**For each story in the sprint:**

**Step 1: Read Story Aloud (2 min per story)**
- Read the "As a... I want... So that..." statement
- Read acceptance criteria
- Ask: "Does everyone understand what we're building?"

**Step 2: Clarify Acceptance Criteria (3 min)**
- Are criteria specific enough to test?
- Any edge cases missing?
- Do we need to add/remove criteria?

**Step 3: Break Into Tasks (5 min)**
- Ask: "What technical work is needed?"
- Brainstorm tasks (frontend, backend, testing, analytics)
- Write tasks down (1 per sticky note or GitHub issue)

**Step 4: Estimate Hours (2 min)**
- Each task: 1-5 hours (if more, break it down)
- Use past experience
- When unsure, add 50% buffer

**Repeat for all stories in sprint (typically 5-8 stories)**

**Timebox Tip:** If you have 6 stories and 30 min, spend 5 min per story. Use a timer.

---

### Part 3: Capacity Check (10 minutes)

**Step 1: Calculate Team Capacity**

```
Available Hours per Person:
= Hours/week × Number of weeks
= 15 hours/week × 2 weeks
= 30 hours per person

Team Capacity (4 people):
= 30 hours × 4 people
= 120 hours

Buffer for unknowns (20%):
= 120 hours × 0.20
= 24 hours

Net Capacity:
= 120 - 24
= 96 hours available for sprint
```

**Step 2: Sum Task Hours**

Add up all task hours across all stories:
- US-001: 13 hours
- US-002: 11 hours
- US-003: 15 hours
- US-004: 12 hours
- US-005: 18 hours
- US-006: 14 hours
- **Total:** 83 hours

**Step 3: Capacity Check**

✅ **PASS:** 83 hours ≤ 96 hours capacity  
❌ **FAIL:** If total > 96 hours, need to descope

**If you fail capacity check:**
- Remove lowest-priority story (move to Sprint 2)
- OR reduce scope of a story (move some acceptance criteria to "nice to have")
- OR ask: Did we overestimate? Can we pair program to be more efficient?

---

### Part 4: Task Assignment (10 minutes)

**Step 1: Match Skills to Tasks**
- Backend tasks → Backend Lead (+ backup)
- Frontend tasks → Frontend Lead (+ backup)
- Analytics tasks → Analytics Lead
- Cross-functional tasks → Pair programming

**Step 2: Balance Load**
- Aim for 20-25 hours per person
- No one should have >30 hours (leaves no buffer)
- No one should have <10 hours (underutilized)

**Step 3: Identify Pair Programming Opportunities**
- Complex tasks (>5 hours)
- New technology
- Tasks requiring cross-functional knowledge

**Step 4: Write Names on Tasks**
- Each task has an owner (primary) and backup
- If task blocked, backup can jump in

---

## Sprint Planning Anti-Patterns (What NOT to Do)

### Anti-Pattern 1: No Clear Sprint Goal

**Problem:**
Team commits to stories but doesn't know what they're collectively building toward.

**Consequence:**
- Team loses focus during sprint
- Can't make prioritization decisions when blocked
- Sprint review feels disjointed

**Solution:**
Always start sprint planning with: "What's the ONE thing we must accomplish?"

---

### Anti-Pattern 2: Overcommitting ("We Can Do It All!")

**Problem:**
Team commits to 120 hours of work with only 80 hours capacity.

**Consequence:**
- Team burns out
- Stories incomplete at end of sprint
- Technical debt (rushed, buggy code)
- Morale drops

**Solution:**
- Calculate capacity FIRST
- Use 20% buffer for unknowns
- When in doubt, commit to less
- Better to finish 5 stories than partially complete 8

**Remember:** Velocity improves over time. Sprint 1 is for learning, not heroics.

---

### Anti-Pattern 3: Vague Tasks ("Work on the API")

**Problem:**
Task is too large or vague to estimate or assign.

**Consequence:**
- No one knows who should do it
- No one knows when it's done
- Gets stuck in "In Progress" for entire sprint

**Solution:**
Break tasks into specific, concrete units:
- ❌ "Work on API"
- ✅ "Create GET /api/tasks endpoint"
- ✅ "Add authentication middleware to API"
- ✅ "Write unit tests for task endpoints"

**Rule:** Each task should be completable in a single work session (1-5 hours).

---

### Anti-Pattern 4: Not Identifying Dependencies

**Problem:**
Team commits to stories without realizing Story B depends on Story A.

**Consequence:**
- Developer blocked waiting for other work
- Parallel work impossible
- Sprint slows down

**Solution:**
During task breakdown, ask:
- "What needs to be done first?"
- "Does this task depend on anything?"
- Document dependencies in sprint plan
- Order tasks: dependencies first, dependent tasks later

---

### Anti-Pattern 5: Ignoring Carryover Work

**Problem:**
Team has unfinished stories from last sprint but doesn't account for them.

**Consequence:**
- Overcommitting (again)
- Old stories never get done
- Velocity calculation inaccurate

**Solution:**
- List carryover stories FIRST
- Estimate remaining work (not original estimate)
- Subtract from capacity
- THEN add new stories

**Example:**
```
Sprint 2 Capacity: 96 hours
Carryover from Sprint 1:
- US-006: 8 hours remaining
Net Capacity for New Stories: 96 - 8 = 88 hours
```

---

## Capacity Planning Deep Dive

### How to Calculate Individual Capacity

**Formula:**
```
Individual Capacity = (Hours/day available) × (Days in sprint) × (Focus factor)
```

**Example:**

**Person A:**
- Available: 2 hours/day on weekdays, 4 hours/day on weekends
- Sprint duration: 2 weeks = 10 weekdays + 4 weekend days
- Calculation: (2h × 10) + (4h × 4) = 20 + 16 = 36 hours
- Focus factor (80%): 36 × 0.8 = ~29 hours net capacity

**Focus factor** accounts for:
- Meetings (standups, planning, review, retro)
- Context switching
- Unexpected interruptions
- Code reviews
- Helping teammates

**Typical focus factors:**
- 100%: Unrealistic (no interruptions, no meetings)
- 80%: Ideal (some meetings, some reviews)
- 60%: Typical (busy schedule, many interruptions)
- 40%: Red flag (too many commitments, reconsider)

---

### Team Capacity Adjustments

**Adjust capacity for:**

**Week 9 (Midterm):** -50% capacity
- Example: Normally 15 hours/week → 7-8 hours

**Holidays/Exams:** -30-50% depending on impact

**New Team Member:** -20% for first sprint (learning curve)

**Sick Leave (Planned):** -100% for that person

---

## Velocity Tracking

**Velocity** = Amount of work completed per sprint (in story points or hours)

**Why track velocity?**
- Helps predict future capacity
- Improves estimation over time
- Indicates if team is improving

**How to calculate:**

**Sprint 1:**
- Committed: 80 hours
- Completed: 70 hours
- Velocity: 70 hours

**Sprint 2 Planning:**
- Use Sprint 1 velocity as baseline
- Commit to ~70 hours (or slightly more if confidence high)

**After 3 sprints, calculate average:**
```
Average Velocity = (Sprint 1 + Sprint 2 + Sprint 3) / 3
                 = (70 + 75 + 80) / 3
                 = 75 hours average
```

Use average velocity to plan future sprints.

---

## Task Breakdown Techniques

### Technique 1: Frontend-Backend Split

**Story:** "As a user, I want to see my task dashboard."

**Tasks:**
- **Backend:**
  - Create database schema for tasks table
  - Build GET /api/tasks endpoint
  - Add authentication middleware
  - Write unit tests for endpoint
- **Frontend:**
  - Create TaskDashboard React component
  - Fetch tasks from API
  - Display tasks in table format
  - Add loading and error states
- **Analytics:**
  - Instrument Dashboard_Viewed event
- **Testing:**
  - Manual testing on mobile
  - User testing with 1 person

---

### Technique 2: User Flow Breakdown

**Story:** "As a user, I want to sign up for the app."

**Tasks (in order of user flow):**
1. Create sign-up form UI (email, password fields)
2. Add form validation (email format, password strength)
3. Create POST /api/signup endpoint
4. Hash password and save user to database
5. Send confirmation email
6. Implement email verification flow
7. Add analytics: Signup_Started, Signup_Completed
8. Write tests for signup flow

---

### Technique 3: Happy Path + Edge Cases

**Story:** "As a user, I want to assign a task to a teammate."

**Tasks:**
- **Happy Path:**
  - Add "Assign" button to task
  - Show teammate dropdown
  - Update task with assigned teammate
  - Send notification to assigned teammate
- **Edge Cases:**
  - Handle case: No teammates available (show message)
  - Handle case: Task already assigned (allow reassignment)
  - Handle case: Teammate doesn't have permission (error message)

---

## Effective Sprint Planning Tips

### Tip 1: Do Pre-Planning

**Before sprint planning meeting:**
- Groom backlog (ensure stories meet Definition of Ready)
- Ensure acceptance criteria are clear
- Identify obvious dependencies
- Tech Lead reviews technical feasibility

**In the meeting:**
- Focus on commitment and task breakdown
- Don't waste time clarifying vague stories (those should be in backlog grooming)

---

### Tip 2: Use Timeboxes

**60-minute sprint planning:**
- Sprint goal: 10 min (strict)
- Story walkthrough: 30 min (5 min per story)
- Capacity check: 10 min
- Task assignment: 10 min

**Use a visible timer.** When time's up, move on.

---

### Tip 3: Visualize with a Board

**Physical or Digital Kanban:**
- Backlog → To Do → In Progress → In Review → Done

**During planning:**
- Move committed stories from Backlog → To Do
- Attach task cards to each story
- Assign names to tasks

---

### Tip 4: Ask "What If?" Questions

**Risk Planning:**
- "What if the API takes 2x longer than estimated?"
- "What if we can't get API access to WhatsApp?"
- "What if [Team Member] is sick Week 2?"

**Document mitigation:**
- "If API takes longer, we'll use mock data and move real integration to Sprint 2"
- "If no WhatsApp API, we'll manually import messages as CSV"
- "If [Name] sick, [Backup] takes over their tasks"

---

### Tip 5: Don't Forget Non-Dev Work

**Include in sprint hours:**
- Sprint ceremonies: 2-3 hours (planning, review, retro)
- Daily standups: 1 hour total (10 min × 6 days)
- Code reviews: 3-5 hours
- User testing: 2-3 hours
- Buffer for unknowns: 20% of total

**Example:**
```
Total capacity: 120 hours
- Ceremonies: 3 hours
- Standups: 1 hour
- Code reviews: 4 hours
- User testing: 2 hours
- Buffer (20%): 24 hours
= 34 hours overhead
Net capacity for dev tasks: 86 hours
```

---

## Sprint Planning Checklist

**Before the Meeting:**
- [ ] Backlog groomed (stories have acceptance criteria)
- [ ] Previous sprint retrospective action items reviewed
- [ ] Team knows their individual availability for upcoming sprint
- [ ] Tech Lead reviewed technical feasibility of top stories

**During the Meeting:**
- [ ] Sprint goal defined and agreed upon
- [ ] Stories reviewed and clarified
- [ ] Stories broken into tasks (each 1-5 hours)
- [ ] Task hours estimated
- [ ] Total hours ≤ team capacity
- [ ] Tasks assigned to owners (with backups)
- [ ] Dependencies identified
- [ ] Risks discussed and mitigated
- [ ] Team commits to sprint plan

**After the Meeting:**
- [ ] Sprint plan document updated and committed to GitHub
- [ ] Tasks added to GitHub Projects board
- [ ] Sprint goal posted in team Slack channel
- [ ] Calendar invites sent for sprint ceremonies

---

## Common Questions

### Q: What if we finish early?

**A:** Great problem to have! Options:
1. Pull highest-priority story from Sprint 2
2. Add polish (improve UI, add tests, refactor)
3. Tackle technical debt
4. Extra user testing

**Don't:** Just mark sprint complete and stop working. Use the time productively.

---

### Q: What if we're behind midweek?

**A:** During Wednesday check-in:
1. Identify what's blocked or delayed
2. Ask: Can we unblock it?
3. If not, which stories can we descope or defer?
4. Move low-priority tasks to Sprint 2
5. Focus on sprint goal (not completing every story)

**Remember:** It's better to fully complete 4 stories than partially complete 6.

---

### Q: How do we handle bugs found during sprint?

**A:** Two options:

**Option 1: Bug in current sprint work**
- Fix immediately (part of Definition of Done)
- Include bug fix time in task estimates

**Option 2: Bug in old sprint work (P1 or below)**
- Log as GitHub issue
- Add to backlog for next sprint
- Only fix immediately if P0 (critical, blocks users)

---

### Q: Can we change the sprint plan mid-sprint?

**A:** Yes, but carefully:
- **Add work:** Only if team finished early and has capacity
- **Remove work:** Yes, if blocked or behind schedule (discuss in midweek check-in)
- **Swap stories:** Rarely. Only if new priority emerges (discuss with full team)

**Avoid:** Constantly changing scope. It indicates poor planning or unclear priorities.

---

## Sprint Planning Smells (Red Flags)

**🚩 Red Flag 1:** Sprint planning takes >90 minutes
- **Cause:** Stories aren't ready (no acceptance criteria, too vague)
- **Fix:** Do backlog grooming before sprint planning

**🚩 Red Flag 2:** Team argues about estimates for >5 minutes per task
- **Cause:** Lack of shared understanding or experience
- **Fix:** Use relative sizing (story points), not absolute hours

**🚩 Red Flag 3:** One person has 40 hours, another has 10 hours
- **Cause:** Imbalanced assignment
- **Fix:** Redistribute tasks, use pair programming

**🚩 Red Flag 4:** "We can fit one more story..." (overcommitting)
- **Cause:** Optimism bias, lack of buffer
- **Fix:** Stick to capacity calculation, always leave 20% buffer

**🚩 Red Flag 5:** No one wants to commit to the sprint plan
- **Cause:** Sprint goal unclear, stories too vague, or unrealistic scope
- **Fix:** Clarify sprint goal, refine stories, or reduce scope

---

## Resources

**Books:**
- "Agile Estimating and Planning" by Mike Cohn
- "Scrum: The Art of Doing Twice the Work in Half the Time" by Jeff Sutherland

**Tools:**
- GitHub Projects (free, integrated with code)
- Jira (enterprise-grade, complex)
- Trello (simple, visual)
- Miro (collaborative, great for remote teams)

**Templates:**
- Sprint planning template in this lab folder
- Sprint retrospective template (upcoming labs)

---

**Key Takeaway:** Sprint planning is about commitment, not wishful thinking. Be honest about capacity, conservative in estimates, and ruthless in prioritization.
