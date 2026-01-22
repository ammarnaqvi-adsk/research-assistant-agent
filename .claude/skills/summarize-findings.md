---
skill: summarize-findings
description: Synthesize findings from transcripts without hallucination
---

# Summarize Findings

Synthesizes pain points and opportunities from session transcripts using **anti-hallucination protocol** - extracting ONLY what's explicitly in the data, never inferring or creating findings.

## When to Use

- After completing research sessions (typically 5-8 for qualitative)
- User has session notes/transcripts ready for synthesis
- User requests "summarize findings" or "what did we learn?"

## CRITICAL: Anti-Hallucination Protocol

**Non-Negotiable Rules**:

1. **Extract ONLY from provided transcripts** - Never infer, assume, or create findings not explicitly stated
2. **Quote with evidence** - Every pain point must have participant quotes with IDs and timestamps
3. **Label confidence** - Mark frequency (X/N participants) and confidence level
4. **Flag insufficient data** - If data is insufficient, say so and explain what's missing
5. **No extrapolation** - Don't generalize beyond your sample (e.g., "5/8 users" not "most users")
6. **Mark assumptions** - If inferring context, label it clearly as interpretation

**If you can't find evidence in transcripts, DO NOT include the finding.**

## Workflow

1. **Read all session notes** from `memory/session-notes/[project-name]/`

2. **Read research plan** for context:
   - Research goals (what we were trying to learn)
   - Hypothesis (what we were validating)
   - Methodology and participants

3. **Extract pain points** from transcripts:
   - User problems, friction, blockers
   - Behaviors indicating struggle
   - Stated frustrations or complaints
   - Task failures or workarounds

4. **For each pain point, document**:
   - Clear description
   - Frequency (how many participants mentioned)
   - Severity (impact on user experience)
   - Supporting evidence (quotes with participant IDs and timestamps)
   - Affected product area

5. **Identify opportunities** for each pain point:
   - What could be improved?
   - Expected impact on UX
   - Priority (based on frequency + severity)

