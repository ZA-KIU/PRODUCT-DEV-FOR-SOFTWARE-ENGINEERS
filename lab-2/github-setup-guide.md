# GitHub Repository Setup Guide for Teams

**Course:** Product Development for Software Engineers  
**Instructor:** Zeshan Ahmad  
**Purpose:** This guide helps your team set up a well-organized GitHub repository for the entire semester.

---

## Table of Contents

1. [Creating Your Team Repository](#creating-your-team-repository)
2. [Repository Structure Overview](#repository-structure-overview)
3. [Initial Setup Checklist](#initial-setup-checklist)
4. [Folder Structure Details](#folder-structure-details)
5. [GitHub Best Practices](#github-best-practices)
6. [Milestone Tracking](#milestone-tracking)
7. [Common Issues & Solutions](#common-issues--solutions)

---

## Creating Your Team Repository

### Step 1: Create Organization or Use Personal Account

**Option A: GitHub Organization (Recommended)**
1. One team member creates a GitHub Organization
   - Go to https://github.com/organizations/plan
   - Choose "Free" plan
   - Organization name: `kiu-pd-2025-team-[number]`
   - Example: `kiu-pd-2025-team-03`

2. Invite all team members
   - Settings → People → Invite member
   - Give members "Write" access

**Option B: Personal Repository with Collaborators**
1. One team member creates repository in their account
2. Settings → Collaborators → Add people
3. Add all team members with "Write" access

### Step 2: Create Repository

1. Click "New repository"
2. **Repository name:** `product-capstone-2025`
3. **Description:** "[Your Problem Name] - KIU CS Product Development Capstone"
4. **Visibility:** 
   - Private (during development)
   - Will make public at end of semester
5. **Initialize with:**
   - ✅ README.md
   - ✅ .gitignore (choose: Node or Python depending on your stack)
   - ✅ MIT License (or your preferred open-source license)

6. Click "Create repository"

### Step 3: Clone Repository Locally

Each team member runs:
```bash
git clone https://github.com/[org-or-username]/product-capstone-2025.git
cd product-capstone-2025

Repository Structure Overview
Your repository should have this structure by the end of the semester:
product-capstone-2025/
├── README.md                          # Project overview, setup instructions
├── .gitignore                         # Git ignore file
├── LICENSE                            # Open source license
│
├── 00-foundation/                     # Week 1-2: Team & Problem
│   ├── team-contract.md
│   ├── all-problem-statements.md
│   ├── team-problem-statement.md
│   └── team-icp.md
│
├── 01-discovery/                      # Weeks 2-5: Customer Discovery
│   ├── interview-script-v1.md
│   ├── interview-script-v2.md (final)
│   ├── interview-logs/
│   │   ├── interview-01.md
│   │   ├── interview-02.md
│   │   └── ... (10+ logs)
│   ├── synthesis/
│   │   ├── affinity-map.md
│   │   ├── patterns-analysis.md
│   │   └── final-problem-statement.md
│   └── outreach/
│       ├── outreach-messages.md
│       └── interview-scheduling-tracker.md
│
├── 02-design/                         # Weeks 3-8: Design & Prototyping
│   ├── design-sprint/
│   │   ├── brainstorm-notes.md
│   │   ├── sketches/
│   │   └── design-decisions.md
│   ├── prototypes/
│   │   ├── low-fidelity/
│   │   │   ├── wireframes/
│   │   │   └── prototype-v1.md
│   │   └── high-fidelity/
│   │       └── figma-link.md
│   └── user-testing/
│       ├── test-plan.md
│       ├── test-session-logs/
│       └── usability-findings.md
│
├── 03-build/                          # Weeks 6-12: MVP Development
│   ├── architecture/
│   │   ├── system-design.md
│   │   ├── tech-stack.md
│   │   ├── architecture-diagram.png
│   │   └── risk-spikes.md
│   ├── src/                           # Source code
│   │   ├── frontend/
│   │   ├── backend/
│   │   └── ... (your code structure)
│   ├── analytics/
│   │   ├── event-schema.md
│   │   ├── dashboard-link.md
│   │   └── instrumentation-plan.md
│   ├── reliability/
│   │   ├── slo-sheet.md
│   │   ├── error-budget.md
│   │   └── incident-logs/
│   └── privacy-security/
│       ├── privacy-notice.md
│       ├── consent-form.md
│       ├── data-handling-plan.md
│       └── security-tabletop.md
│
├── 04-gtm/                            # Weeks 9-13: Go-to-Market
│   ├── experiments/
│   │   ├── pricing-test.md
│   │   ├── packaging-test.md
│   │   └── experiment-results.md
│   ├── financials/
│   │   ├── unit-economics.md
│   │   ├── ltv-cac-analysis.md
│   │   └── 12-month-model.xlsx
│   ├── traction/
│   │   ├── design-partner-mous/
│   │   ├── waitlist-metrics.md
│   │   └── usage-growth.md
│   └── marketing/
│       ├── landing-page-link.md
│       ├── outbound-test.md
│       └── content-strategy.md
│
├── 05-fundraising/                    # Weeks 10-14: Investor Materials
│   ├── pitch-deck.pdf
│   ├── one-pager.pdf
│   ├── investor-update.md
│   ├── data-room/
│   │   ├── index.md
│   │   ├── metrics-dashboard-link.md
│   │   ├── financial-model.xlsx
│   │   └── legal-docs/
│   └── valuation/
│       ├── valuation-method.md
│       └── comps-analysis.md
│
├── 06-strategy/                       # Weeks 12-14: Strategy & Roadmap
│   ├── product-roadmap.md
│   ├── prioritization-framework.md
│   ├── portfolio-management.md
│   └── risk-mitigation.md
│
├── 07-team/                           # Weeks 13-14: Team Management
│   ├── team-dynamics.md
│   ├── conflict-resolution-log.md
│   ├── contribution-logs/
│   │   ├── midterm-peer-assessment.md
│   │   └── final-peer-assessment.md
│   └── retrospectives/
│       ├── week-08-retro.md
│       └── week-14-retro.md
│
├── 08-legal/                          # Week 13: Legal & IP
│   ├── legal-structure.md
│   ├── ip-strategy.md
│   └── open-source-licensing.md
│
├── 09-final/                          # Week 15: Final Deliverables
│   ├── demo-video.md (link)
│   ├── demo-script.md
│   ├── case-study.md
│   ├── venture-packet.pdf
│   └── portfolio-package/
│       ├── README.md
│       ├── setup-instructions.md
│       └── evaluation-guide.md
│
├── docs/                              # General Documentation
│   ├── setup.md
│   ├── contributing.md
│   ├── deployment.md
│   └── api-docs/
│
├── tests/                             # Test files
│   ├── unit/
│   ├── integration/
│   └── e2e/
│
└── milestones/                        # Milestone Tracking
    ├── week-02-milestone.md
    ├── week-05-milestone.md
    ├── week-09-milestone.md
    ├── week-12-milestone.md
    └── week-15-milestone.md

Initial Setup Checklist
Complete these steps in Lab 2 (Week 2):
Before Lab Ends:

 Repository created with all team members as collaborators
 Basic README.md created (see template below)
 Folder structure created:

 00-foundation/
 01-discovery/
 milestones/


 .gitignore configured for your tech stack
 All team members can clone and push to repo
 Team contract committed: 00-foundation/team-contract.md
 Problem statement committed: 00-foundation/team-problem-statement.md
 ICP committed: 00-foundation/team-icp.md
 Interview script v1 committed: 01-discovery/interview-script-v1.md

By End of Week 2:

 README.md updated with:

 Team members listed
 Problem description
 Tech stack (preliminary)
 Setup instructions (will expand later)


 Milestone template created: milestones/week-02-milestone.md
 GitHub Issues enabled and first issues created
 GitHub Projects board created (optional but recommended)


Folder Structure Details
00-foundation/ (Weeks 1-2)
Purpose: Team formation and problem selection
Created: Week 1-2
Updated: Rarely after Week 2
Files:

team-contract.md - Roles, decisions, communication, conflict resolution
all-problem-statements.md - All team members' 3 problems each
team-problem-statement.md - Chosen problem with 4 Filters scores
team-icp.md - Detailed Ideal Customer Profile


01-discovery/ (Weeks 2-5)
Purpose: Customer discovery through interviews
Created: Week 2-5
Most Active: Weeks 3-5
Structure:
01-discovery/
├── interview-script-v1.md              # Draft script from Lab 2
├── interview-script-v2.md              # Final refined script
├── interview-logs/                     # One file per interview
│   ├── interview-01.md
│   ├── interview-02.md
│   └── ... (minimum 10 logs)
├── synthesis/                          # Week 5 synthesis work
│   ├── affinity-map.md                 # Notes from affinity mapping
│   ├── patterns-analysis.md            # Top 3-5 patterns identified
│   └── final-problem-statement.md      # Evidence-based final statement
└── outreach/
    ├── outreach-messages.md            # Templates for recruiting
    └── interview-scheduling-tracker.md # Track who, when, status
Key Files:
interview-logs/interview-[number].md:

Use provided template
One file per interview
Must have 3+ verbatim quotes
Complete within 24 hours of interview

synthesis/final-problem-statement.md:

Evidence-based problem statement
Cites 8+ interviews
Includes root cause analysis
Due: End of Week 5


02-design/ (Weeks 3-8)
Purpose: Design thinking, prototyping, user testing
Created: Week 3-8
Most Active: Weeks 6-8
Structure:
02-design/
├── design-sprint/
│   ├── brainstorm-notes.md          # Ideation session notes
│   ├── sketches/                    # Images of paper sketches
│   │   ├── concept-1.jpg
│   │   ├── concept-2.jpg
│   │   └── ...
│   └── design-decisions.md          # Why we chose concept X
├── prototypes/
│   ├── low-fidelity/
│   │   ├── wireframes/              # Paper or digital wireframes
│   │   └── prototype-v1.md          # Description, link, screenshots
│   └── high-fidelity/
│       ├── figma-link.md            # Link to Figma/design tool
│       └── prototype-v2.md          # Clickable prototype details
└── user-testing/
    ├── test-plan.md                 # Who, when, what tasks
    ├── test-session-logs/           # One file per session
    │   ├── session-01.md
    │   └── ...
    └── usability-findings.md        # Summary, patterns, priorities
Key Deliverables:

Low-fidelity prototype (paper or digital)
User testing with 5+ users
Usability findings document


03-build/ (Weeks 6-12)
Purpose: MVP development, analytics, reliability
Created: Week 6-12
Most Active: Weeks 8-12
Structure:
03-build/
├── architecture/
│   ├── system-design.md              # High-level architecture
│   ├── tech-stack.md                 # Technologies chosen & why
│   ├── architecture-diagram.png      # Visual diagram
│   ├── risk-spikes.md                # Technical risks identified
│   └── api-design.md                 # API endpoints, contracts
├── src/                              # Your source code
│   ├── README.md                     # Setup instructions
│   ├── frontend/
│   ├── backend/
│   ├── database/
│   └── ...
├── analytics/
│   ├── event-schema.md               # All events tracked
│   ├── dashboard-link.md             # Link to analytics dashboard
│   └── instrumentation-plan.md       # What, where, how we track
├── reliability/
│   ├── slo-sheet.md                  # Service Level Objectives
│   ├── error-budget.md               # Error budget tracking
│   └── incident-logs/
│       ├── incident-001.md
│       └── ...
└── privacy-security/
    ├── privacy-notice.md             # User-facing privacy notice
    ├── consent-form.md               # Research consent template
    ├── data-handling-plan.md         # How we handle user data
    └── security-tabletop.md          # Security review notes
