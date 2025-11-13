# Lab 7: Hypothesis-Driven Experimentation Workshop

**Duration:** 120 minutes (2 hours)  
**Week:** 8  
**Due Date:** Experiment plan and refined hypothesis due by end of lab. First experiment must be LIVE by next Sunday.

## 🎯 Lab Overview

After planning your roadmap in Lab 6, this lab teaches you to **TEST assumptions before building**. You'll learn to design experiments that validate (or invalidate) your riskiest assumptions using the hypothesis-driven development framework.

**By the end of this lab, you will:**
1. ✅ Transform vague assumptions into testable hypotheses
2. ✅ Design 2-3 experiments using the experiment spectrum (smoke tests → MVP)
3. ✅ Build a simple landing page or fake door test (no coding your actual product!)
4. ✅ Create a detailed experiment launch plan with success metrics

## 📋 Prerequisites

**Bring to Lab:**
- [ ] Your product roadmap from Lab 6 (`/03-build/roadmap/`)
- [ ] The risky assumption you identified in the Week 8 lecture exercise
- [ ] Your team's problem statement and ICP
- [ ] Laptop with internet access
- [ ] Access to your GitHub repo

**Review Before Lab:**
- Week 8 lecture slides (Hypothesis-Driven Development)
- The Airbnb photo hypothesis case study
- Buffer's MVP validation example

---

## 🗓️ Lab Structure

| Time | Activity | Output |
|------|----------|--------|
| **0:00-0:30** | Part 1: Hypothesis Refinement | `hypothesis.md` |
| **0:30-1:10** | Part 2: Experiment Design Workshop | `experiment-plan.md` |
| **1:10-1:40** | Part 3: Landing Page/Smoke Test Build | Live page or fake door |
| **1:40-2:00** | Part 4: Launch Plan & Team Shareout | `launch-plan.md` |

---

## 📚 Part 1: Hypothesis Refinement (30 min)

### Step 1: Review Your Risky Assumption (5 min)

Look at the assumption you identified during the Week 8 lecture's 2-minute exercise.

**Common vague assumptions:**
- ❌ "Students will use our app"
- ❌ "People want this feature"
- ❌ "Users will pay for this"

### Step 2: Use the Hypothesis Template (15 min)

📝 **Complete:** [`templates/hypothesis-template.md`](./templates/hypothesis-template.md)

**The Formula:**
```
We believe [doing X] for [target user] will result in [measurable outcome] 
because [assumption about user behavior].
```

**Example from StudySpot:**
```
We believe showing library occupancy % for KIU CS students will result in 
30+ signups opening the app 3+ times/week because students currently waste 
15 min/day finding study spots and want real-time info.
```

**Make it pass the tests:**
- ✅ **Specific user:** Not "students" — "KIU commuter students in years 2-3"
- ✅ **Measurable outcome:** Not "engagement" — "50+ email signups in 1 week"
- ✅ **Testable timeframe:** "Within 1 week" not "eventually"
- ✅ **Clear assumption:** Why you think this will work

### Step 3: Identify Hypothesis Type (5 min)

Which type is your hypothesis?

| Type | Question | Example Test |
|------|----------|--------------|
| 🔍 **Problem** | Is the problem real and painful? | Interviews, time-tracking study |
| 💡 **Solution** | Will this solution solve the problem? | Prototype testing, fake door |
| 💰 **Value** | Will users pay or adopt this? | Landing page, pricing page |
| 📈 **Growth** | Will users tell others or come back? | Referral tracking, usage analytics |

**Your hypothesis is likely a ___________ hypothesis.**

### Step 4: Team Review (5 min)

Read your hypothesis aloud to your team.

**Good Hypothesis Checklist:**
- [ ] Does it have a specific user segment?
- [ ] Is the outcome measurable?
- [ ] Is it testable in 1-2 weeks?
- [ ] Is the assumption clear?

**If NO to any:** Revise now before moving forward.

---

## 🧪 Part 2: Experiment Design Workshop (40 min)

### Step 1: Choose Experiment Type(s) (10 min)

Review the **Experiment Spectrum** from lecture:

```
Lowest Fidelity ←──────────────────────────────→ Highest Fidelity
└── Preotype ──┴── Smoke Test ──┴── Wizard of Oz ──┴── MVP ──┘
```

