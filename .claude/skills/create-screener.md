---
skill: create-screener
description: Generate participant recruitment screeners
---

# Create Screener

Generates participant recruitment screeners to ensure you recruit the RIGHT users for qualitative research, not just any users.

## When to Use

- After creating a research plan with target participant criteria
- User needs to recruit participants for interviews or usability testing
- User wants to filter for specific user segments (churned, active, new, power users, etc.)

## Why This Matters

**Common Problem**: Teams don't use screeners → Get wrong participants → Low-quality insights → Bad decisions

**Examples**:
- Researching churn but interview active users
- Testing enterprise features with individual users
- Studying onboarding with power users who don't remember it

**Solution**: Screener questions filter for the RIGHT participants with qualifying and disqualifying criteria.

## Workflow

1. **Read research plan** to understand target participants:
   - Persona description
   - Usage patterns
   - Specific behaviors or characteristics
   - Sample size needed

2. **Generate screener structure**:

```markdown
# [Project Name] Participant Screener

## Target Participant Profile
**Persona**: [Detailed description from research plan]

**Key Characteristics**:
- [Job role/experience level]
- [Product usage patterns]
- [Specific behaviors we need]

## Sample Size
**Need**: [N] participants
**Rationale**: [Why this number - e.g., "5-8 for qualitative pattern identification"]

## Qualifying Criteria (Must-Haves)

These are REQUIRED for participation:

1. **[Criterion 1]** - [Why this matters]
   - Example: Job role is Product Manager, Designer, or Engineer
   - Why: Our product targets these roles

2. **[Criterion 2]** - [Why this matters]
   - Example: Used [product] in past 6 months
   - Why: Need recent experience to recall details

[Continue for all must-haves...]

## Disqualifying Criteria (Exclusions)

These AUTOMATICALLY disqualify participants:

1. **Wrong user segment**
   - Example: If researching churn, exclude currently active users

2. **Competitors**
   - Works for [list competitor companies]

3. **Research/UX professionals**
   - Job role is UX Researcher, Research Ops, User Researcher
   - Why: They know research techniques and may alter behavior

4. **Over-recruited**
   - Participated in user research in past 6 months
   - Why: Avoid professional research participants

5. **Internal users**
   - Works for Autodesk (unless internal research)
   - Why: Not representative of external users

## Screener Questions

### Question 1: [Job Role Filter]
**Question**: "Which of the following best describes your current job role?"

**Answer Options**:
- Product Manager ✅ (Qualifies)
- Designer ✅ (Qualifies)
- Engineer/Developer ✅ (Qualifies)
- UX Researcher ❌ (Disqualifies - internal bias)
- Marketing ❌ (Disqualifies - wrong persona)
- Other: _____ (Review manually)

**Logic**: Recruit only if ✅ selected

---

### Question 2: [Product Usage Filter]
**Question**: "When did you last use [Product Name]?"

**Answer Options**:
- Within the past week ✅ or ❌ (Depends on research goal)
- Within the past month ✅ or ❌
- 1-3 months ago ✅ or ❌
- More than 3 months ago ❌ (For active user research)
- Never used it ❌

**Logic**: [Specify which answers qualify based on research goals]

---

### Question 3: [Behavior/Experience Filter]
[Continue with specific behavior questions...]

---

### Question 4: [Disqualifier - Over-recruitment]
**Question**: "Have you participated in user research or usability testing in the past 6 months?"

**Answer Options**:
- Yes ❌ (Disqualifies)
- No ✅ (Qualifies)

**Logic**: Automatically disqualify if "Yes"

---

### Question 5: [Disqualifier - Competitor]
**Question**: "Do you currently work for any of these companies?"

**Answer Options**: [List competitor companies]
- [Competitor 1] ❌
- [Competitor 2] ❌
- None of the above ✅

**Logic**: Disqualify if any competitor selected

## Booking System Integration

**Format for**: Calendly / Microsoft Bookings / [Specify system]

**Screening Logic**:
```
IF (Q1 in [PM, Designer, Engineer])
AND (Q2 in [Past week, Past month])
AND (Q4 = No)
AND (Q5 = None)
THEN → Allow booking
ELSE → Show "Thank you, but you don't meet criteria for this study"
```

## Recruitment Tips

- **Incentives**: [Specify if applicable - gift cards, etc.]
- **Session length**: [From research plan - e.g., "60 minutes"]
- **Format**: Remote (Zoom/Teams) or In-person
- **Timeline**: [Recruitment window]

---

**Note**: All external participants must sign CRA agreement before session. Include CRA link in booking confirmation.
```

