---
skill: create-report
description: Generate stakeholder-friendly research reports
---

# Create Report

Generates stakeholder-friendly research reports in various formats (one-pager, slide deck, detailed report) from findings summaries.

## When to Use

- After synthesizing findings (`/summarize-findings`)
- User wants to share research with stakeholders
- User requests "create a report" or "make this shareable"

## Workflow

1. **Read findings summary** from `memory/findings/[project-name]-findings.md`

2. **Ask about audience and format**:
   - **Audience**: Executives / Stakeholders / Product Team / Designers
   - **Format**: One-pager / Slide deck / Detailed report

3. **Generate report** in requested format (see templates below)

4. **Include video evidence references**: Timestamps for key quotes so stakeholders can watch clips

5. **Save** to `memory/reports/[project-name]-report.md`

6. **Suggest next steps**: "Ready to share this? Use `/share-research` to file in repository and share to Slack"

## Report Formats

### Format 1: One-Pager (For Executives)

**When**: Executive summary for leadership or busy stakeholders

**Length**: 1 page (600-800 words)

**Structure**:

```markdown
# [Project Name] - Research Findings

**Date**: [YYYY-MM-DD] | **Researcher**: [Name] | **Participants**: N [personas]

---

## TL;DR

[2-3 sentences: What we learned and why it matters for the business]

---

## Top Findings

1. **[Finding 1 title]** (X/N users)
   - Impact: [Business/UX impact in 1 sentence]
   - Evidence: "[Key quote]" (P0X)

2. **[Finding 2 title]** (X/N users)
   - Impact: [Business/UX impact]
   - Evidence: "[Key quote]" (P0X)

3. **[Finding 3 title]** (X/N users)
   - Impact: [Business/UX impact]
   - Evidence: "[Key quote]" (P0X)

---

## Recommendations

**Priority 1**: [Actionable recommendation]
- Why: [Business rationale]
- Impact: [Expected outcome]

**Priority 2**: [Actionable recommendation]
- Why: [Business rationale]
- Impact: [Expected outcome]

**Priority 3**: [Actionable recommendation]
- Why: [Business rationale]
- Impact: [Expected outcome]

---

## Next Steps

- [Action item 1 with owner]
- [Action item 2 with owner]
- [Follow-up research needed, if any]

---

**Full findings**: See `memory/findings/[project-name]-findings.md`
**Video evidence**: Contact [researcher] for clips
```

---

### Format 2: Slide Deck (For Stakeholders)

**When**: Presenting findings in meetings or sharing broadly

**Length**: 8-12 slides

**Structure**:

```markdown
# [Project Name] Research Findings
## Slide Deck

---

### Slide 1: Title & Context

**[Project Name]**
Research Findings

**Date**: [YYYY-MM-DD]
**Researcher(s)**: [Names]
**Participants**: N [personas]
**Method**: [Interviews / Usability Testing / Survey]

---

### Slide 2: Executive Summary

**What we learned:**
- [Key finding 1]
- [Key finding 2]
- [Key finding 3]

**Why it matters:**
[Business impact in 1-2 sentences]

---

### Slide 3: Research Approach

**Research Goals:**
- [Goal 1]
- [Goal 2]
- [Goal 3]

**Participants:** N [personas] ([recruitment approach])
**Method:** [Methodology]
**Timeline:** [Date range]

---

### Slide 4: Hypothesis Validation

**We hypothesized:** [Original hypothesis]

**Result:** ✅ Supported / ❌ Refuted / ⚠️ Partially Supported

**Evidence:** [1-2 sentences with participant count]

---

### Slide 5: Finding 1 - [Title]

**Pain Point:** [Clear description]

**Frequency:** X/N participants

**Evidence:**
- "Quote from transcript" (P0X, MM:SS) 🎥
- "Another quote" (P0X, MM:SS) 🎥

**Impact:** [User and business impact]

**Opportunity:** [What we could improve]

---

### Slide 6: Finding 2 - [Title]

[Same structure as Slide 5]

---

### Slide 7: Finding 3 - [Title]

[Same structure as Slide 5]

---

[Continue for top 3-5 findings]

---

### Slide N-2: Key Themes

| Pain Point | Frequency | Severity | Opportunity |
|-----------|-----------|----------|-------------|
| [Finding 1] | X/N | High | [Opportunity] |
| [Finding 2] | X/N | High | [Opportunity] |
| [Finding 3] | X/N | Medium | [Opportunity] |

---

### Slide N-1: Recommendations

**Priority 1: [Recommendation]**
- Action: [Specific action]
- Expected impact: [Outcome]

**Priority 2: [Recommendation]**
- Action: [Specific action]
- Expected impact: [Outcome]

**Priority 3: [Recommendation]**
- Action: [Specific action]
- Expected impact: [Outcome]

---

### Slide N: Next Steps

- [ ] [Action item 1] - Owner: [Name]
- [ ] [Action item 2] - Owner: [Name]
- [ ] [Follow-up research, if any]

**Questions?** Contact [researcher]
**Video clips:** Available upon request

---

**Note**: 🎥 indicates video clip available for this quote
```

---

