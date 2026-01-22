# Hackathon Test Plan: Research Assistant Agent

**Goal**: Validate that the agent can guide a non-researcher through the complete research lifecycle

**Duration**: 30-45 minutes for full test | 15-20 minutes for demo

**Team**: 4 people - assign roles below

---

## 👥 Team Roles

1. **Driver**: Interacts with the agent (plays non-researcher role)
2. **Observer 1**: Takes notes on what works well
3. **Observer 2**: Takes notes on pain points / issues
4. **Facilitator**: Keeps time, documents test results

---

## 🎯 Test Scenario

**Context**: You're a Product Manager who needs to understand why users are churning from Forma, but you've never conducted formal user research before.

**Your goal**: Use the agent to plan research, create materials, conduct interviews, and share findings.

---

## 🧪 Test Flow

### Phase 1: Research Planning (5 minutes)

**Command**: `/plan_research`

**Expected Agent Behavior**:
1. Asks: "Do you have a research plan?"
2. Guides through planning questions:
   - What decision will this inform?
   - What are your research goals?
   - What's your hypothesis?
   - What methodology?
   - Who are target participants?
3. Generates research plan using Autodesk template
4. Saves to `memory/research-plans/forma-churn-research-plan.md`

**Test Input**:
- "I need to understand why Forma users are churning"
- Decision: "Whether to prioritize retention features or acquisition"
- Goal: "Understand why users stop using Forma after onboarding"
- Hypothesis: "Users churn because onboarding is too complex"
- Methodology: "User interviews"
- Participants: "Users who stopped using Forma 1-6 months ago"

**Success Criteria**:
- ✅ Research plan created with all required sections
- ✅ Follows Autodesk template structure
- ✅ Hypothesis is clear and testable
- ✅ File saved to correct location

**Validation**:
- Read the generated file
- Check that it includes: Goals, Hypothesis, Methodology, Participants, Compliance checklist

---

### Phase 2: Script Generation & Leading Question Detection (5 minutes)

**Command**: `/generate_script`

**Expected Agent Behavior**:
1. Reads research plan
2. Generates interview script with:
   - Introduction & consent (including CRA mention)
   - Warm-up questions
   - Core questions (mapped to research goals)
   - Closing questions
3. **CRITICAL**: Scans for leading questions
4. Flags any biased language and suggests alternatives
5. Saves to `memory/research-scripts/forma-churn-script.md`

**Test Input**:
- Use the research plan from Phase 1
- Ask agent to include questions about onboarding experience and reasons for churning

**Success Criteria**:
- ✅ Script includes all required sections
- ✅ Questions are open-ended, not leading
- ✅ CRA and recording consent mentioned in intro
- ✅ Questions mapped to research goals
- ✅ File saved to correct location

**Validation**:
- Read the script
- Intentionally suggest a leading question and see if agent catches it:
  - **Test**: "Should I ask: 'Don't you think onboarding is too complicated?'"
  - **Expected**: Agent should flag this as leading and suggest: "What was your experience with onboarding?"

---

### Phase 3: Screener Questions (5 minutes)

**Command**: `/create_screener`

**Expected Agent Behavior**:
1. Reads research plan to understand target participants
2. Generates screener with:
   - Target participant profile
   - Qualifying criteria (must-haves)
   - Disqualifying criteria (exclusions)
   - Sample screener questions with filtering logic
3. Saves to `memory/screener-questions/forma-churn-screener.md`

**Test Input**:
- Target: "Forma users who churned 1-6 months ago"
- Need to filter out: Active users, never-users, competitors, recent research participants

**Success Criteria**:
- ✅ Screener filters for churned users (not active users)
- ✅ Includes time-based question (when last used Forma)
- ✅ Excludes recent research participants
- ✅ Excludes Autodesk employees and competitors
- ✅ Sample size rationale provided (5-8 for qualitative)

**Validation**:
- Read screener questions
- Verify that someone who used Forma yesterday would be DISQUALIFIED
- Verify that someone who stopped 3 months ago would be QUALIFIED

---

### Phase 4: Compliance Check (3 minutes)

**Command**: `/check_compliance`

**Expected Agent Behavior**:
1. Reviews research plan
2. Generates compliance checklist with:
   - CRA agreement process
   - Recording consent process
   - PII handling procedures
   - Data storage plan
   - Incentives
   - Accessibility
3. Flags any missing items
4. Provides links to CRA form
5. Saves to `memory/compliance/forma-churn-compliance.md`