3. **Customize based on research type**:
   - **Churned users**: Filter for "Stopped using product in past 3 months but used for 6+ months before"
   - **New users**: Filter for "Started using in past 2 weeks"
   - **Power users**: Filter for "Use 3+ times per week for 6+ months"
   - **Enterprise users**: Filter for company size, role in purchasing decision

4. **Validate screening logic**:
   - Qualifying criteria aren't too broad (won't get specific enough users)
   - Qualifying criteria aren't too narrow (won't find enough participants)
   - Disqualifying criteria cover all edge cases

5. **Save** to `memory/screener-questions/[project-name]-screener.md`

6. **Provide recruitment guidance**:
   - Where to post (internal channels, recruitment services)
   - How many to recruit (usually 2x target to account for no-shows)
   - Timeline considerations

## Sample Screener Questions by Research Type

### Churned User Research
```
Q: "When did you last use [Product]?"
- Within past 2 weeks ❌ (Still active)
- 1-3 months ago ✅ (Recently churned)
- 3-6 months ago ✅ (Churned)
- More than 6 months ago ❌ (Too long ago, may not remember)
- Never used ❌

Q: "Before you stopped using [Product], how long had you been using it?"
- Less than 1 month ❌ (Never really adopted)
- 1-6 months ✅
- 6+ months ✅ (Ideal - was engaged, then churned)
```

### Power User Research
```
Q: "How often do you use [Product]?"
- Daily ✅
- 3-4 times per week ✅
- 1-2 times per week ❌
- Less than weekly ❌

Q: "Which features do you use regularly?" (Select all that apply)
- [Advanced feature 1] ✅ (Indicates power user)
- [Advanced feature 2] ✅
- [Basic feature only] ❌ (Not power user)
```

### New User Research (Onboarding)
```
Q: "When did you first start using [Product]?"
- Within past week ✅ (Ideal - very fresh)
- 1-2 weeks ago ✅
- 3-4 weeks ago ⚠️ (Borderline - may have forgotten details)
- More than 1 month ago ❌ (Not "new" anymore)
```

## Quality Checks

Before finalizing screener:

- ✅ **Criteria match research plan**: Target participants align with research goals
- ✅ **Specific enough**: Not just "users" but specific user segments
- ✅ **Not too narrow**: Can realistically find enough participants
- ✅ **Includes disqualifiers**: Competitors, over-recruited, wrong segments
- ✅ **Clear logic**: Obvious which answers qualify vs disqualify
- ✅ **Integrated with booking**: Can be configured in Calendly/Bookings/etc.

## Example Interaction

**User**: "Create a screener for churned users research"

**Agent**: [Reads research plan]

**Agent**: "I've created a screener for churned users research. Key filters:

**Qualifying** (must meet ALL):
- Used product 6+ months before churning (not trial users)
- Stopped using 1-3 months ago (recent enough to remember, churned enough to be valid)
- Job role: PM, Designer, or Engineer (your target personas)

**Disqualifying** (automatic exclusions):
- Currently active users (still using weekly)
- Never really adopted (used < 1 month)
- Competitors, researchers, over-recruited

**Screening logic**: 5 questions → ~2 minute screener

The screener is saved at `memory/screener-questions/churned-users-screener.md`.

**Recruitment tip**: Aim to recruit 10-12 qualified participants to account for no-shows, and get your target of 5-8 completed sessions.

Would you like me to:
1. Review your research script (`/review-questions`)?
2. Check compliance requirements (`/check-compliance`)?"

## Related Skills

- `/plan-research` - Define target participants before creating screener
- `/generate-script` - Create interview script after screener is ready
- `/check-compliance` - Validate CRA and consent requirements
