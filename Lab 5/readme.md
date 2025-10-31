# Lab 5: Problem Synthesis & Analytics Planning
## Student Guide - Week 5 Homework

**Due:** Friday, November 7th Week 5, 11:59 PM  
**Total Deliverables:** 6 files  
**Estimated Time:** 9-12 hours  
**Total Points:** 25 points (+ 5 participation = 30 total)

---

## 🎯 What You're Doing This Week

This week is the **most important week** of the semester. You're going to:

1. **Validate your problem** (through synthesis of your 10 interviews)
2. **Plan how to measure success** (through analytics design)

Everything you build for the next 10 weeks depends on getting this right.

**Get this right** → Build something people actually need and can measure  
**Get this wrong** → Waste 10 weeks building the wrong thing or can't tell if it works

---

## 📦 What You're Submitting (6 Files)

### PART A: Synthesis (20 points)
Transform your 10 interview logs into a validated problem statement.

**Folder:** `/01-discovery/synthesis/`

1. **affinity-map.md** (5 pts) - 60-90 min
2. **patterns-analysis.md** (7 pts) - 90-120 min
3. **final-problem-statement.md** (8 pts) - 90-120 min

### PART B: Analytics (5 points - NEW!)
Plan how you'll measure if your solution actually works.

**Folder:** `/02-analytics/` (create this folder!)

4. **north-star-metric.md** (3 pts) - 45-60 min
5. **event-schema.md** (4 pts) - 60-90 min
6. **analytics-plan.md** (5 pts) - 90-120 min

---

## 🗂️ Your Repo Structure (After This Week)

```
your-team-repo/
│
├── 00-foundation/
│   ├── team-contract.md
│   ├── team-problem-statement.md
│   └── team-icp.md
│
├── 01-discovery/
│   ├── interview-logs/
│   │   ├── interview-01.md
│   │   ├── interview-02.md
│   │   └── ... (8-10 total)
│   │
│   └── synthesis/                    ← YOU CREATE THIS IN LAB
│       ├── affinity-map.md           ← DELIVERABLE 1
│       ├── patterns-analysis.md      ← DELIVERABLE 2
│       └── final-problem-statement.md ← DELIVERABLE 3
│
└── 02-analytics/                     ← YOU CREATE THIS FOR HOMEWORK
    ├── north-star-metric.md          ← DELIVERABLE 4
    ├── event-schema.md               ← DELIVERABLE 5
    └── analytics-plan.md             ← DELIVERABLE 6
```

---

## 📋 Part A: Synthesis (4-6 hours)

### What You Did in Lab (Friday)

You spent 2 hours in lab doing:
- Reviewing all 10 interview logs together
- Creating an affinity map (50-100 sticky notes clustered into themes)
- Identifying patterns (frequency + intensity)
- Starting your problem statement draft

### What You Do for Homework

Now you **document** and **finalize** that work.

---

### Deliverable 1: Affinity Map Documentation

