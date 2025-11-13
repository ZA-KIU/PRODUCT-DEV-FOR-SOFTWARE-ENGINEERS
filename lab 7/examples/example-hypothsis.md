# Example Hypothesis: StudySpot Team

**Team Name:** StudySpot  
**Date Created:** November 13, 2025  
**Created By:** Sarah Chen, Michael Rodriguez, Anano Beridze, David Kim

---

## 📋 Your Hypothesis

### Full Hypothesis Statement

**Our complete hypothesis:**

```
We believe showing real-time library occupancy percentages for KIU CS students 
in years 2-3 who commute will result in 50+ email signups with 15+ checking 
occupancy 3+ times/week within 1 week because these students currently waste 
15 minutes/day walking to campus only to find the library full.
```

---

## 🎯 Hypothesis Components

### 1. What We're Testing (The "X")

**Action/Solution/Feature:**
> Showing real-time library occupancy percentages on a mobile-friendly web app

### 2. Target User (Be Specific!)

**Your Target User:**
> KIU CS students in years 2-3 (ages 19-21) who commute from Tbilisi to Kakheti 
> campus and study on campus between classes.

**Why this segment?**
> From our interviews:
> - They commute 1-2 hours to campus (high cost to wasted trips)
> - They have 2-4 hour gaps between classes (need study time)
> - They can't go home between classes (too far)
> - They mentioned "finding empty spots" as top frustration 3 times in interviews
> - They're tech-savvy and check phones frequently

### 3. Measurable Outcome

**Your Measurable Outcome:**
> 50+ email signups within 1 week, with at least 15 active users checking 
> occupancy 3+ times/week

**How will you measure it?**
> - Email signups: Google Forms (auto-counted)
> - App opens: We won't have app yet, so we'll track landing page return visits 
>   via Google Analytics (cookie-based tracking)
> - Alternative: Ask in signup form: "How many times/week would you check this?"

### 4. Underlying Assumption

**What must be true for this to work?**

> Students currently waste significant time (15+ min/day) walking to library 
> during peak hours (11am-2pm) only to find it full. They want real-time 
> information to avoid wasted trips. They value their time enough to check an 
> app before going.

**Evidence supporting this assumption:**

Interview evidence:
- 8/10 CS students interviewed mentioned "finding study spots" as daily frustration
- 6/10 said they've walked to library during midterms and found it completely full
- Average wasted time reported: 15-20 minutes per attempt
- Quote from Interview #4: "I literally opened the library door, saw it was packed, 
  and just left. Wasted 20 minutes walking there and back."

Observational evidence:
- During midterms week (Nov 6-10), we observed library entrance:
  - 23/50 students turned away after entering (46% rejection rate)
  - Peak times: 11:30am and 1:00pm (between common class times)

---

## 🔍 Hypothesis Classification

### Hypothesis Type

- [X] **Problem Hypothesis** - Testing if the problem is real and painful
- [X] **Solution Hypothesis** - Testing if this solution solves the problem  
- [ ] **Value Hypothesis** - Testing if users will pay or adopt this
- [ ] **Growth Hypothesis** - Testing if users will tell others or return

**Why this type?**
> This is primarily a Problem + Solution hypothesis. We're testing:
> 1. Is "finding empty study spots" painful enough to act on? (Problem)
> 2. Does real-time occupancy data solve this problem? (Solution)
>
> We're NOT YET testing value (pricing) or growth (virality). Those come after we 
> validate the core problem-solution fit.

---

## ✅ Hypothesis Quality Checklist

### Specificity Test
- [X] **Target user is specific** - "KIU CS year 2-3 commuters" (not just "students")
- [X] **Action/solution is clear** - "showing real-time library occupancy percentages"
- [X] **Outcome is concrete** - "50+ email signups, 15+ active users 3x/week"

### Measurability Test  
- [X] **Success metric is a number** - "50+ signups" and "15+ active users"
- [X] **Has a timeframe** - "within 1 week"
- [X] **You can actually measure it** - Google Forms + Analytics

### Testability Test
- [X] **Can be tested in 1-2 weeks** - Yes, 1 week experiment
- [X] **Can be tested without building full product** - Landing page + fake data
- [X] **Success/failure is clear** - 50+ = validated, <20 = invalidated

### Assumption Test
- [X] **Assumption is explicit** - "Students waste 15 min/day, want real-time info"
- [X] **Assumption is based on evidence** - 10 interviews + observation
- [X] **Assumption is risky** - If wrong, our entire product pivot is misguided

---

## 🎲 Risk Assessment

### What's the riskiest part of this hypothesis?

> The assumption that students will CHECK an app proactively rather than just 
> walking to library out of habit. 
>
> Even if the problem is real, students might not change their behavior. They 
> might say "this is useful" but never actually use it.

