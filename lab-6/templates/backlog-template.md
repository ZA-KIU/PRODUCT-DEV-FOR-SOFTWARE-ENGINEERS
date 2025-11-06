# Product Backlog (User Stories)

**Team:** [Your Team Name]  
**Date Created:** [Date]  
**Last Updated:** [Date]

---

## What Is a Product Backlog?

Your **product backlog** is a prioritized list of all user stories for your MVP. It's your single source of truth for "what needs to be built."

**Key Principles:**
- Stories are prioritized using MoSCoW (Must/Should/Could/Won't)
- Each story follows the format: "As a [user], I want [action], so that [benefit]"
- Each story has clear acceptance criteria
- Stories are small enough to complete in 1-5 days
- Stories are sorted by priority (highest first)

---

## Backlog Statistics

**Total Stories:** [X]
- Must Have: [Y] stories
- Should Have: [Z] stories
- Could Have: [A] stories
- Won't Have (This Time): [B] stories

**Sprint Allocation:**
- Sprint 1 (Weeks 7-8): [X] stories
- Sprint 2 (Weeks 9-10): [Y] stories
- Sprint 3 (Weeks 11-12): [Z] stories
- Future/Backlog: [A] stories

---

## Must Have Stories (Priority 1)

*These are CRITICAL for MVP. Product doesn't work without them.*

---

### Story ID: US-001

**Epic:** [Epic Name]  
**Priority:** Must Have  
**Sprint:** Sprint 1  
**Status:** Not Started  
**Assigned To:** [Team Member]

#### User Story

```
As a [type of user],
I want to [perform some action],
So that [I can achieve some goal/benefit].
```

#### Why This Matters (Evidence)
[Cite interview evidence. Which pain point does this address? How many interviewees mentioned this?]

Example: "8 out of 10 interviewees (80%) mentioned the pain of checking multiple tools. Interview #3 quote: 'I waste 20 minutes every morning just figuring out what my tasks are.'"

#### Acceptance Criteria

**Definition of Done (must be observable and testable):**

- [ ] **Criteria 1:** [Specific, testable condition]
- [ ] **Criteria 2:** [Specific, testable condition]
- [ ] **Criteria 3:** [Specific, testable condition]
- [ ] **Criteria 4 (Analytics):** [Event tracked correctly]

**Example:**
- [ ] Dashboard loads and displays all tasks for logged-in user
- [ ] Tasks show status (To Do / In Progress / Done)
- [ ] Page loads in under 2 seconds
- [ ] Task_Dashboard_Viewed event fires on page load

#### Estimated Effort
**Story Points:** [1, 2, 3, 5, 8, 13] or **Hours:** [X hours]

#### Dependencies
- [ ] [Technical dependency, e.g., "User authentication must work"]
- [ ] [Design dependency, e.g., "Dashboard mockup approved"]
- [ ] [Data dependency, e.g., "Database schema created"]

#### Analytics Events
**Which events need to be tracked for this story?**
- `[Event_Name]` - Fires when [trigger condition]
- `[Event_Name]` - Fires when [trigger condition]

#### Notes / Questions
[Any open questions, technical concerns, or clarifications needed]

---

### Story ID: US-002

**Epic:** [Epic Name]  
**Priority:** Must Have  
**Sprint:** Sprint 1  
**Status:** Not Started  
**Assigned To:** [Team Member]

#### User Story

```
As a [type of user],
I want to [perform some action],
So that [I can achieve some goal/benefit].
```

#### Why This Matters (Evidence)
[Cite interview evidence]

#### Acceptance Criteria

- [ ] **Criteria 1:** 
- [ ] **Criteria 2:** 
- [ ] **Criteria 3:** 
- [ ] **Criteria 4 (Analytics):**

#### Estimated Effort
**Story Points:** [1-13] or **Hours:** [X hours]

#### Dependencies
- [ ] [Dependency 1]

#### Analytics Events
- `[Event_Name]` - [When it fires]

#### Notes / Questions

---

### Story ID: US-003

[Repeat structure for each Must Have story]

---

### Story ID: US-004

[Continue for all Must Have stories...]

---

## Should Have Stories (Priority 2)

*Important but not critical for MVP launch. Include if time permits in Sprint 2-3.*

---

### Story ID: US-010

**Epic:** [Epic Name]  
**Priority:** Should Have  
**Sprint:** Sprint 2 or 3  
**Status:** Not Started  
**Assigned To:** [Team Member]

#### User Story

```
As a [type of user],
I want to [perform some action],
So that [I can achieve some goal/benefit].
```

#### Why This Matters (Evidence)
[Cite interview evidence. This should still address a validated pain, just less critical.]

#### Acceptance Criteria

- [ ] **Criteria 1:** 
- [ ] **Criteria 2:** 
- [ ] **Criteria 3:** 

#### Estimated Effort
**Story Points:** [1-13] or **Hours:** [X hours]

#### Dependencies
- [ ] [Dependency 1]

#### Analytics Events
- `[Event_Name]` - [When it fires]

#### Notes / Questions

---

### Story ID: US-011

[Repeat structure for each Should Have story]

---

## Could Have Stories (Priority 3)

*Nice to have. Only if Sprint 1-2 finish early AND you have extra capacity in Sprint 3.*

---

### Story ID: US-020

**Epic:** [Epic Name]  
**Priority:** Could Have  
**Sprint:** Sprint 3 (if time permits)  
**Status:** Not Started  
**Assigned To:** Unassigned

#### User Story

```
As a [type of user],
I want to [perform some action],
So that [I can achieve some goal/benefit].
```

#### Why This Matters (Evidence)
[Optional: Cite if evidence exists, but it's okay if this is lower priority]

#### Acceptance Criteria

- [ ] **Criteria 1:** 
- [ ] **Criteria 2:** 

#### Estimated Effort
**Story Points:** [1-13] or **Hours:** [X hours]

#### Notes / Questions
[Note: "Only build if Sprint 1-2 complete ahead of schedule"]

---

### Story ID: US-021

[Repeat structure for each Could Have story]

---

## Won't Have (This Time) - Priority 4

*Out of scope for 8-week capstone. Log these for future iterations or post-course work.*

---

### Story ID: US-030

**Epic:** [Epic Name]  
**Priority:** Won't Have  
**Future Consideration:** Yes / No

#### User Story

```
As a [type of user],
I want to [perform some action],
So that [I can achieve some goal/benefit].
```

#### Why Deprioritized
[Explain why this isn't in MVP scope. Examples: too complex, low ROI, technical constraints, time constraints]

#### Notes for Future
[Any ideas or considerations if this gets built post-capstone]

---

### Story ID: US-031

[Repeat for each Won't Have story]

---

## Backlog Prioritization Rationale

**How we decided priority:**

1. **Must Have Criteria:**
   - Solves a pain point mentioned by 8+ interviewees
   - Critical for core product functionality
   - High impact on North Star metric
   - Technically feasible in 2-week sprint

2. **Should Have Criteria:**
   - Solves a pain point mentioned by 5-7 interviewees
   - Enhances core functionality but not critical
   - Medium impact on North Star metric
   - Realistic for Sprint 2-3 if Sprint 1 on track

3. **Could Have Criteria:**
   - Mentioned by < 5 interviewees OR
   - "Nice to have" enhancement OR
   - Lower impact on North Star OR
   - High technical complexity (risk)

4. **Won't Have Criteria:**
   - Out of technical scope for 8 weeks
   - Doesn't address validated pain point
   - Requires resources/access we don't have
   - Can be added post-capstone

---

## Story Estimation Guide

**How we estimate effort:**

**Story Points (Fibonacci):**
- **1 point:** Trivial (1-2 hours) - e.g., change button color
- **2 points:** Simple (3-4 hours) - e.g., add new API endpoint
- **3 points:** Moderate (1 day) - e.g., new React component with state
- **5 points:** Complex (2-3 days) - e.g., database integration + UI
- **8 points:** Very complex (3-5 days) - e.g., real-time sync feature
- **13 points:** Epic-level (1 week+) - **BREAK THIS DOWN**

**Rule:** If a story is 13 points, it's too big. Split it into 2-3 smaller stories.

---

## Sprint Allocation Summary

### Sprint 1 (Weeks 7-8): Foundation
**Goal:** Build core MVP feature #1 that solves biggest pain point

**Stories:** US-001, US-002, US-003, US-004, US-005, US-006  
**Total Points:** [X] points or [Y] hours  
**Capacity:** [Z] hours (team of 4 × 20 hours/person = 80 hours)  
**Buffer:** [A]% (recommended: 20%)

### Sprint 2 (Weeks 9-10): Expansion
**Goal:** Add feature #2 and integrate with analytics
**Note:** Week 9 = Midterm, reduced capacity

**Stories:** US-007, US-008, US-009, US-010, US-011  
**Total Points:** [X] points or [Y] hours  
**Capacity:** [Z] hours (reduced due to midterm)  
**Buffer:** [A]%

### Sprint 3 (Weeks 11-12): Polish
**Goal:** Refinement, analytics dashboard, and any Should-Have stories

**Stories:** US-012, US-013, US-014, US-015  
**Total Points:** [X] points or [Y] hours  
**Capacity:** [Z] hours  
**Buffer:** [A]%

---

## Connection to Analytics (Event Schema)

**How stories map to your event schema from Week 5:**

| Story ID | Event(s) Tracked | AARRR Stage | Purpose |
|----------|------------------|-------------|---------|
| US-001 | Dashboard_Viewed | Activation | Track initial engagement |
| US-002 | Task_Created | Activation | Core value delivery |
| US-003 | Task_Completed | Retention | Measure repeat usage |
| US-004 | Share_Clicked | Referral | Viral growth |
| ...    | ...              | ...         | ... |

---

## Story Lifecycle & Status Tracking

**Story Status Flow:**
1. **Not Started** → Initial state
2. **In Progress** → Someone is actively working on it
3. **In Review** → PR submitted, awaiting review
4. **Done** → Merged, acceptance criteria met, deployed

**Update this backlog weekly** as stories progress through sprints.

---

## Team Review & Commitment

**Team members have reviewed and committed to this backlog:**

- [ ] [Team Member 1] - I understand my assigned stories and accept capacity allocation
- [ ] [Team Member 2] - I understand my assigned stories and accept capacity allocation
- [ ] [Team Member 3] - I understand my assigned stories and accept capacity allocation
- [ ] [Team Member 4] - I understand my assigned stories and accept capacity allocation

**Date of Team Agreement:** [Date]

**Instructor Feedback:** [Leave blank for instructor]

---

## Backlog Grooming Notes

**Date Last Groomed:** [Date]  
**Changes Made:** [What changed and why]  
**Next Grooming:** [Date of next backlog review]

---

**File Location:** `/03-build/user-stories/backlog.md`  
**Created:** [Date]  
**Last Updated:** [Date]  
**Version:** 1.0