6. **Validate hypothesis** from research plan:
   - Supported (evidence confirms hypothesis)
   - Refuted (evidence contradicts hypothesis)
   - Partially supported (mixed evidence)
   - Insufficient data (can't determine)

7. **Generate structured findings** using template below

8. **Quality check** against anti-hallucination protocol

9. **Save** to `memory/findings/[project-name]-findings.md`

10. **Suggest next steps**: "Ready to create a report? Use `/create-report`"

## Findings Template

```markdown
# [Project Name] - Research Findings

**Date**: [YYYY-MM-DD]
**Researcher(s)**: [Names]
**Study Type**: [Interviews / Usability Testing / Survey]

---

## Executive Summary

[Top 3-5 findings in 5 concise bullets - what stakeholders need to know]

1. [Key finding 1 with impact]
2. [Key finding 2 with impact]
3. [Key finding 3 with impact]
4. [Key finding 4 with impact]
5. [Key finding 5 with impact]

---

## Hypothesis Validation

**Original Hypothesis**: [From research plan]

**Result**: ✅ Supported / ❌ Refuted / ⚠️ Partially Supported / ❓ Insufficient Data

**Evidence Summary**:
[1-2 paragraphs explaining whether evidence supports or refutes hypothesis, with participant counts and key quotes]

**Confidence Level**: High / Medium / Low
**Rationale**: [Why this confidence level - sample size, consistency of findings, etc.]

---

## Participant Overview

- **Total Participants**: [N]
- **Personas**: [Anonymized demographics - roles, experience levels]
- **Recruitment**: [How they were recruited, any recruitment bias to note]
- **Sessions**: [Date range, duration]

**Sample Limitations**:
- [Any biases or limitations in sample - e.g., "All participants were power users" or "Small sample size"]

---

## Top Pain Points

### Pain Point 1: [Clear, descriptive title]

**Description**:
[2-3 sentences describing the pain point clearly]

**Evidence**:
- "Direct quote from transcript showing this pain point" (P01, 12:34)
- "Another quote demonstrating the same issue" (P03, 08:15)
- "Third quote providing more context" (P05, 23:45)

**Frequency**: X/N participants mentioned this
**Severity**: High / Medium / Low
**Severity Rationale**: [Why this severity - e.g., "Blocks task completion" or "Causes minor annoyance"]

**Affected Product Area**: [Feature/workflow/screen]

**User Impact**:
[Specific impact on user - task failure, workarounds, abandonment, etc.]

**Opportunity**:
[What could be improved? Expected UX impact if addressed?]

**Priority**: High / Medium / Low
**Priority Rationale**: [Based on frequency + severity + business impact]

---

### Pain Point 2: [Title]

[Same structure as Pain Point 1]

---

[Repeat for each pain point - typically 3-7 major pain points from qualitative research]

---

## Theme Table

Quick reference of all themes:

| Pain Point | Frequency | Severity | Confidence | Product Opportunity |
|-----------|-----------|----------|------------|-------------------|
| [Pain point 1] | X/N | High | High | [Opportunity area] |
| [Pain point 2] | X/N | Medium | Medium | [Opportunity area] |
| [Pain point 3] | X/N | Low | High | [Opportunity area] |

---

## Recommendations

### Priority 1: [Recommendation title]
**Action**: [Specific, actionable recommendation for product/design team]
**Expected Impact**: [What will improve for users]
**Rationale**: [Why this is priority 1 - frequency, severity, business alignment]
**Supporting Evidence**: [Pain points that drive this recommendation]

### Priority 2: [Recommendation title]
[Same structure]

### Priority 3: [Recommendation title]
[Same structure]

---

## What to Validate Next

**Open Questions**:
- [Question 1 that wasn't fully answered by this research]
- [Question 2 that emerged during research]

**Suggested Follow-up Research**:
- [Type of research needed to answer open questions]
- [Methodology and participants for follow-up]

**Contradictions to Explore**:
- [Any conflicting evidence that needs deeper investigation]

---

## Appendix: Participant Details (Anonymized)

**P01**: [General role, experience, usage pattern - no PII]
**P02**: [Same]
**P03**: [Same]
[Continue for all participants]

---

**Note**: All quotes include participant IDs and timestamps for video clip creation. Contact [Researcher] for access to video recordings.
```

## Quality Checks

Before finalizing findings:

### Anti-Hallucination Validation
- ✅ **Every pain point has quotes**: No pain point without direct evidence
- ✅ **Quotes have participant IDs**: Format is "Quote" (PXX, MM:SS)
- ✅ **Frequency is accurate**: Count matches number of participants who mentioned it
- ✅ **No assumptions stated as facts**: Interpretations clearly labeled
- ✅ **Sample size noted**: Don't generalize beyond your sample
- ✅ **Confidence levels marked**: High/Medium/Low for each finding

### Research Quality
- ✅ **Mapped to research goals**: Findings answer the research questions from plan
- ✅ **Hypothesis addressed**: Clear statement on whether hypothesis was supported
- ✅ **Actionable recommendations**: Specific enough for teams to act on
- ✅ **Video evidence ready**: Timestamps allow stakeholders to watch clips
- ✅ **Limitations acknowledged**: Any biases or gaps in data noted

## Severity Levels

**High Severity**:
- Blocks task completion
- Causes user to abandon product
- Results in significant errors or data loss
- Affects core workflows

**Medium Severity**:
- Causes friction but task can be completed
- Requires workarounds
- Causes frustration or confusion
- Affects secondary workflows

**Low Severity**:
- Minor annoyance
- Doesn't block progress
- Cosmetic or preference issues
- Rarely encountered

## Confidence Levels

**High Confidence**:
- 5+ participants mentioned it
- Consistent across different personas
- Strong, specific evidence
- Aligns with other research

**Medium Confidence**:
- 3-4 participants mentioned it
- Some variation in how it manifests
- Clear evidence but limited
- May be persona-specific

**Low Confidence**:
- 1-2 participants mentioned it
- Conflicting evidence
- Vague or unclear evidence
- May be outlier or edge case

## Example Interactions

### Scenario 1: Sufficient Data, Clear Findings

**User**: "Summarize findings for churned users research"

**Agent**: [Reads 8 session transcripts + research plan]

**Agent**:
```
Analyzing 8 session transcripts for churned-users research...

Found 5 major pain points with strong evidence:

1. **Onboarding is too long and unclear** (7/8 participants)
   - High severity: Caused early frustration and disengagement
   - Strong evidence with quotes from P01, P02, P03, P04, P05, P06, P08

2. **Missing collaboration features** (6/8 participants)
   - High severity: Primary reason for switching to competitor
   - Evidence from P01, P02, P04, P05, P07, P08

3. **Performance issues with large files** (5/8 participants)
   - Medium severity: Caused workarounds and frustration
   - Evidence from P03, P04, P05, P06, P07

[Continue with remaining pain points...]

**Hypothesis**: "Users churn because onboarding takes too long"
**Result**: ✅ Supported - 7/8 participants cited onboarding as early friction point that set negative tone

Findings saved to `memory/findings/churned-users-findings.md`

Ready to create a report for stakeholders? Use `/create-report`
```

---

### Scenario 2: Insufficient Data

**User**: "Summarize findings for power user workflows"

**Agent**: [Reads 2 session transcripts]

**Agent**:
```
⚠️ Insufficient data for reliable synthesis

**Sessions completed**: 2/5 planned

**What I found so far**:
- 1 participant mentioned keyboard shortcut issues (P01)
- 1 participant mentioned export workflow friction (P02)

**Problem**: With only 2 participants, I cannot:
- Identify patterns (need 5+ to see recurring themes)
- Assess frequency with confidence
- Determine severity reliably
- Make evidence-backed recommendations

**Recommendation**: Complete 3 more sessions before synthesizing findings. Qualitative research needs 5-8 participants to identify patterns.

Would you like me to wait until more sessions are complete?
```

---

### Scenario 3: Hypothesis Refuted

**User**: "Summarize findings for forma-onboarding"

**Agent**: [Reads transcripts]

**Agent**:
```
**Hypothesis**: "Users struggle with onboarding because steps are unclear"

**Result**: ❌ Refuted

**Evidence**: 6/8 participants found steps clear but cited different issues:
- 5/8: "Onboarding is too long, even though steps are clear" (P01, P02, P03, P05, P07)
- 4/8: "Too much information upfront, overwhelming" (P02, P04, P06, P08)
- 0/8 mentioned unclear steps

**Key insight**: Problem isn't clarity, it's cognitive overload from too much at once.

**Recommendation**: Reduce onboarding length and introduce features progressively, not all upfront.

This is a great example of research preventing teams from solving the wrong problem!

Findings saved to `memory/findings/forma-onboarding-findings.md`
```

## Common Pitfalls to Avoid

### ❌ Hallucinating Findings
**Don't**: "Users are frustrated with the UI"
**Do**: "5/8 users mentioned frustration with specific UI elements: 'I don't understand this button' (P03, 12:34)"

### ❌ Vague Evidence
**Don't**: "Most users had issues"
**Do**: "6/8 participants experienced [specific issue]"

### ❌ Over-generalizing
**Don't**: "Users hate this feature"
**Do**: "6/8 participants in this study (power users) found this feature difficult"

### ❌ Missing Timestamps
**Don't**: "P03 said it was confusing"
**Do**: "P03 said 'I don't understand what this does' (08:45)"

### ❌ Unsupported Recommendations
**Don't**: "We should redesign the UI" (no evidence)
**Do**: "Simplify button labels - 6/8 users didn't understand 'Commit' vs 'Push'"

## Related Skills

- `/add-session-notes` - Add session transcripts before synthesis
- `/create-report` - Create stakeholder report from findings
- `/plan-research` - Research plan defines goals for synthesis to address
