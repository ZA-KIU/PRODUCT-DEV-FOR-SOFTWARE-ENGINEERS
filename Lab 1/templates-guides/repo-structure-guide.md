# GitHub Repository Structure Guide

## 📂 Recommended Folder Organization

Your team's repository should follow this structure for maximum clarity and collaboration:

```
/team-[your-team-name]/
│
├── README.md                          # Team overview & project summary
│
├── /00-foundation/                    # Week 1 foundational documents
│   ├── team-contract.md
│   ├── icp-draft-1.md
│   └── initial-problem-statement.md
│
├── /01-discovery/                     # Week 2-3 user research
│   ├── interview-guide.md
│   ├── /interviews/
│   │   ├── interview-001-[name].md
│   │   ├── interview-002-[name].md
│   │   └── ...
│   ├── /synthesis/
│   │   ├── patterns-analysis.md
│   │   ├── key-insights.md
│   │   └── icp-v2.md
│   └── /recordings/                   # If you have consent
│       └── [interview-recordings]
│
├── /02-ideation/                      # Week 4 solution brainstorming
│   ├── solution-concepts.md
│   ├── feature-prioritization.md
│   ├── /sketches/
│   │   └── [wireframe-images]
│   └── mvp-definition.md
│
├── /03-prototyping/                   # Week 5-6 building
│   ├── /src/                          # Your code
│   ├── /designs/                      # Figma links, mockups
│   ├── technical-decisions.md
│   └── prototype-changelog.md
│
├── /04-validation/                    # Week 7-8 testing
│   ├── usability-test-plan.md
│   ├── /test-sessions/
│   │   └── [test-notes]
│   ├── iteration-log.md
│   └── final-learnings.md
│
├── /05-delivery/                      # Week 9-10 final prep
│   ├── pitch-deck.pdf
│   ├── demo-script.md
│   ├── product-roadmap.md
│   └── reflection.md
│
└── /resources/                        # Reference materials
    ├── meeting-notes/
    ├── references.md
    └── tools-we-use.md
```

---

## 📝 Key Files Explained

### Root Level

**`README.md`** - Your Team's Homepage
```markdown
# Team [Name]

## Problem Statement
[One sentence describing the problem you're solving]

## Team Members
- [Name] - [Role] - [GitHub: @username]
- [Name] - [Role] - [GitHub: @username]
...

## Project Status
[Current phase, what you're working on]

## Quick Links
- [Team Contract](./00-foundation/team-contract.md)
- [Latest ICP](./01-discovery/synthesis/icp-v2.md)
- [Prototype](./03-prototyping/src/)
- [Final Pitch](./05-delivery/pitch-deck.pdf)
```

### 00-foundation/

**`team-contract.md`**
- Your working agreement
- Roles, decision rules, conflict resolution
- Update if your process changes

**`icp-draft-1.md`**
- Initial Ideal Customer Profile
- Will evolve—keep this as "v1" for reference

**`initial-problem-statement.md`**
- Your first hypothesis about the problem
- Useful to look back and see how you pivoted

### 01-discovery/

**`interview-guide.md`**
- Your 10 interview questions
- Follow-up prompts
- Opening/closing scripts

**`interviews/interview-[###]-[name].md`** Template:
```markdown
# Interview #[###] - [Participant Name/Pseudonym]

**Date:** [Date]
**Duration:** [X minutes]
**Interviewer:** [Your name]
**Match to ICP:** [Yes/No] - [Why?]

## Key Quotes
- "[Direct quote 1]"
- "[Direct quote 2]"

## Summary
[3-4 sentences of main takeaways]

## Detailed Notes
[Q1: Your question]
[Their response...]

## Insights
- ✅ Confirmed: [What this validated]
- ❌ Contradicted: [What this challenged]
- 💡 New learning: [Unexpected insight]

## Follow-up Actions
- [ ] Re-contact for [specific reason]
- [ ] Get intro to [person they mentioned]
- [ ] Investigate [new angle they raised]
```

**`synthesis/patterns-analysis.md`**
After 5+ interviews, document:
- Recurring themes
- Frequency of pain points
- Common current solutions
- Validated vs invalidated assumptions

**`synthesis/icp-v2.md`**
- Refined customer profile based on interview data
- More specific than v1
- Update as you learn

### 02-ideation/

**`solution-concepts.md`**
- Brainstormed solution ideas
- How each addresses validated pain points
- Pros/cons of each approach

**`feature-prioritization.md`**
- Must-have vs. nice-to-have features
- Rationale for each decision
- MVP scope

