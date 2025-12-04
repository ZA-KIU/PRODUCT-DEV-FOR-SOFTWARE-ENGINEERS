# 12-Month Financial Model - Spreadsheet Structure
**Team Name:** [Your Team Name]  
**Product:** [Your Product Name]

---

## 📊 Spreadsheet Setup Instructions

**Create a Google Sheet or Excel file with the following tabs:**

1. **Instructions** - This guide
2. **Assumptions** - All your key assumptions
3. **Revenue Model** - Customer acquisition & revenue projections
4. **Cost Model** - All expenses month-by-month
5. **P&L (Profit & Loss)** - Combined view
6. **Unit Economics** - CAC, LTV, ratios
7. **Cohort Analysis** - Customer retention by cohort
8. **Dashboard** - Visual summary

---

## TAB 1: Instructions

**What to put here:**
- Link to this Lab 9 guide
- Your team member names and roles
- Last updated date
- Key contact for questions about the model
- Version history

---

## TAB 2: Assumptions

**Create a table like this:**

| Category | Assumption | Value | Source | Confidence |
|----------|------------|-------|---------|------------|
| **PRICING** | | | | |
| Monthly subscription price | | $____ | [Lab X] | High/Med/Low |
| Annual discount % | | ___% | Industry | High/Med/Low |
| Average contract length | | ___ months | Estimate | High/Med/Low |
| **GROWTH** | | | | |
| Starting customers (Month 1) | | ___ | Current | High |
| Monthly customer growth % | | ___% | Projection | High/Med/Low |
| Growth acceleration/deceleration | | | | |
| **CHURN** | | | | |
| Monthly churn rate | | ___% | Industry benchmark | Low |
| When churn starts | | Month ___ | Assumption | Med |
| **COSTS** | | | | |
| COGS per customer % | | ___% | Estimate | Med |
| CAC (per customer) | | $____ | Lab 9 calculation | High |
| Developer salary | | $____/mo | Market rate | High |
| Marketing budget growth | | ___% MoM | Plan | Med |
| **FUNDING** | | | | |
| Starting cash | | $____ | Current | High |
| Funding to raise | | $____ | To be decided | Med |
| Funding timing | | Month ___ | To be decided | Low |

**Why document assumptions:**
- Easy to update if things change
- Shows investors you're thoughtful
- Makes it clear what's fact vs. estimate

---

## TAB 3: Revenue Model

**Column Structure:**

```
Month 1 | Month 2 | Month 3 | ... | Month 12
```

**Rows to include:**

### A. Customer Acquisition
1. New customers acquired
2. Churned customers (from previous months)
3. Net new customers
4. Total active customers (cumulative)

### B. Revenue Calculations
5. MRR from new customers (New customers × Price)
6. MRR from existing customers ((Active - New) × Price)
7. Total MRR (Monthly Recurring Revenue)
8. One-time revenue (if applicable)
9. **Total Revenue**

### C. Growth Metrics
10. MoM growth %
11. Customer count growth %
12. ARPU (Average Revenue Per User)

---

### Example Month 1 Calculations:

**Assumptions:**
- Monthly price: $50
- Starting customers: 10
- Growth rate: 20% per month
- Churn: 0% (starts Month 3)

**Month 1:**
```
New customers acquired: 10
Churned customers: 0
Net new: 10
Total active: 10

MRR from new: 10 × $50 = $500
MRR from existing: 0 × $50 = $0
Total MRR: $500
One-time revenue: $0
Total Revenue: $500

MoM growth: N/A (first month)
Customer growth: N/A
ARPU: $500 / 10 = $50
```

**Month 2:**
```
New customers acquired: 12 (20% growth)
Churned customers: 0
Net new: 12
Total active: 22

MRR from new: 12 × $50 = $600
MRR from existing: 10 × $50 = $500
Total MRR: $1,100
One-time revenue: $0
Total Revenue: $1,100

MoM growth: ($1,100 - $500) / $500 = 120%
Customer growth: (22 - 10) / 10 = 120%
ARPU: $1,100 / 22 = $50
```

