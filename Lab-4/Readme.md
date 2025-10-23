# Lab 4 Templates - Discovery Synthesis

This folder contains all templates needed for Lab 4: Synthesis & Problem Validation

---

## 📁 Templates Included

### 1. `synthesis-readiness-checklist.md`
**Purpose:** Assess if your team is ready for synthesis or needs catch-up work  
**When to use:** First thing in Lab 4 (0:00-0:10)  
**Where to save:** `/01-discovery/synthesis/synthesis-readiness-checklist.md`

**What it includes:**
- Interview completion audit
- Quality metrics checklist
- Repository organization check
- Team readiness assessment

---

### 2. `affinity-map-template.md`
**Purpose:** Document your affinity mapping exercise  
**When to use:** During/after affinity mapping (0:30-1:00 in lab)  
**Where to save:** `/01-discovery/synthesis/affinity-map.md`

**What it includes:**
- Cluster documentation (themes/patterns identified)
- Sample insights from each cluster
- Outliers and unique findings
- Initial observations and surprises
- Relationship mapping between clusters

**Note:** Also take a photo of your physical board and save as `affinity-map-photo.jpg`

---

### 3. `patterns-analysis-template.md`
**Purpose:** Analyze and rank patterns by frequency, intensity, and root cause  
**When to use:** After affinity mapping (1:00-1:30 in lab)  
**Where to save:** `/01-discovery/synthesis/patterns-analysis.md`

**What it includes:**
- Frequency analysis table
- Pain intensity assessment (1-5 scale)
- Root cause analysis using Five Whys
- Final pattern ranking
- Top 3 validated patterns identification
- Product direction implications

---

### 4. `final-problem-statement-template.md`
**Purpose:** Write your evidence-based problem statement  
**When to use:** After pattern analysis (1:30-1:50 in lab)  
**Where to save:** `/01-discovery/synthesis/final-problem-statement.md`

**What it includes:**
- Problem statement component breakdown:
  - WHO (Specific segment/ICP)
  - WHAT (Specific problem)
  - WHEN/WHERE (Context)
  - WHY (Root cause)
  - IMPACT (Measurable consequences)
- Complete assembled problem statement
- Problem statement evolution (Week 1 hypothesis → Week 4 validation)
- Quality validation checklist
- Evidence summary with interview citations
- Team sign-off section
- Design direction implications

---

### 5. `emergency-interview-template.md`
**Purpose:** Condensed interview log for catch-up work  
**When to use:** ONLY if conducting emergency interviews during Lab 4 (0:00-0:30)  
**Where to save:** `/01-discovery/interview-logs/interview-[XX].md`

**What it includes:**
- Basic metadata
- Quick ICP verification
- The story (most important)
- 3 key quotes (required)
- Pain intensity rating
- One-sentence insight
- Current workaround

**⚠️ IMPORTANT:** This is a condensed version. Must be expanded to full log within 24 hours.

---

### 6. `week-04-milestone-template.md`
**Purpose:** Track Week 4 completion and transition to Week 5  
**When to use:** End of Week 4, after all deliverables complete  
**Where to save:** `/milestones/week-04-milestone.md`

**What it includes:**
- Completion status checklist
- Interview summary and statistics
- Key findings summary (top 3 patterns)
- Final problem statement
- Team performance assessment
- Individual contributions tracking
- Lessons learned
- Pivot or persevere decision
- Week 5 preparation plan
- Repository status
- Instructor feedback section

---

## 🚀 How to Use These Templates

### Step 1: Copy Templates to Your Repo

**Option A: Individual files**
```bash
# From your team repo root
mkdir -p 01-discovery/synthesis
mkdir -p milestones

# Copy each template and rename appropriately
cp [path-to-templates]/synthesis-readiness-checklist.md 01-discovery/synthesis/
cp [path-to-templates]/affinity-map-template.md 01-discovery/synthesis/affinity-map.md
cp [path-to-templates]/patterns-analysis-template.md 01-discovery/synthesis/patterns-analysis.md
cp [path-to-templates]/final-problem-statement-template.md 01-discovery/synthesis/final-problem-statement.md
cp [path-to-templates]/week-04-milestone-template.md milestones/week-04-milestone.md
```

**Option B: All at once**
```bash
# Download all templates
git clone https://github.com/ZA-KIU/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS.git temp
cp -r temp/Lab-4/templates/* ./
rm -rf temp
```

---

### Step 2: Fill Out in Order

**During Lab 4:**

1. **First 10 min:** Fill out `synthesis-readiness-checklist.md`
   - Audit your interview completion
   - Determine if ready for synthesis or need catch-up

2. **0:30-1:00:** Complete affinity mapping, then fill `affinity-map.md`
   - Document all clusters
   - Take photo of board
   - Note initial observations

3. **1:00-1:30:** Complete pattern analysis, then fill `patterns-analysis.md`
   - Count frequencies
   - Assess pain intensity
   - Complete Five Whys for top patterns
   - Rank patterns

