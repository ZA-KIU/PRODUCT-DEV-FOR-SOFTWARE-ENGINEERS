# Sample Problem Statement

**NOTE TO STUDENTS:** This is an example showing what a well-written problem statement looks like. Your problem will be different, but the level of detail and structure should be similar.

## Problem Title

Group Project Coordination Chaos

## Problem Description

### The Problem (1-2 sentences)

Computer Science students struggle to effectively coordinate multi-person group projects across multiple courses, leading to duplicated work, missed contributions, unclear task ownership, and last-minute scrambles before deadlines.

### Who Experiences It

**Specific user segment:**
Second- and third-year Computer Science students at KIU taking 3 or more courses with group project components (typically Database Systems, Software Engineering, Operating Systems, Web Development).

**NOT:** All students (too broad)  
**NOT:** First-year students (they typically have fewer group projects)  
**NOT:** Students in other majors (different project structures and tools)

### When/Where Does It Occur

**Context - When:**
- Throughout the semester but especially critical during midterm (weeks 6-8) and final project periods (weeks 13-15)
- Most acute 2-4 days before project deadlines
- During async coordination (not in-person meetings, but when trying to work independently)

**Context - Where:**
- Across multiple communication channels (WhatsApp groups, email, occasional in-person conversations)
- When working remotely or at different locations
- When team members have different schedules and can't meet synchronously

---

## Why It Matters

### Pain Level

**HIGH** (7-8/10)

**Evidence:**
- Students report spending 2-4 hours per week just on coordination overhead (not actual project work)
- Multiple students describe feeling "stressed" and "frustrated" specifically about coordination
- Common to hear phrases like "I don't know what others are doing" or "We're doing duplicate work"
- Last-minute scrambles are the norm, not the exception

### Frequency

**Very High** - This problem occurs:
- Multiple times per week during active project phases
- Affects 3-5 different projects simultaneously (across different courses)
- Compounds throughout semester as project deadlines overlap

**Calculation:**
If a student has 3 courses with group projects, and each project has coordination issues 2-3 times per week, that's 6-9 coordination pain points per week × 15 weeks = 90-135 instances per semester.

### Consequences

**Academic Impact:**
- Lower project grades due to poor integration of individual work
- Incomplete submissions because someone's contribution wasn't integrated
- Unequal workload distribution (some do more, others do less)
- Team conflicts affecting all members' grades

**Time Impact:**
- 2-4 hours per week wasted on coordination overhead
- Last-minute all-nighters because coordination delays pushed actual work to deadline
- Time wasted redoing work that was duplicated or misaligned