---

## TAB 4: Cost Model

**Column Structure:** Same as Revenue (Month 1 - Month 12)

**Rows to include:**

### A. Cost of Goods Sold (COGS)
1. Hosting/infrastructure costs
2. API costs (if applicable)
3. Support costs
4. Payment processing fees
5. **Total COGS**
6. **COGS per customer** (Total COGS / Active customers)
7. **Gross margin %** ((Revenue - COGS) / Revenue)

### B. Sales & Marketing
8. Ad spend (Facebook, Google, etc.)
9. Marketing tools (email, analytics)
10. Content creation
11. Sales team salaries
12. Events/conferences
13. **Total S&M**
14. **S&M per customer** (Total S&M / New customers acquired)

### C. Research & Development
15. Developer salaries
16. Designer salaries
17. PM salaries
18. Development tools & software
19. **Total R&D**

### D. General & Administrative
20. Office rent (if applicable)
21. Legal/accounting
22. Insurance
23. Administrative software
24. Miscellaneous
25. **Total G&A**

### E. Total Costs
26. **Total Operating Expenses** (S&M + R&D + G&A)
27. **Total Costs** (COGS + OpEx)

---

### Example Month 1 Costs:

**With 10 customers and $500 revenue:**

```
COGS:
- Hosting: $50
- APIs: $20
- Support: $30
- Payment processing (3%): $15
Total COGS: $115
COGS per customer: $115 / 10 = $11.50
Gross margin: ($500 - $115) / $500 = 77%

Sales & Marketing:
- Ad spend: $500
- Marketing tools: $100
- Content: $200
- Sales salaries: $0 (founders doing it)
Total S&M: $800
S&M per customer: $800 / 10 = $80 (this is your CAC!)

Research & Development:
- Developer salary: $4,000
- Tools: $200
Total R&D: $4,200

General & Administrative:
- Legal: $200
- Software: $100
Total G&A: $300

Total Operating Expenses: $800 + $4,200 + $300 = $5,300
Total Costs: $115 + $5,300 = $5,415
```

---

## TAB 5: P&L (Profit & Loss)

**This combines Revenue and Cost tabs:**

**Column Structure:** Month 1 - Month 12

**Rows:**

```
Revenue:
1. Total Revenue                    [From Revenue tab]
2. - Total COGS                     [From Cost tab]
3. = Gross Profit                   [Row 1 - Row 2]
4. Gross Margin %                   [Row 3 / Row 1]

Operating Expenses:
5. Sales & Marketing                [From Cost tab]
6. Research & Development           [From Cost tab]
7. General & Administrative         [From Cost tab]
8. = Total OpEx                     [Rows 5+6+7]

9. = EBITDA                         [Row 3 - Row 8]
10. EBITDA Margin %                 [Row 9 / Row 1]

Cash Flow:
11. Starting cash balance           [Previous month ending or initial $]
12. + Cash in (revenue)             [Row 1]
13. - Cash out (costs)              [Row 2 + Row 8]
14. + Funding raised (if any)       [From assumptions]
15. = Ending cash balance           [11+12-13+14]

Metrics:
16. Monthly burn rate               [Row 13 - Row 12]
17. Runway (months)                 [Row 15 / Row 16]
18. Customers                       [From Revenue tab]
19. MRR                            [From Revenue tab]
20. CAC                            [S&M / New customers]
21. Payback period (months)         [CAC / (ARPU × GM%)]
```

---

### Example Month 1 P&L:

