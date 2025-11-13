# Lab 7: Architecture Planning + Experiment Design Workshop

**Duration:** 120 minutes (2 hours)  
**Week:** 8  
**Phase:** Transition from Discovery to Build

---

## Overview

This lab bridges **hypothesis-driven development** with **technical implementation**. You'll plan your system architecture AND design experiments to validate your MVP assumptions.

**By the end of this lab, you will have:**
1. ✅ Complete system architecture plan
2. ✅ Tech stack decisions documented
3. ✅ Risk spikes identified and planned
4. ✅ Refined product hypothesis
5. ✅ 2-3 designed experiments
6. ✅ One experiment launched (landing page or smoke test)

---

## Pre-Lab Requirements

**Before arriving at lab, you must have:**

- [ ] Last week's sprint plan (from Lab 6)
- [ ] Team problem statement and ICP
- [ ] Rough idea of MVP scope (from PRD)
- [ ] Laptop with:
  - GitHub access
  - Drawing tool installed (Excalidraw, draw.io, or paper + phone camera)
  - Internet connection for deployment

**Bring:**
- Your MVP feature list
- Any technical questions or concerns
- Your team's risky assumptions (from Week 8 lecture exercise)

---

## Lab Structure

| Time | Activity | Deliverables |
|------|----------|--------------|
| **0:00-0:10** | Review & Setup | Folder structure created |
| **0:10-0:30** | System Architecture Design | Architecture diagram |
| **0:30-0:45** | Tech Stack Selection | `tech-stack.md` |
| **0:45-1:00** | Risk Spike Planning | `risk-spikes.md` |
| **1:00-1:15** | Hypothesis Refinement | `hypothesis.md` |
| **1:15-1:45** | Experiment Design | `experiment-plan.md` |
| **1:45-2:00** | Landing Page Setup & Deploy | Live URL |

---

## Part 1: Review & Setup (10 minutes)

### Activity: Create Folder Structure

Navigate to your team repository and create the following structure:
/03-build/
  /architecture/
    - system-design.md (Template 1)
    - tech-stack.md (Template 2)
    - risk-spikes.md (Template 3)
  /experiments/
    - hypothesis.md (Template 4)
    - experiment-plan.md (Template 5)
    - experiment-results.md (Template 6)
```bash
cd product-capstone-2025

# Create folders
mkdir -p 03-build/architecture
mkdir -p 03-build/experiments
mkdir -p 03-build/src

# Navigate to architecture folder
cd 03-build/architecture

# Create template files
touch system-design.md
touch tech-stack.md
touch risk-spikes.md

# Navigate to experiments folder
cd ../experiments
touch hypothesis.md
touch experiment-plan.md
touch experiment-results.md

# Commit structure
git add .
git commit -m "Add Week 8 architecture and experiments structure"
git push
```

**Verify:** You should now have `/03-build/architecture/` and `/03-build/experiments/` folders in your repository.

---

## Part 2: System Architecture Design (20 minutes)

### Activity: Draw Your System Architecture

**Step 1: Map User Actions (5 minutes)**

As a team, write down the **core user flow** for your MVP:

**Example (StudySpot):**
1. Student opens app
2. Views map of study locations
3. Sees real-time occupancy
4. Selects location
5. Books time slot
6. Receives confirmation

**Your Turn:** Write your core user flow (3-6 steps)

---

**Step 2: Identify Components (7 minutes)**

For each step in the user flow, identify what technical components are needed:

**Template:**
| User Action | Frontend Needs | Backend Needs | Database Needs |
|-------------|----------------|---------------|----------------|
| Views map | Map component | Location data API | Locations table |
| Sees occupancy | Real-time display | Occupancy calculator | Bookings table |

**Your Turn:** Fill this out for your core user flow

---

**Step 3: Draw Architecture Diagram (8 minutes)**

Using Excalidraw, draw.io, Miro, or paper, create a diagram showing:

1. **Frontend** (what users see)
2. **Backend** (your server logic)
3. **Database** (data storage)
4. **External APIs** (third-party services)
5. **Arrows showing data flow**

**Minimum Requirements:**
- Clearly labeled boxes for each component
- Arrows showing direction of data flow
- Labels on arrows (e.g., "HTTP API call", "SQL query", "WebSocket")

