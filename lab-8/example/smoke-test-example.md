# Example: Smoke Test for StudySync

**Team:** Discovery Engine  
**Product:** StudySync - Group Project Coordination Tool  
**Created:** November 15, 2025

---

## Objective

Validate that CS students want a dedicated project coordination tool enough to sign up for early access BEFORE we build it.

---

## Hypothesis

**We believe that** second and third-year CS students taking 3+ project-based courses experience enough coordination pain with current tools (WhatsApp, Drive, GitHub) that **they will** provide their email address to join a waitlist for a better solution.

**We will know we're right when** 15% or more of students who see our landing page sign up for early access.

---

## Test Design

### Value Proposition

**Problem:** "You're juggling 3 group projects. Tasks buried in WhatsApp. Files scattered across Drive. Deadlines slipping. You waste 2-4 hours per week just figuring out who's doing what."

**Solution promise:** "StudySync: See all your team projects in one place. Know exactly who's working on what, when things are due, and what's blocking progress. Built specifically for KIU CS students."

**Target user:** Second and third-year CS students at KIU taking multiple project-based courses simultaneously.

---

### Smoke Test Asset

**Type:** Landing page with email signup

**Why this type:** 
- Quickest to build (4-6 hours)
- Tests interest without building product
- Email signup is low friction
- Can follow up with interviews

**Tools:**
- **Landing page:** Carrd.co (Free tier)
- **Email collection:** Airtable form
- **Analytics:** Google Analytics
- **URL:** studysync.carrd.co

---

## Asset Content

### Headline
"Stop Wasting Hours Coordinating Group Projects"

**Why:** Leads with pain point students immediately recognize

---

### Subheadline
"KIU CS students waste 2-4 hours per week coordinating across WhatsApp, Drive, and GitHub. StudySync puts your team's status in one glance—built for the way you actually work."

**Why:** Quantifies pain, mentions familiar tools, hints at solution

---

### Key Benefits

- 📊 **One Dashboard:** All your projects, all your teams, one place
- ✅ **Real Status:** See who's working on what right now, not 3 days ago
- ⏰ **Never Miss Deadlines:** Smart reminders when tasks are falling behind
- 🎯 **Built for Students:** Free while you're at KIU, works on mobile, integrates with what you use

**Why these:** Each addresses a specific pain from interviews

---

### Social Proof

"Based on 10+ interviews with KIU CS students about how they coordinate group projects."

**Why:** Shows we understand the problem through research

---

### Call to Action

**Primary CTA:** "Join the Waitlist" (button)

**Secondary text:** "Be among the first 50 students to try StudySync. We'll reach out in 2 weeks for early access."

**After signup:** "Thanks! Check your email for next steps. We'll contact you within 48 hours."

**Why:** Clear action, creates urgency (first 50), sets expectations

---

### Wireframe

```
[Header Logo: StudySync]

[Hero Section]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
   STOP WASTING HOURS COORDINATING
           GROUP PROJECTS
   
   KIU CS students waste 2-4 hours per week...
   
   [Join the Waitlist] ← Big button
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[Problem Section]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
   Sound familiar?
   
   ❌ WhatsApp flooded with updates
   ❌ Can't find that file from 2 weeks ago  
   ❌ "Wait, who was doing that?"
   ❌ Last-minute scrambles before deadlines
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[Solution Section]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
   How StudySync Helps
   
   [Icon] One Dashboard
   All projects, all teams, one place
   
   [Icon] Real Status
   See who's working on what right now
   
   [Icon] Never Miss Deadlines
   Smart reminders when tasks fall behind
   
   [Icon] Built for Students
   Free at KIU, mobile-friendly
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[Social Proof Section]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
   Built by KIU CS students who felt your pain
   
   Based on 10+ interviews with students
   about group project coordination
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[Final CTA Section]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
   Be Among the First 50 Students
   
   Join waitlist for early access
   
   [Email Input Field]
   [Join the Waitlist] ← Big button
   
   We'll contact you within 48 hours
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[Footer]
Made with ❤️ by KIU CS students
```