```
Revenue:
1. Total Revenue: $500
2. Total COGS: $115
3. Gross Profit: $385
4. Gross Margin: 77%

Operating Expenses:
5. S&M: $800
6. R&D: $4,200
7. G&A: $300
8. Total OpEx: $5,300

9. EBITDA: $385 - $5,300 = -$4,915
10. EBITDA Margin: -983% (losing money, normal for early stage!)

Cash Flow:
11. Starting cash: $50,000 (example)
12. Cash in: $500
13. Cash out: $5,415
14. Funding raised: $0
15. Ending cash: $50,000 + $500 - $5,415 = $45,085

Metrics:
16. Burn rate: $5,415 - $500 = $4,915/month
17. Runway: $45,085 / $4,915 = 9.2 months
18. Customers: 10
19. MRR: $500
20. CAC: $80
21. Payback: $80 / ($50 × 77%) = 2.1 months
```

---

## TAB 6: Unit Economics

**This pulls key metrics from other tabs:**

**Create a summary table:**

| Metric | Month 1 | Month 3 | Month 6 | Month 12 | Notes |
|--------|---------|---------|---------|----------|-------|
| **Revenue Metrics** | | | | | |
| MRR | $500 | | | | |
| ARPU | $50 | | | | |
| Total customers | 10 | | | | |
| **Cost Metrics** | | | | | |
| CAC | $80 | | | | S&M / New customers |
| COGS per customer | $11.50 | | | | |
| **Unit Economics** | | | | | |
| Gross margin % | 77% | | | | |
| LTV (estimated) | $______ | | | | From Lab 9 calc |
| LTV:CAC ratio | ___:1 | | | | |
| Payback period (mo) | 2.1 | | | | |
| **Business Health** | | | | | |
| Monthly churn % | 0% | | | | |
| MRR growth % | N/A | | | | |
| Burn rate | $4,915 | | | | |
| Runway (months) | 9.2 | | | | |

**Color coding:**
- 🟢 Green: Metric is healthy
- 🟡 Yellow: Metric needs attention
- 🔴 Red: Metric is concerning

---

## TAB 7: Cohort Analysis

**Track retention by signup month:**

**Structure:**

```
        | Month 0 | Month 1 | Month 2 | Month 3 | Month 6 | Month 12 |
--------|---------|---------|---------|---------|---------|----------|
Oct     | 100%    | 95%     | 90%     | 87%     | 80%     | 70%      |
Nov     | 100%    | 95%     | 92%     | 88%     | ?       | ?        |
Dec     | 100%    | 96%     | ?       | ?       | ?       | ?        |
```

**Month 0 = Signup month (always 100%)**  
**Month 1 = Next month retention**  
**Month 2 = Two months after signup**  

**Calculate:**
- Average retention by month: (Oct M1 + Nov M1 + Dec M1) / 3
- Churn rate: 100% - Retention %

**Example:**
```
If Month 1 retention average = 95%
Then Month 1 churn = 5%

This 5% becomes your churn assumption for LTV calculation!
```

---

## TAB 8: Dashboard (Visual Summary)

**Create these visualizations:**

### 1. Revenue Growth Chart
- Line graph: MRR over 12 months
- Y-axis: $ MRR
- X-axis: Months

### 2. Customer Growth Chart
- Line graph: Total customers over 12 months
- Y-axis: # Customers
- X-axis: Months

### 3. Cash Runway Chart
- Line graph: Cash balance over 12 months
- Y-axis: $ Cash
- X-axis: Months
- Add horizontal line for "$0" to show when you run out

### 4. Unit Economics Summary (Text Box)
```
┌─────────────────────────────────────┐
│   KEY METRICS (Month 12)            │
├─────────────────────────────────────┤
│ MRR: $________                      │
│ Customers: _____                    │
│ CAC: $______                        │
│ LTV: $______                        │
│ LTV:CAC: ____:1                     │
│ Payback: ____ months                │
│ Runway: ____ months                 │
│ Break-even: Month ____              │
└─────────────────────────────────────┘
```

### 5. Cost Breakdown (Pie Chart)
- COGS: ____%
- S&M: ____%
- R&D: ____%
- G&A: ____%

---

## 🎯 Key Formulas to Use

**In Google Sheets / Excel:**

### Revenue Calculations:
```
Total Revenue = MRR + One-time revenue
MRR = Active customers × Price
ARPU = Total Revenue / Active customers
MoM growth % = (This month - Last month) / Last month
```