**For Week 8-9, focus on Smoke Tests:**

| Type | What It Is | Use When | Build Time |
|------|------------|----------|------------|
| **Fake Door Test** | Button/link for feature that doesn't exist yet | Testing interest/demand | 1 day |
| **Landing Page** | Single page describing product + email signup | Testing value prop | 1-3 days |
| **Concierge MVP** | Manually deliver service to early users | Testing solution fit | 1 week |
| **Wizard of Oz** | Users think it's automated, but humans do the work | Testing core workflow | 1-2 weeks |

📝 **Document:** Choose 2-3 experiment types in [`templates/experiment-plan-template.md`](./templates/experiment-plan-template.md)

**Example Decision:**
> "We'll create a landing page (Test 1) to validate demand, then a fake door test (Test 2) 
> in our prototype to see which feature students click most."

### Step 2: Define Success Metrics (15 min)

For EACH experiment, define:

**Using SMART Criteria:**

| Letter | Meaning | Bad Example | Good Example |
|--------|---------|-------------|--------------|
| **S** | Specific | "signups" | "email signups" |
| **M** | Measurable | "good engagement" | "50+ signups" |
| **A** | Actionable | "pageviews" | "signup → activation rate" |
| **R** | Relevant | "clicks" | "completed tasks" |
| **T** | Time-bound | "eventually" | "in 1 week (Nov 19-20)" |

**Success vs. Failure Criteria:**

For each experiment, define:
- ✅ **Success threshold:** "If 50+ students sign up, build it. 15% considered validated."
- ❌ **Failure threshold:** "If <10 signups in 1 week, not enough demand."
- 🤔 **Learn threshold:** "10-49 signups = interview signups to understand why."

📝 **Document:** Complete metrics section of [`templates/experiment-plan-template.md`](./templates/experiment-plan-template.md)

### Step 3: Identify What You'll Learn (10 min)

For each experiment, write:

**If validated (hypothesis proven):**
- What will you do next?
- What will you build?

**If invalidated (hypothesis disproven):**
- What did you learn?
- How will you pivot?

**Example:**
```
If validated: Build MVP starting with real-time occupancy display
If invalidated: Interview signups to understand why they signed up but didn't engage
```

### Step 4: Set Timeline (5 min)

**This week (Nov 13-20):**
- Design experiment: ___ hours
- Build landing page/test: ___ hours  
- Launch experiment: By ___ (date)
- Run experiment: ___ days
- Analyze results: By ___ (date)

⚠️ **Critical:** You must RUN at least ONE experiment for 3+ days minimum by next Sunday.

---

## 🎨 Part 3: Landing Page/Smoke Test Build (30 min)

### Choose Your Tool

Pick ONE based on your experiment type:

