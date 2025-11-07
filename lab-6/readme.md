# Lab 6: From Discovery to Development
## Bridging Customer Insights to Sprint Planning

**Duration:** 120 minutes (2 hours)  
**Week:** 6 Friday November 7th, 2025
**Phase:** Transition from "Define" to "Develop"

---

## 🎯 Lab Objectives

By the end of this lab, your team will:

1. ✅ Transform interview insights into **user stories** with acceptance criteria
2. ✅ Create a comprehensive **Product Requirements Document (PRD)** using the PRD Generator prompt in the Guides folder
3. ✅ Define **MVP scope** using evidence-based prioritization
4. ✅ Build a **product roadmap** for the next 8 weeks (3 sprints)
5. ✅ Complete **Sprint 1 planning** with specific tasks and assignments
6. ✅ Set up **development infrastructure** in GitHub

---

## 📍 Where You Are

**You've completed:**
- ✅ 10+ customer interviews with detailed logs
- ✅ Synthesis workshop with pattern identification
- ✅ Evidence-based final problem statement
- ✅ Understanding of AARRR framework and analytics
- ✅ Knowledge of development processes (Lean, Agile, Waterfall)

**Today you'll create:**
- Your product's feature set based on interview evidence
- A clear plan for the next 6 weeks of development
- Sprint 1 tasks ready for immediate execution

---

## ⏱️ Lab Timeline

| Time | Activity | Output |
|------|----------|--------|
| 0:00-0:20 | Part 1: Synthesis Review & User Story Creation | 8-12 user stories |
| 0:20-0:40 | Part 2: MVP Definition & Feature Prioritization | MVP feature list |
| 0:40-1:10 | Part 3: Product Roadmap Creation | 8-week roadmap |
| 1:10-1:40 | Part 4: Sprint 1 Planning | Sprint 1 backlog |
| 1:40-2:00 | Part 5: Development Setup & Next Steps | GitHub structure |

---

## 📦 What You'll Create Today

### Folder Structure
```
/03-build/
├── prd/
│   └── product-requirements.md           # Comprehensive PRD
├── user-stories/
│   ├── user-stories-list.md             # All user stories
│   └── story-mapping.md                 # User story map
├── roadmap/
│   ├── product-roadmap.md               # 8-week timeline
│   ├── mvp-definition.md                # MVP scope & rationale
│   └── feature-prioritization.md        # Prioritization matrix
├── sprints/
│   ├── sprint-1-plan.md                 # Weeks 7-8
│   ├── sprint-2-plan.md                 # Weeks 9-10 (outline)
│   └── sprint-3-plan.md                 # Weeks 11-12 (outline)
├── architecture/
│   ├── tech-stack.md                    # Technology decisions
│   └── system-design-v1.md              # Initial architecture
└── process/
    └── team-workflow.md                 # Your Agile process map
```

---

## Part 1: Synthesis Review & User Story Creation
### Duration: 20 minutes (0:00 - 0:20)

### Objective
Transform interview insights into actionable user stories that directly address validated pain points.

### Instructions

1. **Quick Synthesis Review (5 min)**
   - Open `/01-discovery/synthesis/final-problem-statement.md`
   - Each team member silently reviews top 3 pain points
   - Note current workarounds users mentioned
   
2. **Individual Story Writing (7 min)**
   - Each person writes 3-5 user stories on sticky notes
   - Format: "As a [user type], I want to [action], so that [benefit]"
   - Must cite interview number that supports this need
   - Example: "As a commuter student, I want to see real-time study room availability, so that I don't waste 15 minutes wandering buildings (Interviews #3, #7, #12)"

3. **Team Consolidation (8 min)**
   - Share all stories
   - Group similar stories together
   - Remove duplicates
   - Select 8-12 strongest stories (backed by multiple interviews)
   - Document in template

### Deliverable
✅ `/03-build/user-stories/user-stories-list.md` with 8-12 evidence-backed user stories

**Quality Check:**
- [ ] Each story cites specific interview numbers
- [ ] Stories focus on outcomes, not solutions
- [ ] At least 8 unique stories
- [ ] Stories directly address validated pain points

---

