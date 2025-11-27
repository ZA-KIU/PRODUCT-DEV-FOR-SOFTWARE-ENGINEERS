# Hypothesis Prioritization Template

**Team:** [Team Name]  
**Date:** [Date]  
**Created By:** [Names]

---

## Instructions

1. **Brainstorm** all assumptions (aim for 20+)
2. **Score** each on Impact (1-5) and Confidence (1-5)
3. **Calculate** Risk Score = (6 - Confidence) × Impact
4. **Rank** by risk score
5. **Select** top 3 for testing

---

## Customer Assumptions

> Assumptions about WHO your customers are and HOW they behave

**Example:** "We believe CS students check their team project status at least once per day"

| # | Assumption | Impact | Confidence | Risk Score |
|---|------------|--------|------------|------------|
| C1 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |
| C2 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |
| C3 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |

---

## Problem Assumptions

> Assumptions about the PROBLEM you're solving

**Example:** "We believe students waste 15+ minutes per day on project coordination"

| # | Assumption | Impact | Confidence | Risk Score |
|---|------------|--------|------------|------------|
| P1 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |
| P2 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |
| P3 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |

---

## Solution Assumptions

> Assumptions about your PROPOSED SOLUTION

**Example:** "We believe a simple dashboard will be easier to use than current tools"

| # | Assumption | Impact | Confidence | Risk Score |
|---|------------|--------|------------|------------|
| S1 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |
| S2 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |
| S3 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |

---

## Value Assumptions

> Assumptions about willingness to USE or PAY

**Example:** "We believe students will switch from WhatsApp to our tool"

| # | Assumption | Impact | Confidence | Risk Score |
|---|------------|--------|------------|------------|
| V1 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |
| V2 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |
| V3 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |

---

## Technical Assumptions

> Assumptions about TECHNICAL FEASIBILITY

**Example:** "We believe we can build real-time sync in 2 weeks"

| # | Assumption | Impact | Confidence | Risk Score |
|---|------------|--------|------------|------------|
| T1 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |
| T2 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |
| T3 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |

---

## Market Assumptions

> Assumptions about MARKET CONDITIONS and COMPETITION

**Example:** "We believe there's no good solution for student project coordination"

| # | Assumption | Impact | Confidence | Risk Score |
|---|------------|--------|------------|------------|
| M1 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |
| M2 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |
| M3 | We believe that [assumption statement] | [1-5] | [1-5] | [score] |

---

## Risk Score Calculation Guide

### Impact if Wrong (1-5)
- **5 = Critical:** Product completely fails if wrong
- **4 = Major:** Requires significant pivot
- **3 = Moderate:** Requires feature changes
- **2 = Minor:** Requires adjustment
- **1 = Minimal:** Negligible impact

### Confidence Level (1-5)
- **5 = Very High:** Validated with strong evidence (10+ data points)
- **4 = High:** Good evidence (5-9 data points)
- **3 = Medium:** Some evidence, not conclusive
- **2 = Low:** Anecdotal evidence only
- **1 = Very Low:** Pure guess, no evidence

### Risk Score = (6 - Confidence) × Impact

Higher risk score = more urgent to test

---

## Priority Rankings

**Sort all assumptions by Risk Score (highest first):**

| Rank | ID | Assumption | Impact | Conf | Risk | Category |
|------|----|------------|--------|------|------|----------|
| 1 | [ID] | [Brief statement] | 5 | 2 | 20 | [Cat] |
| 2 | [ID] | [Brief statement] | 4 | 2 | 16 | [Cat] |
| 3 | [ID] | [Brief statement] | 5 | 3 | 15 | [Cat] |
| 4 | [ID] | [Brief statement] | 4 | 3 | 12 | [Cat] |
| 5 | [ID] | [Brief statement] | 3 | 3 | 9 | [Cat] |
| ... | ... | ... | ... | ... | ... | ... |

---

## Top 3 Riskiest Assumptions

### 🔴 Priority #1: [Assumption Title]

**Full Statement:**  
We believe that [complete assumption statement]

**Category:** [Customer / Problem / Solution / Value / Technical / Market]

**Why This is Risky:**
- **Impact if wrong (5):** [Explain consequences]
- **Confidence level (2):** [What evidence do we have? Why low confidence?]
- **Risk score: 20**

**Current Evidence:**
- [What we know so far]
- [Sources of information]
- [Gaps in our knowledge]

**If This is Wrong:**
- [Major consequence 1]
- [Major consequence 2]
- [What would need to change]

---

### 🟡 Priority #2: [Assumption Title]

**Full Statement:**  
We believe that [complete assumption statement]

**Category:** [Customer / Problem / Solution / Value / Technical / Market]

**Why This is Risky:**
- **Impact if wrong ([1-5]):** [Explain]
- **Confidence level ([1-5]):** [Explain]
- **Risk score: [score]**

**Current Evidence:**
- [What we know]

**If This is Wrong:**
- [Consequences]

---

### 🟢 Priority #3: [Assumption Title]

**Full Statement:**  
We believe that [complete assumption statement]

**Category:** [Customer / Problem / Solution / Value / Technical / Market]

**Why This is Risky:**
- **Impact if wrong ([1-5]):** [Explain]
- **Confidence level ([1-5]):** [Explain]
- **Risk score: [score]**

**Current Evidence:**
- [What we know]

**If This is Wrong:**
- [Consequences]

---

## Testing Strategy

**Order of Testing:**
1. Test Priority #1 first (highest risk)
2. Test Priority #2 second
3. Test Priority #3 third
4. Reassess and rerank after each test

**Rationale:**
[Why testing in this order makes sense for your product]

---

## Decision Criteria

**When to pivot:**
- If Priority #1 is invalidated → [Major pivot needed]
- If Priority #2 is invalidated → [Moderate changes needed]
- If Priority #3 is invalidated → [Minor adjustments]

**When to persevere:**
- All top 3 validated → Full speed ahead on build
- 2 of 3 validated → Proceed with caution, iterate on weak point
- 1 of 3 validated → Serious reconsideration needed

---

## Notes & Observations

[Any additional thoughts, team discussions, or context]

---

## Change Log

| Date | Change | Reason |
|------|--------|--------|
| [Date] | Initial prioritization | Lab 8 exercise |
| [Date] | Updated after Experiment 1 | [Learning from results] |