**Example Structure:**
```
[Frontend: React]
    ↓ (API calls)
[Backend: Node.js + Express]
    ↓ (SQL queries)
[Database: PostgreSQL]

External:
- Google Maps API
- Firebase Auth
```

---

**Step 4: Document in `system-design.md`**

Copy the template from `/labs/lab-7/templates/system-design-template.md` to your `03-build/architecture/` folder and fill it out.

**Required sections:**
1. High-level architecture diagram (image or ASCII art)
2. Component descriptions
3. Data flow explanation
4. Key design decisions

**Time:** Remaining 3-5 minutes of this section

---

## Part 3: Tech Stack Selection (15 minutes)

### Activity: Choose and Document Your Technologies

**Step 1: Team Discussion (10 minutes)**

Answer these questions as a team:

**Frontend:**
- What do you know? (React, Vue, vanilla JavaScript, etc.)
- What does your MVP need? (complex interactions vs. simple pages)
- Decision: _________________

**Backend:**
- What do you know? (Node.js, Python/Flask, Ruby/Rails, etc.)
- What does your MVP need? (real-time updates, complex logic, simple API, etc.)
- Decision: _________________

**Database:**
- What kind of data? (relational vs. documents)
- What scale? (hundreds vs. millions of records)
- Decision: _________________

**Deployment:**
- Where will you host? (Vercel, Heroku, AWS, Railway, etc.)
- Continuous deployment or manual?
- Decision: _________________

**Key Libraries/Frameworks:**
- Authentication: _________________
- Maps/Location: _________________
- Styling: _________________
- Other: _________________

---

**Step 2: Document in `tech-stack.md` (5 minutes)**

Copy the template from `/labs/lab-7/templates/tech-stack-template.md` and fill it out.

**For EACH technology, include:**
1. **What** you chose
2. **Why** you chose it
3. **Alternative considered**
4. **Risk/Trade-off**

**Example:**
```markdown
### Frontend: React

**Why:**
- Team knows React from previous coursework
- Large ecosystem of libraries
- Good documentation and community support

**Alternative Considered:**
Vue.js - simpler learning curve but team less familiar

**Risk:**
React learning curve for state management. Mitigation: Use simple state, add Redux only if needed.
```

---

## Part 4: Risk Spike Planning (15 minutes)

### Activity: Identify and Plan Technical Spikes

**Step 1: List Technical Uncertainties (5 minutes)**

What don't you know how to build yet? List everything your team is uncertain about:

**Examples:**
- "Can we get real-time data from the library system?"
- "Can we integrate Google Maps without exceeding free tier?"
- "Can we deploy a Python backend on Vercel?"
- "Can we scrape data from the university website?"

**Your Turn:** List 3-5 technical uncertainties

---

**Step 2: Prioritize by Risk (3 minutes)**

For each uncertainty, rate:
- **Impact if it fails:** High / Medium / Low
- **Likelihood of failure:** High / Medium / Low

**Formula:** Risk = Impact × Likelihood

Prioritize the HIGH RISK items (high impact + high likelihood of failure)

---

**Step 3: Design Risk Spikes (7 minutes)**

For your top 2-3 risks, design a spike:

**Template:**
```markdown
### Spike #1: [Name of uncertainty]

**Risk:** What could go wrong?

**Hypothesis:** "If we can [do X], then we can proceed with [building Y]"

**Experiment:**
- Time-box: 2-3 hours
- What you'll build: Minimal proof-of-concept
- Success criteria: Specific measurable outcome

**If it succeeds:** How does this change your plan?
**If it fails:** What's your backup plan?

**Owner:** Who will run this spike?
**Deadline:** When by?
```

**Your Turn:** Document in `risk-spikes.md`

---

## Part 5: Hypothesis Refinement (15 minutes)

### Activity: Refine Your Product Hypothesis

**Step 1: Review Week 8 Hypothesis Template (3 minutes)**

**Template:**
> "We believe [doing X] for [target user] will result in [measurable outcome] because [assumption about user behavior]."

**Must include:**
- ✅ Specific action/feature
- ✅ Specific user segment (ICP)
- ✅ Measurable outcome with number
- ✅ Clear assumption to test

---

**Step 2: Write Your Hypothesis (7 minutes)**

Using the 2-minute exercise from lecture, refine your hypothesis with your team.

**Example (StudySpot):**
> "We believe showing real-time library occupancy % for KIU students will result in 30+ signups in Week 1 because students currently waste 15 min/day finding quiet spots and want real-time info."