### Cost Calculations:
```
Gross Margin % = (Revenue - COGS) / Revenue
CAC = Total S&M / New customers acquired
COGS per customer = Total COGS / Active customers
```

### Cash Flow:
```
Burn rate = Total costs - Total revenue
Runway = Current cash / Burn rate
```

### Unit Economics:
```
LTV = ARPU × Gross Margin × (1 / Churn rate)
LTV:CAC = LTV / CAC
Payback period = CAC / (ARPU × Gross Margin)
```

---

## ✅ Validation Checklist

Before submitting, check:

**Formulas:**
- [ ] All formulas are correct (no #REF! or #DIV/0! errors)
- [ ] Revenue formulas link correctly to assumptions
- [ ] Cost formulas pull from right places
- [ ] P&L balances (Revenue - Costs = EBITDA)
- [ ] Cash flow math is correct

**Logic:**
- [ ] Customers can't go negative
- [ ] Churn can't be more than 100%
- [ ] Growth rates are realistic
- [ ] Costs scale with customer growth
- [ ] Revenue grows faster than costs (eventually)

**Completeness:**
- [ ] All 12 months filled out
- [ ] All tabs complete
- [ ] Dashboard shows key metrics
- [ ] Assumptions documented
- [ ] Sources cited

**Realism:**
- [ ] Numbers are defendable
- [ ] Growth isn't too optimistic
- [ ] Costs aren't underestimated
- [ ] Matches your actual experiments/traction

---

## 💡 Pro Tips

### 1. Use Named Ranges
Instead of cell references like `B23`, name them:
- `monthly_price`
- `growth_rate`
- `churn_rate`

Makes formulas readable: `=active_customers * monthly_price`

### 2. Color Code Assumptions
- Blue text = Hard-coded numbers (you input)
- Black text = Calculated (formulas)
- Red text = Needs attention/decision

### 3. Build Scenarios
Create 3 versions:
- Pessimistic (slower growth, higher costs)
- Base (your realistic projection)
- Optimistic (faster growth, lower costs)

Toggle between them with dropdown

### 4. Add Comments
Use spreadsheet comments to explain:
- Why you picked that number
- Source of data
- What could change it

### 5. Link to Real Data
If you have a dashboard (Mixpanel, Google Analytics):
- Reference actual metrics
- Show the link
- Update model monthly with real data

---

## 📤 File Naming & Location

**Save as:**
```
[TeamName]-Financial-Model-12mo.xlsx
OR
[TeamName]-Financial-Model-12mo (Google Sheets link)
```

**Save to:**
```
/04-gtm/financials/12-month-model.xlsx
OR
/04-gtm/financials/12-month-model-link.md (with Google Sheets URL)
```

---

## 🆘 Common Mistakes to Avoid

### 1. "Hockey Stick" Growth
❌ Don't assume 100% MoM growth forever  
✅ Show it slowing down over time (50% → 30% → 20% → 10%)

### 2. Underestimating Costs
❌ Forgetting about payment processing, taxes, insurance  
✅ Add 10-15% buffer for "miscellaneous"

### 3. Overestimating Retention
❌ Assuming 0% churn for 12 months  
✅ Use industry benchmarks, be conservative

### 4. Not Scaling Costs
❌ Same costs in Month 1 and Month 12  
✅ Hiring, infrastructure, support all scale with customers

### 5. Ignoring Seasonality
❌ Every month is the same  
✅ Consider holidays, summer, academic calendar, etc.

---

## 📊 Example Completed Model Reference

**See instructor's example:**
- Example-Team-Financial-Model.xlsx
- Shows all tabs filled out
- Comments explain key decisions
- Use as template, DON'T COPY numbers

---

**Questions?**
- Ask during lab
- Office hours: Tuesdays 2-4 PM
- Email: zeshan.ahmad@kiu.edu.ge

**Good luck! 🚀**