**File:** `/01-discovery/synthesis/affinity-map.md`  
**Template:** [Download here](computer:///mnt/user-data/outputs/Lab-5-COMPLETE-WITH-ANALYTICS/templates/affinity-map-template.md)  
**Time:** 60-90 minutes  
**Worth:** 5 points

**What to include:**
- Photos or screenshots of your affinity map from lab
- List all your clusters (5-8 clusters)
- For each cluster, include 3-5 sample quotes from interviews
- Short reflection on your process

**Tips:**
- Take clear photos if you used physical sticky notes
- If digital (Miro/FigJam), export or screenshot the board
- Make sure interviewee IDs are visible (P001, P002, etc.)
- Write brief descriptions of what each cluster represents

**Common mistakes to avoid:**
❌ Forgetting to take photos of your physical board  
❌ Not documenting which interviews mentioned each theme  
❌ Vague cluster names like "Problem 1" instead of "WhatsApp message overload"

---

### Deliverable 2: Patterns Analysis

**File:** `/01-discovery/synthesis/patterns-analysis.md`  
**Template:** [Download here](computer:///mnt/user-data/outputs/Lab-5-COMPLETE-WITH-ANALYTICS/templates/patterns-analysis-template.md)  
**Time:** 90-120 minutes  
**Worth:** 7 points

**What to include:**
- **Frequency table:** Count how many interviews mentioned each cluster
- **Intensity ratings:** Rate emotional impact (High 🔥 / Medium 😐 / Low 😶)
- **Root cause analysis:** Use "5 Whys" for your top 3-5 patterns
- **Current workarounds:** What do people do today?

**Example frequency table:**
| Cluster | # Interviews | # Quotes | Intensity |
|---------|-------------|----------|-----------|
| WhatsApp overload | 8/10 | 12 | 🔥 High |
| Last-minute panic | 9/10 | 15 | 🔥 High |
| Unclear ownership | 7/10 | 10 | 😐 Medium |

**Tips:**
- Be honest about the data - if a pattern only appeared in 2/10 interviews, that's a weak pattern
- Focus your root cause analysis on HIGH frequency AND HIGH intensity patterns
- The 5 Whys technique: Keep asking "why?" until you get to the real underlying cause

**Common mistakes to avoid:**
❌ Confusing symptoms with root causes ("students are stressed" is a symptom, not a root cause)  
❌ Guessing numbers instead of actually counting interviews  
❌ Picking patterns YOU like instead of what the DATA shows

---

### Deliverable 3: Final Problem Statement

**File:** `/01-discovery/synthesis/final-problem-statement.md`  
**Template:** [Download here](computer:///mnt/user-data/outputs/Lab-5-COMPLETE-WITH-ANALYTICS/templates/final-problem-statement-template.md)  
**Time:** 90-120 minutes  
**Worth:** 8 points

**What to include:**
- **Your problem statement** following the template:
  > "[Specific user segment] [lose/waste/experience] [quantified impact] because [root cause] [in context], leading to [consequences]."
  
- **8+ supporting quotes** from your interviews
- **Decision:** Did you KEEP, REFINE, or PIVOT from your Week 2 problem?
- **Confidence assessment:** How sure are you this is the right problem?

**Example problem statement:**
> "KIU CS students working on group projects miss 30-40% of milestones because they lack shared visibility into task ownership and deadlines across fragmented tools (LMS, WhatsApp, Discord), leading to last-minute scrambles, duplicated work, and grade penalties."

**What makes a GOOD problem statement:**
- ✅ Specific user segment (not "students" but "KIU CS students in group projects")
- ✅ Quantified impact (30-40% of milestones, not just "struggle")
- ✅ Root cause identified (lack of visibility, not "are confused")
- ✅ Context specified (group projects, not "always")
- ✅ Real consequences (grade penalties, not "annoyed")

**Tips:**
- Every claim should cite specific interviews: "Validated by P001, P002, P003..."
- Include powerful verbatim quotes that support your statement
- Be honest about your confidence level - if you're not sure, say why
- If pivoting, explain clearly why your original problem wasn't validated

**Common mistakes to avoid:**
❌ Too vague: "Students have trouble with organization"  
❌ Not quantified: "Students waste time" (how much time?)  
❌ No context: "Students can't find study spots" (when? where? which students?)  
❌ Weak evidence: Only citing 3-4 interviews instead of 8+

---

## 📊 Part B: Analytics (5-6 hours)

### Why Analytics Matters

You validated your problem. Now you need to know:
- **Did we solve it?** (Need metrics to measure success)
- **Are people using our solution?** (Need events to track behavior)
- **What's working and what's not?** (Need dashboard to see data)

Without analytics, you're building blind. You won't know if your MVP actually helps.

---

### Deliverable 4: North Star Metric

**File:** `/02-analytics/north-star-metric.md`  
**Template:** [Download here](computer:///mnt/user-data/outputs/Lab-5-COMPLETE-WITH-ANALYTICS/templates/north-star-metric-template.md)  
**Time:** 45-60 minutes  
**Worth:** 3 points

**What to include:**
- **Your North Star Metric:** The ONE number that shows your product is working
- **Why this metric:** How it connects to your problem statement
- **Targets:** What "good" looks like (MVP target)
- **How you'll measure it:** Which events power this metric

**Example:**
- **NSM:** Weekly Active Study Sessions Completed
- **Why:** Each completed session means a student used our unified system instead of bouncing between 4+ tools, directly addressing our validated problem
- **MVP Target:** 100 sessions/week by end of Week 8
- **How:** Track `study_session_completed` events

**What makes a GOOD North Star Metric:**
- ✅ Measures VALUE delivery (not vanity like total signups)
- ✅ Connected to your problem statement
- ✅ Predicts long-term success
- ✅ Everyone on your team can understand it

**Tips:**
- Think about the "aha moment" when users experience your value
- Don't pick something easy to measure - pick what MATTERS
- Your NSM should go up if you're solving the problem

**Common mistakes to avoid:**
❌ Picking vanity metrics: "Total users" tells you nothing about value  
❌ Too complex: If you need a calculator to explain it, it's wrong  
❌ Not connected to problem: If NSM goes up but problem still exists, wrong metric

---

### Deliverable 5: Event Schema

**File:** `/02-analytics/event-schema.md`  
**Template:** [Download here](computer:///mnt/user-data/outputs/Lab-5-COMPLETE-WITH-ANALYTICS/templates/event-schema-template.md)  
**Time:** 60-90 minutes  
**Worth:** 4 points

**What to include:**
- **6-10 core events** you'll track in your MVP
- **Event naming convention:** `object_action` format (e.g., `study_session_started`)
- **Properties for each event:** What data you'll capture
- **Event-to-metric mapping:** How events power your NSM

**Example events:**
1. `user_signup_completed` - When account is created
2. `study_session_started` - When user creates a session
3. `study_session_completed` - When user finishes a session
4. `resource_shared` - When user shares materials
5. `invite_sent` - When user invites others
6. `user_logged_in` - Daily active usage

**Event properties example:**
```json
{
  "event_name": "study_session_completed",
  "user_id": "user_12345",
  "session_id": "session_67890",
  "session_type": "group",
  "subject": "mathematics",
  "duration_minutes": 45,
  "participants_count": 4,
  "timestamp": "2025-10-30T14:23:45Z"
}
```

**Tips:**
- Start with AARRR framework (Acquisition → Activation → Retention → Referral → Revenue)
- Each stage needs at least 1 event
- Include properties that help you understand WHY things happen
- Follow the naming convention strictly (makes data analysis easier later)

**Common mistakes to avoid:**
❌ Too many events: 6-10 is enough for MVP, don't try to track everything  
❌ Inconsistent naming: `SessionStart` vs `session_started` vs `start_session`  
❌ Missing properties: You'll wish you captured more context later  
❌ Including PII: Never track emails, phone numbers, or names in events

---

### Deliverable 6: Analytics Implementation Plan

**File:** `/02-analytics/analytics-plan.md`  
**Template:** [Download here](computer:///mnt/user-data/outputs/Lab-5-COMPLETE-WITH-ANALYTICS/templates/analytics-plan-template.md)  
**Time:** 90-120 minutes  
**Worth:** 5 points

**What to include:**
- **Technology stack:** What tools you'll use (Segment? Mixpanel? Custom?)
- **Architecture diagram:** How data flows from app → dashboard
- **Implementation timeline:** Week-by-week plan for Weeks 6-8
- **Dashboard design:** What your team will look at weekly
- **Team responsibilities:** Who implements what

**Week-by-week plan example:**
- **Week 6:** Set up analytics platform, implement first 2 events
- **Week 7:** Implement remaining events, build basic dashboard
- **Week 8:** Deploy to production, monitor, train team

**Tips:**
- Keep it simple for MVP - you can always upgrade later
- Free tiers are fine (Segment free, Google Analytics, etc.)
- Focus on your NSM dashboard first, fancy stuff later
- Make sure every team member knows what to build

**Common mistakes to avoid:**
❌ Over-engineering: You don't need a data warehouse for MVP  
❌ No timeline: "We'll figure it out" won't work  
❌ Vague responsibilities: Everyone owns it = no one owns it  
❌ Forgetting testing: Plan time to verify events actually fire

---

## ⏱️ Time Management Strategy

**Total time:** 9-12 hours

### Recommended Schedule:

**Friday Night (3 hours):**
- Deliverable 1: Affinity Map (90 min)
- Deliverable 4: North Star Metric (60 min)
- Start Deliverable 2: Patterns Analysis (30 min)

**Saturday (4 hours):**
- Finish Deliverable 2: Patterns Analysis (90 min)
- Deliverable 5: Event Schema (90 min)
- Start Deliverable 3: Problem Statement (60 min)

**Sunday (3 hours):**
- Finish Deliverable 3: Problem Statement (90 min)
- Deliverable 6: Analytics Plan (90 min)

**Monday-Thursday (2 hours buffer):**
- Review everything as team
- Fix any issues
- Get feedback if needed

---

## ✅ Quality Checklist

Before submitting, verify:

**All Deliverables:**
- [ ] All 6 files created and committed to GitHub
- [ ] Files in correct folders (`/01-discovery/synthesis/` and `/02-analytics/`)
- [ ] All team members reviewed and signed off
- [ ] No placeholder text like "[Your Team Name]" left in files

**Synthesis:**
- [ ] Problem statement cites 8+ interviews with quotes
- [ ] Impact is quantified (hours, money, emotion)
- [ ] Root cause identified (not just symptom)
- [ ] Clear decision on KEEP/REFINE/PIVOT

**Analytics:**
- [ ] North Star Metric connects to problem statement
- [ ] 6-10 events properly named (object_action format)
- [ ] Analytics plan has realistic timeline
- [ ] Dashboard design focuses on NSM

---

## 🚨 Common Pitfalls

### Synthesis Mistakes:

**❌ "We only did 6 interviews"**  
→ You need 8+ for strong patterns. Do 2-4 more this weekend.

**❌ "Our problem statement is too vague"**  
→ Add specifics: WHO exactly, WHAT failure, HOW MUCH impact, WHEN/WHERE context

**❌ "We're forcing data to fit our original idea"**  
→ Follow the evidence. If interviews don't validate your problem, PIVOT.

**❌ "We can't agree on the problem"**  
→ Use data to decide. Which statement has more supporting interviews?

### Analytics Mistakes:

**❌ "Our NSM is total signups"**  
→ That's vanity. Pick something that measures VALUE delivery.

**❌ "We're tracking 20 events"**  
→ Too many. Start with 6-10 core events. Add more later.

**❌ "We'll figure out implementation later"**  
→ No. You need a concrete plan NOW so Week 6 build includes analytics.

**❌ "We don't know what tools to use"**  
→ Start simple: Segment (free), Google Analytics, or custom DB logging.

---

## 💡 Pro Tips

### For Synthesis:

1. **Trust the process:** Affinity mapping feels chaotic at first. Keep going.
2. **Be specific:** "KIU CS students in group projects" > "students"
3. **Quote obsessively:** Every claim should reference specific interviews
4. **Embrace pivots:** Discovering your original problem is wrong = SUCCESS

### For Analytics:

1. **Think about the "aha moment":** When does a user first get value? That's your NSM.
2. **Start simple:** You can always add more events later. Start with 6-10.
3. **Test early:** In Week 6, implement analytics FIRST, then features.
4. **Make it visible:** If the team doesn't look at the dashboard, analytics is worthless.

### General:

1. **Start early:** Don't wait until Thursday night. This is 10 hours of work.
2. **Divide and conquer:** Split templates among team members, then review together.
3. **Use office hours:** Stuck? Come to office hours Tues/Thurs 2-4 PM.
4. **Cite everything:** When in doubt, add more interview citations.

---

## 🆘 Getting Help

### During Lab:
- Raise your hand
- Instructor will come to your team

### After Lab:
- **Office Hours:** Thursdays 1-3 PM
- **Email:** zeshan.ahmad@kiu.edu.ge

### What to Bring to Office Hours:
- Your draft deliverables (even if incomplete)
- Specific questions: "Is this a root cause or symptom?"
- Your interview logs for reference

**Don't wait until Thursday night to ask for help!**

---

## 📥 Download Templates

Click to download each template:

**Synthesis:**
1. [Affinity Map Template]templates/affinity-map-template.md)
2. [Patterns Analysis Template]templates/patterns-analysis-template.md)
3. [Final Problem Statement Template] templates/final-problem-statement-template.md)

**Analytics:**
4. [North Star Metric Template]templates/north-star-metric-template.md)
5. [Event Schema Template]templates/event-schema-template.md)
6. [Analytics Plan Template]templates/analytics-plan-template.md)

