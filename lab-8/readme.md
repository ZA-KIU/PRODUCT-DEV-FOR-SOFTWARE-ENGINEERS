# Lab 8: Hypothesis-Driven Development & MVP Validation

**Week 10 | Duration:** 120 minutes (2 hours)  
**Prerequisites:** Lab 7 completed, Week 8 lecture attended  
**Repo Location:** `/03-build/experiments/` and `/03-build/validation/`

---

## 🎯 Lab Overview

You've built your technical architecture (Labs 6-7) and now it's time to answer the critical question: **Will anyone actually want what you're building?**

Today you'll apply hypothesis-driven development principles to identify your riskiest assumptions and design lean experiments to test them BEFORE investing months in building features nobody wants.

### What You'll Build Today

1. ✅ Map all assumptions underlying your MVP (15-25 assumptions)
2. ✅ Score and prioritize by risk (identify top 3 "leap of faith" assumptions)
3. ✅ Design 3 lean experiments to test those assumptions
4. ✅ Define success metrics (North Star + AARRR framework)
5. ✅ Plan your first smoke test (landing page/waitlist)
6. ✅ Create a 2-week validation sprint plan

---

## 📚 Context: Why This Matters

### The Lean Startup Approach

**Traditional approach (❌):**
1. Build entire product (3-6 months)
2. Launch to market
3. Discover nobody wants it
4. Pivot or die

**Lean approach (✅):**
1. Identify riskiest assumption (1 day)
2. Design experiment to test it (1 day)
3. Run experiment (1-2 weeks)
4. Learn and iterate
5. Build only validated features

### Real Examples

- **Dropbox:** Made video before coding anything → 75,000 signups
- **Airbnb:** Manual process, professional photos → proved demand
- **Zappos:** No inventory, manually bought shoes → validated model

**Your goal today:** Set up validation experiments so you learn fast and build right.

---

## 🗓️ Lab Structure

| Time | Part | Activity | Deliverable |
|------|------|----------|-------------|
| 0:10-0:40 | Part 1 | Hypothesis Mapping | 15-25 assumptions documented |
| 0:40-1:00 | Part 2 | Risk Prioritization | Top 3 riskiest identified |
| 1:00-1:30 | Part 3 | Experiment Design | 3 experiments planned |
| 1:30-1:50 | Part 4 | Success Metrics & Smoke Test | Metrics + smoke test plan |
| 1:50-2:00 | Part 5 | Validation Sprint Planning | 2-week sprint plan |

---

## 📋 Learning Objectives

By the end of this lab, you will be able to:

✅ **Identify assumptions** - Map all underlying product assumptions across 6 categories  
✅ **Prioritize risks** - Score assumptions by impact and confidence to find "leap of faith" assumptions  
✅ **Design experiments** - Create lean experiments with clear success criteria  
✅ **Define metrics** - Establish North Star metric and AARRR framework  
✅ **Plan validation** - Create executable 2-week validation sprint

---

## 📊 Part 1: Hypothesis Mapping (30 minutes)

**Goal:** Identify ALL assumptions your MVP is based on.

### Create File
`03-build/experiments/hypothesis-prioritization.md`

Use template: `/templates/hypothesis-prioritization-template.md`

### Process

