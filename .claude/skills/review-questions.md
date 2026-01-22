
# Review Questions

Reviews existing research questions (from scripts, surveys, or ad-hoc lists) and identifies leading or biased language that could compromise research quality.

## When to Use

- User has existing interview questions that need review
- User wants to validate their questions aren't leading
- After generating a script, user wants a second pass
- Before sending survey questions

## Workflow

1. **Ask for questions** to review:
   - File path to existing script/survey
   - Paste questions directly
   - Specific questions user is unsure about

2. **Analyze each question** for bias patterns:
   - Leading language (suggests desired answer)
   - Loaded terms (emotionally charged words)
   - Assumptions (presumes behavior/knowledge)
   - Multiple questions in one
   - Binary questions that should be open-ended
   - Confirmation bias patterns

3. **Flag problematic questions** with:
   - **Issue**: What's wrong with the question
   - **Why it matters**: How this could bias results
   - **Corrected version**: Neutral alternative

4. **Provide summary**:
   - Total questions reviewed
   - Number flagged
   - Confidence in remaining questions

5. **Offer to update** the original file if questions came from a script

## Leading Question Patterns to Detect

### 1. Suggests Desired Answer
- ❌ "Don't you think this feature is useful?"
- ❌ "Wouldn't you agree that this is better?"
- ❌ "Isn't it obvious that X is better than Y?"

**Fix**: Remove the leading framing
- ✅ "What are your thoughts on this feature?"
- ✅ "How would you compare X and Y?"

### 2. Loaded Terms (Before User Mentions)
- ❌ "How frustrating is the onboarding process?"
- ❌ "What do you hate about this feature?"
- ❌ "How slow is the performance?"

**Fix**: Use neutral language
- ✅ "Tell me about your experience with the onboarding process."
- ✅ "What are your thoughts on this feature?"
- ✅ "How would you describe the performance?"

### 3. Assumes Behavior/Knowledge
- ❌ "When you use this feature daily, what do you think?"
- ❌ "As a power user, how do you feel about this?"
- ❌ "What do you do when this error happens?" (assumes error happens)

**Fix**: Ask about actual behavior first
- ✅ "How often do you use this feature?"
- ✅ "Tell me about your experience level with this product."
- ✅ "Have you encountered any errors? [If yes] Tell me about that."

### 4. Multiple Questions in One
- ❌ "What do you think about this feature and would you use it?"
- ❌ "How easy was this to use and what would you change?"

**Fix**: Split into separate questions
- ✅ "What are your thoughts on this feature?" [Then later] "Would you use this in your workflow?"

### 5. Binary Questions (Should Be Open-Ended)
- ❌ "Is this easy to use?"
- ❌ "Did you like this design?"
- ❌ "Was the onboarding clear?"

**Fix**: Make open-ended
- ✅ "How would you describe your experience using this?"
- ✅ "What are your thoughts on this design?"
- ✅ "Tell me about going through the onboarding."

### 6. Confirmation Bias
- ❌ "This feature is confusing, right?"
- ❌ "Most users struggle with this. How about you?"
- ❌ "We think X is a problem. Do you agree?"

**Fix**: Don't reveal your hypothesis
- ✅ "Walk me through your experience with this feature."
- ✅ "What challenges, if any, have you encountered?"

## Review Output Format

For each flagged question, provide:

```markdown
### Question [N]: "[Original question]"

**Issue**: [What's problematic]
**Why it matters**: [How this biases results]
**Confidence**: High/Medium/Low that this is leading

**Corrected version**: "[Neutral alternative]"

---
```

## Example Review

**User**: "Review these questions:
1. How confusing is our onboarding?
2. What do you think about the new feature?
3. Don't you think the UI is cluttered?"

**Agent**:

```
I reviewed 3 questions and flagged 2 for leading/biased language:

---

### Question 1: "How confusing is our onboarding?"

**Issue**: Uses loaded term "confusing" before user mentions it
**Why it matters**: Assumes onboarding IS confusing and only asks for degree. User may feel pressured to agree.
**Confidence**: High - this is a leading question

**Corrected version**: "Tell me about your experience with the onboarding process."
**Follow-up (if they mention confusion)**: "What aspects were confusing?"

---

### Question 2: "What do you think about the new feature?"

**Issue**: None - this is a neutral, open-ended question ✅

---

### Question 3: "Don't you think the UI is cluttered?"

**Issue**: Directly suggests the desired answer (that UI is cluttered)
**Why it matters**: Creates pressure to agree. Highly leading question.
**Confidence**: High - this will bias results

**Corrected version**: "What are your impressions of the UI?"
**Follow-up (if they mention clutter)**: "Tell me more about that."

---

**Summary**:
- ✅ 1 question approved
- ⚠️ 2 questions flagged and corrected
- Overall quality: Good after corrections

Would you like me to update the original script with these corrections?
```

## Quality Standards

A question is **approved** when it:
- ✅ Is open-ended (not binary yes/no)
- ✅ Uses neutral language (no loaded terms)
- ✅ Doesn't suggest desired answer
- ✅ Asks about actual behavior (not hypotheticals)
- ✅ Focuses on one topic per question
- ✅ Doesn't assume knowledge or behavior

## Use Cases

### 1. Review Script Questions
**User**: `/review-questions memory/research-scripts/churned-users-script.md`

**Agent**: [Reads file, analyzes all questions, flags issues, offers to update file]

### 2. Review Pasted Questions
**User**: "Review these questions: [paste questions]"

**Agent**: [Analyzes questions, provides feedback inline]

### 3. Review Specific Question
**User**: "Is this question okay: 'How frustrating is the checkout process?'"

**Agent**:
```
⚠️ This question has leading language:

**Issue**: Uses "frustrating" before user mentions it
**Better**: "Tell me about your experience with the checkout process."

Then you can follow up based on what they say:
- If they mention frustration: "What was frustrating about it?"
- If they don't: "What went smoothly? What could be improved?"
```

## Related Skills

- `/generate-script` - Generate script with automatic leading question detection
- `/plan-research` - Create research plan before scripting
