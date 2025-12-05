# Lab 9: Financial Modeling & Valuation 📊
**Product Development for Software Engineers**

**Lab Date:** Thursday, December 5, 2025  
**Due Date:** Thursday, December 11th, 2025 Lab 8 / Lab 9 Homework

---

## 🎯 What You'll Build Today

1. **Calculate your unit economics** (CAC, LTV, ratios) ← Week 10 work you haven't completed yet
2. **Build a 12-month financial model** with automated projections
3. **Value your company** using VC Method and comparable companies ← Week 11 work from today's lecture
4. **Create an investor-ready valuation slide** for your pitch deck

**By the end of today, you'll have the financial foundation for your entire investor pitch.**

---

## 📚 What We're Covering

### Week 10 Content (First 30 minutes)
- ✅ Customer Acquisition Cost (CAC)
- ✅ Lifetime Value (LTV)
- ✅ LTV:CAC ratio and payback period
- ✅ 12-month financial projections

### Week 11 Content (Next 60 minutes)
- ✅ Company valuation using VC Method
- ✅ Comparable companies research
- ✅ Sensitivity analysis (3 scenarios)
- ✅ Valuation slide creation

**Why both weeks?** Labs run 1-2 weeks behind lectures. You learned unit economics in Week 10 lecture but didn't complete the work. You learned valuation in yesterday's lecture (Week 11). This lab lets you complete both!

---

## ⏱️ Today's Schedule (2 Hours)

```
0:00 - 0:10 (10 min)  → Setup & Get Started
0:10 - 0:40 (30 min)  → Part 1: Calculate Unit Economics
0:40 - 1:10 (30 min)  → Part 2: Build Financial Model & Calculate Valuation
1:10 - 1:30 (20 min)  → Part 3: Create Sensitivity Analysis
1:30 - 1:50 (20 min)  → Part 4: Make Your Valuation Slide
1:50 - 2:00 (10 min)  → Final Checks & Submit to GitHub
```

**Don't worry if you don't finish everything in lab!** You have until next Thursday to complete and polish.

---

## 📦 Materials You Need

### 📝 Templates to Fill Out:
1. **[Unit Economics Template](templates/unit-economics-template.md)** - For CAC, LTV calculations (Part 1)
2. **[Valuation Method Template](templates/company-valuation-analysis-template.md)** - For VC Method calculations (Part 2)
3. **[Comparables Analysis Template](templates/comparable-companies-template.md)** - For researching similar companies (Part 2)
4. **[Financial Model Structure Template](templates/financial-model-structure-template.md)** - Reference for spreadsheet structure