## Part 2: MVP Definition & Feature Prioritization
### Duration: 20 minutes (0:20 - 0:40)

### Objective
Define your Minimum Viable Product - what you'll build in 6 weeks to validate your solution hypothesis.

### Instructions

1. **Feature Extraction (5 min)**
   - Review your user stories
   - For each story, brainstorm 2-3 features that would fulfill it
   - Be specific: Not "dashboard" but "real-time occupancy heatmap"
   - Write each feature on a sticky note
   - Aim for 20-30 potential features

2. **Value vs. Effort Scoring (10 min)**
   - Draw a 2x2 matrix: Value (High/Low) vs Effort (High/Low)
   - For each feature, team discusses:
     - **Value**: How many interviews mentioned this pain? How intense was it? (1-5 scale)
     - **Effort**: Technical complexity? Time needed? (1-5 scale)
   - Plot each feature on the matrix
   - Use template: `/lab-6/templates/feature-prioritization-template.md`

3. **MVP Selection (5 min)**
   - Select features from "High Value, Low-Medium Effort" quadrant
   - Choose 5-8 features that form a **coherent user experience**
   - Test: Can someone complete a full workflow with just these features?
   - Document rationale for each inclusion/exclusion

### Deliverable
✅ `/03-build/roadmap/mvp-definition.md` - MVP scope with justification
✅ `/03-build/roadmap/feature-prioritization.md` - Scoring matrix with all features

**Quality Check:**
- [ ] 5-8 features selected for MVP
- [ ] Each feature has Value and Effort scores
- [ ] MVP forms a complete user journey
- [ ] Rationale tied to interview evidence
- [ ] Excluded features are documented with reasons

---

## Part 3: Product Roadmap Creation
### Duration: 30 minutes (0:40 - 1:10)

### Objective
Create a tactical 8-week roadmap showing how you'll build, test, and iterate your product across 3 sprints.

### Instructions

1. **Define Sprint Themes (10 min)**
   
   **Sprint 1 (Weeks 7-8): Foundation & Core Features**
   - Goals: Build basic infrastructure, implement 2-3 core features
   - Success: Users can complete basic workflow
   - Validation: Internal testing with team
   
   **Sprint 2 (Weeks 9-10): User Testing & Iteration**
   - Goals: Complete remaining MVP features, conduct user testing
   - Success: 5+ real users test and provide feedback
   - Validation: Usability testing, metrics tracking begins
   
   **Sprint 3 (Weeks 11-12): Polish & Analytics Integration**
   - Goals: Iterate based on feedback, add analytics, prepare demo
   - Success: Production-ready MVP with instrumentation
   - Validation: Success metrics defined and tracking

2. **Feature Allocation (15 min)**
   - Assign your 5-8 MVP features to sprints
   - Consider technical dependencies (what must be built first?)
   - Balance complexity across sprints
   - Add specific validation activities to each sprint
   - Include buffer for unexpected complexity

   **Example allocation:**
   - Sprint 1: User authentication, database setup, Feature A, Feature B
   - Sprint 2: Feature C, Feature D, Feature E, user testing sessions
   - Sprint 3: Feedback iteration, analytics integration, polish, demo prep

3. **Risk Documentation (5 min)**
   - Identify 3-5 biggest risks in your roadmap
   - For each risk: What's the mitigation plan?
   - Example: "Risk: External API might be unreliable. Mitigation: Build caching layer in Sprint 1"

### Deliverable
✅ `/03-build/roadmap/product-roadmap.md` - Complete 8-week roadmap with sprints, features, and risks

**Quality Check:**
- [ ] All MVP features assigned to sprints
- [ ] Each sprint has clear goals and success criteria
- [ ] Validation activities included in roadmap
- [ ] Technical dependencies considered
- [ ] 3-5 risks identified with mitigations
- [ ] Visual timeline or Gantt chart included

---

## Part 4: Sprint 1 Planning
### Duration: 30 minutes (1:10 - 1:40)

### Objective
Create a detailed, actionable Sprint 1 plan that your team can execute starting Monday.

### Instructions