### 03-prototyping/

**`/src/`**
- Your actual code
- Follow standard conventions for your tech stack
- Include README in this folder for setup instructions

**`technical-decisions.md`**
Document:
- Tech stack choices (and why)
- Architecture decisions
- Tradeoffs you made
- Lessons learned

### 04-validation/

**`usability-test-plan.md`**
- What you're testing
- Tasks for users to complete
- Success metrics

**`test-sessions/test-[###]-[date].md`** Template:
```markdown
# Usability Test #[###]

**Date:** [Date]
**Participant:** [Name/pseudonym]
**Prototype Version:** [v0.1, v0.2, etc.]

## Tasks
1. [Task 1] - ✅/❌ - [Time: X seconds]
2. [Task 2] - ✅/❌ - [Time: X seconds]

## Observations
- [What worked well]
- [What caused confusion]
- [Unexpected behavior]

## Quotes
- "[What they said]"

## Changes Needed
- [ ] Fix: [Specific issue]
- [ ] Improve: [Enhancement]
```

### 05-delivery/

**`pitch-deck.pdf`**
- Your final presentation
- 10-15 slides max
- Problem → Solution → Demo → Impact

**`reflection.md`**
- What you learned
- What you'd do differently
- Individual team member reflections

---

## 🔧 File Naming Conventions

### General Rules
- **Use lowercase** with hyphens: `my-file-name.md`
- **Be descriptive**: `interview-insights.md` not `notes.md`
- **Include dates when relevant**: `meeting-2024-10-15.md`
- **Number sequentially**: `interview-001.md`, `interview-002.md`

### Examples

✅ **Good:**
- `icp-draft-2.md`
- `interview-012-student-commuter.md`
- `wireframe-v3-home-screen.png`
- `usability-test-plan-round-1.md`

❌ **Bad:**
- `ICP.md` (not descriptive enough)
- `Notes.md` (too generic)
- `interview.md` (no sequence number)
- `final FINAL v2 (1).md` (messy versioning)

---

## 📊 Commit Message Best Practices

### Format
```
[TYPE] Brief description

Optional: More detailed explanation if needed
```

### Types
- `[DOCS]` - Documentation changes
- `[FEAT]` - New feature
- `[FIX]` - Bug fix
- `[REFACTOR]` - Code restructuring
- `[TEST]` - Test-related changes
- `[RESEARCH]` - Interview/discovery work

### Examples

✅ **Good commits:**
- `[DOCS] Add interview #007 notes and key insights`
- `[FEAT] Implement user authentication flow`
- `[RESEARCH] Update ICP based on 10 interviews`
- `[DOCS] Team contract: update meeting cadence to 3x/week`

❌ **Bad commits:**
- `updates`
- `stuff`
- `asdf`
- `fixed it`

---

## 🗂️ File Management Tips

### Version Control

**For evolving documents (ICP, problem statement):**
- Keep old versions with clear naming:
  - `icp-draft-1.md` (original)
  - `icp-draft-2.md` (after 5 interviews)
  - `icp-final.md` (validated version)

**For code:**
- Use Git branches for features
- Merge to main when tested
- Tag releases: `v0.1`, `v0.2`, etc.

### Collaboration

**Use Issues for:**
- Tracking tasks
- Assigning responsibilities
- Discussing blockers

**Use Pull Requests for:**
- Code reviews
- Document reviews (for major changes)
- Getting team sign-off

**Use Wikis for:**
- Longer-form documentation
- Onboarding new team members mid-project
- FAQ that doesn't fit in README

### Backup Strategy

- **Don't only rely on GitHub** - also backup locally
- **Key deliverables:** Keep in Google Drive too (pitch deck, final report)
- **Recordings:** Store in cloud (Dropbox, Drive) with links in repo

---

## 🚀 Setting Up Your Repo

### Initial Setup (Week 1)

```bash
# 1. Clone the class repo
git clone https://github.com/ZA-KIU/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS.git

# 2. Navigate to repo
cd PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS

# 3. Create your team folder
mkdir team-[your-name]
cd team-[your-name]

# 4. Create basic structure
mkdir 00-foundation 01-discovery resources
touch README.md
touch 00-foundation/team-contract.md
touch 00-foundation/icp-draft-1.md

# 5. Commit and push
git add .
git commit -m "[DOCS] Initial team folder structure"
git push origin main
```

### Ongoing Maintenance

**Weekly:**
- [ ] Update README with current status
- [ ] Commit interview notes within 24 hours
- [ ] Tag completed milestones