**Your Turn:** Write your hypothesis in `hypothesis.md`

---

**Step 3: Define Success Criteria (5 minutes)**

For your hypothesis, specify:

**Success Threshold:**
- What number would validate your hypothesis?
- Example: "50+ email signups in 1 week"

**Failure Threshold:**
- What number would invalidate it?
- Example: "<10 signups in 1 week"

**Gray Zone:**
- What number would be inconclusive?
- Example: "10-50 signups → need more data"

**Time Frame:**
- How long will you run the experiment?
- Example: "1 week (Nov 19-26)"

---

## Part 6: Experiment Design (30 minutes)

### Activity: Design 2-3 Experiments to Test Your Hypothesis

**Step 1: Choose Experiment Types (10 minutes)**

Review the Experiment Spectrum from lecture:

**Level 1: Prototype** (fastest, lowest fidelity)
- Paper sketches, Google Forms, Manual spreadsheet
- Use when: Testing if problem exists

**Level 2: Smoke Test** (1-3 days, low fidelity)
- Landing page, Fake door test, Concierge service
- Use when: Testing interest/demand

**Level 3: Wizard of Oz** (1-2 weeks, medium fidelity)
- Manual backend, Human-powered automation, No-code tools
- Use when: Testing if solution works

**Level 4: MVP** (4-8 weeks, medium-high fidelity)
- Coded core feature, Basic automation, Real infrastructure
- Use when: Testing product-market fit

**Your Task:** Choose 2-3 experiments at different levels that build on each other

**Example (StudySpot):**
1. **Smoke Test:** Landing page with "Get real-time library occupancy updates"
2. **Wizard of Oz:** Manual checking of library + texting students with updates
3. **MVP:** Automated web scraping + real-time dashboard

---

**Step 2: Design Each Experiment (15 minutes)**

For EACH experiment, document:

**Template:**
```markdown
## Experiment #1: [Name]

**Type:** Smoke Test / Wizard of Oz / MVP / etc.

**Hypothesis Testing:**
Which assumption does this test?

**Setup:**
- What you'll build (be specific)
- Tools you'll use
- Time to build

**Metrics:**
- Primary metric: [Example: email signups]
- Secondary metrics: [Example: landing page visits, click-through rate]
- How you'll track: [Example: Google Forms responses]

**Success Criteria:**
- Success: [Specific number]
- Failure: [Specific number]

**Timeline:**
- Build: [X days]
- Run: [X days]
- Analyze: [X hours]

**Budget:** $0 (must use free tools)

**Next Steps:**
- If succeeds: [What you'll build next]
- If fails: [What you'll pivot to]
```

**Your Turn:** Fill this out for 2-3 experiments in `experiment-plan.md`

---

**Step 3: Prioritize and Commit (5 minutes)**

As a team, decide:
1. **Which experiment to launch TODAY:** (must be launchable in 30 minutes)
2. **Which experiment to launch THIS WEEK:** (more complex, needs 2-3 days)
3. **Which experiment for NEXT WEEK:** (if first two validate)

**Document:** In `experiment-plan.md`, note which experiment you're starting with

---

## Part 7: Landing Page Setup & Deploy (15 minutes)

### Activity: Build and Launch Your First Smoke Test

**Objective:** Have a LIVE landing page by end of lab

**Tool Options:**
1. **Carrd.co** (recommended for beginners)
   - Templates available
   - Free tier includes 3 sites
   - Custom domain optional

2. **Notion** (good if you already use it)
   - Create page + share publicly
   - Add Google Form for signups

3. **Google Sites** (free, simple)
   - Easy drag-and-drop
   - Integrate with Google Forms

4. **HTML + GitHub Pages** (if you know HTML)
   - Full control
   - Free hosting

---

**Minimum Requirements for Landing Page:**

**Must Include:**
1. ✅ **Clear headline:** What problem are you solving?
2. ✅ **Subheadline:** For whom? Why now?
3. ✅ **Visual:** Screenshot, mockup, or illustration
4. ✅ **Value proposition:** 3 key benefits
5. ✅ **Call-to-action:** Email signup or "Join Waitlist" button
6. ✅ **Social proof** (optional): "100+ KIU students interested"

