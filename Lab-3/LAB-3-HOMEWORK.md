# Lab 3 Homework Assignment

Assignment: Customer discovery interview execution  
Due Date: Friday, October 24, 2025 at 11:59 PM  
Submission Method: Git commit and tag  
Total Points: 15 points

## Assignment Overview

Your task is to conduct and document three to five high‑quality customer discovery interviews using the Mom Test framework and the Five Whys technique. This assignment builds directly on Lab 2 where you created your interview script and ICP. Now you will execute that plan, document what you learn, and assess whether your original problem statement still holds.

## Objectives

By completing this assignment you will:

1. Execute customer discovery interviews using proper techniques.
2. Document interviews systematically with structured logs.
3. Capture verbatim user insights that reveal genuine problems.
4. Review your problem statement based on early evidence.
5. Begin pattern identification across multiple data points.
6. Maintain research velocity to reach at least ten interviews by Week 5.

## Deliverables

### 1. Interview Logs (required)

* Location: `/01-discovery/interview-logs/`
* Files: `interview-001.md`, `interview-002.md`, `interview-003.md`, and optionally `interview-004.md` and `interview-005.md`.
* Each log must include:
  * Complete interview metadata (date, time, duration, location, method).
  * ICP verification section with screener responses.
  * Interviewee background and context.
  * A minimum of three verbatim quotes (exact words in quotation marks).
  * A detailed problem deep dive narrative (300–500 words).
  * Evidence of the Five Whys technique.
  * Exploration of current solutions and workarounds.
  * Key insights, surprises, and contradictions.
  * Next steps or follow‑up opportunities.

Interview logs must be completed within 24 hours of each interview and should be 800–1500 words. Use the interview log template provided.

### 2. Interview Tracker (required)

* Location: `/01-discovery/outreach/interview-tracker.md`
* Must include all scheduled interviews (completed and upcoming), contact method, date of outreach, interview date, status, team member responsible, and notes.
* Track progress toward at least ten interviews by Week 5.


### 3. Problem Statement Review (required)

* Location: `/01-discovery/working-notes/problem-statement-review.md`
* Include your original problem statement and key findings from interviews.
* Analyse which aspects were validated and which were challenged.
* Record surprising insights.
* Decide whether to keep, refine, or pivot your problem statement and provide reasoning and evidence.
* If you refine or pivot, provide a revised statement.
* Assess your confidence level and note open questions and next steps.

### 4. Updated README (required)

* Location: `/README.md`
* Update with current project status, interview progress (e.g., 3/10 completed), key learnings, problem statement status, and next steps.

## Submission Instructions

1. Ensure all deliverables are complete and in the correct folders.
2. Commit your changes with a descriptive message:

git add 01-discovery/interview-logs/
git add 01-discovery/outreach/
git add 01-discovery/working-notes/
git add README.md
git commit -m "[LAB-3] Completed interviews with documentation and problem statement review"
git push origin main

3. Create a submission tag:
git tag lab-3-submission
git push origin lab-3-submission

4. Verify that all files and the tag are visible in your repository.
5. Submit your GitHub URL and tag in the LMS along with the list of team members who conducted interviews and the status of your problem statement (kept, refined, or pivoted).

## Grading Rubric

**Interview Execution Quality (6 points)**

*6 points:* Four to five interviews completed and documented; strong Mom Test compliance; deep problem exploration; clear evidence of Five Whys; natural conversation flow; no pitching.

*4–5 points:* Three to four interviews completed; mostly Mom Test compliant; adequate problem exploration; some evidence of Five Whys; generally good questioning.

*2–3 points:* Two to three interviews or multiple Mom Test violations; surface‑level questioning; limited follow‑up.

*0–1 points:* Zero to one interviews or complete non‑compliance with interview principles.

**Documentation Quality (5 points)**

*4 points:* All templates used correctly and fully; rich verbatim quotes; clear narrative; insights and surprises documented; professional and organised.

*3 points:* Templates mostly used correctly; most sections complete; adequate quotes and context.

*1–2 points:* Templates misused or sections missing; limited quotes; poor organisation.

*0 points:* No documentation.

**Problem Statement Review Quality (4 points)**

*3 points:* Critical assessment; specific evidence; well‑reasoned decision; acknowledges validation and challenges; no confirmation bias; identifies open questions; adjusts interview strategy accordingly.

*2 points:* Basic reflection with some evidence and reasonable decision.

*1 point:* Superficial analysis; little evidence; weak justification; confirmation bias evident.

*0 points:* Not submitted or completely lacking critical thinking.


### Bonus Points

Up to two bonus points are available for completing five interviews and demonstrating exceptional interview technique, such as uncovering emotional pain points, generating excellent referrals, or delivering an outstanding problem statement review.

## Common Mistakes to Avoid

* Pitching your solution during the interview.
* Asking hypothetical or leading questions.
* Talking more than listening.
* Taking answers at face value without digging deeper.
* Waiting too long to document and paraphrasing instead of quoting.
* Ignoring surprises or contradictions.

## Timeline

*Friday, October 17:* Conduct one to two interviews after lab, document them immediately, and draft the problem statement review.
*Weekend (October 19–20):* Conduct one to two more interviews, document, update problem statement review, and schedule additional interviews for next week.
*Monday–Wednesday (October 21–23):* Finish any remaining interviews, finalise documentation, and complete pattern observations. Ensure the problem statement review is comprehensive.
*Thursday, October 24:* Perform a final quality check and submit the assignment by 11:59 PM.

Do not wait until the last minute. Interview scheduling takes time, and people cancel.

## Frequently Asked Questions

**Q:** Can we interview friends or roommates?

A: Yes, if they genuinely match your ICP. Do not interview people solely because they are convenient.

**Q:** What if someone only partially matches our ICP?

A: Interview them and note the differences. Clearly document how they differ from your ICP.

**Q:** Can we record interviews?

A: Yes, with permission. Always ask first. If they decline, take detailed notes instead.

**Q:** What if an interviewee starts suggesting solutions?

A: Politely redirect them back to discussing their problem: “That’s interesting—before we talk about solutions, I’d like to understand your experience more deeply.”

**Q:** How do we know if a quote is strong?

A: A good quote reveals emotion, pain, specific behaviour, or consequences. Generic statements like “it’s annoying sometimes” are weak.

**Q:** What if people keep cancelling?

A: Normal! Schedule twice as many interviews as you need and ask for referrals from each interviewee.

**Q:** Do all team members have to interview someone?

A: Yes. Each member should conduct at least one interview. Document who conducted each.

**Q:** What if we discover our problem isn’t real?

A: Great—this is the purpose of discovery. Document the evidence in your problem statement review and be ready to pivot if necessary.

**Q:** Can we update our interview script?

A: Yes. Save the new version as `interview‑script‑v2.md`, but maintain enough consistency to compare across interviews.

**Q:** How should we handle uncertainty in the problem statement review?

A: Be honest. It is better to say “medium confidence—we need more data” than to pretend certainty. Identify what information will increase your confidence.

**Q:** What if the team disagrees on keep/refine/pivot?

A: Document the disagreement with evidence from both perspectives. Use remaining interviews to resolve.

## Final Reminders

The goal is learning, not validation. Each interview should reveal something new or surprising. Document everything while it is fresh. Be honest about your problem statement. Share your insights within the team continuously. Stay curious, dig deep, and remember that a pivot in Week 3 saves pain in Week 12.

Good luck—you are about to learn something real about your users.
