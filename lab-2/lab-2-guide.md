# Lab 2 Detailed Guide: Team Foundation & Discovery Planning

## Part 1: Team Contract (0:00 - 0:20)

### Why This Matters

Your team will work together for 15 weeks. Teams fail due to:
- Unclear roles and responsibilities
- Poor communication
- Unresolved conflicts
- Unequal contribution

A team contract prevents these issues.

### Instructions

1. Open `templates/team-contract-template.md`
2. Copy it to your repo: `/00-foundation/team-contract.md`
3. Work through each section as a team
4. All members must agree and "sign" (add name)

### Key Sections to Discuss

**1. Team Roles** (5 minutes)
Assign these three core roles:

- **Tech Lead:** Oversees technical decisions, architecture, code quality
- **Discovery Lead:** Manages user research, interviews, synthesis
- **Program Lead:** Tracks deadlines, coordinates meetings, manages repo/docs

**Tips:**
- Roles can rotate mid-semester if needed
- One person can't hold all roles
- Choose based on strengths and interest

**2. Decision-Making Process** (5 minutes)

How will you make decisions when team disagrees?

Options:
- Consensus (everyone agrees - can be slow)
- Majority vote (fastest, but some may feel unheard)
- Role-based authority (Tech Lead decides tech, etc.)
- Escalate to instructor (last resort)

**Choose ONE primary method.**

**3. Communication Norms** (3 minutes)

Agree on:
- Primary channel (WhatsApp, Telegram, Slack, etc.)
- Response time expectation (within 24 hours? 12 hours?)
- Meeting frequency (2x per week minimum recommended)
- Meeting format (in-person, hybrid, online)

**4. Contribution Tracking** (3 minutes)

How will you track who does what?

Options:
- GitHub commits and PR descriptions
- Shared task board (Trello, Notion, GitHub Projects)
- Weekly standup logs
- Time tracking (optional, can be overkill)

**5. Conflict Resolution Path** (4 minutes)

When conflicts arise:

**Step 1:** Direct conversation between people involved (24-48 hour timeline)  
**Step 2:** Mediation with third team member (48-hour timeline)  
**Step 3:** Escalate to instructor (if Steps 1-2 fail)

Write down your specific process.

### Deliverable

`/00-foundation/team-contract.md` committed to GitHub with all sections completed and all team members' names as signatures.

---

## Part 2: Problem Statement Presentations (0:20 - 0:40)

### Instructions

Each team member presents their 3 problem statements from individual work.

### Presentation Format (4 minutes per person)

For each of your 3 problems, share:
1. **Problem:** What's the problem in one sentence?
2. **Who experiences it:** Target user segment
3. **Why it matters:** Why is this painful/important?
4. **Evidence so far:** Anecdotal or observed evidence
5. **Feasibility:** Can we build something for this in 10 weeks?

### Documentation

One person acts as scribe. Create document: `/00-foundation/all-problem-statements.md`

Use this format:
```
# All Team Problem Statements

## [Member 1 Name]'s Problems

### Problem 1: [Title]
- **Problem:** [One sentence]
- **ICP:** [Who experiences it]
- **Why it matters:** [Brief explanation]
- **Evidence:** [What you've observed]
- **Feasibility:** [High/Medium/Low]

### Problem 2: [Title]
...

### Problem 3: [Title]
...

## [Member 2 Name]'s Problems

### Problem 1: [Title]
...

[Continue for all team members]
```

**Rules During Presentations**

✅ No interrupting during presentations  
✅ Ask clarifying questions after each person finishes  
✅ No judging yet - just listen and understand  
❌ Don't debate or argue about problems yet

### Deliverable

`/00-foundation/all-problem-statements.md` with all team members' problems documented.

---

## Part 3: Problem Selection & Decision (0:40 - 1:00)

### The Goal

Select ONE problem the team will pursue for the entire semester.

### Step 1: Narrow to Top Candidates (5 minutes)

Quick first pass:

Each person names their TOP problem from what they heard (can be their own or someone else's). Tally votes. Top 3-4 problems move to detailed evaluation.

### Step 2: Apply 4 Filters to Top Candidates (10 minutes)

Create this evaluation matrix on whiteboard or shared doc:

```
Problem | Hair on Fire | Access | Feasibility | Team Energy | TOTAL
Problem A | ?/5 | ?/5 | ?/5 | ?/5 | ?/20
Problem B | ?/5 | ?/5 | ?/5 | ?/5 | ?/20
Problem C | ?/5 | ?/5 | ?/5 | ?/5 | ?/20
```

**Filter 1: Hair on Fire Test (0-5)**

How painful is this problem? Will people actively seek solutions?

Scoring:

- 5 = Severe pain, people desperately need solution
- 3 = Annoying, people tolerate it but wish for better
- 1 = Mild inconvenience, nice-to-have

**Filter 2: Access Test (0-5)**

Can we find 10+ people who experience this at KIU? Do we have direct access to this user segment?

Scoring:

- 5 = Can easily find 20+ people this week
- 3 = Can find 10 people with moderate effort
- 1 = Very difficult to access this user segment

**Filter 3: Feasibility Test (0-5)**

Can we build a meaningful MVP in 8-10 weeks? Do we have the skills or can we learn them?

Scoring:

- 5 = Definitely buildable with our current skills
- 3 = Challenging but achievable, need to learn some new things
- 1 = Requires skills/resources we can't acquire in time

**Filter 4: Team Energy Test (0-5)**

How excited is the team about this problem? Will team stay motivated for 15 weeks?

Scoring:

- 5 = Everyone is genuinely excited
- 3 = Mix of excitement and neutrality
- 1 = Only one person cares, rest indifferent

### Step 3: Make the Decision (5 minutes)

If scores are clear (one problem 3+ points ahead): → That's your problem. Move forward. If two problems are tied: → Team discussion: Which problem do we want to live with for 15 weeks? → Vote if needed (simple majority). If no consensus: → Program Lead makes final call to keep moving → Document dissent if needed, but commit to decision.

CRITICAL: You MUST leave with ONE chosen problem. No "let's decide later."

### Step 4: Document Decision (remainder of time)

Create: `/00-foundation/team-problem-statement.md`

```
# Team Problem Statement

## The Problem

[2-3 sentence clear description of the problem]

## Ideal Customer Profile (Initial)

[Brief description of who experiences this - will be expanded in next section]

## Why We Chose This Problem

### Evaluation Scores
- Hair on Fire: [X/5] - [Brief reasoning]
- Access: [X/5] - [Brief reasoning]
- Feasibility: [X/5] - [Brief reasoning]
- Team Energy: [X/5] - [Brief reasoning]
- **Total: [X/20]**

### Additional Reasoning
[Why this problem beat the others]

## What We Need to Validate

Through interviews, we need to learn:
- [ ] Is this problem as painful as we think?
- [ ] What's the root cause?
- [ ] What do people currently do?
- [ ] What would make a solution valuable?
- [ ] How much would they value a solution?

## Team Agreement

**Decision Date:** [Today's date]  
**Agreed by:** [All team member names]

**Commitment:** We commit to pursuing this problem for the semester. If interviews reveal it's not a real problem, we'll pivot based on what we learn.
```

### Deliverable

`/00-foundation/team-problem-statement.md` committed to GitHub.

---

## Part 4: ICP Development (1:00 - 1:30)

### The Goal

Create a detailed Ideal Customer Profile for your chosen problem.

### Instructions

Open templates/icp-template.md. Copy to: `/00-foundation/team-icp.md`. Work through each section as a team.

### Key Sections to Complete

**1. Demographic Specifics (10 minutes)**

Be VERY specific:

- ❌ Bad: "Students"
- ✅ Good: "Third-year CS students taking 5+ courses"
- ❌ Bad: "Young professionals"
- ✅ Good: "Junior software engineers (0-2 years experience) working at startups"

Questions to answer:

- Student year / age range?
- Major / department / program?
- Course load (if relevant)?
- Living situation (commuter, dorm, off-campus)?
- Work status (employed, internship, full-time student)?
- Other relevant demographics?

Write these down with specificity.

**2. Behavioral Characteristics (8 minutes)**

How does this person interact with the problem?

Questions:

- How often do they experience this problem? (Daily? Weekly? Per semester?)
- What do they currently do when the problem occurs?
- What tools/methods do they currently use?
- How tech-savvy are they? (Important for solution design)
- How motivated are they to solve this? (High pain tolerance vs low?)

**3. Context & Constraints (7 minutes)**

When and where does the problem occur?

Questions:

- When: Time of day? Day of week? Time of semester? Triggered by what event?
- Where: Physical location? Digital space? Specific situation?
- What are they trying to accomplish? (Broader goal - JTBD preview)
- What constraints do they face? (Time? Money? Authority? Technical skills?)

**4. Primary Pain Point (3 minutes)**

Write 1-2 sentences that capture the specific pain THIS ICP experiences with YOUR problem.

Formula: "[ICP] experiences [specific problem] when [context], causing [consequence]."

Example: "Third-year CS students taking 5+ courses experience notification overload from LMS when checking course updates, causing them to miss critical deadlines."

**5. Where to Find Them (2 minutes)**

List 5-10 SPECIFIC places to find this ICP. Good examples: "Database Systems class (K-301), Tuesdays/Thursdays 2-4 PM". Bad examples: "Campus" or "Online".

### Quality Checks

Before finishing, verify:

- Specific enough: Can a stranger read this and know exactly who to find?
- Accessible: Can we find 10+ of these people at KIU in the next week?
- Homogeneous: Are we describing people with similar experiences?
- Connected to problem: Does this ICP actually experience our problem?

### Deliverable

`/00-foundation/team-icp.md` completed and committed to GitHub.

---

## Part 5: Interview Script Drafting (1:30 - 2:00)

### The Goal

Create a draft interview script you'll use for all 10+ interviews.

### Instructions

Open templates/interview-script-template.md. Copy to: `/01-discovery/interview-script-v1.md`. Adapt the template for YOUR specific problem and ICP.

### Script Structure (5 Sections)

Your script needs these 5 sections:

**Section 1: Opening & Rapport (3-5 min)**

- Introduce yourself and project
- Set expectations
- Get permission to record/take notes

**Section 2: Context & Background (5-7 min)**

- Verify they match ICP
- Understand their routine/context
- Warm-up questions

**Section 3: Problem Deep Dive (10-15 min) ⭐ MOST IMPORTANT**

- Opening: "Tell me about the last time you [experienced problem]..."
- Follow-ups using Five Whys
- Explore emotional impact
- Uncover consequences

**Section 4: Current Solutions (3-5 min)**

- What do they do now?
- What tools/methods?
- What works/doesn't work?

**Section 5: Closing (2-3 min)**

- Thank them
- Ask for referrals
- Future contact

### Requirements

Your draft must have:

- All 5 sections labeled
- At least 12-15 questions total
- At least 6-8 questions in Section 3 (Problem Deep Dive)
- All questions about PAST behavior (Mom Test compliant)
- At least 3 "Five Whys" style follow-ups
- Natural, conversational language

### Tips for Writing Good Questions

✅ DO:
- Ask about specific recent experiences: "Tell me about the LAST TIME..."
- Dig deeper: "Why did that happen?" "Tell me more about that"
- Ask about feelings: "How did that make you feel?"
- Ask about consequences: "What was the impact?"
- Ask about current solutions: "What do you do now when this happens?"

❌ DON'T:
- Ask hypotheticals: "Would you use..." "Do you think..."
- Ask opinions: "Do you like..." "What's your opinion on..."
- Ask leading questions: "Don't you find it frustrating when..."
- Pitch your solution during the interview

### Example Section 3 for Reference

```
## Section 3: Problem Deep Dive (10-15 min)

**Opening story question:**
"Tell me about the last time you [experienced the problem]. Walk me through exactly what happened."

[Wait for their story. Take notes. Then follow up:]

**Follow-up probes:**
- "You mentioned [specific thing they said]. Tell me more about that."
- "What made that [frustrating/difficult/time-consuming]?" (Why #1)
- "Why does that matter to you?" (Why #2)
- "What was the impact? Did it affect anything else?" (Consequences)
- "How did that make you feel?" (Emotional weight)
- "What did you do next?" (Behavior)
- "Has this happened before? Tell me about another time." (Pattern)

**Exploring frequency:**
"Think about this past week. How many times did this happen?"
"Walk me through each time - what were you trying to do?"

**Root cause:**
"Why do you think this problem exists?" (Why #3)
"What would need to change to fix this?"
```

### Deliverable

`/01-discovery/interview-script-v1.md` draft completed and committed to GitHub.

Note: This is a DRAFT. You'll refine it over the next week based on:

- Instructor feedback
- Practice interviews
- Peer review

Final version due next Friday.

---

## After Lab: Next Steps

**This Week (Before Next Friday):**

- Refine all deliverables:
  - Incorporate any instructor feedback
  - Review examples in `/labs/lab-2/examples/`
  - Finalize all documents

- Practice your interview script:
  - Each team member practices with a friend/roommate
  - Get comfortable with the flow
  - Identify any awkward questions

- Begin recruiting interviewees:
  - Use your ICP document to identify where to find people
  - Draft outreach messages
  - Schedule first 3 interviews

---

## Next Lab (Lab 3)

- Practice interviews with team
- Peer review of scripts
- Finalize and approve scripts
- Schedule remaining interviews

---

## Week 4

- Execute 10+ interviews
- Document in interview logs
- Prepare for Week 5 synthesis

---

## Common Questions

**Q: What if our team can't agree on a problem?**  
A: Use the 4-filter scoring system objectively. If still tied, vote. If no consensus, Program Lead makes final call. Document any dissenting opinions, but commit to the decision.

**Q: Can we change our problem later?**  
A: Only if interviews reveal it's not a real problem. This is called a "pivot" and is acceptable in Weeks 4-5. After Week 5, you're committed.

**Q: Our ICP is very broad - is that okay?**  
A: No. Broad ICP = unfocused interviews = weak insights. Go back and add specificity until a stranger could identify your ICP.

**Q: How specific should interview questions be?**  
A: Very specific. Don't ask "Do you use the LMS?" Ask "Tell me about the last time you logged into the LMS. What were you trying to do?"

**Q: Can we work on this outside of lab time?**  
A: Yes! We encourage it. Lab time is for core decisions and teamwork. Refinement can happen async.

---

## Need Help?

- During Lab: Raise your hand, instructor will come to your team
- After Lab: Office hours Tuesdays 2-4 PM
- Email: zeshan.ahmad@kiu.edu.ge
- Review Examples: Check `/labs/lab-2/examples/` folder