**Bi-weekly:**
- [ ] Archive old working files to `resources/archive/`
- [ ] Update main docs (ICP, problem statement) if pivoted
- [ ] Review and clean up Issues

**Before Major Milestones:**
- [ ] Create release/tag (e.g., `v0.1-prototype`)
- [ ] Update all documentation
- [ ] Ensure all links work
- [ ] Test setup instructions

---

## 🎨 Documentation Best Practices

### Markdown Formatting

**Use headers for hierarchy:**
```markdown
# Main Title
## Section
### Subsection
#### Detail
```

**Use lists for readability:**
```markdown
**Bullet points:**
- Item 1
- Item 2

**Numbered steps:**
1. First
2. Second
```

**Emphasize key points:**
```markdown
**Bold** for importance
*Italic* for emphasis
`code` for technical terms
> Blockquotes for key insights
```

### Making Docs Scannable

**✅ Good structure:**
```markdown
# User Interview Insights

## Key Findings
- [3-5 bullet points]

## Detailed Analysis
[Longer explanation]

## Next Steps
- [ ] Action item 1
- [ ] Action item 2
```

**❌ Poor structure:**
```markdown
Here are some things we learned and stuff we should do...
[Wall of text with no breaks]
```

### Linking Between Docs

**Use relative links:**
```markdown
See our [Team Contract](../00-foundation/team-contract.md)
Check [Interview #3](./interviews/interview-003.md)
```

**Create a navigation section in README:**
```markdown
## Quick Navigation
- 📋 [Problem Statement](./00-foundation/initial-problem-statement.md)
- 👥 [Customer Profile](./01-discovery/synthesis/icp-v2.md)
- 🛠️ [Prototype](./03-prototyping/src/)
- 📊 [Research Findings](./01-discovery/synthesis/patterns-analysis.md)
```

---

## 🔍 Quality Checklist

Before each major submission, verify:

### Organization
- [ ] Files in correct folders
- [ ] Consistent naming convention
- [ ] No duplicate/outdated files
- [ ] Clear folder structure

### Documentation
- [ ] README is up-to-date
- [ ] All links work
- [ ] No placeholder text
- [ ] Proper formatting (headers, lists, etc.)

### Collaboration
- [ ] All team members have contributed
- [ ] Clear commit history
- [ ] No merge conflicts
- [ ] Assigned tasks in Issues

### Content
- [ ] Deliverables are complete
- [ ] Evidence-based (screenshots, quotes, data)
- [ ] Conclusions supported by research
- [ ] Next steps clearly defined

---

## 💡 Pro Tips

### 1. Keep a Changelog
Create `CHANGELOG.md` to track major decisions:
```markdown
# Changelog

## Week 3 - Discovery
- Pivoted from "study spots" to "commuter scheduling"
- Updated ICP after 8 interviews revealed different pain point

## Week 5 - Prototyping  
- Decided on React + Firebase stack
- Dropped real-time feature due to complexity
```

### 2. Document As You Go
Don't wait until deadline to write up research. Update docs immediately after:
- Interviews
- Team meetings
- Prototyping sessions
- Testing rounds

### 3. Use Templates
Create templates for recurring documents:
- Interview notes
- Meeting minutes
- Weekly updates

### 4. Tag Team Members
Use GitHub @mentions to assign responsibility:
```markdown
## Action Items
- [ ] Review interview synthesis - @username1
- [ ] Update wireframes - @username2
- [ ] Test prototype - @username3
```

### 5. Protect Main Branch
Consider requiring pull request reviews for main branch to ensure quality.

---

## ❓ Common Questions

**Q: Where should code go?**  
A: In `/03-prototyping/src/` during development. Create a dedicated repo if it becomes a real product post-class.

**Q: Can we reorganize the structure?**  
A: Yes, but keep core folders (foundation, discovery, prototyping, delivery). Customize within those.

**Q: What if we pivot completely?**  
A: Keep the old work in an `/archive/` folder. Start fresh in current folders. Document the pivot in your changelog.

**Q: How detailed should interview notes be?**  
A: Capture key quotes, main insights, and your interpretation. You can always refer to recordings for full detail.

**Q: Should we track hours worked?**  
A: Optional, but helpful for contribution tracking. Create `resources/time-log.md` if desired.

---

## 🎯 Remember

> "A well-organized repo is a sign of a well-organized team.  
> Make it easy for your future self (and your teammates) to find things."

**Your repository is:**
- Your team's memory
- Your project's story
- Your learning artifact
- Your portfolio piece

**Treat it with care! 🚀**