**Success Criteria**:
- ✅ All 6 compliance areas covered
- ✅ CRA link provided
- ✅ Reminders about participant IDs (not real names)
- ✅ Clear checklist format
- ✅ File saved to correct location

**Validation**:
- Read compliance checklist
- Verify CRA link is correct: https://www.autodesk.com/company/contact-us/customer-research-agreement
- Check that PII anonymization is emphasized

---

### Phase 5: Session Notes Upload (Mock Data) (5 minutes)

**Preparation**: Create 3 mock session transcript files

**Command**: `/add_session_notes`

**Expected Agent Behavior**:
1. Prompts user to upload transcripts
2. Reminds to use participant IDs (P01, P02, P03)
3. Reminds to include timestamps for key quotes
4. Saves to `memory/session-notes/forma-churn/P01.md`, P02.md, P03.md

**Test Input - Mock Transcript P01**:
```
P01 (Architect at small firm, churned 2 months ago)

[05:23] "I was really excited about Forma when I first signed up."

[08:15] "But the onboarding was overwhelming. There were too many steps and I didn't know where to start."

[12:34] "I tried to create my first project, but I couldn't figure out how to import my site plan. I spent 30 minutes clicking around."

[15:42] "Eventually I just gave up and went back to AutoCAD. It's familiar, even if it's clunky."

[18:20] "I wish there was a simple guided tour that just showed me the 3-4 things I needed to do to get started."
```

**Success Criteria**:
- ✅ Agent reminds about using participant IDs
- ✅ Agent confirms timestamps are included
- ✅ Files saved to correct location

**Validation**:
- Check that files are in `memory/session-notes/forma-churn/` directory
- Verify participant ID format (P01, not real names)

---

### Phase 6: Findings Synthesis (10 minutes)

**Command**: `/summarize_findings`

**Expected Agent Behavior**:
1. Reads all session notes from `memory/session-notes/forma-churn/`
2. Reads research plan for context
3. **CRITICAL**: Extracts pain points ONLY from provided transcripts (no hallucination)
4. Generates structured findings with:
   - Executive summary
   - Hypothesis validation
   - Top pain points with evidence (quotes + timestamps)
   - Opportunity areas for each pain point
   - Recommendations
5. Saves to `memory/findings/forma-churn-findings.md`

**Expected Findings** (from mock transcripts):
- **Pain Point 1**: Onboarding is overwhelming (P01: "too many steps", "didn't know where to start")
- **Pain Point 2**: Unclear how to perform basic tasks like importing site plans (P01: "couldn't figure out")
- **Pain Point 3**: Lack of guided tour or getting-started help (P01: "wish there was a simple guided tour")
- **Opportunity**: Create a simplified onboarding flow with guided tour

**Success Criteria**:
- ✅ Pain points backed by exact quotes from transcripts
- ✅ Timestamps included for video clip references
- ✅ Frequency noted (e.g., "3/3 participants mentioned")
- ✅ Opportunity areas suggested for each pain point
- ✅ Hypothesis validation (supported/refuted)
- ✅ NO hallucinated findings (only from transcripts)

**Anti-Hallucination Test**:
- Verify agent does NOT invent pain points not mentioned in transcripts
- Check that all quotes are real quotes from the mock transcripts

**Validation**:
- Read findings document
- Cross-reference quotes with original transcripts
- Check that P01 timestamp 12:34 quote is included

---

### Phase 7: Report Creation (5 minutes)

**Command**: `/create_report`

**Expected Agent Behavior**:
1. Asks: "Who is the audience?" (executives/stakeholders/team)
2. Asks: "What format?" (one-pager/slide deck/detailed)
3. Reads findings summary
4. Generates report in requested format
5. Saves to `memory/reports/forma-churn-report.md`

**Test Input**:
- Audience: "Executives"
- Format: "One-pager"

**Success Criteria**:
- ✅ Executive-friendly format (concise, visual, actionable)
- ✅ Top 3 pain points highlighted
- ✅ Quotes included for evidence
- ✅ Recommendations prioritized
- ✅ Next steps clear

**Validation**:
- Report should fit on one page (when formatted)
- Should include key quotes with participant IDs
- Should have clear recommendations

---

### Phase 8: Repository Management & Sharing (5 minutes)

**Command**: `/share_research`

**Expected Agent Behavior**:
1. Asks user to tag research:
   - OKRs: Which objectives does this support?
   - Teams: Which teams should care?
   - Topics: Product areas, user types, features