1. **User Story Selection for Sprint 1 (5 min)**
   - Review your roadmap
   - Select 3-4 user stories for Sprint 1
   - These should be foundational (other features depend on them)
   - Must be completable in 2 weeks by your team

2. **Task Decomposition (15 min)**
   
   For EACH user story, break down into tasks across categories:
   
   **Design Tasks:**
   - Wireframes needed
   - User flow diagrams
   - UI component design
   
   **Frontend Tasks:**
   - Component development
   - State management
   - API integration
   
   **Backend Tasks:**
   - Database schema
   - API endpoints
   - Business logic
   
   **Testing Tasks:**
   - Unit tests
   - Integration tests
   - Manual testing scenarios
   
   **Documentation:**
   - API documentation
   - Setup instructions
   - User guide sections
   
   **Estimate each task:** 2, 4, or 8 hours (no bigger than 8 hours!)

3. **Assignment & Dependencies (10 min)**
   - Assign owner to each task (based on expertise)
   - Identify dependencies: "Task X must finish before Task Y"
   - Set target completion dates within the 2-week sprint
   - Flag any blockers that need immediate resolution
   - Calculate total hours per person (should be 15-20 hours max for this course)

### Deliverable
✅ `/03-build/sprints/sprint-1-plan.md` - Detailed Sprint 1 plan with tasks, owners, estimates, dependencies
✅ `/03-build/sprints/sprint-2-plan.md` - High-level outline (which features, rough goals)
✅ `/03-build/sprints/sprint-3-plan.md` - High-level outline (which features, rough goals)

**Quality Check:**
- [ ] 3-4 user stories selected for Sprint 1
- [ ] Each story broken into specific tasks
- [ ] All tasks have owners assigned
- [ ] Task estimates provided (2, 4, or 8 hours)
- [ ] Dependencies identified
- [ ] Total hours per person is reasonable (15-20 hours)
- [ ] Sprint 2 and 3 have rough outlines

---

## Part 5: Development Setup & Next Steps
### Duration: 20 minutes (1:40 - 2:00)

### Objective
Set up your development infrastructure and ensure everyone is unblocked for Sprint 1.

### Instructions

1. **Tech Stack Documentation (7 min)**
   - Document your final technology choices:
     - Frontend framework (React, Vue, vanilla JS?)
     - Backend framework (Node/Express, Python/Flask, etc.)
     - Database (PostgreSQL, MongoDB, Firebase?)
     - Hosting (Vercel, Heroku, AWS?)
     - Analytics (Mixpanel, Amplitude, PostHog?)
   - For each choice, document WHY (2-3 sentences)
   - Note any "spikes" needed (research tasks for uncertain tech)
   - Complete template: `/lab-6/templates/tech-stack-template.md`

2. **GitHub Infrastructure Setup (8 min)**
   - Create all `/03-build/` subfolders in your team repo
   - Set up GitHub Issues for all Sprint 1 tasks
     - Title format: `[USER STORY] Task name`
     - Assign to owner
     - Add labels: `sprint-1`, `frontend`, `backend`, etc.
   - Optional: Create GitHub Project board for Sprint 1
   - Ensure all team members have write access
   - Test: Everyone can clone, create branch, push

3. **Process Documentation (5 min)**
   - Document your team's Agile workflow:
     - **Standups**: When? (Daily recommended, 5-10 min)
     - **Sprint Review**: End of Week 8 (demo what you built)
     - **Sprint Retrospective**: End of Week 8 (what to improve)
     - **Definition of Done**: What criteria must tasks meet?
     - **Communication**: Slack/WhatsApp for daily, GitHub for code review
   - Complete template: `/lab-6/templates/team-workflow-template.md`
   - All team members must agree and sign off

### Deliverable
✅ `/03-build/architecture/tech-stack.md` - Documented technology decisions
✅ Complete `/03-build/` folder structure in GitHub
✅ Sprint 1 tasks as GitHub Issues
✅ `/03-build/process/team-workflow.md` - Team's Agile process agreement

**Quality Check:**
- [ ] All folders created in `/03-build/`
- [ ] Tech stack choices documented with rationale
- [ ] All Sprint 1 tasks in GitHub Issues with owners
- [ ] Team workflow documented and agreed upon
- [ ] Everyone can access and push to repo
- [ ] Definition of Done is clear and specific