---

## 🎓 Why This Matters

This is the **most important homework** of the semester. Here's why:

**Without good synthesis:**
- You might build a solution to a problem nobody has
- You won't know if your problem is real or assumed
- You'll waste 10 weeks building the wrong thing

**Without good analytics:**
- You won't know if your solution actually works
- You can't measure success or improvement
- You'll make decisions based on guesses, not data

**Get both right:**
- You build what people actually need
- You can measure if it's working
- You can iterate and improve based on real data
- Demo Day goes well because you have PROOF your solution works

---

## 📊 Grading Breakdown

| Deliverable | Points | Key Grading Criteria |
|-------------|--------|---------------------|
| **Lab Participation** | 5 | Completed synthesis workshop in lab |
| **1. Affinity Map** | 5 | Photos clear, all clusters documented with quotes |
| **2. Patterns Analysis** | 7 | Frequency table complete, 5 Whys for top 3-5, evidence cited |
| **3. Problem Statement** | 8 | Evidence from 8+ interviews, quantified impact, clear decision |
| **4. North Star Metric** | 3 | Connected to problem, measurable, realistic targets |
| **5. Event Schema** | 4 | 6-10 events, proper naming, properties defined |
| **6. Analytics Plan** | 5 | Timeline realistic, architecture clear, responsibilities assigned |
| **TOTAL** | **30** | - |

**Late penalty:** -10% per day after Friday 11:59 PM  
**No submissions accepted after:** Tuesday Week 6, 11:59 PM

---

## 🎯 Final Reminders

1. **This is 10 hours of work.** Start Friday night.
2. **Follow the templates.** They have examples and guidance.
3. **Cite your evidence.** Every claim needs interview support.
4. **Be honest about the data.** If your problem isn't validated, PIVOT.
5. **Think ahead to Week 6.** Your analytics plan guides your build.
6. **Work as a team.** Divide work but review together.
7. **Use office hours.** Don't struggle alone.
8. **Submit on time.** Due Friday 11:59 PM.

---

## 📞 Questions?

Post in #lab-5-questions on Slack or come to office hours.

**Good luck! This is hard work but it's THE most important work of the semester. Get this right and everything else gets easier. 🚀**
