
# Generate Script

Creates interview guides and usability test scripts from research plans, with **automatic leading question detection** to ensure unbiased research.

## When to Use

- User has a research plan and needs an interview script
- User requests "generate a script" or "create interview questions"
- After `/plan-research` is completed

## Workflow

1. **Read research plan** to understand:
   - Research goals (questions to answer)
   - Hypothesis (what we're validating)
   - Methodology (interviews vs usability testing)
   - Target participants (context for questions)

2. **Generate script structure** based on methodology:

### For Interviews:
```markdown
# [Project Name] Interview Script

## Introduction (5 minutes)
- Welcome and thank you
- Explain purpose of research
- **CRA reminder**: "Before we begin, please confirm you've signed the CRA agreement"
- **Recording consent**: "Is it okay if I record this session for analysis? You can say no."
- Set expectations (duration, no right/wrong answers)

## Warm-up Questions (5 minutes)
[2-3 rapport-building questions about their background, role, general experience]

## Core Questions (30-40 minutes)
[Questions mapped to each research goal, open-ended, behavioral]

**Goal 1: [Research goal from plan]**
- [Open-ended question]
- Follow-up probes:
  - "Can you tell me more about that?"
  - "What was that experience like for you?"
  - "Walk me through what happened."

[Repeat for each research goal...]

## Closing (5 minutes)
- "Is there anything else you'd like to share?"
- Thank participant
- Explain next steps (incentive, when findings will be shared)
```

### For Usability Testing:
```markdown
# [Project Name] Usability Test Script

## Introduction (5 minutes)
[Same as interviews - CRA, recording consent, expectations]

## Warm-up (5 minutes)
[Questions about their experience with similar tools/workflows]

## Task Scenarios (30-40 minutes)

**Task 1: [Task name]**
- **Scenario**: "[Realistic scenario that provides context]"
- **Starting point**: [Where they begin]
- **Success criteria**: [What completion looks like]
- **Observations to note**: [What to watch for]

**Think-aloud reminder**: "Please narrate what you're thinking and doing as you work through this."

[Repeat for each task...]

## Follow-up Questions (10 minutes)
- What was easy or difficult?
- What would you change?
- How does this compare to your current workflow?

## Closing (5 minutes)
[Same as interviews]
```

3. **CRITICAL: Scan for leading questions**

Run automatic detection for:
- ❌ **Suggests desired answer**: "Don't you think this is confusing?"
- ❌ **Loaded terms**: "love", "hate", "annoying", "frustrating" (before user says it)
- ❌ **Yes/no questions** that should be open-ended: "Is this easy to use?"
- ❌ **Multiple questions in one**: "How do you feel about this and what would you change?"
- ❌ **Assumes behavior**: "When you use this feature daily, what do you think?"

4. **Provide neutral alternatives** for any leading questions found:

Example corrections:
- ❌ "How much do you love this design?"
  ✅ "What are your thoughts on this design?"

- ❌ "This is hard to use, right?"
  ✅ "How would you describe your experience using this?"

- ❌ "Don't you think the onboarding is too long?"
  ✅ "What was your experience with the onboarding process?"

5. **Save** to `memory/research-scripts/[project-name]-script.md`

6. **Offer review**: "Would you like me to review any specific questions for bias using `/review-questions`?"

## Leading Question Detection Rules

### Always Flag:
1. **Suggests answer**: "Don't you think...", "Wouldn't you agree...", "Isn't it obvious..."
2. **Loaded adjectives before user mentions**: "confusing", "difficult", "annoying", "slow"
3. **Binary questions about experience**: "Is this easy?" → "How would you describe using this?"
4. **Assumes behavior**: "When you do X..." (if we don't know they do X)
5. **Multiple questions**: "What do you think and how would you change it?" → Split into two

### Better Alternatives:
- **Open-ended**: "What are your thoughts on..."
- **Behavioral**: "Walk me through how you..."
- **Neutral**: "How would you describe..."
- **Specific past behavior**: "Tell me about the last time you..."

## Quality Checks

Before finalizing the script:

- ✅ **Questions map to research goals**: Each research goal has corresponding questions
- ✅ **Open-ended questions**: Most questions start with "what", "how", "tell me about"
- ✅ **Behavioral focus**: Asks about past behavior, not opinions ("Tell me about the last time..." not "Would you...")
- ✅ **No leading questions**: Script has been scanned and cleaned
- ✅ **Logical flow**: Warm-up → Core → Closing
- ✅ **Includes compliance**: CRA reminder and recording consent in introduction
- ✅ **Appropriate length**: 45-60 minutes total for interviews, 30-60 for usability

## Example Leading Question Review

**Original Question**: "How annoying is it when the save button doesn't work?"

**Problems**:
- Assumes the button doesn't work
- Uses loaded term "annoying" before user mentions it
- Leading toward negative feedback

**Corrected**: "Tell me about your experience with saving your work."

**Follow-up probe (after user mentions an issue)**: "What was that experience like for you?"

## Compliance Reminders

Every script must include:

1. **CRA Agreement confirmation** in introduction:
   - "Before we begin, please confirm you've signed the CRA agreement"
   - Link: https://www.autodesk.com/company/contact-us/customer-research-agreement

2. **Recording consent** (explicit opt-in):
   - "Is it okay if I record this session for analysis? You can say no."
   - Document their response in session notes

3. **Anonymization reminder** in closing:
   - Explain how their data will be used
   - Confirm participant ID will be used (P01, P02), not real name

## Example Interaction

**User**: "Generate a script for my churned users research"

**Agent**: [Reads research plan at `memory/research-plans/churned-users-research-plan.md`]

**Agent**: "I've generated an interview script based on your research plan. I found and corrected 3 leading questions:

1. Changed 'How frustrating was the onboarding?' → 'Tell me about your experience with onboarding'
2. Changed 'Don't you think this is too complicated?' → 'How would you describe using this feature?'
3. Split 'What do you think and would you use this?' → Two separate questions

The script is saved at `memory/research-scripts/churned-users-script.md`.

Would you like me to:
1. Review any specific questions using `/review-questions`?
2. Create screener questions to recruit the right participants (`/create-screener`)?"

## Related Skills

- `/plan-research` - Create the research plan first
- `/review-questions` - Review existing questions for leading/biased language
- `/create-screener` - Generate screener questions for participant recruitment
- `/check-compliance` - Validate compliance requirements