| Tool | Best For | Time | Difficulty |
|------|----------|------|------------|
| **[Carrd.co](https://carrd.co)** | Simple landing pages | 20 min | ⭐ Easy |
| **[Notion](https://notion.so)** | Content-heavy pages | 30 min | ⭐ Easy |
| **[Google Sites](https://sites.google.com)** | Quick team pages | 20 min | ⭐ Easy |
| **[Typeform](https://typeform.com)** | Surveys with signup | 15 min | ⭐ Easy |
| **[Google Forms](https://forms.google.com)** | Simple signups | 10 min | ⭐ Very Easy |

### Landing Page Requirements

Your page MUST include:

1. **Clear headline:** What problem does it solve? (10 words max)
2. **Value proposition:** Why should they care? (1-2 sentences)
3. **Target user:** Who is this for? (Be specific!)
4. **Call-to-action:** Email signup, waitlist, or fake button
5. **Visual:** Screenshot, mockup, or simple diagram

### Fake Door Test Requirements

If building a fake door in your existing prototype:

1. **Clickable element:** Button or link for non-existent feature
2. **Interest capture:** "Coming soon! Enter email for early access"
3. **Thank you message:** "Thanks! We'll notify you when it's ready."
4. **Click tracking:** Log which features get clicked (use Google Analytics or simple counter)

### Build Time: 25 minutes

Work together or split up:
- Designer: Creates page layout and copy
- Developer: Sets up form and tracking
- PM: Writes compelling copy

### Test Your Page (5 min)

Before launching:
- [ ] Submit a test signup
- [ ] Check if you received the email/logged the data
- [ ] Test on mobile (50%+ of traffic will be mobile)
- [ ] Share link with team to verify

📝 **Document:** Save link in [`templates/landing-page-link.md`](./templates/landing-page-link.md)

---

## 🚀 Part 4: Launch Plan & Team Shareout (20 min)

### Step 1: Write Launch Plan (10 min)

📝 **Complete:** [`templates/launch-plan-template.md`](./templates/launch-plan-template.md)

**Your plan must answer:**

**WHO will you target?**
- [ ] Specific user segment (from your ICP)
- [ ] How many people can you reach?
- [ ] Where do they hang out online/offline?

**WHERE will you promote?**
- [ ] Facebook groups
- [ ] WhatsApp groups
- [ ] Instagram stories
- [ ] TikTok
- [ ] Physical flyers
- [ ] Class announcements
- [ ] Other: _______

**WHEN will you launch?**
- [ ] Launch date: ___________
- [ ] Run duration: ___ days (minimum 3 days)
- [ ] Check-in schedule: Daily at ___ PM

**HOW will you measure?**
- [ ] Tool: Google Forms / Typeform / Analytics
- [ ] Metrics tracked: ____________
- [ ] Dashboard link: ____________
- [ ] Daily log: ________________

**WHAT will you do with results?**
- [ ] If validated: ____________
- [ ] If invalidated: ___________
- [ ] If inconclusive: __________

### Step 2: Team Shareout (10 min)

Each team presents (2 minutes max):

**Template:**
> "We're testing the hypothesis that [hypothesis]. We're running a [experiment type] 
> targeting [specific users]. Success looks like [metric]. We'll launch [when] and 
> analyze results by [date]."

**Class gives feedback:**
- ✅ Is the hypothesis testable?
- ✅ Is the metric specific enough?
- ✅ Is 1 week realistic for this experiment?

---

## 📦 Deliverables

### Due by End of Lab (Today):

Create folder `/03-build/experiments/` in your repo:

```
/03-build/experiments/
├── hypothesis.md                  # Your refined hypothesis
├── experiment-plan.md              # 2-3 experiments designed
├── landing-page-link.md            # Link to your live page/test
└── launch-plan.md                  # Who, what, when, where, how
```

**Commit and push to GitHub before leaving lab.**

### Due by Next Sunday (Week 9):

- [ ] **Launch** at least ONE experiment
- [ ] **Run** experiment for minimum 3 days
- [ ] **Track** metrics daily in [`experiment-results.md`](./templates/experiment-results-template.md)
- [ ] **Document** learnings (even if failed!)

**Where to put results:**
```
/03-build/experiments/
├── [PREVIOUS FILES]
└── experiment-results.md           # Daily tracking + final analysis
```

---

## ✅ Success Criteria

**You've succeeded if:**
- [ ] Your hypothesis is testable and specific
- [ ] You can measure success in 1 week
- [ ] Your landing page/test is live and accessible
- [ ] You know exactly who you're targeting and where to find them
- [ ] You have clear success/failure thresholds defined
- [ ] You commit to checking metrics DAILY

**Red flags:**
- ❌ Hypothesis uses vague words like "users" or "engagement"
- ❌ No specific metric or success threshold
- ❌ Planning to build actual MVP features (that's NOT an experiment!)
- ❌ No plan for where to find target users
- ❌ Timeline is >2 weeks

---

## 🧰 Resources

### Required Reading (Do BEFORE next lab):
- **[The Lean Startup, Chapter 6: Test](https://www.amazon.com/Lean-Startup-Entrepreneurs-Continuous-Innovation/dp/0307887898)** - Eric Ries
- **[Hypothesis-Driven Development](https://www.thoughtworks.com/en-us/insights/articles/how-to-implement-hypothesis-driven-development)** - Barry O'Reilly

### Helpful Tools:
- **Landing Pages:** [Carrd.co](https://carrd.co), [Notion](https://notion.so), [Google Sites](https://sites.google.com)
- **Surveys:** [Typeform](https://typeform.com), [Google Forms](https://forms.google.com)
- **Analytics:** [Google Analytics](https://analytics.google.com), [Plausible](https://plausible.io)
- **Fake Product Pages:** [Notion](https://notion.so), [Canva](https://canva.com)

### GitHub Repo:
- Week 8 templates in `/labs/lab-7/templates/`
- Example experiments in `/examples/experiments/`
- Hypothesis tracking spreadsheet

---

## 🏠 Homework (Due Next Sunday Before Week 9)

### 1. Launch Your Experiment (Required)

**Minimum requirements:**
- [ ] Live for 3+ days
- [ ] Reach 30+ people from target segment
- [ ] Track signups/clicks daily
- [ ] Document in `experiment-results.md`

**Promotional requirements:**
- [ ] Post in 2+ relevant channels (groups/forums/social)
- [ ] Include screenshots of posts in `/experiments/promotion/`
- [ ] Track source of signups (where did they come from?)

### 2. Track Metrics Daily (Required)

Create `experiment-results.md` with:

**Daily Log Format:**
```markdown
## Day 1 (Nov 19)
- Signups: 12
- Landing page visits: 87
- Conversion rate: 13.8%
- Top traffic source: CS Facebook group
- Observations: Most signups came after class time (2-5pm)

## Day 2 (Nov 20)
...
```

### 3. Read & Reflect (Required)

**Read:**
- The Lean Startup, Chapter 6: Test (30 pages)

**Write:** 
- 200-word reflection in `experiment-results.md`:
  - What surprised you about running the experiment?
  - How did users respond differently than expected?
  - Would you run this experiment differently next time?

### 4. Optional: Run Second Experiment

If your first experiment completes early, run a second one!

---

## 📊 Grading Rubric (Lab 7 = 10 points)

| Component | Points | Criteria |
|-----------|--------|----------|
| **Hypothesis Quality** | 2 pts | Specific, measurable, testable, clear assumption |
| **Experiment Design** | 2 pts | Appropriate type, clear metrics, realistic timeline |
| **Landing Page/Test** | 2 pts | Live, functional, tracks metrics, professional |
| **Launch Plan** | 2 pts | Specific targets, promotion plan, measurement plan |
| **Execution** | 2 pts | Launched by deadline, ran 3+ days, tracked daily |

**Bonus points (up to +2):**
- Run multiple experiments (+1)
- Achieve statistical significance (+1)
- Creative experiment design (+0.5)
- Exceptional documentation (+0.5)

---

## ❓ Common Questions

**Q: Can we test multiple features at once?**  
A: No! Test ONE variable at a time. Multiple tests = can't tell which variable caused the result.

**Q: What if nobody signs up for our experiment?**  
A: That's valuable data! Document why you think it failed and what you learned. Failure is not bad—building the wrong thing is bad.

**Q: Can we use our existing prototype as the "landing page"?**  
A: Only if you're doing a fake door test. Otherwise, keep experiments SEPARATE from your MVP build.

**Q: How many people do we need to reach statistical significance?**  
A: For a landing page, aim for 30+ signups minimum. For click rates, 100+ visits minimum. Document sample size in your plan.

**Q: What if we can't find enough people in our target segment?**  
A: This might indicate your ICP is too narrow or your distribution strategy needs work. Discuss with instructor ASAP.

---

## 🎯 What's Next

**Week 9 (Next Week):**
- **Lecture:** Midterm Exam (NO LECTURE)
- **Lab 8:** Experiment Analysis & Pivot Workshop
  - Analyze experiment results
  - Decide: Build, pivot, or kill feature
  - Update roadmap based on learnings
  - Plan next experiments

**Upcoming Deadlines:**
- **Week 9 (Next Wednesday):** Midterm Exam covering Weeks 1-7
- **Week 10:** Begin MVP development (based on validated hypotheses!)

---

## 💡 Remember

> **"You can't code your way out of a bad idea. Validate first, build second."**

Experimentation is not extra work—it SAVES you weeks of wasted development time.

By next week, you should have at least ONE experiment running and collecting data. This data will inform what you actually build in Weeks 10-13.

**The best product teams spend 80% of their time learning, 20% building. Not the other way around.**

---

**Questions? Issues? Stuck?**
- Post in #lab-7-help on Discord
- Ask during lab time
- Email: [your-email@kiu.edu.ge]

**See you in Lab 8 next week with your experiment results! 🚀**