**Example Structure (StudySpot):**
```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Never Waste Time Finding Study Spots Again
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

See real-time library occupancy at KIU
Join 50+ students on the waitlist

[Screenshot of mock dashboard]

✓ Save 15+ min/day
✓ Find quiet spots instantly
✓ Plan ahead with occupancy predictions

[Email signup form]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

**Step-by-Step (Using Carrd):**

1. Go to carrd.co
2. Sign up (free)
3. Choose "Start from Scratch" or pick template
4. Add sections:
   - Hero (headline + CTA)
   - Features (3 benefits)
   - Email form (link to Google Form)
5. Publish (get URL)
6. Test on mobile

**Time:** 10-12 minutes to build, 2-3 minutes to deploy

---

**Before You Leave Lab:**

1. **Get your landing page URL**
2. **Share link in team Discord/Slack**
3. **Add URL to `experiment-plan.md`**
4. **Commit all files to GitHub**

---

## Deliverables Checklist

By end of lab, your team must have committed to GitHub:

### Architecture Documents (`/03-build/architecture/`):
- [ ] `system-design.md` with architecture diagram
- [ ] `tech-stack.md` with technology choices and rationale
- [ ] `risk-spikes.md` with top 2-3 technical risks and spike plans

### Experiment Documents (`/03-build/experiments/`):
- [ ] `hypothesis.md` with refined, testable hypothesis
- [ ] `experiment-plan.md` with 2-3 designed experiments
- [ ] `experiment-results.md` (template for tracking data)

### Live Deployment:
- [ ] Landing page or smoke test deployed and accessible via URL
- [ ] URL documented in `experiment-plan.md`

---

## Homework (Due by Sunday)

### 1. Finalize Architecture (if not complete in lab)
- Polish architecture diagram
- Get feedback from another team or instructor
- Update based on feedback

### 2. Run Your Experiment
- **Days 1-3:** Promote landing page (social media, class Discord, word of mouth)
- **Track daily:** # of visits, # of signups, qualitative feedback
- **Document:** Update `experiment-results.md` daily

### 3. Execute Risk Spikes
- **This week:** Complete at least ONE technical spike
- **Document:** What you learned, what worked, what didn't
- **Update:** `risk-spikes.md` with results

### 4. Prepare for Midterm (Week 9)
- Review Weeks 1-7 lecture slides
- Review GitHub deliverables from Labs 1-6
- Practice writing hypotheses
- Study key frameworks (AARRR, 4 D's, Scrum)

---

## Troubleshooting

### "We can't agree on tech stack"

**Solution:**
- Use the "Skills + Time + Requirements" framework
- Vote if needed (simple majority)
- Remember: No choice is perfect. Pick something and iterate.

---

### "We don't know how to draw an architecture diagram"

**Solution:**
- Start simple: 3 boxes (Frontend, Backend, Database)
- Add arrows showing data flow
- Label what each arrow does
- Refine over time

---

### "We have 10 different technical risks"

**Solution:**
- That's normal! You won't eliminate all of them.
- Focus on the top 2-3 HIGH IMPACT risks
- De-risk those first, tackle others later

---

### "Our landing page looks ugly"

**Solution:**
- Ugly landing pages can still validate hypotheses
- Focus on CLEAR messaging over aesthetics
- You can polish it later if experiment succeeds

---

### "No one is signing up for our landing page"

**Solution:**
- Good data! This tells you something.
- Analyze: Is the problem not painful enough? Or is your messaging unclear?
- Pivot if needed. This is WHY we smoke test.

---

## Next Week

**Week 9: MIDTERM EXAM**
- No lecture
- No lab
- 2-hour comprehensive exam covering Weeks 1-7

**After Midterm (Week 10):**
- Sprint 1 kickoff
- Start building based on validated architecture
- Continue experiments and iterate based on data

---

## Resources

**Architecture Design:**
- Excalidraw: https://excalidraw.com
- draw.io: https://app.diagrams.net
- Miro: https://miro.com

**Landing Pages:**
- Carrd: https://carrd.co
- Notion: https://notion.so
- Google Sites: https://sites.google.com
- Lovable / Bolt / Curser + IDE

**Experiment Tracking:**
- Google Forms: https://forms.google.com
- Typeform: https://typeform.com
- Tally: https://tally.so
- Google Analytics

**GitHub Templates:**
All templates available in `/labs/lab-7/templates/`

---

If you need help with:
- Architecture review
- Tech stack decisions
- Risk spike planning
- Experiment design
- Landing page creation
Don't wait until homework is due to ask for help!
