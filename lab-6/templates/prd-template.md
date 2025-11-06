# Product Requirements Document (PRD)

**Product Name:** [Your Product Name]  
**Team:** [Team Name]  
**Version:** 1.0  
**Date:** [Date]  
**Status:** Draft / In Review / Approved  
**Owner:** [Product Manager Name]

---

## Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [Date] | [Name] | Initial draft |
| | | | |

**Approval:**
- [ ] All team members reviewed
- [ ] Technical Lead approved
- [ ] Instructor feedback incorporated

---

## Executive Summary

[2-3 paragraphs that answer: What are we building? Who is it for? Why does it matter? What's the expected impact?]

**One-Line Pitch:** [One sentence description of your product]

**Problem We're Solving:** [One paragraph summary from your discovery research]

**Solution Overview:** [One paragraph describing your approach]

**Success Metric:** [One key number that defines success]

---

## Table of Contents

1. [Problem Statement](#problem-statement)
2. [Target Users](#target-users)
3. [Goals & Success Metrics](#goals--success-metrics)
4. [User Needs & Stories](#user-needs--stories)
5. [Product Overview](#product-overview)
6. [MVP Scope](#mvp-scope)
7. [Features & Requirements](#features--requirements)
8. [User Experience](#user-experience)
9. [Technical Architecture](#technical-architecture)
10. [Assumptions & Dependencies](#assumptions--dependencies)
11. [Risks & Mitigation](#risks--mitigation)
12. [Timeline & Milestones](#timeline--milestones)
13. [Out of Scope](#out-of-scope)
14. [Appendix](#appendix)

---

## 1. Problem Statement

### The Problem

[Detailed description of the problem based on your interview synthesis]

**Problem Severity:**
- **Frequency:** [How often does this problem occur?]
- **Intensity:** [How painful is it when it happens?]
- **Economic Impact:** [Time lost, money wasted, opportunities missed]

**Evidence:**
- Interview #X: "[Quote]"
- Interview #Y: "[Quote]"
- Pattern: [X out of Y] interviews mentioned this problem
- Quantified impact: [Specific numbers from interviews]

### Current Solutions & Why They Fail

**What people do now:**
1. [Current workaround #1]: Why it doesn't work
2. [Current workaround #2]: Why it doesn't work
3. [Current workaround #3]: Why it doesn't work

**Evidence:**
- [Cite interviews describing current solutions and their failures]

### Opportunity

[Why now? Why hasn't this been solved? What's changed that makes this solvable now?]

---

## 2. Target Users

### Primary User Persona: [Name]

**Demographics:**
- Age range: [X-Y years]
- Role/Occupation: [Specific role]
- Location: [Where they are]
- Education: [Level]
- Tech savviness: [Low / Medium / High]

**Psychographics:**
- Goals: [What they're trying to achieve]
- Frustrations: [What annoys them]
- Motivations: [What drives them]
- Behaviors: [How they currently work]

**Quote from Interviews:**
> "[Representative quote from an actual interview]"

**Jobs To Be Done:**
1. When [situation], I want to [action], so that [outcome]
2. When [situation], I want to [action], so that [outcome]

**Interview Evidence:**
- Represents [X] out of [Y] interviewees
- Interviews: #1, #3, #7, #9, #12

---

### Secondary User Persona: [Name] (if applicable)

[Repeat structure above]

---

### User Segmentation

| Segment | Size | Priority | Why |
|---------|------|----------|-----|
| [Segment 1] | [#/%] | High | [Reasoning] |
| [Segment 2] | [#/%] | Medium | [Reasoning] |
| [Segment 3] | [#/%] | Low | [Reasoning] |

**Initial Focus:** [Which segment are you targeting first and why?]

---

## 3. Goals & Success Metrics

### Product Vision

[One paragraph: Where do you see this product in 1 year? What impact will it have?]

### Goals

**Primary Goal:**
[Main objective for MVP period - must be specific and measurable]

**Secondary Goals:**
1. [Goal 2]
2. [Goal 3]

### Success Metrics (AARRR Framework)

**Acquisition:**
- Metric: [How will you acquire users?]
- Target: [Specific number]
- Measurement: [How will you track?]

**Activation:**
- Metric: [What's your "aha moment"?]
- Target: [% of signups who activate]
- Measurement: [Specific event tracking]

**Retention:**
- Metric: [What makes someone a repeat user?]
- Target: [% who return within X days]
- Measurement: [How you'll track]

**Revenue:** (if applicable)
- Metric: [N/A for academic project, or describe if relevant]

**Referral:**
- Metric: [Will you track word-of-mouth?]
- Target: [X referrals per user]

**North Star Metric:**
[One single metric that best captures value delivery]

---

## 4. User Needs & Stories

### Core User Needs (from Discovery)

**Need #1:** [High-priority need]
- **Evidence:** Mentioned in interviews #X, #Y, #Z
- **Intensity:** [Scale 1-10 from interviews]
- **Quotes:** "[Direct quote]"

**Need #2:** [Second priority]
[Repeat structure]

**Need #3:** [Third priority]
[Repeat structure]

### User Stories (Summary)

[Link to full document: `/03-build/user-stories/user-stories-list.md`]

**MVP Stories:**
1. User Story #1: [Title]
2. User Story #2: [Title]
3. User Story #3: [Title]
4. User Story #4: [Title]

**Post-MVP Stories:**
1. User Story #5: [Title]
2. User Story #6: [Title]

[See full user stories document for complete acceptance criteria]

---

## 5. Product Overview

### High-Level Description

[3-4 paragraphs describing what you're building, how it works, and why this approach addresses the validated problem]

### Core Value Proposition

**For** [target user]  
**Who** [statement of need]  
**The** [product name]  
**Is a** [product category]  
**That** [key benefit / problem solved]  
**Unlike** [current alternatives]  
**Our product** [key differentiator]

### Key Differentiators

1. **[Differentiator 1]:** How you're different from alternatives
2. **[Differentiator 2]:** What makes you unique
3. **[Differentiator 3]:** Why users will choose you

**Evidence:** [How do you know these differentiators matter to users?]

---

## 6. MVP Scope

### Definition of MVP

[Describe your Minimum Viable Product philosophy for this project]

**MVP Thesis:**
[One paragraph: This is the minimum set of features needed to validate our core hypothesis: that [your solution] will [solve the problem] for [target users] better than [alternatives]]

### MVP Features (Summary)

[Link to full definition: `/03-build/roadmap/mvp-definition.md`]

| Feature | Why It's in MVP | Value Score | Effort Score |
|---------|----------------|-------------|--------------|
| Feature 1 | [Reasoning] | 5/5 | 2/5 |
| Feature 2 | [Reasoning] | 5/5 | 3/5 |
| Feature 3 | [Reasoning] | 4/5 | 2/5 |
| Feature 4 | [Reasoning] | 4/5 | 3/5 |
| Feature 5 | [Reasoning] | 4/5 | 2/5 |

### MVP User Journey

[Describe the end-to-end experience a user will have with your MVP]

**Step 1:** [User action] → [System response] → [Outcome]  
**Step 2:** [User action] → [System response] → [Outcome]  
**Step 3:** [User action] → [System response] → [Outcome]  
[etc...]

### What's NOT in MVP (and why)

| Feature | Why Excluded | When to Revisit |
|---------|-------------|----------------|
| Feature X | [Reasoning] | Sprint 2 / Post-launch |
| Feature Y | [Reasoning] | Post-launch |
| Feature Z | [Reasoning] | If validation succeeds |

---

## 7. Features & Requirements

### Feature #1: [Feature Name]

**Description:** [What is this feature?]

**User Story:** [Link to user story #X]

**Functional Requirements:**
1. System shall [requirement]
2. System shall [requirement]
3. System shall [requirement]

**Non-Functional Requirements:**
- **Performance:** [Load time, response time requirements]
- **Scalability:** [How many users/requests must it handle?]
- **Security:** [What data protection is needed?]
- **Accessibility:** [Any accessibility requirements?]

**Acceptance Criteria:**
1. Given [context], when [action], then [result]
2. Given [context], when [action], then [result]

**Priority:** P0 (Must-Have) / P1 (Should-Have) / P2 (Nice-to-Have)

**Dependencies:**
- [Technical dependency]
- [Other feature dependency]

**Open Questions:**
- [ ] [Question that needs answer]

---

### Feature #2: [Feature Name]

[Repeat structure for each MVP feature]

---

### Feature #3: [Feature Name]

[Continue for all features...]

---

## 8. User Experience

### Information Architecture

[Describe the structure of your application]

**Main Sections:**
1. [Section 1]: Purpose and contents
2. [Section 2]: Purpose and contents
3. [Section 3]: Purpose and contents

**Navigation Flow:**
[Describe how users move through the application]

### Key User Flows

**Flow 1: [Core User Journey Name]**

1. **Entry Point:** [How user starts]
2. **Step 1:** [Action] → [Screen] → [Result]
3. **Step 2:** [Action] → [Screen] → [Result]
4. **Step 3:** [Action] → [Screen] → [Result]
5. **Success State:** [What happens when completed]
6. **Error States:** [What happens if something goes wrong]

**Flow 2: [Another Key Journey]**
[Repeat structure]

### Wireframes / Mockups

[Include links to Figma, hand-drawn sketches, or describe key screens]

**Screen 1: [Name]**
- Purpose: [What user does here]
- Key elements: [List main UI components]
- Link: [Figma/image link]

**Screen 2: [Name]**
[Repeat]

---

## 9. Technical Architecture

[Link to full document: `/03-build/architecture/system-design-v1.md`]

### Tech Stack

**Frontend:**
- Framework: [React / Vue / Vanilla JS / etc.]
- Key libraries: [List]
- Reasoning: [Why these choices?]

**Backend:**
- Framework: [Express / Flask / etc.]
- Database: [PostgreSQL / MongoDB / etc.]
- Reasoning: [Why these choices?]

**Infrastructure:**
- Hosting: [Vercel / Heroku / AWS / etc.]
- CI/CD: [GitHub Actions / etc.]
- Reasoning: [Why these choices?]

**Analytics:**
- Tool: [Mixpanel / PostHog / etc.]
- Events: [Number of events being tracked]
- Reasoning: [Why this choice?]

### High-Level Architecture

```
[Include a simple diagram or ASCII art showing:]
User → Frontend → API → Backend → Database
                ↓
          Analytics Platform
```

### Data Model (High-Level)

**Entity 1:** [Name]
- Key attributes: [List main fields]
- Relationships: [To other entities]

**Entity 2:** [Name]
- Key attributes: [List main fields]
- Relationships: [To other entities]

### API Endpoints (Key Endpoints)

| Method | Endpoint | Purpose | Auth Required |
|--------|----------|---------|---------------|
| GET | /api/[resource] | [Purpose] | Yes / No |
| POST | /api/[resource] | [Purpose] | Yes / No |
| PUT | /api/[resource]/:id | [Purpose] | Yes / No |
| DELETE | /api/[resource]/:id | [Purpose] | Yes / No |

---

## 10. Assumptions & Dependencies

### Assumptions

**User Assumptions:**
1. [Assumption about user behavior] - **Validation:** [How you'll test]
2. [Assumption about user needs] - **Validation:** [How you'll test]
3. [Assumption about user context] - **Validation:** [How you'll test]

**Technical Assumptions:**
1. [Technical assumption] - **Risk:** [What if wrong?]
2. [Technical assumption] - **Risk:** [What if wrong?]

**Business Assumptions:**
1. [Business assumption] - **Risk:** [What if wrong?]

### External Dependencies

| Dependency | Type | Risk | Mitigation |
|------------|------|------|------------|
| [External API] | Service | High | [Backup plan] |
| [Library X] | Code | Medium | [Alternative] |
| [Service Y] | Infrastructure | Low | [Workaround] |

### Internal Dependencies

| Dependency | Owner | Delivery Date | Impact if Delayed |
|------------|-------|---------------|-------------------|
| [Component X] | [Name] | [Date] | [Impact] |
| [Feature Y] | [Name] | [Date] | [Impact] |

---

## 11. Risks & Mitigation

### High-Priority Risks

**Risk #1: [Risk Description]**
- **Likelihood:** High / Medium / Low
- **Impact:** High / Medium / Low
- **Mitigation:** [What you'll do to prevent/reduce risk]
- **Contingency:** [What you'll do if risk materializes]
- **Owner:** [Who's monitoring this]

**Risk #2: [Risk Description]**
[Repeat structure]

**Risk #3: [Risk Description]**
[Repeat structure]

### Medium-Priority Risks

[List and briefly describe]

### Known Constraints

**Time Constraints:**
- [Constraint and impact]

**Technical Constraints:**
- [Constraint and impact]

**Resource Constraints:**
- [Constraint and impact]

---

## 12. Timeline & Milestones

[Link to full roadmap: `/03-build/roadmap/product-roadmap.md`]

### 8-Week Development Plan

**Sprint 1: Foundation (Weeks 7-8)**
- **Goal:** [Sprint goal]
- **Deliverables:**
  - [ ] Feature A
  - [ ] Feature B
  - [ ] Basic infrastructure
- **Success Criteria:** [How you'll know if successful]

**Sprint 2: User Testing (Weeks 9-10)**
- **Goal:** [Sprint goal]
- **Deliverables:**
  - [ ] Feature C
  - [ ] Feature D
  - [ ] User testing (5+ users)
- **Success Criteria:** [How you'll know if successful]

**Sprint 3: Polish & Launch (Weeks 11-12)**
- **Goal:** [Sprint goal]
- **Deliverables:**
  - [ ] Feature E (iteration)
  - [ ] Analytics integration
  - [ ] Demo preparation
- **Success Criteria:** [How you'll know if successful]

### Key Milestones

| Milestone | Date | Definition of Success |
|-----------|------|----------------------|
| Sprint 1 Complete | Week 8 end | [Criteria] |
| MVP User Testing | Week 10 | [Criteria] |
| MVP Complete | Week 12 | [Criteria] |
| Final Demo | Week 15 | [Criteria] |

---

## 13. Out of Scope

### Explicitly NOT Included in MVP

1. **[Feature/Capability]:** Why it's out of scope, when to revisit
2. **[Feature/Capability]:** Why it's out of scope, when to revisit
3. **[Feature/Capability]:** Why it's out of scope, when to revisit

### Future Considerations (Post-Course)

**Phase 2 Ideas:**
- [Future feature based on interview insights]
- [Future feature based on interview insights]

**Deferred Based on Technical Complexity:**
- [Feature that's too complex for 6 weeks]

**Deferred Based on Market Validation:**
- [Feature to add if initial validation succeeds]

---

## 14. Appendix

### A. Interview Summary

**Total Interviews Conducted:** [Number]  
**Date Range:** [Start date] - [End date]  
**Interview Documentation:** `/01-discovery/interview-logs/`  
**Synthesis Results:** `/01-discovery/synthesis/`

**Key Insights:**
1. [Insight 1]
2. [Insight 2]
3. [Insight 3]

### B. Research & Competitive Analysis

[Link to research documents if completed]

### C. Technical Spikes

[Link to spike reports: `/03-build/architecture/spike-*.md`]

### D. References

**Industry Research:**
- [Source 1]
- [Source 2]

**Technical Documentation:**
- [Framework docs]
- [API docs]

### E. Glossary

| Term | Definition |
|------|------------|
| [Term 1] | [Definition] |
| [Term 2] | [Definition] |

---

## Sign-Off

**Team Agreement:**
- [ ] [Team Member 1] - Reviewed and approved
- [ ] [Team Member 2] - Reviewed and approved
- [ ] [Team Member 3] - Reviewed and approved
- [ ] [Team Member 4] - Reviewed and approved

**Instructor Feedback:**
[Space for instructor comments]

**Approval Date:** [Date]

---

## Document Maintenance

**Update Frequency:** Review and update after each sprint

**Change Log:**
| Date | Section | Change | Reason |
|------|---------|--------|--------|
| [Date] | [Section] | [What changed] | [Why] |

**Next Review Date:** [End of Sprint 1]

---

**Document Location:** `/03-build/prd/product-requirements.md`  
**Related Documents:**
- User Stories: `/03-build/user-stories/user-stories-list.md`
- Product Roadmap: `/03-build/roadmap/product-roadmap.md`
- Technical Architecture: `/03-build/architecture/system-design-v1.md`
- Interview Synthesis: `/01-discovery/synthesis/final-problem-statement.md`

---

**Questions or Feedback?** Contact [Team Lead] or post in #lab-6-questions