### 📖 Guides to Reference:
- **[Build Your Financial Model Guide](guides/build-your-financial-model-guide.md)** - How to auto-generate your 12-month model
- **[Professor Zeshan AI Financial Modeler](https://aistudio.google.com/apps/drive/1f4HhQVSoAEN6Q7S5s9FaBVf127vjZkdP?fullscreenApplet=true&showPreview=true&showAssistant=true)** - AI assistant for generating your model

### 🎓 Background Reading:
- Week 10 Lecture Slides: Unit Economics
- Week 11 Lecture Slides: Valuation Methods (yesterday's lecture)

---

## 🚀 Getting Started (Do This First!)

### Step 1: Gather What You Need

**From Previous Work:**
- [ ] Lab 8 validation experiment results
- [ ] Your pricing model (what you charge customers)
- [ ] Your revenue data (if you have any customers yet)
- [ ] Your cost estimates (marketing, development, operations)

**Tools You'll Use:**
- [ ] Laptop with internet access
- [ ] Google Sheets (or Excel)
- [ ] GitHub access
- [ ] Calculator
- [ ] Browser tabs: Crunchbase, TechCrunch (for research)

**Create These Folders in Your GitHub Repo:**
```bash
/04-gtm/financials/
/05-fundraising/valuation/
```

---

## 📊 Part 1: Calculate Your Unit Economics (30 min)

### What You're Doing:
Calculating the fundamental metrics that show if your business model works.

### Use This Template:
**[Unit Economics Template](templates/unit-economics-template.md)**

### You'll Calculate:

**1. CAC (Customer Acquisition Cost)** (10 min)
```
CAC = Total Sales & Marketing Spend / New Customers Acquired
```

**What to include:**
- Ad spend (Facebook, Google, etc.)
- Marketing tools (email, analytics)
- Content creation costs
- Your time (value it at $50-100/hour)

**Example:** If you spent $1,600 and got 8 customers → CAC = $200

**2. LTV (Lifetime Value)** (10 min)
```
LTV = ARPU × Gross Margin % × (1 / Churn Rate)
```

**What you need:**
- ARPU: Average revenue per user per month
- Gross Margin: (Revenue - COGS) / Revenue
- Churn Rate: % who cancel per month (use industry benchmark if you don't have data yet)

**Example:** $50 ARPU × 80% margin × (1 / 5% churn) = $800 LTV

**3. Analyze Your Ratios** (10 min)

Calculate:
- **LTV:CAC Ratio** = LTV / CAC (Target: >3:1)
- **Payback Period** = CAC / (ARPU × Gross Margin) (Target: <12 months)

**Health Check:**
- ✅ LTV:CAC > 3:1? You're healthy!
- ⚠️ LTV:CAC < 3:1? Document your improvement plan

### Save Your Work:
```
/04-gtm/financials/unit-economics.md
```

---

## 💻 Part 2: Build Your Financial Model (15 min)

### What You're Doing:
Creating an automated 12-month financial projection that uses YOUR numbers.

### Use This Guide:
**[Build Your Financial Model Guide](guides/build-your-financial-model-guide.md)**

### The Easy Way (Google Sheets Apps Script):

**Step 1:** Open new Google Sheet

**Step 2:** Go to Extensions → Apps Script

**Step 3:** Copy/paste the script from the guide (it's all there!)

**Step 4:** Customize with YOUR numbers:
- Your pricing
- Your starting customers
- Your growth rate
- Your costs (this is where your CAC calculation goes!)

**Step 5:** Run the script → Model builds automatically! ✨

**Step 6:** Update the blue cells in the "Assumptions" tab with your actual numbers

### What You Get:
- ✅ 12-month revenue projections
- ✅ Full cost breakdown
- ✅ P&L statement
- ✅ Cash flow and runway
- ✅ Automatic CAC/LTV calculations
- ✅ Dashboard with health checks

### Save Your Work:
```
/04-gtm/financials/12-month-model-link.md
(Include link to your Google Sheet)
```

---

## 🏆 Part 3: Calculate Your Valuation (30 min)

### What You're Doing:
Figuring out how much your company is worth using two methods.

### Use This Template:
**[Valuation Method Template](templates/company-valuation-analysis-template.md)**

### Method 1: VC Method (20 min)

**Step 1: Project Year 5 Revenue** (5 min)
- Start with your Year 1 revenue (from your model)
- Project forward with realistic growth rates
- Document your assumptions!

**Example:**
```
Year 1: $100K
Year 2: $300K (3x growth)
Year 3: $900K (3x growth)
Year 4: $1.8M (2x growth)
Year 5: $3.6M (2x growth)
```

**Step 2: Find Exit Multiple** (10 min)
- Research 3-5 comparable companies
- Use Crunchbase, TechCrunch, company blogs
- Calculate: Valuation / Revenue = Multiple
- Take the median

**Use this template:** [Comparables Analysis Template](templates/comparable-companies-template.md)

**Example Comparables:**
- Company A: 10x revenue multiple
- Company B: 12x revenue multiple
- Company C: 8x revenue multiple
- **Median: 10x**

**Step 3: Calculate Terminal Value** (2 min)
```
Terminal Value = Year 5 Revenue × Exit Multiple
Terminal Value = $3.6M × 10x = $36M
```

**Step 4: Apply Target ROI** (3 min)
```
Pre-Money Valuation = Terminal Value / Target ROI

For Seed stage: Use 20x ROI
$36M / 20x = $1.8M valuation
```

### Method 2: Comparables (10 min)

Sanity check using your current revenue:
```
Valuation = Current Revenue × Median Multiple
$100K × 10x = $1M
```

**Compare the two:**
- VC Method: $1.8M
- Comparables: $1M
- **Range: $1M - $1.8M** ✓

If they're more than 3x apart, recheck your assumptions!

### Save Your Work:
```
/05-fundraising/valuation/valuation-method.md
/05-fundraising/valuation/comps-analysis.md
```

---

## 🎲 Part 4: Build Sensitivity Analysis (20 min)

### What You're Doing:
Showing how your valuation changes under different scenarios.

### Create 3 Scenarios:

**Pessimistic (Conservative):**
- Lower revenue growth
- Lower exit multiple (7x instead of 10x)
- Higher ROI requirement (25x instead of 20x)
- **Example Result: $560K**

**Base Case (Most Likely):**
- Your main calculation from Part 3
- **Example Result: $1.8M**

**Optimistic (Best Case):**
- Higher growth maintained longer
- Higher exit multiple (12x)
- Lower ROI (15x)
- **Example Result: $5.6M**

### Your Final Range:
**"We're valued between $560K and $5.6M, with $1.8M as our base case."**

### Save Your Work:
```
/05-fundraising/valuation/valuation-method.md
(Add sensitivity section to same file)
```

---

## 🎨 Part 5: Create Your Valuation Slide (20 min)

### What You're Doing:
Making ONE investor-ready slide for your pitch deck.

### Required Elements:

```
┌─────────────────────────────────────┐
│     VALUATION & FUNDING ASK         │
├─────────────────────────────────────┤
│                                     │
│ Market Opportunity:                 │
│ • TAM: $__B                         │
│ • Year 5 Target: $__M               │
│                                     │
│ Valuation Analysis:                 │
│ ┌────────────────────────────┐      │
│ │ VC Method    │ $__M        │      │
│ │ Comparables  │ $__M        │      │
│ │ Range        │ $__M - $__M │      │
│ └────────────────────────────┘      │
│                                     │
│ Comparable Companies:               │
│ • Company A: 10x multiple           │
│ • Company B: 12x multiple           │
│ • Company C: 8x multiple            │
│                                     │
│ ┌───────────────────────────────┐   │
│ │ Raising $__M at $__M pre-money│   │
│ │ (~__% dilution)               │   │
│ └───────────────────────────────┘   │
└─────────────────────────────────────┘
```

### Tools You Can Use:
- Google Slides
- PowerPoint
- Canva
- Figma

**Make it professional, clean, and easy to read!**

### Save Your Work:
```
/05-fundraising/valuation-slide.pdf
OR
/05-fundraising/valuation-slide-link.md (if Google Slides)
```

---

## ✅ Final Checklist (Before You Leave Lab)

### Week 10 Deliverables (Unit Economics):
- [ ] CAC calculated with breakdown
- [ ] LTV calculated with assumptions documented
- [ ] LTV:CAC ratio and payback period analyzed
- [ ] 12-month financial model built and saved
- [ ] File saved: `/04-gtm/financials/unit-economics.md`
- [ ] File saved: `/04-gtm/financials/12-month-model-link.md`

### Week 11 Deliverables (Valuation):
- [ ] Year 5 revenue projection documented
- [ ] 3-5 comparable companies researched
- [ ] VC Method valuation calculated
- [ ] Sensitivity analysis completed (3 scenarios)
- [ ] Valuation slide created
- [ ] File saved: `/05-fundraising/valuation/valuation-method.md`
- [ ] File saved: `/05-fundraising/valuation/comps-analysis.md`
- [ ] File saved: `/05-fundraising/valuation-slide.pdf`

### Quality Check:
- [ ] All math double-checked
- [ ] Numbers consistent across all documents
- [ ] All assumptions documented
- [ ] Sources cited for comparable companies
- [ ] No typos or errors
- [ ] Professional formatting

---

## 📤 Submission Instructions

### Due: Thursday, December 11, 2025 at 11:59 PM

**What to Submit:**

1. **Push everything to GitHub:**
```
git add .
git commit -m "Lab 9: Complete financial model and valuation"
git push origin main
```

2. **Post in class Slack/Teams:**
- Share link to your valuation slide
- Brief summary: "Team [Name]: Valued at $X-Y million based on [key reason]"

3. **Verify submission:**
- Check that all files are visible in your GitHub repo
- Ensure links work (Google Sheets, Google Slides)
- Confirm your teammates can see everything

### Late Policy:
- 0-24 hours late: -10 points
- 24-48 hours late: -20 points
- >48 hours late: -40 points
- After December 12: Not accepted (too close to Week 12 pitch)

---

## 🎯 Grading (100 Points Total)

| Component | Points | What We're Looking For |
|-----------|--------|------------------------|
| **Unit Economics** | 35 | CAC, LTV correctly calculated with clear methodology |
| **Financial Model** | 25 | Complete 12-month projections with realistic assumptions |
| **Valuation Analysis** | 30 | VC Method + Comparables, good research, sensitivity analysis |
| **Presentation** | 10 | Professional slide, clean GitHub, consistent numbers |

---

## 💡 Success Tips

### Before Lab:
1. **Review your Lab 8 results** - You need this data for CAC calculation
2. **Know your pricing** - What do you charge? What's your revenue model?
3. **Bring cost estimates** - How much are you spending on marketing? Development?
4. **Come with questions** - This is complex stuff!

### During Lab:
1. **Start with the checklist** - Check off tasks as you go
2. **Ask for help early** - Don't spend 20+ minutes stuck
3. **Use the templates** - They're designed to guide you step-by-step
4. **Collaborate** - Help each other, share comparable companies
5. **Document assumptions** - Write down WHY you picked each number

### After Lab:
1. **Finish incomplete sections** - Don't just submit partial work
2. **Double-check math** - Use a calculator for all calculations
3. **Proofread everything** - Typos look unprofessional
4. **Test your links** - Make sure Google Sheets/Slides are accessible
5. **Get feedback** - Come to office hours if you're unsure

---

## 🆘 Getting Help

### During Lab:
- 🙋 Raise your hand - Professor will come to your table
- 👥 Ask classmates - Collaboration is encouraged!
- 📖 Check templates - Step-by-step instructions included
- ✅ Use checklist - Keeps you on track

### After Lab:
- **Email:** zeshan.ahmad@kiu.edu.ge
- **Slack/Teams:** #lab-9-help channel
- **1-on-1 Meetings:** Schedule if you need deep help

### Common Issues:

**"I don't have real CAC data yet"**
→ Use estimated costs + time investment valued at $50-100/hour

**"I can't find comparable companies"**
→ Search: "[your industry] startup funding [year]" on Google
→ Use Crunchbase filters
→ Ask professor for suggestions

**"My LTV:CAC ratio is terrible"**
→ Document honestly, show improvement plan
→ Better to be realistic than optimistic!

**"My two valuation methods don't match"**
→ If >3x apart, recheck your assumptions
→ Show both numbers, explain the difference

---

## ❓ Frequently Asked Questions

**Q: Do I need to finish everything in lab today?**  
A: No! Use today to make solid progress, but you have until Thursday to complete everything.

**Q: What if I don't have customers yet?**  
A: Use estimated CAC based on your planned marketing spend. Use industry benchmark churn rates. Document as "Estimated - to be validated."

**Q: Can I work on this outside of lab?**  
A: Absolutely! Many teams will need extra time to polish their work.

**Q: How detailed should my comparable company research be?**  
A: Find 3-5 companies minimum. Document their revenue, valuation, and source. Calculate the multiple. That's enough.

**Q: What if my unit economics are bad (LTV:CAC < 3:1)?**  
A: Be honest! Document your current state and your improvement plan. Investors appreciate honesty and a clear strategy.

**Q: Do I need to use the Google Sheets script or can I build manually?**  
A: Use the script! It saves hours and ensures your formulas are correct. But if you prefer Excel/manual, that's okay too.

**Q: Should I include my valuation in my pitch deck now?**  
A: Not yet! Week 12 Lab will be about building your complete pitch deck. Today you're just creating the slide that will go in it.

**Q: What if I can't run the Apps Script (permission issues)?**  
A: Use a personal Google account, not a school/work account. Or build the spreadsheet manually following the structure guide.

---

## 🎓 Learning Objectives

By completing Lab 9, you will be able to:

✅ Calculate and interpret unit economics (CAC, LTV, ratios)  
✅ Build comprehensive 12-month financial projections  
✅ Value an early-stage startup using multiple methods  
✅ Research and analyze comparable companies  
✅ Create sensitivity analyses for different scenarios  
✅ Communicate your financial story to investors  
✅ Defend your assumptions under questioning  

**These are critical skills for any founder or product manager!**

---

## 📅 What Happens Next

### Week 12 (Next Week):
- **Lecture:** Pitching, investor communication, deck structure
- **Lab 10:** Build your complete pitch deck (including today's valuation slide)

### Week 13:
- **Lecture:** Product strategy and roadmapping
- **Lab 11:** Finalize all investor materials

### Week 15:
- **Demo Day:** December 27th - Present your full pitch!

**Today's work feeds directly into your final pitch and capstone project.**

---

## 🌟 Why This Matters

**For Your Capstone:**
- Valuation slide goes in your pitch deck
- Financial model goes in your data room
- Unit economics show you understand your business model
- This is what investors REALLY care about

**For Your Career:**
- Every startup needs these financial fundamentals
- Product managers must understand unit economics
- Founders must be able to value their companies
- These skills translate to any tech company

**This lab is one of the most practical, immediately applicable things you'll do this semester!**

---

## ✨ You've Got This!

This is a lot of work, but you're not doing it alone:
- Your team is with you
- Templates guide you step-by-step
- Professor is here to help
- You have all weekend to polish

**Take it one step at a time. Follow the checklist. Ask questions. You'll do great!**

---

## 📚 Quick Links

### Templates:
- [Unit Economics Template](templates/unit-economics-template.md)
- [Valuation Method Template](templates/company-valuation-analysis-template.md)
- [Comparables Analysis Template](templates/comparable-companies-template.md)
- [Financial Model Structure Template](templates/financial-model-structure-template.md)

### Guides:
- [Build Your Financial Model Guide](guides/build-your-financial-model-guide.md)
- [AI Financial Modeler Tool](https://aistudio.google.com/apps/drive/1f4HhQVSoAEN6Q7S5s9FaBVf127vjZkdP?fullscreenApplet=true&showPreview=true&showAssistant=true)

---

## 🚀 Ready to Start?

1. ✅ Open [Unit Economics Template](templates/unit-economics-template.md)
2. ✅ Create your GitHub folders
3. ✅ Start with Part 1: Calculate your CAC!

**See you in lab! Let's build something great! 🎉**

---

**Lab 9: Financial Modeling & Valuation**  
**CS-PD-2025: Product Development for Software Engineers**  
**Kutaisi International University**  
**Professor Zeshan Ahmad**

**Questions?** zeshan.ahmad@kiu.edu.ge