4. **1:30-1:50:** Write problem statement in `final-problem-statement.md`
   - Assemble all components
   - Write complete statement
   - Validate with quality checklist
   - Get team sign-off

**After Lab 4 (by Friday):**

5. **End of Week 4:** Complete `week-04-milestone.md`
   - Summarize all Week 4 work
   - Document learnings
   - Plan for Week 5
   - Get instructor review

---

## 📋 Required vs. Optional

### REQUIRED Templates (Must complete):
- ✅ `synthesis-readiness-checklist.md` (if any doubt about readiness)
- ✅ `affinity-map.md` + photo
- ✅ `patterns-analysis.md`
- ✅ `final-problem-statement.md`
- ✅ `week-04-milestone.md`

### OPTIONAL Templates (Use if needed):
- `emergency-interview-template.md` (only if conducting catch-up interviews)

---

## 🎯 Quality Standards

Each template has built-in quality checks. Make sure:

### Affinity Map:
- [ ] 50-80+ sticky notes/insights extracted
- [ ] 5-8 distinct clusters identified
- [ ] Each cluster has clear label
- [ ] Photo documentation included

### Pattern Analysis:
- [ ] Frequency count for each pattern
- [ ] Pain intensity (1-5) with evidence
- [ ] Five Whys completed for top 3 patterns
- [ ] Patterns ranked by strength

### Problem Statement:
- [ ] All 5 components present (WHO, WHAT, WHEN/WHERE, WHY, IMPACT)
- [ ] Cites 8+ interviews with specific evidence
- [ ] Includes quantified impact (numbers)
- [ ] Passes all quality checklist items
- [ ] Team sign-off completed

### Milestone:
- [ ] All deliverables marked complete
- [ ] Individual contributions documented
- [ ] Lessons learned captured
- [ ] Week 5 plan included

---

## ❓ Frequently Asked Questions

**Q: Do I need to fill out every single field in each template?**  
A: Yes, for required templates. Empty brackets [] should be replaced with your actual content. If a section truly doesn't apply, write "N/A" and explain why.

**Q: Can I modify these templates?**  
A: Yes, but keep the core structure. You can add sections but don't remove required sections.

**Q: What if we don't have 10 interviews yet?**  
A: Use the first 30 minutes of lab for catch-up. Use `emergency-interview-template.md` if needed. You MUST have 10 interviews to proceed with synthesis.

**Q: How long should each document be?**  
A: 
- Synthesis Readiness: 2-3 pages
- Affinity Map: 3-5 pages
- Pattern Analysis: 5-8 pages
- Problem Statement: 6-10 pages
- Milestone: 4-6 pages

**Q: Do we need instructor approval before moving on?**  
A: Yes, instructor will checkpoint at 0:30, 1:00, 1:30, and 1:50 during lab. Final problem statement needs approval before Week 5.

---

## 🆘 Getting Help

**If you're stuck:**
1. Check the examples in `/Lab-4/examples/` folder
2. Review Lab 4 guide: `/Lab-4/README.md`
3. Ask instructor during lab checkpoints
4. Post in Discord `#lab-help` channel
5. Attend office hours: Tuesdays 2-4 PM

**Common issues:**
- **Can't identify patterns:** Review the affinity mapping section in Lab 4 guide
- **Patterns seem forced:** Let data speak, don't force themes
- **Problem statement too vague:** Add more specifics from interviews, use exact quotes
- **Low confidence:** May need more interviews or deeper Five Whys analysis

---

## 📚 Additional Resources

**Related Documents:**
- Lab 4 Guide: `/Lab-4/lab-4-guide.md`
- Lab 4 Examples: `/Lab-4/examples/`
- Week 2 Resources (Mom Test, JTBD): `/Lab-2/resources/`
- Synthesis Guide: `/Lab-2/resources/decision-frameworks.md` (Section 6)

**Readings:**
- "Behind Every Great Product" by Marty Cagan
- "What, Exactly, Is A Product Manager" by Martin Eriksson
- "The Mom Test" by Rob Fitzpatrick (review)

---

## ✅ Template Completion Checklist

Use this to track your progress:

**Week 4 Lab (During):**
- [ ] Synthesis readiness checklist completed
- [ ] Affinity map completed and documented
- [ ] Affinity map photo taken and saved
- [ ] Pattern analysis completed
- [ ] Problem statement drafted
- [ ] All documents committed to GitHub

**Week 4 Lab (After):**
- [ ] Problem statement finalized with instructor feedback
- [ ] Week 4 milestone document completed
- [ ] README.md updated with problem statement
- [ ] All synthesis documents reviewed and polished
- [ ] Ready for Week 5 design sprint

---

**Last Updated:** October 23, 2025  
**Course:** CS-PD-2025 Product Development for Software Engineers  
**Instructor:** Zeshan Ahmad  
**Lab:** Lab 4 - Synthesis & Problem Validation