---

## Success Criteria

### Primary Metric

**Metric:** Conversion rate (signups / visitors)

**Success thresholds:**
- **20%+** = Strong validation → Build MVP immediately
- **10-19%** = Good validation → Interview signups, then build
- **5-9%** = Weak signal → Interview both signups and non-signups
- **<5%** = Invalid → Rethink problem or positioning

**Minimum sample size:** 100 visitors

**Why 100?** With 100 visitors and 15% conversion, we get ±7% margin of error at 95% confidence—good enough for MVP decision.

---

### Secondary Metrics

| Metric | Target | Tool |
|--------|--------|------|
| Time on page | > 45 seconds | Google Analytics |
| Scroll depth | > 75% | GA Event tracking |
| CTA click rate | > 20% | GA Events |
| Bounce rate | < 60% | GA |
| Mobile vs desktop | Track ratio | GA |

---

## Distribution Plan

### Channel 1: KIU CS WhatsApp Groups

**Tactic:** Post message with link in 3 active groups

**Expected reach:** 200 students

**Expected CTR:** 25% (50 visitors)

**Cost:** Free

**Timeline:** Monday 10 AM

**Message:**
"Hey everyone 👋

We're building something to make group project coordination less painful (because we're all tired of digging through WhatsApp for that one file...)

If juggling multiple group projects drives you crazy, check this out and let us know if you'd use it: studysync.carrd.co

Takes 30 seconds. Not selling anything, just validating if this is worth building.

—Discovery Engine Team"

---

### Channel 2: In-Person (Database Systems Class)

**Tactic:** 2-minute presentation before class with QR code

**Expected reach:** 60 students

**Expected CTR:** 40% (24 visitors)

**Cost:** Free

**Timeline:** Wednesday 2:00 PM

**Script:**
"Quick question: How many of you are in 3+ group projects right now? [hands up]

How many waste time every week just figuring out who's doing what? [hands up]

We interviewed 10 CS students about this pain. Now we're building StudySync to fix it. 

Scan this QR code if you'd want early access. Takes 30 seconds.

[QR code displayed]

Thanks!"

---

### Channel 3: KIU CS Student Discord

**Tactic:** Post in #general and #projects channels

**Expected reach:** 150 students

**Expected CTR:** 20% (30 visitors)

**Cost:** Free

**Timeline:** Tuesday 6 PM (peak activity)

**Message:**
"quick poll: who here is currently juggling 3+ group projects? 🙋

we interviewed a bunch of CS students about project coordination pain (WhatsApp chaos, Drive mess, last-minute deadline panic)

building something to fix it. check it out if you're interested: studysync.carrd.co

early access for first 50 signups 👀"

---

### Total Expected Reach

| Channel | Reach | Est. CTR | Est. Visitors |
|---------|-------|----------|---------------|
| WhatsApp | 200 | 25% | 50 |
| In-person | 60 | 40% | 24 |
| Discord | 150 | 20% | 30 |
| **TOTAL** | **410** | **25%** | **104** |

**Confidence:** Should hit 100 visitors in 3-4 days.

---

## Timeline

```
Day 1 (Mon):   Build landing page (4 hours)
Day 2 (Tue):   Set up analytics, test everything (2 hours)
Day 3 (Wed):   Launch to all 3 channels
Day 4-9:       Monitor, respond to signups within 24hrs
Day 10 (Fri):  Close test, analyze data
Day 11 (Mon):  Make decision
```

**Start:** November 18  
**End:** November 28  
**Duration:** 11 days

---

## Follow-Up Plan

### For Signups (Automated)

**Email 1: Immediate Thank You**

Subject: "You're on the StudySync waitlist!"

