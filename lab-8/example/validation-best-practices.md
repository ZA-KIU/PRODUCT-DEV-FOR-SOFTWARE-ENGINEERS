# Validation Best Practices & Decision Frameworks

---

## The Build-Measure-Learn Cycle

```
    ┌──────────────┐
    │   IDEAS      │ Your assumptions
    └──────┬───────┘
           │
           ↓
    ┌──────────────┐
    │    BUILD     │ Minimum viable experiment
    └──────┬───────┘
           │
           ↓
    ┌──────────────┐
    │   PRODUCT    │ Smoke test, prototype, MVP
    └──────┬───────┘
           │
           ↓
    ┌──────────────┐
    │   MEASURE    │ Data collection
    └──────┬───────┘
           │
           ↓
    ┌──────────────┐
    │    DATA      │ Quantitative + qualitative
    └──────┬───────┘
           │
           ↓
    ┌──────────────┐
    │    LEARN     │ Insights & decisions
    └──────┬───────┘
           │
           ↓  (REPEAT)
    [Back to IDEAS]
```

**Key principle:** Minimize time through this loop.

---

## Hypothesis Statement Framework

### Good Hypothesis Format

**Template:**
"We believe that [target users] experience [specific problem]. If we [proposed solution], they will [measurable behavior] because [underlying motivation]."

**Example:**
"We believe that second-year CS students experience coordination chaos across multiple group projects. If we provide a single dashboard showing all project statuses, they will check it daily because they're anxious about missing deadlines and letting teammates down."

---

### Bad vs. Good Hypotheses

❌ **BAD:** "Students need better tools"
- Not testable
- No specific user
- No measurable outcome

✅ **GOOD:** "Second-year CS students in 3+ projects will sign up for our coordination tool at 15%+ rate"
- Testable
- Specific user segment
- Measurable outcome

---

## Experiment Selection Matrix

| Assumption Type | Best Experiment Method | Time to Run | Sample Size Needed |
|----------------|------------------------|-------------|-------------------|
| **Interest** (Will they care?) | Smoke test / Landing page | 1-2 weeks | 50-100 visitors |
| **Value** (Will they use it?) | Concierge MVP | 1-2 weeks | 5-10 users |
| **Usability** (Can they use it?) | Prototype test | 1 week | 5-8 users |
| **Workflow** (Does it fit?) | Wizard of Oz | 2-3 weeks | 5-10 users |
| **Willingness to pay** | Pricing experiment | 2-4 weeks | 50+ visitors |
| **Feature importance** | Fake door test | 1-2 weeks | 50+ users |

---

## Success Criteria Guidelines

### Conversion Benchmarks

**Landing page signups:**
- 20%+ = Exceptional (strong validation)
- 10-19% = Good (solid validation)
- 5-9% = Okay (weak signal, need more data)
- 2-5% = Industry average (inconclusive for MVP)
- < 2% = Problem with positioning or no demand

**Prototype usability testing:**
- 80%+ task completion = Good
- 60-79% = Needs improvement
- < 60% = Major usability issues

**Retention (Day 7):**
- 40%+ = Excellent
- 20-39% = Good
- 10-19% = Okay
- < 10% = Poor retention

---

### Sample Size Calculator

**For conversion rates:**

| Desired Confidence | Margin of Error | Min Sample Size |
|-------------------|-----------------|-----------------|
| 95% | ±10% | 100 |
| 95% | ±5% | 385 |
| 90% | ±10% | 68 |
| 90% | ±5% | 270 |

**Rule of thumb:** For MVP validation, 50-100 data points is usually sufficient.

---

## Pivot vs. Persevere Framework

### The 3 Paths

**1. PERSEVERE**
- Hypothesis validated
- Hit or exceeded success criteria
- Qualitative feedback aligns with quantitative
- Clear path to next milestone

**Action:** Build next feature, scale experiment

---

**2. ITERATE**
- Mixed results (some metrics hit, some missed)
- Qualitative insights suggest small changes would help
- Core assumption still seems valid

**Action:** Redesign experiment, test refined approach

---

**3. PIVOT**
- Hypothesis clearly invalidated
- Missed success criteria significantly
- Qualitative feedback reveals fundamental misunderstanding

