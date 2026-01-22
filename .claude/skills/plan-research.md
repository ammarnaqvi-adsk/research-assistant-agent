
# Plan Research

Guides non-researchers through structured research planning and generates compliant Autodesk research plans.

## When to Use

- User says "I need to do research" or "I want to plan research"
- User needs to define research goals, hypothesis, and methodology
- User wants to create a formal research plan document

## Workflow

1. **Ask**: "Do you have an existing research plan?" (Yes/No)

2. **If No**, guide through planning conversation with these questions:
   - What decision will this research inform? (business goal)
   - What are your research goals? (top 3-5 questions you need answered)
   - What's your hypothesis? (what you believe and want to validate)
   - What methodology will you use? (interviews, usability tests, surveys, etc.)
   - Who are your target participants? (specific personas, not just "users")
   - What constraints do you have? (timeline, sample size, budget)

3. **If Yes**, ask for the file path and review it for:
   - Autodesk template compliance
   - Quality standards (see below)
   - Missing sections or gaps

4. **Generate research plan** using Autodesk template structure:
   - Project name and overview
   - Business context and decision to inform
   - Research goals (3-5 specific questions)
   - Hypothesis (testable statement)
   - Methodology and rationale
   - Target participants (detailed personas)
   - Sample size with rationale
   - Timeline and milestones
   - Success metrics

5. **Save** to `memory/research-plans/[project-name]-research-plan.md`
   - Use kebab-case for project name
   - Example: `churned-users-research-plan.md`

6. **Confirm** with user and allow refinements

7. **Automatically trigger** compliance check by suggesting: "Would you like me to run `/check-compliance` to validate your research meets Autodesk requirements?"

8. **Suggest next steps**: "Would you like me to generate an interview script (`/generate-script`) or screener questions (`/create-screener`)?"

## Quality Checks

Before finalizing the research plan, validate:

- ✅ **Research goals are clear and answerable**: Each goal should be specific, not vague
  - ❌ Bad: "Understand users"
  - ✅ Good: "Understand why users churned in the past 3 months"

- ✅ **Hypothesis is testable**: Should be a statement that can be supported or refuted
  - ❌ Bad: "Users might have problems"
  - ✅ Good: "Users churn because onboarding takes too long"

- ✅ **Methodology matches decision type**:
  - Interviews: Understand "why" (behaviors, motivations, pain points)
  - Usability testing: Validate "how" (task success, friction points)
  - Surveys: Validate "what" at scale (prevalence, preferences)

- ✅ **Participants are specific**: Not just "users" but detailed personas
  - ❌ Bad: "Users of our product"
  - ✅ Good: "Users who churned within past 3 months, previously active for 6+ months, used collaboration features"

- ✅ **Sample size is appropriate**:
  - Qualitative (interviews, usability): 5-8 participants (enough to identify patterns)
  - Quantitative (surveys, metrics): 30+ for statistical significance

## Template Reference

The research plan should follow this structure (see `docs/reference/Research plan template.pdf`):

```markdown
# [Project Name] Research Plan

## Overview
- **Project Name**: [Descriptive name]
- **Date**: [YYYY-MM-DD]
- **Researcher(s)**: [Names/roles]
- **Stakeholders**: [Teams/individuals]

## Business Context
**Decision to Inform**: [What business decision will this research support?]

## Research Goals
1. [Specific question 1]
2. [Specific question 2]
3. [Specific question 3]
...

## Hypothesis
[Testable statement about what you believe and want to validate]

## Methodology
**Approach**: [Interviews / Usability Testing / Survey / Mixed Methods]
**Rationale**: [Why this methodology is appropriate for the goals]

## Target Participants
**Persona**: [Detailed description]
- Job role and experience level
- Product usage patterns
- Specific behaviors or characteristics
- Any exclusion criteria

**Sample Size**: [Number] participants
**Rationale**: [Why this sample size is sufficient]

## Timeline
- **Planning**: [Dates]
- **Recruitment**: [Dates]
- **Research Sessions**: [Dates]
- **Analysis**: [Dates]
- **Report Delivery**: [Date]

## Success Metrics
- [How will we know this research was successful?]
- [What decisions will be made with these insights?]

## Compliance
- [ ] CRA agreement process defined
- [ ] Recording consent documented
- [ ] PII handling procedures in place
```

## Compliance Reminders

Always include these in the research plan:

- **CRA Agreement**: Required for all external participants (not Autodesk employees)
- **Recording Consent**: Explicit consent needed for audio/video recording
- **Privacy**: Use participant IDs (P01, P02), never real names in findings

## Example Interaction

**User**: "I need to do research on why users are churning"

**Agent**: "I'll help you plan this research. Do you already have a research plan, or should I guide you through creating one?"

**User**: "Guide me through it"

**Agent**: "Let's start with the business context. What decision will this research inform? For example, is this for product prioritization, feature development, retention strategy?"

[Continue conversation...]

**Agent**: [After gathering all information] "Here's your research plan. I've saved it to `memory/research-plans/churned-users-research-plan.md`.

Would you like me to:
1. Run `/check-compliance` to validate this meets Autodesk requirements?
2. Generate an interview script (`/generate-script`)?
3. Create screener questions for recruitment (`/create-screener`)?"

## Related Skills

- `/generate-script` - Create interview script from this plan
- `/create-screener` - Generate screener questions based on target participants
- `/check-compliance` - Validate compliance requirements (CRA, privacy, recording)
