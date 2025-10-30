# North Star Metric Definition

**Team:** [Your Team Name]  
**Date:** [Date]  
**Product:** [Your Product Name]  
**Problem Statement Reference:** See `/01-discovery/synthesis/final-problem-statement.md`

---

## What is a North Star Metric?

Your North Star Metric (NSM) is the **single metric** that best captures the core value your product delivers to users. It's the one number that, if it goes up, indicates your product is succeeding at solving the validated problem you identified in your synthesis.

**Key Characteristics:**
- ✅ Measures value delivery, not vanity metrics
- ✅ Reflects user engagement with your core solution
- ✅ Predicts long-term product success
- ✅ Aligns team around what matters most

---

## Our North Star Metric

### The Metric

**North Star Metric:** [Name of your metric]

**Formula/Calculation:** [How you'll measure it]

**Example:**
- Metric: "Weekly Active Study Sessions Completed"
- Formula: COUNT(DISTINCT user_id WHERE completed_study_session = true AND session_date WITHIN last_7_days)

---

### Why This Metric?

**Connection to Problem Statement:**  
[2-3 sentences explaining how this metric directly measures whether you're solving the validated problem from your synthesis]

**Example:**
"Our problem statement identified that students waste 2-15 hours weekly consolidating information across fragmented tools. Our NSM measures successful study sessions because each completed session represents a student finding value in our unified system instead of bouncing between 4+ apps. When this number goes up, it means we're delivering on our promise to reduce time waste."

**Value Delivery:**  
[2-3 sentences on why this metric indicates users are getting value from your product]

**Long-term Success Indicator:**  
[2-3 sentences on why growth in this metric predicts long-term product viability]

---

## Alternative Metrics Considered

### Alternative 1: [Metric Name]

**Description:** [What it measures]

**Why we considered it:** [Rationale]

**Why we rejected it:** [Reason - e.g., vanity metric, doesn't measure core value, lagging indicator]

**Example:**
- **Metric:** Total Sign-ups
- **Why considered:** Easy to measure, shows growth
- **Why rejected:** Doesn't measure actual value delivery - students could sign up and never use the product

---

### Alternative 2: [Metric Name]

**Description:** [What it measures]

**Why we considered it:** [Rationale]

**Why we rejected it:** [Reason]

---

### Alternative 3: [Metric Name]

**Description:** [What it measures]

**Why we considered it:** [Rationale]

**Why we rejected it:** [Reason]

---

## AARRR Alignment

### Where Our NSM Sits in the Funnel

**Primary Stage:** [Acquisition / Activation / Retention / Referral / Revenue]

**Why this stage:**  
[1-2 sentences on why your NSM is most closely tied to this AARRR stage]

**Example:**
"Our NSM sits in the **Activation** stage because completing a study session is our 'aha moment' - when students first experience the value of having everything in one place. This is more important than Acquisition (signups) because signup without activation means we haven't solved the problem yet."

### How NSM Impacts Other Stages

| AARRR Stage | Impact of NSM Growth |
|-------------|---------------------|
| **Acquisition** | [How NSM growth affects new user acquisition] |
| **Activation** | [How NSM growth affects user activation] |
| **Retention** | [How NSM growth affects user retention] |
| **Referral** | [How NSM growth affects referrals] |
| **Revenue** | [How NSM growth affects revenue - if applicable] |

**Example:**
- **Acquisition:** As more students complete sessions, word-of-mouth increases, driving organic acquisition
- **Activation:** This IS our activation metric
- **Retention:** Students who complete 3+ sessions per week are 4x more likely to return next week
- **Referral:** Students completing sessions are natural advocates who invite study partners
- **Revenue:** (N/A for MVP - free product)

---

## Target & Benchmarks

### Current Baseline

**Current Performance:** [Your current NSM value - if you have any early data]

**Measurement Period:** [e.g., Week 1 of Beta, Pre-launch estimate]

**Data Source:** [Where this number comes from - analytics, manual tracking, estimate]

**Example:**
- Current: 0 (not launched yet)
- Baseline estimate: Based on our 10 interviews, average student does 5 study sessions per week. If we capture 20% of KIU CS students (40 students), target = 40 students × 5 sessions × 20% engagement = 40 weekly active sessions

---

### MVP Target

**Target Value:** [Specific number you're aiming for]

**Timeframe:** [By when - e.g., End of Week 8, End of Semester]

**Rationale:** [Why this target is realistic and ambitious]

**Example:**
- Target: 100 weekly active study sessions
- Timeframe: End of Week 8 (MVP launch + 2 weeks)
- Rationale: Conservative estimate assuming 25 active users × 4 sessions/week. This validates core value proposition before scaling.

---

### Success Criteria

**Minimum Viable Success:** [What's the minimum NSM value that proves your solution works?]

**Strong Success:** [What NSM value would indicate you're ready to scale?]

**Exceptional Success:** [What NSM value would exceed expectations?]

**Example:**
- **Minimum (Validation):** 50 weekly sessions - Proves at least 10-15 students find consistent value
- **Strong (Ready to Scale):** 150 weekly sessions - Proves product-market fit with early adopters
- **Exceptional (Viral Growth):** 300+ weekly sessions - Indicates word-of-mouth is working

---

## Measurement Strategy

### How We'll Track This Metric

**Primary Tracking Method:** [e.g., Custom analytics events, Google Analytics, Mixpanel]

**Event(s) That Power This Metric:** [List specific events from your event schema]

**Example:**
- Primary Method: Custom analytics via Segment
- Key Events:
  - `study_session_started` (when user creates/joins session)
  - `study_session_completed` (when user marks session as complete)
- Calculation: COUNT(DISTINCT user_id, session_id WHERE event = 'study_session_completed' AND timestamp WITHIN last_7_days)

---

### Reporting Cadence

**How often we'll review this metric:**
- [ ] Daily
- [ ] Weekly  
- [ ] Bi-weekly
- [ ] Monthly

**Review process:** [How the team will review and discuss the metric]

**Example:**
- **Weekly** review every Monday morning
- Team reviews dashboard showing:
  - Current NSM value
  - Week-over-week change
  - Breakdown by user segment
  - Trend line since launch

---

### Dashboard & Visualization

**Where the metric lives:** [Tool/platform - e.g., Grafana, Amplitude, Google Data Studio]

**Visualization format:** [Line graph, bar chart, number card]

**Additional breakdowns:** [How you'll segment the data]

**Example:**
- Location: Grafana dashboard (link: [URL])
- Format: Line graph showing 7-day rolling average
- Breakdowns:
  - By user cohort (Week 1 users, Week 2 users, etc.)
  - By session type (individual study, group study)
  - By time of day (peak usage hours)

---

## Leading Indicators

Your North Star Metric is a **lagging indicator** - it tells you what already happened. You also need **leading indicators** that predict NSM movement.

### Leading Indicator 1: [Metric Name]

**What it measures:** [Description]

**Why it predicts NSM:** [How it leads to NSM growth]

**Target:** [What value you're aiming for]

**Example:**
- **Metric:** New User Activation Rate (% who complete first session within 48 hours)
- **Prediction:** Users who complete first session quickly are 3x more likely to become weekly active
- **Target:** 60% activation rate

---

### Leading Indicator 2: [Metric Name]

**What it measures:** [Description]

**Why it predicts NSM:** [How it leads to NSM growth]

**Target:** [What value you're aiming for]

---

### Leading Indicator 3: [Metric Name]

**What it measures:** [Description]

**Why it predicts NSM:** [How it leads to NSM growth]

**Target:** [What value you're aiming for]

---

## Relationship to Problem Statement

### Problem Statement (Reference)

**Your validated problem:** [1-sentence summary from final-problem-statement.md]

**Core user segment:** [Who experiences this problem]

**Quantified impact:** [Time/money/emotional cost]

---

### How NSM Measures Problem Solution

**If our NSM goes up, it means:**  
[2-3 bullet points connecting NSM growth to problem being solved]

**Example:**
- Students are successfully consolidating their workflow into our platform (reducing tool fragmentation)
- Users are finding enough value to return weekly (solving the "time waste" problem)
- The core promise of our problem statement is being delivered

**If our NSM stays flat or decreases, it means:**  
[2-3 bullet points on what low NSM indicates]

**Example:**
- We're not solving the core problem (students don't see value)
- Activation is happening but retention is failing (onboarding issue)
- Wrong user segment or problem validation was incorrect (need to pivot)

---

## Risks & Mitigation

### Risk 1: Gaming the Metric

**How users could game it:** [Ways the metric could be artificially inflated]

**Mitigation strategy:** [How you'll prevent gaming]

**Example:**
- **Gaming:** Students could create fake sessions to inflate numbers
- **Mitigation:** Track session duration and quality signals (notes added, materials uploaded). Filter out sessions <2 minutes.

---

### Risk 2: Metric Doesn't Reflect True Value

**Potential disconnect:** [How the metric might not capture real value delivery]

**Mitigation strategy:** [How you'll validate the metric]

**Example:**
- **Risk:** Students complete sessions but don't actually find them useful
- **Mitigation:** Quarterly user interviews asking "How much time did we save you this month?"

---

### Risk 3: [Other Risk]

**Description:** [What could go wrong]

**Mitigation:** [How you'll address it]

---

## Experimentation & Optimization

### How We'll Improve This Metric

**Hypothesis-driven approach:**  
When NSM growth slows or stalls, we'll run experiments to identify bottlenecks.

**Example experiment:**

**Hypothesis:** "If we add a 'Quick Start' tutorial, then new user activation will increase by 20%, leading to 15% NSM growth"

**Test:** A/B test with/without tutorial for 2 weeks

**Success criteria:** 20% lift in first-session completion rate

**If successful:** 15% increase in weekly active sessions within 4 weeks

---

### Planned Experiments (3-5)

1. **Experiment:** [Description]
   - **Expected NSM impact:** [Quantified prediction]
   
2. **Experiment:** [Description]
   - **Expected NSM impact:** [Quantified prediction]

3. **Experiment:** [Description]
   - **Expected NSM impact:** [Quantified prediction]

---

## Team Alignment

### How We'll Use This Metric

**In team meetings:** [How NSM will guide discussions]

**In product decisions:** [How NSM will inform prioritization]

**In roadmap planning:** [How NSM will shape what we build next]

**Example:**
- **Meetings:** Every Monday standup starts with NSM review
- **Decisions:** Any feature request must articulate expected NSM impact
- **Roadmap:** Top 3 initiatives are those with highest predicted NSM lift

---

### Accountability

**Metric owner:** [Team member name and role]

**Review cadence:** [How often we review as a team]

**Escalation criteria:** [When we need to have hard conversations]

**Example:**
- Owner: [Product Lead name]
- Review: Weekly on Mondays
- Escalation: If NSM declines 2 weeks in a row, we hold emergency strategy session

---

## Evolution of the Metric

### When We Might Change Our NSM

**Conditions that would trigger a change:**
- [ ] Problem statement pivots significantly
- [ ] User behavior shows a different "aha moment"
- [ ] Product expands to serve multiple use cases
- [ ] Current NSM stops predicting retention/success

**Example:**
"If we discover that students value our social features more than study sessions, we'd consider changing NSM to 'Weekly Active Connections Made' or similar social engagement metric."

---

### Post-MVP Evolution

**How this metric might evolve:** [Plans for future iterations]

**Example:**
"In V2, we may expand NSM to 'Weekly Value Moments' which includes study sessions, group collaborations, and resource sharing - a more holistic measure of engagement."

---

## Validation Checklist

Before finalizing this North Star Metric, verify:

- [ ] It directly measures value delivery (not vanity)
- [ ] It connects to your validated problem statement
- [ ] It's measurable with your event schema
- [ ] It's understandable by all team members
- [ ] It predicts long-term product success
- [ ] It's not easily gamed by users
- [ ] All team members agree this is THE most important metric
- [ ] You have leading indicators defined
- [ ] You have a plan to track and report it
- [ ] You know what "good" looks like (targets set)

---

## References

- **Problem Statement:** `/01-discovery/synthesis/final-problem-statement.md`
- **Event Schema:** `/02-analytics/event-schema.md`
- **Analytics Plan:** `/02-analytics/analytics-plan.md`
- **Week 5 Lecture:** AARRR Framework and Metrics

---

## Sign-off

**All team members have reviewed and agreed on this North Star Metric:**

- [Name 1] - Role - Date
- [Name 2] - Role - Date
- [Name 3] - Role - Date
- [Name 4] - Role - Date
- [Name 5] - Role - Date (if applicable)

**Program Lead final approval:**  
[Name] - Date

---

## Notes & Discussion

[Space for any additional context, debates, or decisions made during NSM selection]

---

**Remember: Your North Star Metric should be the ONE number that everyone on the team can rally around. If it's going up, you're winning. If it's flat or declining, you need to figure out why and fix it.**