**Action:** Change customer segment, problem focus, or solution approach

---

### Pivot Types

**1. Customer Segment Pivot**
- **When:** Wrong user segment
- **Example:** "Enterprise customers don't want this, but students do"

**2. Customer Need Pivot**
- **When:** Solving wrong problem
- **Example:** "They don't need status updates, they need deadline reminders"

**3. Solution Pivot**
- **When:** Solution doesn't solve problem
- **Example:** "Dashboard doesn't help, but automated summaries do"

**4. Value Capture Pivot**
- **When:** Can't monetize as planned
- **Example:** "Won't pay subscription, but will pay per-project"

**5. Technology Pivot**
- **When:** Technical approach doesn't work
- **Example:** "Real-time sync too complex, async updates sufficient"

---

## Common Validation Mistakes

### Mistake 1: Asking Instead of Observing

❌ **Wrong:** "Would you use a feature like this?"  
✅ **Right:** Give them the feature, measure if they actually use it

**Why:** People are bad at predicting future behavior. Actual behavior > stated intentions.

---

### Mistake 2: Waiting for Perfect Data

❌ **Wrong:** "We need 1000 users to be sure"  
✅ **Right:** "50 users give us directional signal to make next decision"

**Why:** Perfect is the enemy of done. In early stages, directional signals are enough.

---

### Mistake 3: Ignoring Qualitative Data

❌ **Wrong:** "15% converted, we're good"  
✅ **Right:** "15% converted AND users said it solves their problem"

**Why:** Numbers without context can mislead. Always combine quant + qual.

---

### Mistake 4: Confirmation Bias

❌ **Wrong:** "3 people liked it, let's build!"  
✅ **Right:** "3 liked it, 7 didn't—let's understand both groups"

**Why:** We naturally focus on validating data. Actively seek disconfirming evidence.

---

### Mistake 5: Changing Experiments Mid-Flight

❌ **Wrong:** "Traffic is low, let's change the messaging"  
✅ **Right:** "Traffic is low, let's boost distribution OR restart with new design"

**Why:** Changing experiments invalidates data. Either stick to plan or start fresh.

---

## Data Analysis Checklist

### Quantitative Analysis

- [ ] Compare results to success criteria
- [ ] Calculate conversion rates / completion rates
- [ ] Look for patterns over time
- [ ] Segment by user type
- [ ] Check for statistical significance (if sample allows)
- [ ] Identify outliers and investigate

---

### Qualitative Analysis

- [ ] Review all user quotes
- [ ] Identify recurring themes (3+ mentions)
- [ ] Look for strong language (emotional words)
- [ ] Note surprises (unexpected feedback)
- [ ] Distinguish features requests from needs
- [ ] Connect quotes to quantitative patterns

---

### Combined Interpretation

- [ ] Do quant and qual tell same story?
- [ ] If not, which is more reliable and why?
- [ ] What explains the gap?
- [ ] What are we most/least confident about?
- [ ] What additional data would help?

---

## Smoke Test Best Practices

### Landing Page Must-Haves

✅ **Clear headline:** One sentence, benefit-focused  
✅ **Specific problem:** User recognizes themselves  
✅ **Concrete solution:** What you're building (not vague)  
✅ **Social proof:** Interviews completed, early users, credentials  
✅ **Strong CTA:** Action verb + benefit  
✅ **Low friction:** Email only, no phone/address  
✅ **Mobile optimized:** 70% of traffic is mobile  
✅ **Fast loading:** < 3 seconds

---

### Landing Page Common Mistakes

