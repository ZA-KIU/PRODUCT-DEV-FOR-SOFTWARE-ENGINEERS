# Product Development for Software Engineers
Repo: https://github.com/ZA-KIU/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS

This README is a navigation layer. Use it to move through the full product lifecycle, from problem selection to launch, measurement, and iteration.

---

## Quick start path
Follow this order, do not skip deliverables.

1. **Lab 1** → pick problem, segment, outcomes, constraints  
2. **Lab 2** → discovery interviews and evidence log  
3. **Lab 3** → ICP, jobs, pains, current alternatives  
4. **Lab 4** → solution framing and MVP scope  
5. **Lab 5** → UX flow, prototype, test plan  
6. **Lab 6** → metrics, event model, activation  
7. **Lab 7** → pricing and packaging (if relevant)  
8. **Lab 8** → go-to-market, distribution, funnel  
9. **Lab 9** → experiment design, iteration loop  
10. **Lab 10** → roadmap, execution plan, risks  
11. **Lab 11** → final ship checklist, pitch, handoff

---

## Repo map (labs)
- Lab 1: https://github.com/ZA-KIU/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS/tree/main/Lab%201  
- Lab 2: https://github.com/ZA-KIU/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS/tree/main/lab-2  
- Lab 3: https://github.com/ZA-KIU/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS/tree/main/Lab-3  
- Lab 4: https://github.com/ZA-KIU/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS/tree/main/Lab-4  
- Lab 5: https://github.com/ZA-KIU/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS/tree/main/Lab%205  
- Lab 6: https://github.com/ZA-KIU/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS/tree/main/lab-6  
- Lab 7: https://github.com/ZA-KIU/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS/tree/main/lab%207  
- Lab 8: https://github.com/ZA-KIU/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS/tree/main/lab-8  
- Lab 9: https://github.com/ZA-KIU/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS/tree/main/lab-9  
- Lab 10: https://github.com/ZA-KIU/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS/tree/main/lab-10  
- Lab 11: https://github.com/ZA-KIU/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS/tree/main/lab-11  

---

## Stage-by-stage guide
Each stage below states: goal, outputs, and a “done” checklist.

### Stage 1. Problem selection (Lab 1)
**Goal:** Choose a problem with a clear buyer/user, clear context, and observable pain.

**Outputs:**
- Problem statement (1 paragraph)
- Target segment (bounded)
- Success outcome (measurable)
- Constraints (time, budget, tech, channels)

**Done checklist:**
- Names a specific user with a specific context
- States a pain tied to a real workflow
- Defines success with units + time window
- States what you refuse to build in v1

---

### Stage 2. Customer discovery (Lab 2)
**Goal:** Replace opinions with evidence from past behavior.

**Outputs:**
- Interview script (past-behavior questions)
- Interview notes (per participant)
- Evidence log (what you heard, how many, what you infer)

**Done checklist:**
- Questions focus on “last time” and “walk me through”
- Captures current alternatives and switching costs
- Tracks quotes + concrete events
- Separates observation from interpretation

---

### Stage 3. ICP + positioning (Lab 3)
**Goal:** Decide who this product is for, and why they switch.

**Outputs:**
- ICP definition (role, firmographics, context, trigger)
- Jobs-to-be-done summary
- “Current alternatives” list
- Positioning statement

**Done checklist:**
- ICP includes trigger event and constraints
- Alternatives include “do nothing” and manual workflows
- Defines one primary wedge, not many

---

### Stage 4. MVP scope (Lab 4)
**Goal:** Build the smallest thing that proves a key assumption.

**Outputs:**
- Assumption list (ranked by risk)
- MVP scope (in / out)
- Key user journey (happy path)
- Non-goals

**Done checklist:**
- MVP proves one risky assumption first
- Scope fits a short build cycle
- Each feature ties to a specific assumption

---

### Stage 5. Prototype + usability test (Lab 5)
**Goal:** Test comprehension and workflow fit before full build.

**Outputs:**
- Low-fi or clickable prototype
- Task list for usability sessions
- Findings list (issues, severity, fixes)

**Done checklist:**
- Tests tasks users already do today
- Measures time-to-complete and failure points
- Produces specific UI changes, not vague notes

---

### Stage 6. Metrics + instrumentation (Lab 6)
**Goal:** Define activation, retention signals, and event tracking.

**Outputs:**
- North Star and supporting metrics
- Activation definition (event + properties + time window)
- Event taxonomy (names, properties)
- Basic dashboard outline

**Done checklist:**
- Metrics include units and time windows
- Activation describes a real value moment
- Events use consistent naming and properties

---

### Stage 7. Pricing + packaging (Lab 7)
**Goal:** Match price to value and reduce buying friction.

**Outputs:**
- Pricing model hypothesis
- Package tiers (if needed)
- Objection list + responses
- Trial or pilot plan

**Done checklist:**
- Pricing ties to buyer budget and value metric
- Packages map to different needs, not feature clutter
- Includes a plan to test willingness-to-pay

---

### Stage 8. Go-to-market (Lab 8)
**Goal:** Decide distribution, funnel steps, and first channel.

**Outputs:**
- Channel thesis (1 primary, 1 backup)
- Funnel steps (visit → activate → retain → refer)
- ICP targeting list (where to reach them)
- Sales or onboarding script

**Done checklist:**
- One channel first, with a measurable target
- Funnel defines conversion metrics per step
- Includes a weekly outreach/shipping cadence

---

### Stage 9. Experiments + iteration loop (Lab 9)
**Goal:** Run small tests, learn fast, update plan.

**Outputs:**
- Experiment backlog (hypothesis, method, metric, threshold)
- Weekly review template
- Decision log (ship/kill/iterate)

**Done checklist:**
- Each test has a pass/fail threshold
- Tracks learnings and next actions
- Keeps product scope aligned to evidence

---

### Stage 10. Roadmap + execution (Lab 10)
**Goal:** Plan delivery without turning it into a wish list.

**Outputs:**
- 4–8 week roadmap
- Risk register
- RICE (or similar) prioritization
- Release checklist draft

**Done checklist:**
- Roadmap links items to metrics and assumptions
- Risks list mitigations, owners, deadlines
- Prioritization uses consistent criteria

---

### Stage 11. Ship + handoff (Lab 11)
**Goal:** Launch, measure, support, and communicate.

**Outputs:**
- Launch plan (timeline, roles, comms)
- Support plan (triage, SLA targets, feedback loop)
- Post-launch review template
- Final pitch or demo narrative

**Done checklist:**
- Clear release gates and rollback plan
- Support workflow exists before launch
- Post-launch metrics review scheduled

---

## Suggested repo upgrades (small, high impact)
Add these files to make navigation “self-documenting”:

1. `/_templates/`  
   - `interview-script.md`  
   - `evidence-log.csv`  
   - `icp-one-pager.md`  
   - `mvp-scope.md`  
   - `event-taxonomy.md`  
   - `experiment-backlog.md`  
   - `weekly-review.md`  

2. Inside each lab folder, add a `README.md` with:
   - Purpose of the lab  
   - Inputs needed  
   - Outputs expected  
   - Rubric (“done checklist”)  
   - Links to templates used in that lab

3. Add an index file:
- `NAVIGATION.md` that mirrors the “Repo map” plus deep links to key artifacts.

---

## How to use this repo for a real product
- Pick one idea, one ICP, one channel.
- Ship a thin MVP.
- Instrument from day one.
- Run one experiment per week.
- Update ICP and scope based on evidence.

---