**Stress/Mental Impact:**
- High stress and anxiety about "what is everyone else doing?"
- Frustration with team members (even when they're trying their best)
- Resentment when workload feels unequal
- Dread of group projects (vs excitement about collaborative learning)

**Learning Impact:**
- Less actual learning because time spent coordinating instead of building
- Poorer quality final products
- Negative associations with teamwork and collaboration

**Most Significant Consequence:**
Students spend more time coordinating work than actually doing work, resulting in worse learning outcomes and higher stress levels.

---

## Current Solutions

### What People Do Now

**Primary solution:** Multiple disconnected tools
- WhatsApp for quick communication
- Google Drive for document sharing
- GitHub for code (some teams)
- Occasional in-person meetings
- Text messages for urgent items
- Email for formal communication with professor

**Backup solution:** Last-minute heroics
- One person (usually the same person) consolidates everything 12-24 hours before deadline
- Frantically messaging everyone "Where's your part?"
- Working through the night to integrate mismatched contributions

**Common workaround:** Divide and pray
- Divide work at beginning
- Everyone works independently
- Hope it all fits together at the end (spoiler: it often doesn't)

### Gaps in Current Solutions

**WhatsApp problems:**
- Messages get buried quickly
- Hard to track what's been decided vs what's just discussion
- No visibility into who's actually working on what
- Difficult to find information later ("What did we decide about the database schema?")

**Google Drive problems:**
- Version confusion (multiple people editing simultaneously)
- No clear structure for organizing project files
- Hard to see progress or status
- Comments and suggestions get lost

**GitHub problems:**
- Not everyone comfortable with Git
- Doesn't help with non-code coordination (planning, design, documentation)
- Many teams don't use it at all

**In-person meetings problems:**
- Hard to schedule when everyone has different timetables
- Meetings often unproductive without clear agendas
- Decisions made in meetings forgotten later

**The fundamental gap:**
There's no single source of truth for:
- Who is doing what
- What has been completed
- What decisions have been made
- What's blocking progress
- When things are due

---

## Evidence

### What Makes You Think This is Real?

**Personal Experience:**
- I (problem author) am currently experiencing this in 3 group projects
- Spent 3 hours last week just trying to figure out status of everyone's work
- Missed a deadline contribution because I didn't know it was my responsibility

**Observed Evidence:**
- Overheard 6+ conversations in library study area about "group project chaos"
- Common complaint in class WhatsApp groups
- Students regularly asking "Has anyone started the X part?" at last minute

**Social Validation:**
- Posted in KIU CS student group: "Anyone else struggling with group project coordination?" → 23 reactions and 14 comments agreeing
- Multiple friends independently complained about this in past 2 weeks

### Initial Observations

**Quotes overheard/collected:**

1. "I have no idea what my teammates are doing until the day before it's due." - Third-year student in library, Oct 1

2. "We have 5 different WhatsApp conversations about the same project and I can't keep track." - Classmate in Database Systems, Sept 28

3. "I spent 2 hours redoing work because I didn't know someone else already did it." - Friend, Sept 25

4. "Our team uses WhatsApp, Google Drive, GitHub, and email. It's a mess." - Student in cafeteria, Oct 2

**Patterns observed:**
- Students checking multiple apps/tools frantically before class
- Last-minute panic messages in class group chats
- Complaints about "free riders" (but often it's coordination failure, not laziness)
- One person doing disproportionate "manager" work

---

## Feasibility Assessment

### Technical Feasibility

**Can we build something in 8-10 weeks?** YES

**MVP concept:**
A simple web app that combines:
- Task board (who's doing what)
- Lightweight chat/updates (not trying to replace WhatsApp, just project-specific)
- File organization (links to Google Drive/GitHub, not trying to replace them)
- Decision log (record what was decided and when)
- Deadline tracking

**Technical requirements:**
- Frontend: React or Vue (we know this)
- Backend: Node.js/Express or Python/FastAPI (we know this)
- Database: PostgreSQL or MongoDB (we know this)
- Auth: Simple email/password, maybe Google OAuth
- Hosting: Can use free tiers (Vercel, Render, etc.)

**Technical feasibility:** HIGH - All required skills are within our current capabilities or easily learnable.

### Access to Users

**Can we find 10+ people at KIU?** YES, EASILY

**Where to find them:**
1. Our own classmates (second and third-year CS)
2. Database Systems class (60+ students, all have group projects)
3. Software Engineering class (50+ students, all have group projects)
4. Web Development class (40+ students, all have group projects)
5. KIU CS student WhatsApp group (200+ members)
6. Library study areas (students actively working on group projects)

**Access feasibility:** VERY HIGH - We can easily find 20-30+ people experiencing this problem.

---

## Initial Ideas (Optional)

**Hypothesis for solution:**
A lightweight project coordination tool specifically designed for student group projects that provides:
- Single source of truth for task status
- Easy way to update "I'm working on X"
- Quick decision logging
- Deadline awareness
- Low friction (easier than current multi-tool chaos)

**Key design principles (hypotheses to test):**
- Must be simpler than setting up Trello/Asana (too complex for small projects)
- Must integrate with, not replace, WhatsApp and Google Drive (students won't abandon those)
- Must work on mobile (students check on phones constantly)
- Must require minimal "management" overhead (no one wants to be project manager)
- Must show progress visually (reduces "what's everyone doing?" anxiety)

**NOT trying to build:**
- A full project management tool (Jira, Asana clone)
- A communication tool (WhatsApp replacement)
- A file storage tool (Google Drive replacement)

**What we are building:**
The thin layer of coordination that's currently missing between all those tools.

---

**Created By:** Nino Beridze  
**Date:** October 3, 2025  
**Version:** 1.0

**Notes:** This problem was validated through 3 initial conversations and observation over 2 weeks. Need to conduct formal interviews to validate severity and understand root causes more deeply.