### What happens if you're WRONG?

**If hypothesis is invalidated (50 signups):**

Possible reasons:
1. Problem isn't painful enough (students don't mind wasted time)
2. Solution doesn't resonate (real-time data isn't what they want)
3. Distribution failed (couldn't reach target users)
4. Timing was bad (tested during non-midterm week)

**Our pivot plan:**
- Interview the <20 people who DID sign up: why them?
- Interview 10 target users who didn't sign up: what would make them care?
- Consider alternative problems: maybe it's not about finding spots, but about 
  finding QUIET spots or COLLABORATIVE spots?
- Consider alternative users: maybe year 1 students or international students 
  have this problem more acutely?

### What happens if you're RIGHT?

**If hypothesis is validated (>50 signups):**

Next steps:
1. Build minimal prototype (Week 10-11):
   - Manual data collection (team members check library hourly)
   - Simple web app showing occupancy %
   - Beta test with the 50+ signups

2. Next hypothesis to test:
   - "Students who see occupancy data will check 5+ times/week and save average 
     10 min/day" (testing actual usage, not just interest)

3. Roadmap changes:
   - Move real-time occupancy to Sprint 1 (highest priority)
   - De-prioritize study room booking feature (test later)
   - Add analytics to track actual check frequency

---

## 🔄 Hypothesis Evolution

### Previous Versions (if any)

**Version 1 (From Lecture Exercise):**
> "Students will use our app to find study spots"

**Why we changed it:**
- WAY too vague
- "Students" = who? All students? Grad students? First-years?
- "Use our app" = what action exactly?
- "Find study spots" = no measurable outcome
- No assumption stated explicitly

**Version 2 (First Draft in Lab):**
> "We believe KIU students will sign up for an app that shows library occupancy 
> because they waste time finding spots"

**Why we changed it:**
- Better, but still not specific enough
- "KIU students" = too broad (we learned year 2-3 commuters have this problem most)
- "Sign up" = okay, but how many? When?
- "Waste time" = evidence? How much time?

**Version 3 (Current - After Team Discussion):**
> [The final hypothesis at top of document]

---

## 📝 Team Agreement

### Team Sign-Off

By signing below, our team agrees:
- This hypothesis is testable in 1 week
- We have a clear experiment plan to test it
- We commit to analyzing results objectively
- We will pivot if hypothesis is invalidated

**Team Members:**

- [X] Sarah Chen - Product Manager - Nov 13, 2025
- [X] Michael Rodriguez - Developer - Nov 13, 2025
- [X] Anano Beridze - Designer - Nov 13, 2025
- [X] David Kim - Growth/Marketing - Nov 13, 2025

---

## 💭 Notes & Discussion

**Team debate during hypothesis writing:**

Anano initially wanted to test "study room booking" instead of occupancy, arguing 
that's the REAL pain point from interviews. But we decided:
- Booking requires more complex MVP to test
- Occupancy is simpler and faster to validate
- We can test booking AFTER validating occupancy

Michael worried 50 signups was too ambitious. But Sarah pushed back:
- If we can't get 50 CS students (out of ~300) interested, the market is too small
- Better to set high bar and learn if there's real demand
- 50 = ~15% of year 2-3 CS commuters (reasonable conversion if problem is real)

---

## 🔗 Related Documents

- Link to experiment plan: [`experiment-plan.md`](./experiment-plan.md)
- Link to ICP: [`/01-discovery/team-icp.md`](../../01-discovery/team-icp.md)
- Link to problem statement: [`/00-foundation/team-problem-statement.md`](../../00-foundation/team-problem-statement.md)
- Link to interview synthesis: [`/01-discovery/synthesis/patterns-analysis.md`](../../01-discovery/synthesis/patterns-analysis.md)

**Interview evidence cited:**
- Interview #4 (Giorgi, Year 2 CS): "I wasted 20 minutes walking to full library"
- Interview #7 (Mariam, Year 3 CS): "I check 3 different study spots before finding one"
- Interview #9 (Luka, Year 2 CS): "During midterms, library is always packed 11am-2pm"

---

**Last Updated:** November 13, 2025  
**Status:** [X] Final | [ ] Testing | [ ] Validated | [ ] Invalidated

---

## 📊 Quick Reference Card

**For sharing with teammates:**

```
HYPOTHESIS: Show library occupancy → 50+ signups in 1 week
TARGET: Year 2-3 CS commuters
WHY: They waste 15 min/day finding spots
SUCCESS: 50+ emails + 15+ would check 3x/week
TEST: Landing page + Google Forms
LAUNCH: Nov 19 (Monday)
```