---

## 📝 Homework (Due Thursday 11:59 PM)

### Individual Homework (Choose ONE, 30-45 min)

**Option A: Technical Spike Report**
- Research ONE technical risk/uncertainty from your roadmap
- Try a quick proof-of-concept if possible
- Document findings: What works? What doesn't? Recommendation?
- File: `/03-build/architecture/spike-[topic-name].md`
- Example topics: API integration, real-time updates, authentication, database scaling

**Option B: Competitive Analysis**
- Analyze 3 existing solutions (competitors or adjacent products)
- Create comparison table: Features, pricing, strengths, weaknesses
- Identify gaps your product will fill
- File: `/03-build/research/competitive-analysis.md`

**Option C: Process Workflow Diagram**
- Create visual diagram of your team's development workflow
- Include: git branching strategy, code review process, deployment pipeline
- Use draw.io, Miro, or hand-drawn + photo
- File: `/03-build/process/workflow-diagram.png` + `/03-build/process/workflow-explanation.md`

### Team Homework (60-90 min, meet together or async)

**Required Deliverables:**

1. **Complete PRD** (45 min)
   - Use template: `/lab-6/templates/prd-template.md`
   - Consolidate all lab work into comprehensive PRD
   - Include: Problem statement, user personas, user stories, MVP features, success metrics
   - File: `/03-build/prd/product-requirements.md`

2. **Refine Sprint 1 Plan** (20 min)
   - Add more detail to tasks based on lab discussion
   - Update estimates if needed
   - Verify all team members understand their assignments
   - Add any missing tasks discovered during homework

3. **Development Environment Setup** (15 min)
   - Set up shared dev resources (APIs, databases, hosting)
   - Create `.env.example` file with required environment variables
   - Ensure all team members can run "Hello World" in your stack
   - Document setup steps in `/03-build/architecture/setup-instructions.md`

4. **Sprint Kickoff Meeting** (10 min)
   - Schedule your Sprint 1 kickoff for Monday or Tuesday
   - Agenda: Review sprint goals, confirm task assignments, address blockers
   - Calendar invite to all team members

### Submission Checklist

- [ ] Individual spike/analysis/diagram completed and committed
- [ ] PRD complete and reviewed by all team members
- [ ] Sprint 1 plan refined with detailed tasks
- [ ] Development environment set up and tested
- [ ] Sprint kickoff meeting scheduled
- [ ] All files committed to GitHub in proper folders
- [ ] README updated with current status

---

## ✅ Success Criteria

### Minimum (Passing)
- 8+ user stories with interview citations
- MVP defined with 5+ features and prioritization
- 8-week roadmap with 3 sprints outlined
- Sprint 1 plan with tasks and owners
- GitHub structure created
- Homework completed

### Target (Excellent)
- User stories directly quote interviews
- Feature prioritization with quantitative matrix
- Roadmap includes detailed validation milestones
- Sprint 1 has task dependencies and realistic estimates
- GitHub Issues created with labels and assignments
- Tech stack decisions thoroughly justified
- Team workflow with Definition of Done
- All homework exceeds minimum requirements

---

## 🚨 Common Pitfalls & How to Avoid Them

| ❌ Pitfall | ✅ Solution |
|-----------|-----------|
| User stories too vague or solution-focused | Cite specific interviews, focus on user outcomes |
| Including features not backed by research | Every feature must trace to interview evidence |
| Overcommitting in Sprint 1 | Be conservative, you don't know your velocity yet |
| Choosing tech based on "cool factor" | Select familiar stack unless spike validated new tech |
| Treating roadmap as rigid | Build in flexibility, expect to adapt |
| Not documenting decisions | Future-you will forget why you chose X over Y |
| Skipping Definition of Done | Leads to "90% done" tasks that drag on |
| Tasks larger than 8 hours | Break down further, smaller = more trackable |

---

## 📚 Resources

### Templates (All in `/lab-6/templates/`)
- `user-story-template.md`
- `prd-template.md`
- `mvp-definition-template.md`
- `product-roadmap-template.md`
- `sprint-plan-template.md`
- `tech-stack-template.md`
- `team-workflow-template.md`
- `feature-prioritization-template.md`