**Step 1:** Brainstorm assumptions across 6 categories:
1. Customer Assumptions (who and how they behave)
2. Problem Assumptions (what problem you're solving)
3. Solution Assumptions (your proposed solution)
4. Value Assumptions (willingness to use/pay)
5. Technical Assumptions (feasibility)
6. Market Assumptions (market conditions)

**Step 2:** Write as "We believe that..." statements

**Step 3:** Aim for 20-25 total assumptions (4-5 per category)

**Checkpoint:** You should have 15-25 distinct, testable assumptions documented.

---

## 💰 Part 2: Risk Prioritization (20 minutes)

**Goal:** Identify your 3 riskiest "leap of faith" assumptions.

### Process

**Step 1:** Score each assumption on two dimensions:
- **Impact if Wrong** (1-5): What happens if false?
- **Confidence Level** (1-5): How sure are you it's true?

**Step 2:** Calculate Risk Score:
```
Risk Score = (6 - Confidence) × Impact
```

**Step 3:** Sort by Risk Score (highest first)

**Step 4:** Document top 3 with:
- Why it's risky
- Current evidence (or lack thereof)
- Consequences if wrong

**Checkpoint:** Top 3 assumptions identified with full rationale.

---

## 🧪 Part 3: Experiment Design (30 minutes)

**Goal:** Design 3 lean experiments to test your riskiest assumptions.

### Create File
`03-build/experiments/experiment-plan.md`

Use template: `/templates/experiment-plan-template.md`

### For Each Experiment, Define:

1. **Hypothesis Statement**  
   "We believe [assumption]. We'll know we're right when [measurable outcome]."

2. **Experiment Method**  
   Choose: Smoke test, Concierge MVP, Wizard of Oz, Prototype test, Survey

3. **Success Metrics**  
   Primary metric + threshold (e.g., "15%+ conversion rate validates")

4. **Test Procedure**  
   4 phases: Setup → Run → Measure → Analyze

5. **Timeline**  
   Specific dates, total duration (should be 1-2 weeks max)

6. **Potential Outcomes**  
   If validated / invalidated / inconclusive → next steps

**Checkpoint:** 3 complete experiment designs with all sections filled.

---

## 📈 Part 4: Success Metrics & Smoke Tests (20 minutes)

**Goal:** Define what "success" means and plan your first validation test.

### Create Files
1. `03-build/validation/success-metrics.md`
2. `03-build/validation/smoke-test-plan.md`

### Success Metrics (10 min)

**North Star Metric:** One metric that captures value delivered  
Examples: Active users, Tasks completed, Time saved

**AARRR Framework:** Set targets for:
- **Acquisition:** How users find you
- **Activation:** First valuable action
- **Retention:** Return behavior (Day 7)
- **Revenue/Value:** Engagement if not monetized
- **Referral:** Word of mouth

### Smoke Test Plan (10 min)

Design a landing page or waitlist to validate demand:
- Headline and value proposition
- 3-5 key benefits
- Call to action
- Success criteria (conversion rate threshold)
- 3 distribution channels with expected reach

**Checkpoint:** Success metrics defined and smoke test designed.

---

## 🏃 Part 5: Validation Sprint Planning (10 minutes)

**Goal:** Plan the next 2 weeks of validation work.

### Create File
`03-build/validation/validation-sprint-plan.md`

Use template: `/templates/validation-sprint-plan-template.md`

### Plan Structure

**Week 1:**
- Days 1-2: Build experiment assets
- Day 3: Launch
- Days 4-7: Monitor and collect data

**Week 2:**
- Days 1-3: Continue testing
- Day 4: Analyze results
- Day 5: Team decision (pivot/persevere)

Include:
- Daily tasks with owners
- Success criteria for sprint
- Risks and backup plans

**Checkpoint:** 2-week plan with daily breakdown complete.

---

## ✅ Lab Deliverables

Before you leave today, commit these 5 files:

- [ ] `03-build/experiments/hypothesis-prioritization.md`
- [ ] `03-build/experiments/experiment-plan.md`
- [ ] `03-build/validation/success-metrics.md`
- [ ] `03-build/validation/smoke-test-plan.md`
- [ ] `03-build/validation/validation-sprint-plan.md`

```bash
git add 03-build/experiments/ 03-build/validation/
git commit -m "Lab 8: Hypothesis-driven development plan complete"
git push origin main
```

---

## 🎯 Grading (10 points)

**Lab Participation:**
- Hypothesis Mapping: 2 pts (15+ assumptions)
- Risk Prioritization: 2 pts (all scored, top 3 identified)
- Experiment Design: 3 pts (3 complete experiments)
- Success Metrics: 2 pts (North Star + AARRR)
- Validation Sprint: 1 pt (2-week plan)

**Homework:** 100 points (due 1 week from today)  
See `LAB-8-HOMEWORK.md` for details.

---

## 📚 Resources

### Templates (in /templates/)
- hypothesis-prioritization-template.md
- experiment-plan-template.md
- success-metrics-template.md
- smoke-test-plan-template.md
- validation-sprint-plan-template.md

### Examples (in /examples/)
- smoke-test-example.md - Complete StudySync case study

### Guides (in /resources/)
- validation-best-practices.md - Comprehensive methodology guide

---

## ❓ FAQ

**Q: Can we skip validation and just build?**  
A: No. 70% of startups fail because they build things nobody wants. Validation is required.

**Q: What if we don't have users to test with yet?**  
A: That's what smoke tests are for—validate interest BEFORE building.

**Q: Our experiment will take 4 weeks. Is that okay?**  
A: No. That's not lean. Break it into a 1-2 week experiment that tests one assumption.

**Q: What if our results are negative?**  
A: That's valuable! Better to learn now in Week 10 than in Week 15 during your final demo.

---

## 🚀 What's Next

### This Week (Homework)
- Execute Experiment 1
- Collect data (minimum sample size)
- Analyze results
- Make pivot/persevere decision
- Update roadmap based on learnings

### Next Week (Lab 9)
- Unit Economics & Financial Modeling
- LTV:CAC analysis
- 12-month financial projections
- Business model validation

---

## 💡 Remember

> "The goal of a startup is to learn what customers really want, and will pay for, as quickly as possible." - Eric Ries

**You're not trying to prove you're right.**  
**You're trying to learn fast and build something people actually want.**

---

**Let's validate those assumptions! 🚀**
