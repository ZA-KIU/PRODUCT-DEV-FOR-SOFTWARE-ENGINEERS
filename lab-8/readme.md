# Lab 8: Financial Modeling & Go-to-Market Foundation

**Week 10 | Duration:** 120 minutes (2 hours)  
**Prerequisites:** Lab 7 completed, Week 10 lecture attended  
**Repo Location:** `/04-gtm/` and `/04-gtm/financials/`

---

## 🎯 Lab Overview

This week marks a critical transition in your capstone project. You've built technical foundations in Labs 6-7 (architecture, analytics, agents). Now it's time to think like a founder: **How will your product make money? How much will it cost to acquire customers? How do you prove traction?**

### What You'll Build Today

1. ✅ Calculate unit economics for your product
2. ✅ Complete LTV:CAC analysis
3. ✅ Create a 12-month financial model
4. ✅ Plan your first pricing experiment
5. ✅ Design a landing page/waitlist strategy
6. ✅ Set up traction measurement framework

---

## 📚 Context: Where We Are

### Timeline Pressure ⏰

**Weeks Remaining:** 5 weeks until final presentations

**What's at stake:**
- Week 12: Pitch deck due
- Week 13: One-pager and investor materials
- Week 15: Final demo and presentation

**Without financial clarity:**
- Can't make informed product decisions
- Can't prioritize features effectively
- Can't present credible business case

---

## 🗓️ Lab Structure

| Time | Activity | Deliverable |
|------|----------|-------------|
| 0:00-0:15 | Overview & Team Setup | Roles assigned |
| 0:15-0:45 | Unit Economics Workshop | `unit-economics.md` |
| 0:45-1:15 | LTV:CAC Analysis | `ltv-cac-analysis.md` |
| 1:15-1:45 | 12-Month Model Building | `12-month-model.xlsx` |
| 1:45-2:00 | Next Steps & Homework | Action items |

---

## 📋 Getting Started (0:00-0:15)

### Key Concepts

**Unit Economics:** Revenue and costs for ONE customer

**LTV (Lifetime Value):** Total profit from one customer over their lifetime

**CAC (Customer Acquisition Cost):** Cost to acquire one paying customer

**Golden Rule:** LTV:CAC ≥ 3:1 (earn $3 for every $1 spent)

**Payback Period:** Time to recover CAC (target: <12 months)

### Team Roles

Assign for efficiency:
- **Finance Lead:** Owns calculations and assumptions
- **Market Researcher:** Finds pricing data and benchmarks
- **Customer Lead:** References interview insights
- **Scribe:** Documents decisions and rationale

---

## 📊 Part 1: Unit Economics (0:15-0:45)

### Create `/04-gtm/financials/unit-economics.md`

Use template from `/lab-8/templates/unit-economics-template.md`

### Activities

**Step 1: Choose Monetization Model (5 min)**

Options:
- **Subscription:** $X/month recurring
- **Transaction Fee:** Y% per transaction  
- **Freemium:** Free + paid premium
- **Usage-Based:** Pay per API call/action
- **One-Time:** Single purchase price

**Step 2: Define Your Unit (5 min)**
- Be specific: "one team account (5-10 users) at $49/month"
- NOT: "a user" (too vague)

**Step 3: Calculate Revenue Per Unit (10 min)**
```
Example - Subscription:
$29/month × 12 months × (1 - churn rate)
= $29 × 12 × 0.6 = $209 annual revenue per user
```

**Step 4: Calculate Costs Per Unit (15 min)**

Direct costs (COGS):
- Cloud hosting per user
- Third-party API costs
- Support time allocated
- Payment processing fees

**Step 5: Calculate Gross Margin (5 min)**
```
Gross Margin = (Revenue - COGS) / Revenue × 100%

Target: 70-90% for SaaS
```

### Deliverable ✅

`/04-gtm/financials/unit-economics.md` with:
- Monetization model chosen
- Unit defined
- Revenue calculated
- Costs itemized
- Gross margin calculated

---

## 💰 Part 2: LTV:CAC Analysis (0:45-1:15)

### Create `/04-gtm/financials/ltv-cac-analysis.md`

Use template from `/lab-8/templates/ltv-cac-template.md`

### Activities

**Step 1: Calculate LTV (15 min)**

```
Simple Formula:
LTV = ARPU × Gross Margin % × (1 / Churn Rate)

Example:
$29/month × 76% × (1 / 0.05) = $440.80
```

**Step 2: Estimate CAC (15 min)**

Pick primary acquisition channel:

- **Content/SEO:** $50-100 per customer
- **Paid Ads:** $500-2,500 per customer
- **Outbound Sales:** $600+ per customer
- **Referral/Viral:** $20-50 per customer

