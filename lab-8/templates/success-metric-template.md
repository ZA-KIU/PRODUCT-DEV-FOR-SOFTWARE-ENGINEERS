# Success Metrics Template

**Team:** [Team Name]  
**Product:** [Product Name]  
**Created:** [Date]  
**Last Updated:** [Date]

---

## North Star Metric

> The ONE metric that best captures the core value you deliver to customers

**Metric:** [Name of metric]

**Definition:** [Exactly what you're measuring and how]

**Why This Metric:**  
[2-3 sentences explaining why this is the most important indicator of product success]

**Target:** [Specific number]

**Timeline:** Achieve [target] by [date]

**Current Baseline:** [Starting point if you have data]

---

## AARRR Metrics (Pirate Metrics)

### Acquisition

> How do users find you?

**Primary Metric:** [Metric name]
- **Definition:** [What counts as acquisition]
- **Target:** [X] new users per [week/month]
- **Tracking Method:** [Tool and implementation]
- **Current:** [If you have data]

**Secondary Metrics:**
- Traffic sources: [Top 3 channels]
- Cost per acquisition: [If applicable]
- Channel conversion rates: [By channel]

---

### Activation

> Do users have a great first experience?

**Primary Metric:** [Metric name - e.g., "Aha moment completion"]
- **Definition:** [What action defines activation]
- **Target:** [X]% of new users complete [action] within [timeframe]
- **Tracking Method:** [Tool and events]
- **Current:** [If you have data]

**Example:** 70% of new users add their first task within 24 hours

**Activation Flow:**
1. User signs up/lands
2. [Step 2]
3. [Step 3]
4. **Aha moment achieved** ← This is your activation metric

---

### Retention

> Do users come back?

**Primary Metric:** [Metric name]
- **Definition:** [What counts as retained]
- **Target:** [X]% of users return [timeframe] after activation
- **Tracking Method:** [Tool and cohort analysis]
- **Current:** [If you have data]

**Retention Cohorts:**
- Day 1 retention: [Target]%
- Day 7 retention: [Target]%
- Day 30 retention: [Target]%

**Example:** 60% of users who complete activation return within 7 days

---

### Revenue (or Value)

> For MVPs without revenue: What value do users get?

**If Monetized:**
- **Primary Metric:** [MRR / ARR / Transaction value]
- **Target:** [Amount] by [date]

**If Not Yet Monetized (choose one):**
- **Engagement metric:** [Time spent, features used, tasks completed]
- **Target:** [Specific behavior that indicates value]
- **Example:** Users complete average of 5 tasks per session

---

### Referral

> Do users tell others?

**Primary Metric:** [Metric name]
- **Definition:** [What counts as referral]
- **Target:** [X]% of active users invite/refer others
- **Tracking Method:** [Referral mechanism]
- **Current:** [If you have data]

**Virality Coefficient Goal:** [Number - ideally >1]

---

## Guardrail Metrics

> Metrics that shouldn't get worse while you optimize for growth

| Metric | Threshold | Why It Matters |
|--------|-----------|----------------|
| Load time | < 3 seconds | User experience |
| Error rate | < 1% | Product quality |
| [Your metric] | [Limit] | [Reason] |
| [Your metric] | [Limit] | [Reason] |

---

## Data Collection Plan

### Analytics Stack

**Platform:** [Mixpanel / Amplitude / PostHog / Custom]

**Why chosen:** [Brief justification]

**Implementation status:**
- [ ] Analytics platform set up
- [ ] Events schema defined
- [ ] Key events implemented
- [ ] Dashboard created
- [ ] Team has access

---

### Event Schema

**Link to full schema:** `03-build/analytics/event-schema.md`

**Key events being tracked:**

| Event Name | Trigger | Properties | AARRR Stage |
|------------|---------|------------|-------------|
| user_signed_up | Account created | source, timestamp | Acquisition |
| first_task_added | User adds task | task_type, timestamp | Activation |
| daily_active | User opens app | session_id, features_used | Retention |
| [Your event] | [When] | [What data] | [Stage] |

---

### Dashboard & Reporting

**Dashboard URL:** [Link when ready]

**Refresh frequency:** [Real-time / Daily / Weekly]

**Team access:** [Who can view]

**Key views:**
1. Overview dashboard: All AARRR metrics
2. Cohort analysis: Retention by signup date
3. Funnel analysis: Acquisition → Activation → Retention
4. [Custom view]: [Description]

---

## Success Criteria by Timeline

### Week 1-2 (Validation)
- [ ] [Metric]: [Target]
- [ ] [Metric]: [Target]
- [ ] **Decision point:** Does data warrant continuing?

### Week 3-4 (Early Traction)
- [ ] [Metric]: [Target]
- [ ] [Metric]: [Target]
- [ ] **Decision point:** Can we achieve product-market fit signals?

### Week 5-8 (MVP Scale)
- [ ] [Metric]: [Target]
- [ ] [Metric]: [Target]
- [ ] **Decision point:** Is this worth scaling?

### End of Semester Goals
- [ ] North Star: [Target]
- [ ] Acquisition: [Target]
- [ ] Activation: [Target]
- [ ] Retention: [Target]
- [ ] Referral: [Target]

---

## Metric Definitions & Calculations

### [Metric Name 1]

**Formula:** [How to calculate]

**Example calculation:**  
[Show actual numbers]

**Why we calculate it this way:**  
[Justification]

---

### [Metric Name 2]

**Formula:** [How to calculate]

**Example calculation:**  
[Show numbers]

**Why we calculate it this way:**  
[Justification]

---

## Benchmarks & Context

### Industry Benchmarks

| Metric | Our Target | Industry Average | Top Quartile |
|--------|----------|------------------|--------------|
| Activation rate | [X]% | [Y]% | [Z]% |
| Day 7 retention | [X]% | [Y]% | [Z]% |
| [Your metric] | [X] | [Y] | [Z] |

**Sources:** [Where benchmarks came from]

---

### Our Context

**Why our targets might differ from benchmarks:**
- [Factor 1 - e.g., student market vs. general consumer]
- [Factor 2 - e.g., early MVP vs. mature product]
- [Factor 3]

---

## Weekly Review Process

**When:** Every [day] at [time]

**Who:** [Team members]

**Format:**
1. Review dashboard (5 min)
2. Discuss trends (10 min)
3. Identify concerns (5 min)
4. Decide actions (10 min)

**Questions to ask:**
- Are we hitting our targets?
- What's trending up/down?
- Any surprises in the data?
- What should we do differently this week?

---

## Red Flags & Alerts

**Set up alerts for:**

| Condition | Alert Threshold | Action Required |
|-----------|----------------|-----------------|
| Drop in activation | Below [X]% | Investigate immediately |
| Spike in errors | Above [X]% | All hands debug |
| No new signups | Zero for 2+ days | Check marketing |
| [Your condition] | [Threshold] | [Action] |

---

## Notes & Assumptions

**Key assumptions in our metrics:**
- [Assumption 1]
- [Assumption 2]
- [Assumption 3]

**Limitations:**
- [What we can't measure yet]
- [Data quality concerns]
- [Sample size considerations]

---

## Change Log

| Date | What Changed | Why |
|------|--------------|-----|
| [Date] | Initial metrics defined | Lab 8 |
| [Date] | Adjusted activation target | Low initial conversions |
| [Date] | [Change] | [Reason] |