```
Hi [Name],

Thanks for joining the StudySync waitlist!

You're one of the first [X] KIU CS students interested in making group project coordination less painful.

What happens next:
- We'll reach out within 48 hours
- Quick 15-min chat about how you coordinate now
- Early access when we launch (2-3 weeks)

In the meantime, have a question? Just reply to this email.

—Discovery Engine Team
```

---

### For Signups (Manual, within 48hrs)

**Email 2: Interview Invitation**

Subject: "15 minutes to shape StudySync?"

```
Hey [Name],

Thanks again for signing up!

Since you're an early supporter, we'd love 15 minutes of your time to understand your project coordination pain better. Your input will directly shape what we build.

When works for you this week?
[Calendly link]

As a thank-you, you'll get:
- First access when we launch
- Direct line to us for feature requests
- Free premium features while you're at KIU

Sound good?

—[Your name]
Discovery Engine
```

---

## Measurement & Tracking

### Analytics Setup

**Events tracked:**
- Page view (automatic)
- Scroll to 25%, 50%, 75%, 100%
- CTA button click
- Email form focus
- Email form submit
- Thank you page view
- Traffic source (UTM parameters)

**Dashboard:** Custom GA4 dashboard with:
- Real-time visitors
- Conversion rate (funnel)
- Traffic sources breakdown
- Time-series chart

**URL parameters:**
- WhatsApp: `?utm_source=whatsapp&utm_campaign=smoke_test`
- In-person: `?utm_source=in_person&utm_campaign=smoke_test`
- Discord: `?utm_source=discord&utm_campaign=smoke_test`

---

## Decision Framework

### Actual Results (Filled in after test)

**Visitors:** [104]  
**Signups:** [18]  
**Conversion rate:** [17.3%]  

### Interpretation

| Rate | Visitors | Signups | Interpretation | Action |
|------|----------|---------|----------------|--------|
| 17.3% | 104 | 18 | GOOD VALIDATION | Proceed to build MVP |

**Decision:** PERSEVERE

**Reasoning:**
- Hit 17.3% conversion (above 15% threshold)
- 18 students interested enough to give email
- Good distribution across all 3 channels
- Qualitative feedback in interviews was positive

**Next steps:**
1. Interview all 18 signups (schedule this week)
2. Begin MVP development (Week 12)
3. Beta launch with these 18 users (Week 14)

---

## Risks & Mitigation (Actual)

| Risk | Did it happen? | How we handled it |
|------|----------------|-------------------|
| Can't drive traffic | No | All channels worked well |
| Wrong audience | No | Verified in follow-ups—all CS students in 3+ projects |
| Landing page breaks | No | Tested thoroughly before launch |
| Zero signups | No | 18 signups exceeded expectations |

---

## Key Learnings

### What Worked

✅ **In-person presentation:** 40% CTR (best channel)—face-to-face builds trust

✅ **Specific pain points:** Mentioning "WhatsApp chaos" and "Drive mess" resonated—use this language in product

✅ **"First 50" urgency:** Several signups mentioned this in interviews—scarcity works

✅ **Quick signup:** Email-only (no name/phone) kept friction low—maintain this simplicity

---

### Surprises

😮 **Mobile traffic:** 70% mobile (expected 50%)—MVP must be mobile-first

😮 **Timing matters:** Discord post at 6 PM got 2x engagement vs. morning post—launch features in evening

😮 **Second-years more interested:** 65% of signups were second-years—they have most projects, target them first

---

### What to Improve

🔧 **Landing page load time:** 4.2 seconds on mobile—too slow, optimize images

🔧 **Value prop clarity:** 3 people asked "is this like Trello?"—need clearer differentiation

🔧 **Follow-up speed:** Took 36 hours average to send interview invite—should be < 24 hours

---

## Files & Evidence

- **Landing page:** studysync.carrd.co (archived)
- **Analytics dashboard:** [Link]
- **Raw data:** smoke-test-data.csv
- **Screenshots:** /evidence/ folder
- **Email list:** 18 emails in Airtable

---

This smoke test validated our core assumption: students want a better coordination tool. Time to build!
