---
skill: share-research
description: Tag, file, and share research in repository
---

# Share Research

Tags research with OKRs, teams, and topics, then files it in the searchable repository. Optionally shares to Slack.

## When to Use

- After creating a report (`/create-report`)
- User wants to make research discoverable by other teams
- User says "share this" or "file this research"

## Workflow

1. **Verify research artifacts exist**:
   - Research plan
   - Findings summary
   - Report (at least one format)

2. **Ask for tags**:
   - **OKRs**: Which business objectives does this support? (e.g., "OKR-3: Improve retention")
   - **Teams**: Which teams should care? (e.g., "Forma, AutoCAD, Platform")
   - **Topics**: Product areas, user types, features (e.g., "churned users", "onboarding", "collaboration")

3. **Update repository index** at `memory/README.md`:
   - Add study to "Current Research Studies" table
   - Add to "Search & Discovery" sections (by OKR, team, topic, date)
   - Update statistics (total studies, completion rate, etc.)

4. **Generate shareable link/summary** for Slack:
   - Study name and date
   - Key findings (top 3)
   - Link to report file
   - Relevant teams tagged

5. **Ask**: "Should I post this summary to Slack?" (optional for MVP)

6. **Confirm**: "Research filed and searchable via `/search-repository`"

## Repository Index Format

The `memory/README.md` serves as the research repository index:

```markdown
# Research Repository

Last updated: [YYYY-MM-DD]

## Statistics
- **Total Studies**: X
- **Completed**: Y
- **In Progress**: Z

---

## Current Research Studies

| Project Name | Status | Methodology | Last Updated | Participants | OKRs | Teams | Topics |
|-------------|---------|-------------|--------------|-------------|------|-------|--------|
| churned-users-research | Completed | Interviews | 2026-01-22 | 8 | OKR-3 | Forma | Churn, Retention |
| forma-onboarding | Completed | Usability Testing | 2026-01-15 | 8 | OKR-1 | Forma | Onboarding, New Users |
| power-user-workflows | In Progress | Interviews | 2026-01-20 | 3/8 | OKR-2 | AutoCAD | Power Users, Workflows |

---

## Search & Discovery

### By OKR

**OKR-1 (Accelerate adoption)**:
- forma-onboarding

**OKR-2 (Increase engagement)**:
- power-user-workflows

**OKR-3 (Improve retention)**:
- churned-users-research

### By Team

**Forma**:
- churned-users-research
- forma-onboarding

**AutoCAD**:
- power-user-workflows

### By Topic

**Churned Users**:
- churned-users-research

**Onboarding**:
- forma-onboarding

**Power Users**:
- power-user-workflows

**Retention**:
- churned-users-research

### By Date

**2026-01**:
- churned-users-research (2026-01-22)
- power-user-workflows (2026-01-20 - in progress)
- forma-onboarding (2026-01-15)

---

## How to Use This Repository

**Find research by OKR**: Search "OKR-3" to find all retention-related research
**Find research by team**: Search "Forma" to find all Forma research
**Find research by topic**: Search "onboarding" to find all onboarding studies
**Find research by date**: Browse by month/year

**Commands**:
- `/search-repository [query]` - Search by keyword, OKR, team, or topic
- `/plan-research` - Start new research study
```

## Slack Sharing Format (Optional)

```markdown
# 📊 New Research: [Project Name]

**Date**: [YYYY-MM-DD]
**Study**: [Project name]
**Method**: [Interviews/Usability Testing/Survey]
**Participants**: N [personas]

## Key Findings

1. [Finding 1 with frequency and impact]
2. [Finding 2 with frequency and impact]
3. [Finding 3 with frequency and impact]

## Top Recommendations

- [Priority 1 recommendation]
- [Priority 2 recommendation]

**Full report**: [Link to file]
**Video evidence**: Contact [researcher]

**Tags**: #[OKR] #[Team] #[Topic]

cc: @[Team leads]
```

## Example Interaction

**User**: "Share the churned users research"

**Agent**: [Verifies artifacts exist]

**Agent**: "I'll help you file this research for organizational discovery.

**Tags needed**:
1. Which OKRs does this support? (e.g., 'OKR-3: Improve retention')
2. Which teams should see this? (e.g., 'Forma, Product, Design')
3. What topics? (e.g., 'churn, retention, onboarding')"

**User**: "OKR-3, Forma team, topics are churn and retention"

**Agent**:
```
Filing research in repository...

✅ Updated `memory/README.md`:
- Added to Current Research Studies table
- Indexed under OKR-3 (Improve retention)
- Indexed under Team: Forma
- Indexed under Topics: Churn, Retention
- Indexed by date: 2026-01-22

Research is now searchable:
- `/search-repository churn`
- `/search-repository OKR-3`
- `/search-repository Forma`

Would you like me to post a summary to Slack?
```

**User**: "Yes"

**Agent**: [Generates Slack message with key findings and link]

## Quality Checks

- ✅ **Tagged appropriately**: OKRs, teams, topics all relevant
- ✅ **Index updated**: All search paths added to README
- ✅ **Links work**: Report file path is correct
- ✅ **Anonymized**: Slack summary has no PII

## Related Skills

- `/create-report` - Create report before sharing
- `/search-repository` - Search filed research
- `/summarize-findings` - Create findings before reporting and sharing