### Examples (All in `/lab-6/examples/`)
- `example-user-stories.md` - Good and bad examples
- `example-prd.md` - Sample PRD for a study room finder
- `example-mvp-definition.md` - Well-justified MVP scope
- `example-sprint-planning.md` - Detailed sprint plan with tasks

### Reading (Optional but Recommended)
- "User Stories Applied" by Mike Cohn - Chapter 1
- "The Lean Startup" by Eric Ries - Chapter 5 (MVP)
- Scrum Guide - Sprint Planning section

---

## 🆘 Getting Help

### During Lab
- Raise hand for instructor
- Ask neighboring team for input
- Reference templates and examples
- Use synthesis findings as your north star

### After Lab
- **Email:** zeshan.ahmad@kiu.edu.ge (urgent blockers only)
- **Peer Support:** Reach out to other teams

### Common Questions

**Q: What if we can't finish all MVP features in 6 weeks?**  
A: That's why it's called "Minimum" Viable Product. Cut scope, not quality. Better to deliver 4 polished features than 8 half-done ones.

**Q: Can we change our MVP during the sprints?**  
A: Yes! That's Agile. But document why and ensure changes are evidence-based (user testing, technical constraints).

**Q: How detailed should Sprint 1 tasks be?**  
A: Detailed enough that someone could start working on them Monday morning without asking clarifying questions.

**Q: What if our team can't agree on priorities?**  
A: Use the Value vs Effort matrix objectively. If still deadlocked, program manager decides. Document dissenting opinions but commit to the decision.

---

## 🎯 Preview

### Week 7 Lecture: Agile Fundamentals & Scrum
- Scrum roles (Product Owner, Scrum Master, Dev Team)
- Ceremonies (Sprint Planning, Daily Standup, Review, Retro)
- Story points and estimation techniques
- Velocity and burndown charts

### Week 7 Lab: Sprint 1 Kickoff
- Sprint planning ceremony
- Set up standup routine
- Begin Sprint 1 execution
- First code commits!

**Come prepared:** Sprint 1 plan finalized, dev environment working, ready to code!

---

## 📊 Grading Rubric

### Lab Participation (10 points)
| Component | Points | Criteria |
|-----------|--------|----------|
| User Stories | 2 | 8+ stories with interview citations |
| MVP Definition | 2 | Clear scope with prioritization matrix |
| Product Roadmap | 2 | 8-week timeline with sprint allocation |
| Sprint 1 Plan | 3 | Detailed tasks, owners, estimates, dependencies |
| GitHub Setup | 1 | Proper folder structure and Issues created |

### Homework Quality (5 points)
| Component | Points | Criteria |
|-----------|--------|----------|
| Individual Work | 2 | Spike/analysis/diagram complete and insightful |
| Team PRD | 2 | Comprehensive, evidence-based, well-structured |
| Sprint Refinement | 1 | Sprint 1 plan detailed and actionable |

**Total: 15 points** (1.5% of final grade)

**Note:** Quality matters more than quantity. Better to have 8 excellent user stories than 15 weak ones.

---

## 🎓 Learning Outcomes Alignment

This lab directly supports:
- **LO-3:** Apply product development methodologies (Agile sprint planning)
- **LO-5:** Translate user research into product requirements
- **LO-7:** Plan and execute iterative development cycles
- **LO-9:** Make evidence-based product decisions
- **LO-11:** Document technical and product decisions professionally

---

## 🔄 Continuous Improvement

This is the first semester using this lab structure. Your feedback helps improve it!

**After lab, please complete the 2-minute feedback form:** [Link will be provided in lab]

Quick questions:
- What was most valuable?
- What was confusing?
- What should we add/remove?
- Time management: Too much/too little?

---

**Last Updated:** Week 6, Fall 2025  
**Course:** CS-PD-2025 | Product Development for Software Engineers  
**Instructor:** Zeshan Ahmad | zeshan.ahmad@kiu.edu.ge  
**Office:** Room K-305 | Tuesday & Thursday 2-4 PM
