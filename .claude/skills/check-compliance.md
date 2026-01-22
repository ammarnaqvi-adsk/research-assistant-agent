---
skill: check-compliance
description: Validate CRA, recording consent, and privacy requirements
---

# Check Compliance

Validates that research meets **Autodesk's non-negotiable compliance requirements**: CRA agreements, recording consent, and privacy/anonymization standards.

## When to Use

- After creating a research plan (automatic suggestion)
- Before recruiting participants
- User asks "Is my research compliant?"
- Before conducting research sessions

## Autodesk Compliance Requirements (NON-NEGOTIABLE)

### 1. CRA Agreement ✅

**What it is**: Customer Research Agreement - like an NDA that protects Autodesk confidential information.

**Required for**: ALL external participants (not Autodesk employees)

**Enforcement**: Research Ops will flag studies without CRAs. Research may be invalidated if CRAs are missing.

**Process**:
- Participants sign BEFORE research session begins
- Simple form, low friction (digital signature)
- Include link in recruitment materials and booking confirmation
- Verify signature before starting session

**Link**: https://www.autodesk.com/company/contact-us/customer-research-agreement

**Script reminder**: "Before we begin, please confirm you've signed the CRA agreement."

---

### 2. Recording Consent ✅

**Requirement**: Explicit consent required for audio/video recording

**Process**:
- Ask participant at session start: "Is it okay if I record this session for analysis? You can say no."
- Document their response in session notes
- If they decline, take written notes only (no recording)
- Never record without explicit consent

**Script reminder**: Must be in interview script introduction

**Documentation**: Note in session file:
```
Recording Consent: [Yes/No]
Consent obtained at: [Timestamp]
```

---

### 3. Privacy & Anonymization ✅

**Requirement**: Protect participant personal information

**Rules**:
1. **Use participant IDs** (P01, P02, P03) in ALL:
   - Session notes
   - Findings summaries
   - Reports
   - Presentations
   - Shared documents

2. **Never include** in shared documents:
   - Real names
   - Email addresses
   - Phone numbers
   - Company names (unless aggregated or anonymized)
   - Any personally identifiable information (PII)

3. **Store PII separately** from research findings:
   - Contact info in recruitment tracker only
   - Research outputs use participant IDs only

4. **Data retention**: Follow Autodesk policies (typically 2-3 years)

5. **Sharing**: Only share anonymized findings with stakeholders

---

## Workflow

1. **Ask for research plan** (or script/screener if no plan):
   - File path to research plan
   - Or guide through compliance questions if no plan exists

2. **Review for compliance gaps** across all requirements:
   - CRA agreement process
   - Recording consent process
   - PII handling procedures
   - Data storage plan
   - Incentive compliance (if applicable)
   - Accessibility considerations

3. **Generate compliance checklist**:

```markdown
# [Project Name] Compliance Checklist

## CRA Agreement ✅ / ⚠️ / ❌
- [ ] CRA process defined (when participants sign)
- [ ] CRA link included in recruitment materials
- [ ] CRA link included in booking confirmation
- [ ] Script includes CRA verification step
- [ ] Plan for tracking CRA signatures

**Status**: [Compliant / Missing items]
**Action needed**: [Specific fixes required]

## Recording Consent ✅ / ⚠️ / ❌
- [ ] Script includes explicit recording consent question
- [ ] Consent is opt-in (can decline)
- [ ] Process for documenting consent in session notes
- [ ] Backup plan if participant declines (written notes)

**Status**: [Compliant / Missing items]
**Action needed**: [Specific fixes required]

## Privacy & Anonymization ✅ / ⚠️ / ❌
- [ ] Participant IDs defined (P01, P02, etc.)
- [ ] Process for anonymizing session notes
- [ ] No PII in findings/reports
- [ ] PII stored separately from research outputs
- [ ] Data retention policy understood

**Status**: [Compliant / Missing items]
**Action needed**: [Specific fixes required]

## Data Storage ✅ / ⚠️ / ❌
- [ ] Recording storage location secure (OneDrive, approved cloud)
- [ ] Access limited to research team
- [ ] Retention timeline defined

**Status**: [Compliant / Missing items]
**Action needed**: [Specific fixes required]

## Incentives (if applicable) ✅ / ⚠️ / ❌
- [ ] Incentive amount approved
- [ ] Incentive delivery method compliant
- [ ] Tax documentation if required

**Status**: [Compliant / Not applicable / Missing items]

## Accessibility ✅ / ⚠️ / ❌
- [ ] Accommodations process in place
- [ ] Remote session tools accessible
- [ ] Alternative formats available if needed

**Status**: [Compliant / Not applicable / Missing items]

---

## Overall Compliance Status

**PASS** ✅ - All requirements met, research can proceed
**CONDITIONAL** ⚠️ - Minor gaps, address before recruitment
**FAIL** ❌ - Critical gaps, must fix before proceeding

**Critical Issues** (must fix):
- [List any blocking issues]

**Recommended Improvements** (should fix):
- [List nice-to-haves]

**Next Steps**:
1. [Action item 1]
2. [Action item 2]
```

