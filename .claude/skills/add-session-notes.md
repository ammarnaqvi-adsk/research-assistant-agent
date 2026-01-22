
# Add Session Notes

Adds session transcripts or notes from research sessions to the repository, ensuring proper anonymization and organization.

## When to Use

- After conducting a research session (interview, usability test)
- User has transcripts to upload
- User wants to organize raw research data before synthesis

## Workflow

1. **Ask for session information**:
   - Project name (to know which study this belongs to)
   - Participant ID (P01, P02, etc.) - NOT real name
   - Transcript format (file upload, paste, or manual notes)
   - Session metadata (date, duration, researcher name)

2. **Verify anonymization**:
   - Scan transcript for PII (names, emails, company names)
   - Flag any PII found
   - Offer to anonymize automatically:
     - Replace real names with participant ID
     - Replace specific company names with generic terms (e.g., "Participant's company")
     - Remove email addresses, phone numbers

3. **Add session metadata**:

```markdown
# Session Notes: P0X

**Project**: [Project name]
**Date**: [YYYY-MM-DD]
**Duration**: [Minutes]
**Researcher**: [Your name]
**Participant ID**: P0X
**Session Type**: [Interview / Usability Test / Survey]

## Compliance
**CRA Signed**: [Yes/No]
**Recording Consent**: [Yes/No] - Obtained at [timestamp]

## Participant Context (Anonymized)
- **Persona**: [General description without PII]
- **Experience Level**: [Beginner/Intermediate/Advanced]
- **Usage Pattern**: [How they use the product - no company names]

---

## Transcript / Notes

[Transcript or notes with timestamps]

---

## Key Quotes (for video clips)

[Important quotes with timestamps for later video clip creation]

- "Quote about pain point..." (P0X, 12:34)
- "Quote about behavior..." (P0X, 23:45)

---

## Observer Notes

[Researcher observations, non-verbal cues, context]
```

4. **Organize by project**:
   - Save to `memory/session-notes/[project-name]/participant-0X.md`
   - Example: `memory/session-notes/churned-users/participant-01.md`

5. **Track session completion**:
   - Update session count for project
   - Confirm if more sessions planned
   - Suggest synthesis when sufficient sessions completed (5-8 typical)

6. **Suggest next steps**:
   - If this is final session: "Ready to synthesize findings? Use `/summarize-findings`"
   - If more sessions planned: "I'll wait for remaining sessions before synthesis"

## Anonymization Rules

### ❌ PII to Remove/Replace:

1. **Real names**:
   - ❌ "John Smith said..."
   - ✅ "P03 said..."

2. **Email addresses**:
   - ❌ "My email is john@company.com"
   - ✅ "My email is [redacted]"

3. **Company names** (when identifying):
   - ❌ "I work at Boeing"
   - ✅ "I work at an aerospace company" or "P03's company"

4. **Phone numbers, addresses**:
   - ❌ Any phone/address
   - ✅ [redacted]

5. **Colleague names**:
   - ❌ "My manager Sarah told me..."
   - ✅ "My manager told me..."

### ✅ What to Keep:

- General role descriptions (without names)
- Industry/domain (unless too identifying)
- Product usage patterns
- Behaviors and experiences
- Quotes (anonymized)

## Timestamp Format for Video Clips

For quotes you may want to turn into video clips later:

**Format**: `"Quote text..." (PXX, MM:SS)`

**Examples**:
- "The snapping feature is really confusing" (P03, 12:34)
- "I gave up after trying for 10 minutes" (P05, 08:15)

**Why this matters**: Stakeholders need video evidence. Timestamps let you create clips in Dovetail or other tools later.

## Session Types

### Interview Session Notes
```markdown
# Session Notes: P0X

[Metadata as above]

## Interview Transcript

**Researcher**: Tell me about your experience with [product].

**P0X** (00:30): I started using it about 6 months ago...

[Continue with Q&A format]

## Key Themes Observed
- [Theme 1]: Evidence from session
- [Theme 2]: Evidence from session

## Quotes for Video Clips
- "Quote about pain point" (P0X, 12:34)
```

### Usability Test Session Notes
```markdown
# Session Notes: P0X

[Metadata as above]

## Task Performance

### Task 1: [Task name]
- **Completion**: Success / Partial / Fail
- **Time**: [Minutes:Seconds]
- **Observations**: What we noticed during the task
- **User Comments**: What they said during think-aloud

### Task 2: [Task name]
[Same structure]

## Friction Points
- [Issue 1]: Description with timestamp
- [Issue 2]: Description with timestamp

## Success Moments
- [Success 1]: What went well

## Quotes for Video Clips
- "I don't understand what this button does" (P0X, 08:45)
```

## Quality Checks

Before saving session notes:

- ✅ **Anonymized**: No real names, emails, identifying PII
- ✅ **Participant ID used**: P0X throughout (not real name)
- ✅ **Timestamps included**: For key quotes and moments
- ✅ **Compliance documented**: CRA and recording consent noted
- ✅ **Context captured**: Enough detail for later synthesis
- ✅ **Organized correctly**: Saved in right project folder

## Example Interactions

### Scenario 1: Upload Transcript with PII

**User**: "Add session notes for churned users study" [uploads transcript]

**Agent**: [Scans transcript]

**Agent**:
```
⚠️ PII detected in transcript

Found:
- Real name "John Smith" (5 occurrences)
- Email "john@example.com" (1 occurrence)
- Company name "Boeing" (3 occurrences)

What participant ID should I use? (e.g., P01, P02)
```

**User**: "P01"

**Agent**:
```
Anonymizing transcript:
- "John Smith" → "P01"
- "john@example.com" → [redacted]
- "Boeing" → "P01's company (aerospace)"

Saved anonymized notes to `memory/session-notes/churned-users/participant-01.md`

Sessions completed: 1/8
Would you like to add another session, or wait until you have more sessions for synthesis?
```

---

### Scenario 2: Manual Notes Entry

**User**: "Add session notes for P03"

**Agent**: "I'll help you create session notes for P03.

Which project is this for?"

**User**: "forma-onboarding"

**Agent**: "Got it. Please provide:
1. Session date
2. Duration
3. CRA signed? (Yes/No)
4. Recording consent? (Yes/No)
5. Paste your notes or transcript"

[User provides info]

**Agent**:
```
Created session notes at `memory/session-notes/forma-onboarding/participant-03.md`

Sessions completed: 3/5

Two more sessions to go. I'll suggest synthesis once you have all 5 sessions completed.
```

---

### Scenario 3: Ready for Synthesis

**User**: "Add final session notes for P08"

**Agent**: [Adds notes]

**Agent**:
```
Session notes added: `memory/session-notes/churned-users/participant-08.md`

Sessions completed: 8/8 ✅

All planned sessions are complete. Ready to synthesize findings?

Use `/summarize-findings` to:
- Extract pain points from all 8 transcripts
- Identify opportunities
- Validate your hypothesis
- Create evidence-backed recommendations
```

## File Organization

Session notes are organized by project:

```
memory/session-notes/
├── churned-users/
│   ├── participant-01.md
│   ├── participant-02.md
│   └── participant-03.md
├── forma-onboarding/
│   ├── participant-01.md
│   └── participant-02.md
└── power-user-workflows/
    └── participant-01.md
```

## Compliance Reminder

Every session notes file must document:
- ✅ CRA signed before session
- ✅ Recording consent obtained (or declined)
- ✅ Participant ID used (no real names)

## Related Skills

- `/check-compliance` - Validate session notes meet privacy requirements
- `/summarize-findings` - Synthesize findings once sessions are complete
- `/plan-research` - Research plan defines how many sessions needed
