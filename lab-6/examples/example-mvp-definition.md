# MVP Definition & Scope Justification
# Case Study: StudySpot v1.0

**Purpose:** This document teaches you how to define a Minimum Viable Product (MVP) with clear justification for what's included and excluded. An MVP is NOT "all features done poorly" - it's "the minimum set of features to test your core hypothesis."

**When to use this:** Week 5-6, after problem validation but before prototyping begins.

---

## Table of Contents

1. [What is an MVP?](#what-is-an-mvp)
2. [Common MVP Mistakes](#common-mvp-mistakes)
3. [The MVP Definition Framework](#the-mvp-definition-framework)
4. [Case Study: StudySpot MVP](#case-study-studyspot-mvp)
5. [Feature Prioritization Matrix](#feature-prioritization-matrix)
6. [Scope Justification Template](#scope-justification-template)
7. [When to Pivot vs Persevere](#when-to-pivot-vs-persevere)

---

## What is an MVP?

### The Official Definition

**Minimum Viable Product (MVP):** The smallest version of your product that allows you to test your core value hypothesis with real users and learn from their behavior.

### What an MVP is NOT

❌ **NOT:** A crappy version of your final product  
❌ **NOT:** All planned features with bugs  
❌ **NOT:** A prototype with no user testing  
❌ **NOT:** Something you're embarrassed to show users  

### What an MVP IS

✅ **IS:** The fastest path to testing your riskiest assumption  
✅ **IS:** A fully functional subset of features  
✅ **IS:** Good enough to charge money (if monetization is core hypothesis)  
✅ **IS:** Something you can iterate on based on real usage data  

---

### The MVP Mindset

**Key Question:** *"What's the smallest thing I can build to test if users will actually change their behavior?"*

**Example:**
- **Your idea:** A comprehensive study management platform with calendar, tasks, notes, flashcards, grade tracking, and social features
- **Your MVP question:** Will students actually use digital study planning instead of paper planners?
- **Your MVP:** Just the calendar + task list (nothing else) to test behavior change

---

### MVP vs Prototype vs Pilot

| Aspect | Prototype | MVP | Pilot |
|--------|-----------|-----|-------|
| **Goal** | Validate feasibility | Validate value | Validate scale |
| **Users** | Internal team | 10-50 early adopters | 100-500 target users |
| **Timeline** | 1-2 weeks | 4-8 weeks | 3-6 months |
| **Quality** | Can be buggy | Must be reliable | Production-ready |
| **Data** | Qualitative feedback | Usage metrics + feedback | Business metrics |
| **Example** | Clickable Figma mockup | Working app, manual backend | Automated, paid product |

**Your course:** You're building an MVP (not prototype, not pilot).

---

## Common MVP Mistakes

### Mistake 1: Feature Creep - "Just One More Thing"

**Symptom:**  
Your MVP scope keeps growing. Started with 3 features, now you're at 12.

**Example:**
```
Initial MVP: Show study room availability
Week 2: + room reservations
Week 3: + user profiles
Week 4: + social features
Week 5: + gamification
Week 6: You haven't shipped anything yet
```

**Why it happens:**  
- Fear of launching something "incomplete"
- Competing with imaginary competitors who have more features
- Stakeholder requests ("What about X?")

**Fix:**  
Use the **One Metric That Matters (OMTM)** test:
- If the feature doesn't directly impact your OMTM, it's not in the MVP
- StudySpot OMTM: Time from opening app to decision (<30 seconds)
- Room reservations? Doesn't impact this. Out.

---

### Mistake 2: "Better" Before "Different"

**Symptom:**  
Competing on features instead of solving a fundamentally different problem.

**Example:**
```
Existing solution: Google Calendar for study planning
Your MVP: Google Calendar clone + dark mode + prettier UI + study-specific templates

Problem: Why would users switch? What's fundamentally better?
```

**Fix:**  
Your MVP should solve a problem **10x better** than current solutions, not 10% better.

**StudySpot Example:**
- Existing solution: WhatsApp "Is library full?" messages (response time: 5-30 min, unreliable)
- StudySpot MVP: See availability in <5 seconds, always up-to-date
- **10x better:** Speed and reliability, not just "nicer interface"

---

### Mistake 3: Building for Imaginary Future Users

**Symptom:**  
Including features for users you haven't validated yet.

**Example:**
```
Your interviews: 10 individual students struggling to find study spots
Your MVP: Includes team scheduling, admin dashboards, analytics

Problem: You're building for personas that don't exist in your research
```

**Fix:**  
**Only build for validated user personas.** If group study coordinators weren't in your top 3 interviewed personas, don't build for them in MVP.

---

### Mistake 4: Perfecting Things That Don't Matter

**Symptom:**  
Spending 2 weeks on onboarding animations when your core feature is broken.

**Example:**
```
Week 1-2: Beautiful landing page
Week 3-4: Slick animations
Week 5: "Oh right, we need to actually show room data"
```

**Fix:**  
**Start with the core value loop**, the absolute center of your product's value. Everything else is polish.

**StudySpot Core Value Loop:**
1. User opens app
2. User sees current room availability
3. User makes decision
4. User goes to available room
5. User saves time

If any feature doesn't directly support this loop, it's not MVP.

---

## The MVP Definition Framework

Use this 5-step process to define your MVP scope.

---

### Step 1: Identify Your Riskiest Assumption

**Question:** What's the one thing that, if wrong, makes your entire product fail?

**Example - StudySpot:**
- ❌ Assumption: "Students want to plan study sessions in advance"
- ✅ **Riskiest Assumption:** "Students will trust and act on real-time occupancy data to make faster decisions"

**Why this matters:**  
Your MVP should test this assumption FIRST. Everything else is secondary.

**Other Examples:**

**Project: Group Task Coordinator**
- Riskiest Assumption: "CS students will actually update their task status daily (vs WhatsApp messages they ignore)"

**Project: Course Material Aggregator**
- Riskiest Assumption: "Students will use a centralized platform instead of checking professors' individual sites out of habit"

---

### Step 2: Define Your One Metric That Matters (OMTM)

**Question:** What single metric proves your riskiest assumption is correct?

**Example - StudySpot:**
- Riskiest Assumption: Students will trust and act on occupancy data
- **OMTM: Time from app open to decision** (target: <30 seconds)
- Secondary: % of users who view location details (proves trust)

**Why this matters:**  
Every MVP feature should directly or indirectly improve this metric.

**Decision Framework:**
```
Feature X proposed → Does it improve OMTM?
  ├─ Yes → Consider for MVP (evaluate cost vs impact)
  └─ No → Definitely not MVP (add to v2 backlog)
```

---

### Step 3: Map the Minimum Successful Flow

**Question:** What's the absolute shortest path a user takes from problem → solution?

**Example - StudySpot Minimum Successful Flow:**

```
Step 1: User opens app (on mobile)
   ↓
Step 2: User sees list of 4 study locations with current occupancy
   ↓
Step 3: User taps one location to see room details
   ↓
Step 4: User sees green/yellow/red indicator + room list
   ↓
Step 5: User makes decision (walk to room OR try different building)
   ↓
SUCCESS: User saved 10-15 minutes vs checking buildings physically
```

**What's NOT in this flow:**
- Login/signup
- User profile
- Favorites
- Filters
- Reservations
- Notifications

**All of those are v1.1+ features.** They improve the experience but aren't required for core value.

---

### Step 4: Apply the MoSCoW Method

**MoSCoW = Must Have, Should Have, Could Have, Won't Have**

For each feature, ask:
1. **Without this, does the core value flow break?** → Must Have
2. **Does this significantly improve the value flow?** → Should Have
3. **Would this be nice but not critical?** → Could Have
4. **Is this unrelated or premature?** → Won't Have

---

### Step 5: Validate with "10x Better" Test

**Question:** Is your MVP at least 10x better than current solutions in at least ONE dimension?

**StudySpot Example:**

| Dimension | Current Solution (WhatsApp) | StudySpot MVP | Improvement Factor |
|-----------|----------------------------|---------------|-------------------|
| **Speed** | 5-30 minutes (wait for response) | <5 seconds | **100x faster** ✅ |
| **Reliability** | 40% response rate | 95% uptime | **2.4x more reliable** ✅ |
| **Coverage** | Depends on who responds | All 4 locations | **Better coverage** ✅ |
| Features | Free, familiar | Fewer features | ❌ Not competing here |

**Conclusion:** StudySpot is 10-100x better on speed and reliability. That's enough. We DON'T need feature parity with WhatsApp (group chats, voice messages, etc.)

---

## Case Study: StudySpot MVP

Let's walk through the complete MVP definition for StudySpot, showing justifications for every decision.

---

### Core Value Hypothesis

**Hypothesis Statement:**
> KIU commuter students will use real-time study room occupancy data to make faster decisions about where to study (reducing time wasted from 15 minutes to <3 minutes), IF the data is accurate, mobile-accessible, and updates in under 5 seconds.

**Breaking it down:**
- **Who:** KIU commuter students (validated: 10 interviews)
- **What behavior:** Use occupancy data to decide where to go (not just "look at it")
- **Benefit:** Save 12+ minutes (quantified from research)
- **Conditions:** Accurate, mobile, fast (<5 sec)

**How MVP tests this:**
- ✅ Shows occupancy data (core feature)
- ✅ Mobile-first design (validated need)
- ✅ Loads in <3 seconds (condition met)
- ✅ Will measure time-to-decision via analytics

---

### MVP Scope: What's IN

#### Feature 1: Real-Time Occupancy Display [MUST HAVE]

**What it is:**
- Homepage shows 4 study locations
- Each shows: name, current occupancy (12/50 format), status (green/yellow/red)
- Auto-refreshes every 30 seconds

**Why it's in the MVP:**
- **Directly tests hypothesis:** Core value = seeing occupancy
- **Required for success flow:** User can't make decision without this
- **10x better than current solution:** WhatsApp = 5-30 min wait, this = instant

**Evidence from research:**
- 10/10 interviews mentioned needing "current status"
- 8/10 specifically said "real-time" is critical
- "I just want to know: is it full or not" - Interview #5

**Acceptance Criteria:**
- Shows 4 locations minimum
- Data <5 minutes old (shown with timestamp)
- Loads in <3 seconds on 4G
- Visual indicators (color) are clear

---

#### Feature 2: Location Detail View [MUST HAVE]

**What it is:**
- Tap any location → see room-by-room breakdown
- Each room shows: number (K-201), occupancy (3/20), status indicator

**Why it's in the MVP:**
- **Improves decision quality:** Users want to know WHICH room, not just building
- **Low effort:** Piggybacks on existing data model
- **Validated need:** 7/10 interviews mentioned room-level detail

**Why we debated removing it:**
- Could argue: building-level is "minimum"
- Counter-argument: 7/10 explicitly asked for this
- Decision: Include because it's high-value, low-effort

**Acceptance Criteria:**
- One tap from homepage to room list
- Back button returns to homepage
- Same data freshness as homepage

---

#### Feature 3: Mobile-First Responsive Design [MUST HAVE]

**What it is:**
- Works perfectly on mobile browsers (iOS Safari, Android Chrome)
- No app download required
- Touch targets 44px+, readable without zoom

**Why it's in the MVP:**
- **User behavior:** 10/10 said they'd check "while walking to class"
- **Adoption barrier:** 8/10 said they WON'T download a native app
- **Core to hypothesis:** "Mobile-accessible" is explicit condition

**Why not native app:**
- Native app = 4-6 weeks extra dev time
- MVP needs to ship in 8 weeks total
- Web app tests hypothesis just as well

**Acceptance Criteria:**
- Works on screens 320px-430px wide
- Loads on 4G in <3 seconds
- No horizontal scrolling
- Thumb-reachable buttons

---

#### Feature 4: Data Freshness Indicators [MUST HAVE]

**What it is:**
- Each location shows "Updated 3 min ago"
- Warning if data >5 min old
- Error state if data >15 min old

**Why it's in the MVP:**
- **Trust:** Hypothesis says "IF data is accurate"
- **Validated concern:** 6/10 interviews mentioned trust/staleness
- **Behavior change:** Without trust, users won't act on data

**Why it's not optional:**
- Without freshness indicators, users won't know if data is trustworthy
- Destroys core hypothesis if users don't trust data

**Acceptance Criteria:**
- Timestamps visible on every location card
- Warning at 5min, error at 15min
- Updates every 30 seconds

---

#### Feature 5: Manual Data Entry (Spotter Dashboard) [MUST HAVE]

**What it is:**
- Separate interface for student "spotters"
- Quick update: tap location → adjust count → submit
- PIN-based auth (simple, no user management)

**Why it's in the MVP:**
- **Data source:** We don't have automated sensors
- **Feasible alternative:** Recruit 8 student spotters (2 per location)
- **Lower cost:** Manual = $0, sensors = $5,000+ and 3 months

**Why not automated sensors:**
- Cost: $5,000+ university budget we don't have
- Time: 3+ months procurement and installation
- Permissions: University facilities approval required
- **MVP philosophy:** Test demand BEFORE investing in expensive automation

**Risk mitigation:**
- Gamification (leaderboard, points)
- Weekly prizes for top spotters
- Backup spotters recruited

**Acceptance Criteria:**
- Mobile-optimized interface
- <2 seconds to submit update
- Works offline (syncs when online)
- Simple PIN login

---

### MVP Scope: What's OUT (and Why)

These are features we explicitly decided NOT to include. Each has a clear justification.

---

#### Feature 6: User Accounts & Authentication [OUT - v2.0]

**What it is:**
- Login/signup system
- Saved preferences
- Favorite locations

**Why it's NOT in the MVP:**
- ❌ **Doesn't test core hypothesis:** Can validate value without accounts
- ❌ **Adds 2-3 weeks dev time:** Signup, email verification, password reset = complex
- ❌ **Friction barrier:** 8/10 interviews said "just let me see the data" - no login wanted
- ❌ **Not required for OMTM:** Time-to-decision doesn't need authentication

**When we'll add it:**
- **v1.1 (Week 2 post-launch):** If retention data shows users returning 3+ times per week
- **Trigger:** 40%+ week-2 retention + user requests for "save favorites"

**Evidence:**
- Interview #2: "I don't want another login. Just show me the rooms."
- Interview #8: "If I have to create an account, I won't use it."

**Exception considered:**
- "What if we need accounts for analytics?"
- **Answer:** Anonymous device IDs sufficient for MVP metrics

---

#### Feature 7: Room Reservations [OUT - v3.0+]

**What it is:**
- Book a room for specific time slot
- Calendar integration
- Confirmation emails

**Why it's NOT in the MVP:**
- ❌ **Different hypothesis:** Reservation tests "planning ahead" not "finding NOW"
- ❌ **Policy nightmare:** Requires university approval, booking rules, conflicts
- ❌ **Wrong pain point:** 9/10 interviews said problem is "finding available rooms NOW" not "booking for later"
- ❌ **Scope explosion:** Reservations need: auth, calendar, notifications, admin panel = 3-4 weeks

**Research evidence:**
- Only 2/10 interviews mentioned wanting to "book ahead"
- 9/10 said immediate availability is the pain point
- "I don't plan my study sessions, I just have gaps between classes" - Interview #5

**When we'll reconsider:**
- After MVP proves demand for occupancy data
- If users explicitly request booking feature (>30% ask for it)
- After university facilities partnership (they manage policies)

---

#### Feature 8: Push Notifications [OUT - v2.0]

**What it is:**
- Alert when favorite room becomes available
- Daily digest of occupancy patterns
- Reminder to update if you're a spotter

**Why it's NOT in the MVP:**
- ❌ **Unvalidated need:** 0/10 interviews mentioned wanting notifications
- ❌ **Technical complexity:** Requires PWA setup or native app
- ❌ **Battery concerns:** 2/10 interviews mentioned "too many notifications" as annoyance
- ❌ **Doesn't improve OMTM:** Notifications don't make decision faster (user isn't in app yet)

**Alternative that IS in MVP:**
- Auto-refresh every 30 seconds when user has app open
- This serves same purpose (fresh data) without notification overhead

**When we'll add it:**
- v2.0 if usage patterns show: users check app 5+ times per day waiting for specific room
- After implementing PWA or native app
- After validating users WANT to be notified (survey required)

---

#### Feature 9: Historical Patterns & Predictions [OUT - v3.0+]

**What it is:**
- "Library is usually 80% full on Tuesdays at 2 PM"
- "Best time to find seat: 8-10 AM or after 4 PM"
- Predictive availability

**Why it's NOT in the MVP:**
- ❌ **No data yet:** Need 4-8 weeks of occupancy data before patterns are meaningful
- ❌ **Wrong problem:** Interviews validate "I need to know NOW" not "I want to plan"
- ❌ **Complex analysis:** Requires ML or complex queries
- ❌ **Unvalidated assumption:** We're guessing users want predictions

**When we'll reconsider:**
- After collecting 2+ months of occupancy data
- If analytics show users checking app to "plan ahead" (not immediate decisions)
- After proving core MVP value

**Interesting note:**
- 3/10 interviews said "I wish I knew when library is usually empty"
- BUT: This is a "nice to have" not a "pain point"
- MVP focuses on pain points, not nice-to-haves

---

#### Feature 10: Social Features [OUT - Won't Have]

**What it is:**
- Check-in to study rooms
- See which friends are studying where
- Study buddy matching
- Rate/review rooms

**Why it's NOT in the MVP (or ever):**
- ❌ **Feature creep:** Completely different product direction
- ❌ **Zero evidence:** 0/10 interviews mentioned social aspect
- ❌ **Dilutes core value:** Confuses "find rooms" with "find friends"
- ❌ **Privacy concerns:** Some students study alone intentionally

**Why this is tempting:**
- "Gamification" and "social" are buzzwords
- Seems like it would increase engagement
- Other apps have social features

**Why we're saying NO:**
- MVP discipline = solving ONE problem exceptionally well
- Social features solve DIFFERENT problem (loneliness, networking)
- If we try to solve two problems, we'll solve neither well

**Permanent out of scope.**

---

## Feature Prioritization Matrix

Use this matrix to evaluate any feature for MVP inclusion.

| Feature | Tests Core Hypothesis? | Effort (S/M/L) | User Evidence (n/10) | Risk if Excluded | MVP Decision |
|---------|----------------------|----------------|-------------------|------------------|--------------|
| **Occupancy Display** | ✅ Yes - core value | M (3-4 days) | 10/10 mentioned | Product fails | ✅ MUST HAVE |
| **Room Detail** | ⚠️ Improves decision | S (1-2 days) | 7/10 mentioned | Users frustrated | ✅ MUST HAVE |
| **Mobile-First** | ✅ Yes - condition | M (built-in) | 10/10 mobile | No adoption | ✅ MUST HAVE |
| **Freshness Indicators** | ✅ Yes - trust needed | XS (<1 day) | 6/10 mentioned | Users don't trust | ✅ MUST HAVE |
| **Spotter Dashboard** | ✅ Yes - data source | M (2-3 days) | N/A - operational | No data | ✅ MUST HAVE |
| **User Accounts** | ❌ No | L (2-3 weeks) | 2/10 wanted | None | ❌ OUT |
| **Reservations** | ❌ Different problem | L (3-4 weeks) | 2/10 mentioned | None | ❌ OUT |
| **Notifications** | ❌ Doesn't help OMTM | M (1 week) | 0/10 mentioned | None | ❌ OUT |
| **Predictions** | ❌ Need data first | L (2+ weeks) | 3/10 mentioned | None | ❌ OUT |
| **Building Filter** | ⚠️ Nice to have | S (1 day) | 5/10 mentioned | Minor annoyance | ⚠️ v1.1 |
| **Favorites** | ⚠️ Improves repeat use | S (2 days) | 4/10 mentioned | Minor friction | ⚠️ v1.1 |
| **Capacity Filter** | ⚠️ For groups (secondary persona) | M (2-3 days) | 3/10 mentioned | Groups annoyed | ⚠️ v2.0 |
| **Social Features** | ❌ Different product | XL (4+ weeks) | 0/10 mentioned | None | ❌ NEVER |

**Legend:**
- ✅ MUST HAVE = In MVP, non-negotiable
- ⚠️ v1.1 / v2.0 = Post-launch, backlog
- ❌ OUT = Explicitly not building

---

## Scope Justification Template

Use this template for every feature decision:

```markdown
### Feature: [Name]

**Description:** [1-2 sentences]

**Inclusion Decision:** ✅ IN MVP / ⚠️ POST-LAUNCH / ❌ OUT

**Justification:**

1. **Core Hypothesis Impact:**
   - Does it test our riskiest assumption? [Yes/No]
   - Does it improve our OMTM? [Yes/No/Indirectly]

2. **User Evidence:**
   - How many interviews mentioned this? [X/10]
   - Direct quotes: "[quote from research]"
   - Quantified impact: [time saved, pain reduced, etc.]

3. **Effort vs Impact:**
   - Development effort: [XS/S/M/L/XL] ([X days/weeks])
   - Expected impact: [High/Medium/Low]
   - Ratio: [Worth it / Not worth it for MVP]

4. **Risk if Excluded:**
   - What happens if we don't build this? [Catastrophic / Annoying / No impact]

5. **Alternatives:**
   - Can we test hypothesis without this? [Yes/No, explain]
   - Workarounds for MVP: [describe if applicable]

**Decision:** [Include in MVP / Defer to v1.1 / Defer to v2.0 / Never build]

**Conditions for reconsideration:** [What metrics or feedback would cause us to add this later?]
```

---

## When to Pivot vs Persevere

Your MVP might fail. That's OK - failure teaches you what to build next.

### Signals to Pivot (Change Direction)

**Pivot if:**
- ✅ <20 weekly active users after 2 weeks (target was 50+)
- ✅ Users view data but don't report saved time (suggests no behavior change)
- ✅ <40% week-2 retention (users try once and never return)
- ✅ Qualitative feedback: "This is interesting but I wouldn't actually use it"

**What pivoting looks like:**
- **Pivot #1 - Different User:** Maybe commuter students aren't the right persona? Try residential students.
- **Pivot #2 - Different Problem:** Maybe finding rooms isn't the real pain? Test finding group study spaces instead.
- **Pivot #3 - Different Solution:** Maybe real-time data isn't valuable? Test room booking instead.

---

### Signals to Persevere (Keep Going)

**Persevere if:**
- ✅ 40-50 WAU (close to target, might just need more time/marketing)
- ✅ High engagement among users who DO adopt (suggests product-market fit for subset)
- ✅ 50%+ report time saved (value is there, just need more users)
- ✅ Qualitative feedback: "This is useful, but I wish it had X" (feature requests = engaged users)

**What persevering looks like:**
- **Iterate on MVP:** Add 1-2 P1 features (building filter, favorites)
- **Improve marketing:** Maybe students don't know it exists
- **Fix UX issues:** Maybe adoption is low due to bugs or slow load times

---

### The MVP Learning Loop

```
Week 1-8: Build MVP
    ↓
Week 9-10: Launch + Observe
    ↓
Week 11: Analyze Metrics + Feedback
    ↓
Decision Point:
    ├─ Success (50+ WAU, 70%+ time saved) → v1.1 with P1 features
    ├─ Partial Success (30-50 WAU) → Iterate, fix UX, improve marketing
    ├─ Learning (20-30 WAU, good feedback) → Pivot: try different user or problem
    └─ Failure (<20 WAU, no behavior change) → Hard Pivot or Kill product
```

---

## Checklist: Is Your MVP Scope Correct?

Before finalizing your MVP, verify:

### Hypothesis Clarity
- [ ] You can state your core value hypothesis in one sentence
- [ ] Your riskiest assumption is clear and testable
- [ ] You have one metric that matters (OMTM)

### Scope Discipline
- [ ] Every feature included directly tests your hypothesis
- [ ] You can justify removing each excluded feature
- [ ] Your MVP can be built in 6-8 weeks (not 12+)
- [ ] You're solving ONE problem really well (not 3 problems poorly)

### User Evidence
- [ ] Every included feature is mentioned by 6+ interviewees (or has strong justification)
- [ ] You have quantified impact for your core value prop (X minutes saved, Y% reduction in frustration, etc.)
- [ ] You're building for validated personas (not imaginary future users)

### 10x Better Test
- [ ] Your MVP is 10x better than current solutions in at least ONE dimension
- [ ] You're competing on a different axis (not just "slightly better features")

### Feasibility
- [ ] Your team has skills to build this (or can learn quickly)
- [ ] Your timeline is realistic (not hopeful thinking)
- [ ] You have a plan for biggest technical risk

### Launch Readiness
- [ ] You know how to recruit 10-20 beta testers
- [ ] You have a plan to collect feedback and usage data
- [ ] You know your pivot triggers (what metrics indicate failure)

---

## Key Takeaways

1. **MVP is NOT "all features, poorly done"** - it's "minimum features, done well"

2. **One Metric That Matters** - every feature should improve this, or it's out

3. **Evidence > Opinions** - interview data decides what's in, not team preferences

4. **10x Better** - compete on magnitude, not just "we have more features"

5. **Discipline is Hard** - saying NO to features feels wrong but it's essential

6. **Ship Fast, Learn Fast** - 8 weeks to launch beats 16 weeks to "perfect"

7. **Pivot is OK** - MVP failure teaches you what to build next

---

## Next Steps

After defining your MVP:

1. **Write your PRD** - detail out the features you've decided to include
2. **Create user stories** - break features into implementable tasks
3. **Estimate effort** - size each story, build sprint plan
4. **Identify risks** - what could prevent you from shipping in 8 weeks?
5. **Build, test, launch** - execute your sprint plan
6. **Measure, learn, iterate** - collect data, make decisions

**Remember:** Your MVP scope is NOT set in stone. If you learn something during Week 3 of development that changes your hypothesis, you can adjust scope. But do it consciously, with justification, not by accident.

---

## Further Reading

- **The Lean Startup** by Eric Ries (Chapters 4-6 on MVP)
- **Sprint** by Jake Knapp (MVP prototyping in 5 days)
- **Inspired** by Marty Cagan (Chapter on product discovery)
- **The Mom Test** by Rob Fitzpatrick (Evidence-based product decisions)

---

**Bottom Line:** Your MVP should be the smallest possible product that proves users will actually change their behavior because of your solution. Everything else is v2.