Show your work and assumptions!

**Step 3: Calculate Ratio (5 min)**

```
LTV:CAC Ratio = LTV / CAC

< 1:1 = ❌ NOT VIABLE
1-3:1 = ⚠️ MARGINAL
3-5:1 = ✅ HEALTHY
> 5:1 = 🚀 EXCELLENT
```

**Step 4: Payback Period (10 min)**

```
Payback (months) = CAC / (ARPU × Gross Margin %)

Target: < 12 months
```

### Deliverable ✅

`/04-gtm/financials/ltv-cac-analysis.md` with:
- LTV calculated (assumptions documented)
- CAC estimated for primary channel
- Ratio calculated and assessed
- Payback period calculated
- Action items if ratio < 3:1

---

## 📈 Part 3: 12-Month Model (1:15-1:45)

### Create `/04-gtm/financials/12-month-model.xlsx`

Use template from `/lab-8/templates/12-month-model-template.xlsx`

### Activities

**Step 1: Set Growth Assumptions (10 min)**

**Conservative:**
- Month 3: Launch with 2 customers
- Month 6: 10 customers
- Month 12: 30 customers

**Aggressive (needs proof):**
- Month 3: Launch with 5 customers
- Month 6: 50 customers  
- Month 12: 200 customers

**Step 2: Build Model (15 min)**

Key columns:
- Month
- New Customers
- Churned Customers
- Total Active Customers
- MRR (Monthly Recurring Revenue)
- Marketing Spend
- COGS
- Gross Profit

**Step 3: Sanity Check (5 min)**

Red flags:
- ❌ 0 to 1000 customers in 3 months
- ❌ $0 marketing but rapid growth
- ❌ Profitable in Month 1

Reality checks:
- ✅ Losses early (investing in CAC)
- ✅ Gradual revenue growth
- ✅ Breakeven around Month 10-12

### Deliverable ✅

`/04-gtm/financials/12-month-model.xlsx` with:
- 12-month projections
- Realistic customer growth
- MRR trajectory
- Marketing spend tracked
- Gross profit path shown

---

## 🎬 Part 4: Wrap-up & Homework Preview (1:45-2:00)

### What You Built

Today you:
1. ✅ Defined monetization model
2. ✅ Calculated unit economics
3. ✅ Analyzed LTV:CAC
4. ✅ Created 12-month projection

### Critical Path Forward

**Week 10 (This Week):**
- ✅ Financial model complete
- 🎯 Landing page live
- 🎯 Pricing experiment running

**Week 11:**
- 🎯 Traction metrics (100+ visitors, 5+ signups)
- 🎯 One-pager draft

**Week 12-15:**
- 🎯 Pitch deck
- 🎯 Final refinements
- 🎯 Demo & presentation

### Homework Preview

**Due Monday:** Financial model refined
**Due Wednesday:** Landing page live OR pricing experiment  
**Due Friday:** Traction framework set up

See `HOMEWORK.md` for full details.

---

## 📚 Resources

### Templates
- `/lab-8/templates/unit-economics-template.md`
- `/lab-8/templates/ltv-cac-template.md`
- `/lab-8/templates/12-month-model-template.xlsx`
- `/lab-8/templates/pricing-experiment-template.md`
- `/lab-8/templates/landing-page-template.md`

### Examples
- `/lab-8/examples/sample-unit-economics.md`
- `/lab-8/examples/sample-ltv-cac.md`
- `/lab-8/examples/sample-financial-model.xlsx`

### Reading
- SaaS Metrics 2.0 by David Skok (LTV/CAC section)
- Sequoia Business Plan Template (Financial section)

---

## ❓ FAQ

**Q: Our product will be free. Do we still need this?**
A: Yes! Calculate cost per user and show sustainability path (grants, future monetization).

**Q: All our numbers are guesses. Is that okay?**
A: Yes, WITH documentation. "Assumption: 5% churn based on industry average [source]."

**Q: Our LTV:CAC is 0.5:1. What do we do?**
A: Three options: (1) Lower CAC, (2) Raise LTV, (3) Pivot pricing model.

**Q: How do we estimate churn with zero customers?**
A: Use industry benchmarks: B2B SaaS 5-7%, Consumer 15-25%. Document source.

---

## 🎯 Success Criteria

By end of lab:

- [ ] Unit economics complete with all calculations
- [ ] LTV calculated with documented assumptions
- [ ] CAC estimated for chosen channel
- [ ] LTV:CAC ratio calculated (plan if < 3:1)
- [ ] 12-month model with realistic projections
- [ ] Team ready for homework deliverables

---

**Let's build businesses that make financial sense. 💰🚀**