4. **Flag critical issues** that block research:
   - Missing CRA process
   - No recording consent in script
   - PII exposed in shared documents

5. **Provide templates and links**:
   - CRA link
   - Session notes template with participant IDs
   - Consent documentation format

6. **Save** to `memory/compliance/[project-name]-compliance.md`

7. **Offer to update** research plan/script with compliance fixes

## Compliance Levels

### ✅ PASS - Compliant
All requirements met:
- CRA process defined and verified
- Recording consent explicit and documented
- Participant anonymization in place
- Data storage secure

**Action**: Research can proceed

---

### ⚠️ CONDITIONAL - Minor Gaps
Most requirements met but:
- Missing some documentation
- Process needs clarification
- Small improvements needed

**Action**: Fix before recruiting participants

---

### ❌ FAIL - Critical Gaps
Blocking issues:
- No CRA process
- Recording without consent
- PII exposed in findings
- Insecure data storage

**Action**: MUST fix before proceeding. Research Ops will flag this.

## Example Interactions

### Scenario 1: Missing CRA Process

**User**: "Check compliance for my research plan"

**Agent**: [Reads research plan]

**Agent**:
```
⚠️ CONDITIONAL - Compliance gaps found

## Critical Issue: CRA Agreement
❌ CRA process not defined in research plan

**Why this matters**: All external participants must sign CRA before sessions. Research Ops will flag studies without CRAs.

**Action needed**:
1. Add CRA link to recruitment materials: https://www.autodesk.com/company/contact-us/customer-research-agreement
2. Include CRA link in booking confirmation
3. Add to script introduction: "Before we begin, please confirm you've signed the CRA agreement"

Would you like me to update your research plan and script with CRA requirements?
```

---

### Scenario 2: PII in Findings

**User**: "Check compliance for my findings document"

**Agent**: [Reads findings]

**Agent**:
```
❌ FAIL - Privacy violation found

## Critical Issue: PII Exposure
Found real names in findings document:
- Line 45: "John Smith from Autodesk said..."
- Line 67: "Sarah at Boeing mentioned..."

**Why this matters**: This violates Autodesk privacy requirements. Cannot share findings with PII.

**Action needed**: Replace with participant IDs:
- "John Smith" → "P01"
- "Sarah at Boeing" → "P03 (enterprise user)"

Would you like me to anonymize the findings document now?
```

---

### Scenario 3: Fully Compliant

**User**: "Check compliance for churned users research"

**Agent**: [Reads research plan, script, screener]

**Agent**:
```
✅ PASS - Fully compliant

All Autodesk requirements met:

✅ CRA Agreement:
- Process defined in research plan
- Link in recruitment materials
- Verification step in script

✅ Recording Consent:
- Explicit consent question in script
- Opt-in process
- Documentation process in place

✅ Privacy & Anonymization:
- Participant IDs (P01-P08) defined
- No PII in shared documents
- Secure storage plan

**Status**: Research can proceed

Saved compliance checklist to `memory/compliance/churned-users-compliance.md`
```

## Common Compliance Mistakes

### 1. Forgetting CRA
**Problem**: No CRA process defined
**Fix**: Add CRA link to recruitment, booking confirmation, and script verification

### 2. Implied Consent for Recording
**Problem**: "I'll be recording this session" (not asking)
**Fix**: "Is it okay if I record this session? You can say no."

### 3. Real Names in Findings
**Problem**: "Mike from Company X said..."
**Fix**: "P03 (enterprise user) said..."

### 4. Storing Recordings Insecurely
**Problem**: Recordings on personal laptop or unapproved cloud
**Fix**: OneDrive, approved Autodesk storage only

### 5. No Data Retention Plan
**Problem**: Keeping research data indefinitely
**Fix**: Define retention timeline (typically 2-3 years per Autodesk policy)

## Templates Provided

When compliance issues found, provide:

1. **CRA Script Language**:
```
"Before we begin, I need to confirm you've signed the Customer Research Agreement (CRA). This protects Autodesk confidential information we may discuss. Have you signed it?"

[If no]: "Let me send you the link now. It takes just a minute: [CRA link]"
```

2. **Recording Consent Language**:
```
"Is it okay if I record this session for analysis? The recording will only be used by the research team and stored securely. You can say no and we'll take written notes instead."

[Document response]: Recording Consent: [Yes/No] at [timestamp]
```

3. **Session Notes Template** (with anonymization):
```markdown
# Session Notes: P0X

**Date**: [YYYY-MM-DD]
**Researcher**: [Your name]
**Participant ID**: P0X (do not include real name)
**CRA Signed**: Yes
**Recording Consent**: Yes

## Observations
[Notes with participant ID only, no PII]
```

## Related Skills

- `/plan-research` - Create compliant research plan from the start
- `/generate-script` - Scripts automatically include CRA and consent reminders
- `/add-session-notes` - Session notes template includes anonymization