### Format 3: Detailed Report (For Product Team)

**When**: Product/design team needs full context and all evidence

**Length**: Full findings document (see `/summarize-findings` output)

**Structure**: Use the complete findings summary as the detailed report

```markdown
# [Project Name] - Detailed Research Report

[Include complete findings summary from `/summarize-findings`]

## Additional Context

### Methodology Details
[Expanded methodology notes]

### All Participant Quotes (By Theme)

**Theme 1: [Pain point]**
- "Quote 1" (P01, MM:SS)
- "Quote 2" (P03, MM:SS)
- "Quote 3" (P05, MM:SS)
[All quotes, not just top ones]

**Theme 2: [Pain point]**
[Continue...]

### Observations Beyond Quotes
[Researcher observations, non-verbal cues, context]

### Design Implications
[Specific design recommendations]

### Technical Considerations
[Technical constraints or opportunities]

---

**Full session notes**: See `memory/session-notes/[project-name]/`
```

## Quality Checks

Before finalizing report:

- ✅ **Audience-appropriate**: Language and detail match audience
- ✅ **Evidence included**: Quotes with participant IDs and video timestamps
- ✅ **Actionable**: Recommendations are specific, not vague
- ✅ **Anonymized**: No real names or PII
- ✅ **Prioritized**: Clear priority order for recommendations
- ✅ **Business-aligned**: Connects findings to business goals/OKRs

## Example Interactions

### Scenario 1: One-Pager for Executives

**User**: "Create a report for executives on churned users research"

**Agent**: [Reads findings summary]

**Agent**:
```
Creating one-pager for executive audience...

Key decisions:
- Focus on business impact (retention, churn prevention)
- Top 3 findings only (from 5 total)
- Prioritized recommendations with expected ROI
- Concise format (1 page, ~700 words)

One-pager saved to `memory/reports/churned-users-report.md`

**Preview**:

# Churned Users Research - Executive Summary

**TL;DR**: 7/8 churned users cited onboarding complexity as primary friction. Simplifying onboarding could reduce early churn by addressing the #1 barrier to adoption.

[Continue with top 3 findings and recommendations...]

Ready to share this? Use `/share-research` to file in repository and share to Slack.
```

---

### Scenario 2: Slide Deck for Stakeholders

**User**: "Create a slide deck for forma-onboarding findings"

**Agent**: [Reads findings summary]

**Agent**:
```
Creating slide deck (12 slides) for stakeholder presentation...

Structure:
- Slide 1: Title & Context
- Slide 2: Executive Summary
- Slide 3: Research Approach
- Slide 4: Hypothesis Validation (Refuted!)
- Slides 5-9: Top 5 findings with video evidence
- Slide 10: Key Themes Table
- Slide 11: Recommendations
- Slide 12: Next Steps

Each finding includes:
- Pain point description
- Frequency (X/8 participants)
- Direct quotes with video timestamps 🎥
- Opportunity area

Slide deck saved to `memory/reports/forma-onboarding-report.md`

**Tip**: Quotes marked with 🎥 have timestamps. Create video clips in Dovetail to play during presentation for maximum stakeholder impact.
```

---

### Scenario 3: Detailed Report for Product Team

**User**: "Create a detailed report for the product team"

**Agent**: [Reads findings summary]

**Agent**:
```
Creating detailed report with full context for product team...

Included:
- Complete findings summary (all 5 pain points)
- Full methodology and participant details
- All quotes grouped by theme (not just top quotes)
- Researcher observations and non-verbal cues
- Design implications and recommendations
- Technical considerations

Detailed report saved to `memory/reports/power-user-workflows-report.md`

This report includes everything the product and design teams need to make informed decisions.
```

## Video Evidence Best Practices

**Why video clips matter**: Stakeholders need to SEE users struggle or express pain points. Video clips drive buy-in and urgency.

**How to include video references**:
1. Mark key quotes with video emoji: 🎥
2. Include timestamps in format: (P0X, MM:SS)
3. Note where to access videos: "Contact [researcher] for Dovetail access"

**Example in report**:
```
**Finding 1: Onboarding is overwhelming**
- "I gave up after seeing 10 steps" (P03, 08:45) 🎥
- "This is too much information at once" (P05, 12:30) 🎥
```

**For presentation**: Create 15-30 second clips in Dovetail using these timestamps to show during slides.

## Customization by Audience

### Executives
- **Focus**: Business impact, ROI, strategic alignment
- **Length**: Very short (1 page)
- **Evidence**: Top quotes only
- **Recommendations**: High-level, prioritized

### Stakeholders (PM, Design, Eng leads)
- **Focus**: User problems and opportunities
- **Length**: Medium (slide deck)
- **Evidence**: Key quotes with video references
- **Recommendations**: Specific, actionable

### Product Team (ICs)
- **Focus**: Detailed evidence and design implications
- **Length**: Full report
- **Evidence**: All quotes and observations
- **Recommendations**: Detailed with design/technical considerations

## Related Skills

- `/summarize-findings` - Create findings summary before report
- `/share-research` - Share report and file in repository
- `/plan-research` - Research plan defines business goals for report framing
