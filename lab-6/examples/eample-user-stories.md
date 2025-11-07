# User Stories: Good vs Bad Examples

**Purpose:** This document teaches you how to write effective user stories that drive product decisions and engineering work. User stories are the bridge between customer problems and technical implementation.

**When to use this:** Weeks 5-7, when translating validated problems into actionable development tasks.

---

## Table of Contents

1. [What Makes a Good User Story](#what-makes-a-good-user-story)
2. [The INVEST Criteria](#the-invest-criteria)
3. [Bad Examples (and Why)](#bad-examples-and-why)
4. [Good Examples (and Why)](#good-examples-and-why)
5. [User Story Templates](#user-story-templates)
6. [Common Mistakes](#common-mistakes)
7. [Practice Exercise](#practice-exercise)

---

## What Makes a Good User Story

A user story is NOT a feature specification. It's a **promise for a conversation** about:
- WHO needs something
- WHAT they're trying to accomplish
- WHY it matters to them

**The Standard Format:**
```
As a [type of user],
I want to [action/capability],
So that [benefit/value].
```

**But format alone doesn't make it good.** Quality comes from specificity, testability, and connection to validated user research.

---

## The INVEST Criteria

Good user stories are **INVEST**:

- **I**ndependent: Can be developed separately from other stories
- **N**egotiable: Details can be discussed; not a rigid contract
- **V**aluable: Delivers clear value to a specific user
- **E**stimable: Team can roughly size the effort
- **S**mall: Can be completed in one sprint (1-2 weeks)
- **T**estable: Clear acceptance criteria exist

We'll evaluate each example against these criteria.

---

## Bad Examples (and Why)

### ❌ Bad Example 1: Too Vague

**User Story:**
```
As a student,
I want a better study experience,
So that I can learn more effectively.
```

**Why it's bad:**
- ❌ **Not Valuable:** What does "better" mean? Unmeasurable.
- ❌ **Not Testable:** How do you know when it's "better"?
- ❌ **Not Estimable:** Team has no idea what to build
- ❌ **Not Small:** This is an entire product, not a story
- **Root problem:** No connection to specific user research insight

**What it should address:**
- Which students? (First-year? Commuters? Engineering?)
- What specific part of "study experience" are we improving?
- What does "learn effectively" mean to them?

---

### ❌ Bad Example 2: Too Technical (Feature-Focused)

**User Story:**
```
As a developer,
I want to implement a Redis caching layer,
So that database queries are faster.
```

**Why it's bad:**
- ❌ **Not Valuable to USER:** No end-user benefit articulated
- ❌ **Not Negotiable:** Prescribes the solution (Redis)
- ❌ **Wrong perspective:** Written from developer's view, not user's
- **Root problem:** This is a technical task, not a user story

**What it should be:**
User stories describe user-facing value. Technical implementation should be in acceptance criteria or technical tasks.

**Better version:**
```
As a KIU student checking study room availability,
I want to see room status update within 2 seconds,
So that I can quickly decide which building to go to without wasting time on stale data.

Technical approach: Redis caching with 30-second TTL
```

---

### ❌ Bad Example 3: Actually Multiple Stories

**User Story:**
```
As a student,
I want to find study rooms, see occupancy, reserve a spot, 
get navigation directions, and rate the room afterward,
So that I can have a complete study room experience.
```

**Why it's bad:**
- ❌ **Not Independent:** These are 5+ separate stories bundled together
- ❌ **Not Small:** Would take weeks to complete
- ❌ **Not Estimable:** Too much scope to size accurately
- **Root problem:** Confusing an epic with a story

**How to fix:**
Break into separate stories:
1. Search for available study rooms
2. View real-time occupancy of a specific room
3. Reserve a room for a time slot
4. Get walking directions to a room
5. Rate a room after using it

Each should be independent and deliverable.

---

### ❌ Bad Example 4: Missing the "Why"

**User Story:**
```
As a student,
I want to filter study rooms by capacity.
```

**Why it's bad:**
- ❌ **Not Valuable:** We don't know WHY this matters
- ❌ **Not Negotiable:** Without knowing why, we can't discuss alternatives
- **Root problem:** No connection to user pain point

**Better version:**
```
As a third-year CS student working on group projects,
I want to filter study rooms by capacity (showing 4-6 person rooms first),
So that I don't waste 10 minutes discovering a room is too small after walking there.

Evidence: 7/10 interviews mentioned finding room too small as frustration
```

---

### ❌ Bad Example 5: Solution Before Problem

**User Story:**
```
As a user,
I want push notifications for study room availability,
So that I get notified.
```

**Why it's bad:**
- ❌ **Not Valuable:** "Get notified" isn't a benefit
- ❌ **Prescriptive:** Assumes push notifications are the right solution
- **Root problem:** Describes a feature, not user need

**Better approach:**
Start with the problem, then discuss solutions:
```
As a commuter student who plans study sessions between classes,
I want to know 10 minutes before arriving if my preferred study room is occupied,
So that I can go to an alternate location instead of wasting my 30-minute break.

Potential solutions to discuss:
- Push notifications
- SMS alerts
- In-app "favorites" with status
- Shareable links with live status
```

---

### ❌ Bad Example 6: No Specific User

**User Story:**
```
As a user,
I want to search for rooms,
So that I can find what I need.
```

**Why it's bad:**
- ❌ **Not Valuable:** Every user has different needs
- ❌ **Too generic:** "User" could be anyone
- **Root problem:** No connection to your ICP (Ideal Customer Profile)

**Better version:**
```
As a KIU commuter student with a 2-hour gap between morning and afternoon classes,
I want to search study rooms by building and see which have seats available RIGHT NOW,
So that I can immediately walk to an available quiet spot without checking 3 different buildings.
```

---

## Good Examples (and Why)

### ✅ Good Example 1: Discovery-Based Story

**User Story:**
```
As a KIU commuter student with 1-2 hour gaps between classes,
I want to see which study rooms in K-building have available seats right now,
So that I don't waste 15 minutes walking to the library only to find it full.

Evidence: 8/10 interviewees described this exact scenario; average time wasted = 12-18 min per occurrence, 3x per week
```

**Why it's good:**
- ✅ **Independent:** Focused on one building's availability
- ✅ **Negotiable:** Implementation details not prescribed
- ✅ **Valuable:** Saves 15 minutes, measurable benefit
- ✅ **Estimable:** Team can size effort (API call + UI list)
- ✅ **Small:** Achievable in one sprint
- ✅ **Testable:** Clear success criteria (shows K-building rooms with current availability)
- **Includes evidence** from user research

**Acceptance Criteria:**
```
Given: I am on the home screen
When: I select "K-Building" filter
Then: I see a list of all K-building study rooms with:
  - Room number (e.g., K-201)
  - Current occupancy (e.g., "4/20 seats occupied")
  - Update timestamp (e.g., "Updated 30 seconds ago")
  - Visual indicator (red/yellow/green)
  
And: List updates every 30 seconds automatically
And: If data is stale (>2 min), show warning
```

---

### ✅ Good Example 2: Behavior-Change Focused

**User Story:**
```
As a group project team lead coordinating 4 members across different schedules,
I want to see each member's task status and blockers in one shared view,
So that I can identify who's behind and offer help during our weekly sync, instead of spending 20 minutes at the start of every meeting asking "what's your status?"

Evidence: 9/10 interviews mentioned status updates consuming 15-30 min per meeting; "shared view" mentioned by 6/10 as desired solution
```

**Why it's good:**
- ✅ **Specific user:** Team lead (not generic "student")
- ✅ **Quantified waste:** 20 minutes per meeting
- ✅ **Clear benefit:** Faster meetings, proactive help
- ✅ **Testable:** Measure meeting time reduction
- ✅ **Evidence-backed:** Cites specific interview data

**Acceptance Criteria:**
```
Given: I am logged in as team lead
When: I navigate to "Team Dashboard"
Then: I see all team members with:
  - Name and role
  - Tasks in progress (title + status)
  - Self-reported blockers (if any)
  - Last updated timestamp
  
And: Each member can update their own status
And: Dashboard shows if any member hasn't updated in 3+ days
And: I can filter by "Has Blockers" to quickly see who needs help
```

---

### ✅ Good Example 3: Mobile-First Context

**User Story:**
```
As a commuter student checking study room availability on my phone while walking from the bus stop,
I want to see room availability in under 3 seconds on a 4G connection,
So that I can decide which building to walk to without standing still and losing time.

Evidence: 10/10 interviews mentioned mobile use; 6/10 have <10 GB data plans; avg decision made while walking
```

**Why it's good:**
- ✅ **Context-specific:** Mobile, while walking, limited data
- ✅ **Performance target:** <3 seconds, testable
- ✅ **Real behavior:** Decision made in motion, not stationary
- ✅ **Small scope:** Focused on speed, not feature breadth

**Technical Implications:**
- Aggressive caching strategy
- Lightweight payload (<50 KB)
- Progressive loading (show building list first, details on tap)
- Offline mode with stale data warning

---

### ✅ Good Example 4: Integration Story

**User Story:**
```
As a CS student juggling 5 courses with group projects in 3 of them,
I want to import my team's GitHub issues into our shared task board,
So that I don't manually duplicate tasks between tools and miss important code reviews.

Evidence: 7/10 interviewees use GitHub for code; 5/10 mentioned "forgetting to check GitHub" causing delays; manual duplication cited by 4/10
```

**Why it's good:**
- ✅ **Specific integration:** GitHub (not "version control")
- ✅ **Specific pain:** Manual duplication and missed reviews
- ✅ **Measurable impact:** Task completeness and review response time
- ✅ **Negotiable:** Could discuss other integrations (GitLab, Bitbucket)

**Acceptance Criteria:**
```
Given: Team has connected GitHub repository to task board
When: A new GitHub issue is created or updated
Then: It appears in task board within 5 minutes with:
  - Issue title and description
  - Assignee (mapped to team member)
  - Labels (mapped to task categories)
  - Link back to GitHub issue
  
And: Changes in either system sync bidirectionally
And: Team members can choose which repos to sync
```

---

### ✅ Good Example 5: Accessibility-Focused

**User Story:**
```
As a visually impaired CS student using VoiceOver on iPhone,
I want to navigate the study room list and hear room status announced clearly,
So that I can independently find available study spaces without asking others for help.

Evidence: 1 interview with blind student (Nika, third-year); 2 interviews mentioned classmate with visual impairment struggling with current tools
```

**Why it's good:**
- ✅ **Specific persona:** Screen reader user on iOS
- ✅ **Dignity-focused:** "Independently" without asking for help
- ✅ **Small scope:** Focuses on screen reader support
- ✅ **Evidence from edge case:** Small n, but critical user need

**Acceptance Criteria:**
```
Given: I am using VoiceOver on iOS
When: I navigate to study room list
Then: Each room announces:
  - Building and room number
  - Occupancy status in plain language (e.g., "K-201, mostly empty, 5 of 20 seats used")
  - Freshness indicator (e.g., "updated 1 minute ago")
  
And: Navigation buttons have clear labels ("Filter rooms", "Refresh status")
And: All interactive elements are reachable via swipe gestures
And: App passes iOS Accessibility Inspector with no critical errors
```

---

### ✅ Good Example 6: Onboarding Story

**User Story:**
```
As a first-time user who just downloaded the app from a classmate's recommendation,
I want to see one example room with live occupancy data in under 10 seconds,
So that I immediately understand the value without reading instructions or creating an account.

Evidence: 12/15 users in Week 1 testing abandoned app before seeing any data; "I didn't know what it did" cited by 8/15
```

**Why it's good:**
- ✅ **Time-bound:** <10 seconds to value
- ✅ **No barriers:** Before signup/login
- ✅ **Show, don't tell:** Live example vs instructions
- ✅ **Evidence-driven:** Abandonment data from prototype testing

**Acceptance Criteria:**
```
Given: I am a first-time user (no account)
When: I open the app for the first time
Then: I immediately see:
  - One featured study room (e.g., "Main Library, K-Building")
  - Live occupancy data (e.g., "12/50 seats occupied")
  - Real-time update (e.g., count changes if room status changes)
  - One-tap CTA: "See All Rooms"
  
And: No login/signup required for this view
And: Page loads within 3 seconds on 4G
And: If data unavailable, show placeholder with "Check back soon" message
```

---

## User Story Templates

### Template 1: Standard Format
```
As a [specific user persona with context],
I want to [specific action or capability],
So that [measurable benefit or pain avoided].

Evidence: [Interview citations, quantified impact]
```

### Template 2: Job-to-be-Done Format
```
When [situation],
I want to [motivation],
So I can [expected outcome].

Evidence: [User research backing]
```

**Example:**
```
When I arrive at campus with a 2-hour gap between classes,
I want to immediately know which study rooms near my next class have available seats,
So I can go straight there without wandering or wasting my break time.
```

### Template 3: Feature + Benefit Format
```
As a [persona],
I need [capability]
Because [reason tied to validated pain point].
```

**Example:**
```
As a team lead coordinating async work,
I need to see which tasks have been idle for 3+ days
Because my team misses 30% of deadlines due to unnoticed blockers.
```

---

## Common Mistakes

### Mistake 1: Writing Stories Without User Research
**Problem:** Making up user needs instead of citing evidence.

**Fix:** Every story should trace back to:
- Interview quotes (qualitative)
- Observed behavior (ethnographic)
- Survey data (quantitative)
- Usability test findings (validation)

**Template:**
```
Evidence: 
- Interview #3 (David): "I waste 20 minutes every Tuesday..."
- Interview #7 (Mariam): "The library is always full between 2-4 PM..."
- Observation: 8/10 students we shadowed checked 2+ buildings
- Quantified: Average 15 minutes wasted, 3x per week = 45 min/week
```

---

### Mistake 2: Writing Stories from Developer Perspective

**Bad:**
```
As a developer,
I want to refactor the authentication module,
So that the code is cleaner.
```

**Good:**
```
As a student trying to access study room data during peak hours (12-2 PM),
I want to log in within 5 seconds without the app timing out,
So that I can quickly check availability and make a decision.

Technical note: Current auth latency averages 8-12 seconds at peak; refactoring auth module estimated to reduce to <3 seconds
```

---

### Mistake 3: Bundling Multiple User Needs

**Bad:**
```
As a student, I want study room availability, reservations, notifications, and navigation.
```

**Fix:** Break into separate stories with prioritization:

**Story 1 (P0 - Must Have):**
```
As a commuter, I want to see current room availability...
```

**Story 2 (P1 - Should Have):**
```
As a student planning ahead, I want to reserve a room...
```

**Story 3 (P2 - Nice to Have):**
```
As a regular user, I want notifications when my favorite room opens...
```

---

### Mistake 4: Ignoring Technical Constraints

**Problem:** Writing stories that ignore your tech stack, APIs, or data access.

**Example of avoidable issue:**
```
As a user, I want real-time occupancy updated every second.
```

**Reality check:**
- Do you have sensor access that updates every second?
- Would this drain mobile battery?
- Is sub-second accuracy actually needed?

**Better version:**
```
As a commuter making a quick decision, I want room occupancy accurate within the last 2 minutes, so my data is fresh enough to be useful but doesn't drain my phone battery.

Technical: Update every 30 seconds client-side; poll API every 60 seconds; acceptable staleness = 2 minutes
```

---

### Mistake 5: Stories Without Acceptance Criteria

**Problem:** Team doesn't know when story is "done."

**Fix:** Every story needs **Definition of Done**:

**Bad:**
```
As a student, I want to filter rooms.
```

**Good:**
```
As a student, I want to filter rooms by capacity and quietness level.

Acceptance Criteria:
[ ] Filter button visible on home screen
[ ] Tapping opens filter panel with 2 options: Capacity (slider 1-50) and Noise Level (Quiet/Moderate/Social)
[ ] Applying filter updates room list within 1 second
[ ] Filter persists across app sessions
[ ] Clear filter button resets to "All Rooms"
[ ] Works on iOS and Android
[ ] Accessible via screen readers

Done when: All criteria pass QA + demo to instructor
```

---

## Practice Exercise

### Your Turn: Convert These Problems into User Stories

You conducted interviews and found these validated problems. Write user stories for each:

#### Problem 1:
**Finding:** 9/10 CS students in group projects mentioned that they waste 30-60 minutes per week trying to figure out who's working on what because information is scattered across WhatsApp, email, and Telegram.

**Your user story:**
```
As a _______________,
I want to _______________,
So that _______________.

Evidence: _______________
```

---

#### Problem 2:
**Finding:** First-year students (6/8 interviewed) mentioned feeling confused during the first 2 weeks of each semester because they can't find syllabi, assignments, and course materials. They check 4 different places: email, LMS, professor's website, and WhatsApp groups.

**Your user story:**
```
As a _______________,
I want to _______________,
So that _______________.

Evidence: _______________
```

---

#### Problem 3:
**Finding:** International students (4/5 interviewed) mentioned they often miss campus events because announcements are only posted in Georgian on physical bulletin boards. They only learn about events after they've happened from friends.

**Your user story:**
```
As a _______________,
I want to _______________,
So that _______________.

Evidence: _______________
```

---

### Example Answers (Check After You Try)

<details>
<summary>Click to see example answers</summary>

#### Problem 1 Answer:
```
As a CS student managing 3 concurrent group projects,
I want to see all my teammates' current tasks and status in one centralized view,
So that I don't waste 30-60 minutes per week hunting for status updates across WhatsApp, email, and Telegram.

Evidence: 9/10 interviews cited scattered information; quantified time waste 30-60 min/week; top frustration mentioned in 7/10 interviews
```

#### Problem 2 Answer:
```
As a first-year student in my first 2 weeks of a new semester,
I want to access all my course syllabi and assignment lists in one searchable location,
So that I don't waste 20+ minutes per course checking 4 different platforms (email, LMS, professor sites, WhatsApp) every time I need course information.

Evidence: 6/8 first-year students interviewed; "first 2 weeks" cited as highest confusion period; average 4 platforms checked per course material search
```

#### Problem 3 Answer:
```
As an international student who doesn't read Georgian fluently,
I want to receive campus event notifications in English on my phone,
So that I can attend events instead of learning about them afterward from friends.

Evidence: 4/5 international students interviewed; "learn after it happened" mentioned by all 4; physical bulletin boards in Georgian confirmed as only announcement method
```

</details>

---

## Key Takeaways

1. **User stories are promises for conversations**, not detailed specifications.

2. **Every story must trace back to user research** - interviews, observations, or data.

3. **Format is less important than substance** - focus on WHO, WHAT, WHY with evidence.

4. **Good stories are INVEST** - Independent, Negotiable, Valuable, Estimable, Small, Testable.

5. **Write from user perspective**, not developer perspective. Technical details go in acceptance criteria.

6. **Break large epics into small stories** that can ship independently in 1-2 weeks.

7. **Include acceptance criteria** so the team knows when it's done.

8. **Specificity beats generality** - "KIU commuter student" beats "user".

---

## Checklist: Is Your User Story Ready?

Before considering a story "ready for development," verify:

- [ ] Traces back to specific user research (interview #, quote, observation)
- [ ] Specifies a clear user persona (not generic "user")
- [ ] Describes user benefit, not technical implementation
- [ ] Can be completed in one sprint (1-2 weeks)
- [ ] Has measurable acceptance criteria
- [ ] Team can estimate effort (if not, too vague)
- [ ] Delivers value if shipped alone (not dependent on 5 other stories)
- [ ] Has been reviewed and understood by entire team

---

**Remember:** The best user stories come from deep customer understanding. If you can't write a good user story, you might not understand your users well enough yet. Go back and do more interviews.

**Next Steps:**
- Review your interview synthesis
- Identify top 3 pain points
- Write one user story for each
- Review with your team
- Add acceptance criteria
- Size the effort
- Start building!
