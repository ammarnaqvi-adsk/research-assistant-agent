
# Search Repository

Searches the research repository for past studies by OKR, team, topic, date, or keyword.

## When to Use

- User wants to find past research on a topic
- User asks "Have we researched X before?"
- User wants to see all research for their team or OKR

## Workflow

1. **Parse search query**:
   - OKR (e.g., "OKR-3")
   - Team (e.g., "Forma")
   - Topic (e.g., "onboarding", "churn")
   - Date (e.g., "2026-01", "January 2026")
   - Keyword (any other term)

2. **Search repository index** (`memory/README.md`):
   - Check OKR section
   - Check Team section
   - Check Topic section
   - Check Date section
   - Full-text search if needed

3. **Return matching studies** with:
   - Study name
   - Status (completed/in progress)
   - Date
   - Key findings (1-2 sentences)
   - Link to findings/report

4. **If no matches**: Suggest related topics or offer to start new research

## Example Searches

### By OKR
**User**: `/search-repository OKR-3`

**Agent**:
```
Found 2 studies for OKR-3 (Improve retention):

1. **churned-users-research** (Completed, 2026-01-22)
   - 8 participants, interviews
   - Key finding: 7/8 cited onboarding complexity as primary churn factor
   - Report: memory/reports/churned-users-report.md

2. **user-activation-study** (In progress, 2026-01-15)
   - 5/8 participants completed
   - Findings: TBD

Would you like details on any of these studies?
```

### By Team
**User**: `/search-repository Forma`

**Agent**:
```
Found 3 studies for Forma team:

1. **churned-users-research** (Completed, 2026-01-22)
   - Interviews with 8 churned users
   - Top finding: Onboarding complexity drives churn

2. **forma-onboarding** (Completed, 2026-01-15)
   - Usability testing with 8 new users
   - Top finding: Cognitive overload, not clarity issues

3. **collaboration-features** (In progress, 2026-01-10)
   - 4/8 sessions complete

[Links to reports for each]
```

### By Topic
**User**: `/search-repository onboarding`

**Agent**:
```
Found 2 studies related to "onboarding":

1. **forma-onboarding** (Completed, 2026-01-15)
   - Hypothesis REFUTED: Steps are clear, but too much upfront
   - Recommendation: Progressive onboarding

2. **churned-users-research** (Completed, 2026-01-22)
   - 7/8 participants cited onboarding as early friction point
   - Recommendation: Simplify first-run experience

**Insight**: Both studies point to onboarding length/complexity as critical issue.

[Links to reports]
```

### By Keyword
**User**: `/search-repository collaboration`

**Agent**:
```
Found 1 study matching "collaboration":

1. **collaboration-features** (In progress, 2026-01-10)
   - Researching why users want collaboration features
   - 4/8 sessions complete
   - Preliminary finding: Primary reason for considering competitor switch

Would you like to see session notes or wait for final findings?
```

### No Matches
**User**: `/search-repository mobile app`

**Agent**:
```
No research found for "mobile app".

**Related topics you might be interested in**:
- onboarding (2 studies)
- churned users (1 study)
- power users (1 study)

Would you like to:
1. Start new research on mobile app? (`/plan-research`)
2. Search for a different topic?
```

## Advanced Search

Support combined queries:

**User**: `/search-repository Forma onboarding 2026-01`

**Agent**: Returns studies matching ALL criteria (Forma team + onboarding topic + January 2026)

## Quality Features

- **Contextual results**: Show why each result matched the query
- **Status indicators**: Clearly mark completed vs in-progress
- **Quick links**: Direct links to findings/reports
- **Suggestions**: If no exact match, suggest related topics
- **Insights**: Point out patterns across multiple studies

## Repository Statistics

When user asks for overview:

**User**: `/search-repository stats`

**Agent**:
```
# Research Repository Statistics

**Total Studies**: 12
- Completed: 9
- In Progress: 3

**By Methodology**:
- Interviews: 7
- Usability Testing: 4
- Surveys: 1

**By Team**:
- Forma: 5
- AutoCAD: 3
- Platform: 2
- Multiple teams: 2

**Most Researched Topics**:
1. Onboarding (3 studies)
2. Churn/Retention (2 studies)
3. Collaboration (2 studies)

**Recent Activity**:
- This month: 3 studies completed
- Last 30 days: 5 new studies started
```

## Related Skills

- `/share-research` - File new research in repository
- `/plan-research` - Start new research if nothing found