❌ Too much text (users won't read)  
❌ Generic stock photos (looks fake)  
❌ Asking for too much info upfront  
❌ No social proof (why trust you?)  
❌ Vague value prop ("make your life better")  
❌ Broken on mobile  
❌ No clear CTA  

---

### Distribution Tactics for MVPs

**Free channels (0-5 hours):**
- Class/cohort WhatsApp groups
- University Discord servers
- In-person presentations
- Email to friends/network
- Professor announcements
- Student Facebook groups

**Paid channels (budget required):**
- Facebook ads (min $50)
- Instagram ads (min $50)
- Google ads (min $100)
- Reddit ads (hit or miss)

**Pro tip:** Exhaust free channels first. Paid ads are for scaling, not validating.

---

## User Interview Tips

### During Validation Phase

**Do:**
✅ Show prototype/mockup and observe  
✅ Ask about past behavior  
✅ Probe on specific examples  
✅ Stay quiet and listen  
✅ Record (with permission)

**Don't:**
❌ Ask "would you use this?"  
❌ Explain how it works  
❌ Defend your idea  
❌ Lead them to your desired answer  
❌ Skip the uncomfortable questions

---

### Key Questions

1. "Show me how you [do task] now"  
2. "When was the last time you [experienced problem]?"  
3. "What did you do?"  
4. "What happened?"  
5. "How did that make you feel?"  
6. [Show prototype] "Try to [accomplish task]"  
7. [Stay quiet, observe]  
8. "What confused you?"  
9. "What would you change?"  
10. "Who else should I talk to?"

---

## Metrics to Track During Validation

### Engagement Metrics

| Metric | Good | Okay | Bad |
|--------|------|------|-----|
| **Time to first action** | < 1 min | 1-3 min | > 3 min |
| **Task completion rate** | > 80% | 60-80% | < 60% |
| **Error rate** | < 5% | 5-15% | > 15% |
| **Help requests** | < 10% | 10-25% | > 25% |
| **Abandonment rate** | < 20% | 20-40% | > 40% |

---

### Behavioral Signals

**Strong positive signals:**
- User asks "when can I use this?"
- User shares with others unprompted
- User returns multiple times
- User provides detailed feedback
- User offers to pay

**Weak/negative signals:**
- User politely interested but vague
- User suggests major changes
- User doesn't return after first use
- User says "nice" but nothing specific
- User ghosts after signup

---

## Decision-Making Framework

### The 3-Question Test

Before making any pivot/persevere decision, answer:

**1. What does the DATA clearly show?**
- Not what you hope, not what might be
- Just the facts

**2. What do USERS actually SAY and DO?**
- Not what they might do
- Actual quotes and observed behavior

**3. Does this change our FUNDAMENTAL assumptions?**
- About customer, problem, or solution
- Be honest

If all 3 point same direction → High confidence decision  
If mixed signals → Need more data or pivot to something testable

---

## Validation Timeline Guide

**Week 1-2: First Experiment**
- Build smoke test
- Get 50-100 visitors
- Analyze results
- Decision: Proceed or pivot?

**Week 3-4: Second Experiment**
- Test #2 assumption
- 5-10 user sessions
- Refine based on feedback
- Decision: Continue or iterate?

**Week 5-6: Third Experiment**
- Validate workflow/usability
- Measure actual usage
- Compare to benchmarks
- Decision: Build MVP or pivot?

**Week 7-8: MVP Development**
- Build minimum feature set
- Beta with 10-20 users
- Track engagement daily
- Decision: Scale or pivot?

---

## When to Stop Validating and Start Building

**Build when:**
✅ Top 3 assumptions validated  
✅ Clear user segment identified  
✅ Repeatedly heard same pain  
✅ Users asking "when can I use this?"  
✅ Have path to 100 users  

**Keep validating when:**
❌ Mixed signals  
❌ Can't find users consistently  
❌ Users politely interested but not excited  
❌ Keep changing who target user is  
❌ No clear path to traction  

---

## Resources & Tools

### Recommended Reading
- "The Lean Startup" by Eric Ries (Chapters 5-8)
- "The Mom Test" by Rob Fitzpatrick
- "Testing Business Ideas" by Osterwalder & Pigneur
- "Hypothesis-Driven Development" by Barry O'Reilly

### Tools
- **Landing pages:** Carrd, Webflow, Typedream
- **Analytics:** Google Analytics, Mixpanel, Amplitude
- **User testing:** Maze, UserTesting, Lookback
- **Surveys:** Typeform, Google Forms
- **Heatmaps:** Hotjar, Microsoft Clarity (free)

### Calculators
- Sample size calculator: https://www.calculator.net/sample-size-calculator.html
- A/B test calculator: https://www.optimizely.com/sample-size-calculator/
- Conversion rate: Just divide signups by visitors

---

Remember: **The goal isn't to prove you're right. The goal is to learn fast and build something people actually want.**