2. Updates `memory/README.md` with:
   - Study added to "Current Research Studies" table
   - Tags added to search sections (by OKR, team, topic)
   - Statistics updated
3. Prompts: "Should I share to Slack?" (optional)

**Test Input**:
- OKRs: "OKR-3: Improve retention by 20%"
- Teams: "Forma Product Team, Forma Design Team"
- Topics: "Churn, Onboarding, User Experience"

**Success Criteria**:
- ✅ Research added to repository index
- ✅ Searchable by OKR ("OKR-3")
- ✅ Searchable by team ("Forma")
- ✅ Searchable by topic ("Churn")
- ✅ Statistics updated (Total Studies: 1, Completed: 1)

**Validation**:
- Read `memory/README.md`
- Verify "forma-churn-research" appears in table
- Check tags are properly organized

---

### Phase 9: Search Repository (2 minutes)

**Command**: `/search_repository churn`

**Expected Agent Behavior**:
1. Searches memory/README.md for "churn"
2. Returns matching studies with links
3. Shows: Project name, methodology, date, findings summary link

**Success Criteria**:
- ✅ Finds "forma-churn-research" study
- ✅ Returns link to findings document
- ✅ Shows relevant metadata

**Validation**:
- Search returns expected result
- Links are correct

---

## 📊 Demo Flow (Condensed - 15 minutes)

If you need a shorter demo, follow this condensed flow:

1. **Research Planning** (3 min) - `/plan_research` → Show generated plan
2. **Script Generation** (3 min) - `/generate_script` → Demo leading question detection
3. **Screener Questions** (2 min) - `/create_screener` → Show filtering logic
4. **Compliance** (2 min) - `/check_compliance` → Highlight CRA requirement
5. **Findings Synthesis** (3 min) - `/summarize_findings` → Show pain points with evidence
6. **Report Creation** (2 min) - `/create_report` → Show one-pager format

**Skip**: Session notes upload (pre-populate), repository search (show index instead)

---

## ✅ Success Metrics for Hackathon

At the end of testing, verify:

- [ ] ✅ Agent generated all 7 artifact types
- [ ] ✅ All artifacts follow Autodesk templates
- [ ] ✅ Compliance checklist includes CRA, privacy, recording
- [ ] ✅ Leading questions were detected and flagged
- [ ] ✅ Screener filters for RIGHT participants (churned, not active)
- [ ] ✅ Findings backed by real quotes from transcripts (no hallucination)
- [ ] ✅ Research filed in repository with searchable tags
- [ ] ✅ Agent provided step-by-step guidance throughout

---

## 🐛 Issues to Track

Document any issues encountered:

| Issue | Severity | Phase | Description | Resolution |
|-------|----------|-------|-------------|------------|
| | 🔴 High / 🟡 Medium / 🟢 Low | [Phase #] | [What went wrong] | [How to fix] |

---

## 🎤 Demo Script

**Opening** (1 min):
> "We built a Research Assistant Agent for Autodesk that guides non-researchers through conducting high-quality user research. Let me show you how a Product Manager with no research background would use this to understand why Forma users are churning."

**Demo** (15-20 min):
[Follow condensed demo flow above]

**Closing** (2 min):
> "The agent generated a complete research plan, compliance-checked scripts, screener questions, and synthesized findings—all following Autodesk standards. It identified leading questions, ensured CRA compliance, and prevented recruiting the wrong participants. Most importantly, it made research accessible to non-researchers while maintaining quality."

**Key Points to Emphasize**:
1. ✨ **Non-researcher friendly** - Step-by-step guidance
2. 🔒 **Compliance-first** - CRA, privacy, recording consent enforced
3. 🎯 **Right participants** - Screener prevents wrong user recruitment
4. 🚫 **Anti-hallucination** - Only extracts from transcripts
5. 📹 **Video evidence** - Timestamps for stakeholder buy-in
6. 🔍 **Searchable repository** - Find past research by OKRs, teams, topics

---

## 📝 Post-Hackathon Notes

After testing, document:

**What worked well**:
- [Success 1]
- [Success 2]

**What needs improvement**:
- [Issue 1]
- [Issue 2]

**Features to add**:
- [Feature 1]
- [Feature 2]

**Next steps**:
- [ ] [Action 1]
- [ ] [Action 2]

---

_Test plan for Autodesk Research Assistant Agent hackathon demo_
