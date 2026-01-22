# Product Requirements Document: AI Research Assistant Agent

## Executive Summary

An AI-powered research assistant agent that guides Autodesk teams through the complete user research lifecycle—from planning to sharing insights. The agent ensures compliance with industry standards and Autodesk best practices while reducing the time and effort required to conduct high-quality user research.

## Problem Statement

### Current Pain Points
- **Non-researchers lack guidance**: People without research backgrounds don't know how to create research plans, screener questions, or synthesize findings
- **Wrong participants recruited**: Teams don't use screener questions, so they get low-quality users who don't match target personas (e.g., recruiting active users when looking for churned users)
- **Research planning is time-consuming**: Creating comprehensive research plans with clear goals, hypotheses, and methodologies requires significant upfront effort
- **Script creation lacks consistency**: Research scripts vary in quality and don't always align with the research plan
- **Compliance is manual and error-prone**: Ensuring participants sign CRA agreements (like NDAs) and following ADSK best practices requires manual tracking - Research Ops will flag studies without proper compliance
- **Findings analysis is tedious**: Synthesizing transcripts and recordings into pain points, opportunities, and actionable insights takes considerable time
- **Knowledge sharing is fragmented**: Research insights aren't consistently shared across teams or filed in searchable repositories, leading to duplicated efforts
- **Stakeholder buy-in is difficult**: Without video clips and clear evidence, stakeholders don't believe research findings

### User Impact
- Non-researchers waste time or produce low-quality research without proper guidance
- Teams make decisions based on feedback from wrong users (quality issue)
- Researchers spend 40-60% of their time on administrative tasks rather than actual research
- Compliance issues can delay or invalidate research (Research Ops enforcement)
- Valuable insights remain siloed within teams - can't search for "research about churned users" across the organization
- Duplicated research efforts across teams

## Product Vision

An intelligent research assistant that:
1. Guides teams through structured research planning
2. Generates high-quality research scripts aligned with research goals
3. Automatically ensures compliance with industry and Autodesk standards
4. Synthesizes findings into clear, actionable insights
5. Facilitates seamless knowledge sharing across the organization

## Target Users

### Primary Users
- **Non-Researchers Conducting Research**: PMs, designers, engineers who need to run research but lack research background (e.g., "Kumon" persona from team discussion)
- **UX Researchers** at Autodesk conducting user studies
- **Product Managers** running customer discovery
- **Design Teams** validating design decisions
- **Research Operations Specialists** managing research workflows

### User Characteristics
- **Primary Focus**: People without research training who need to conduct quality research
- May conduct 1-20 research studies per year
- Work across multiple product teams
- Need to comply with Autodesk legal and privacy requirements
- Share findings with cross-functional stakeholders
- Struggle with: creating research plans, writing screener questions, synthesizing findings, knowing next steps

## Success Metrics

### Hackathon Success Criteria
- [ ] Agent can generate a complete research plan from conversational input (using Autodesk template)
- [ ] Agent produces research scripts aligned with the plan
- [ ] Agent generates screener questions for participant recruitment
- [ ] Agent shows recruitment automation flow (booking system integration with screener filtering)
- [ ] Agent validates compliance requirements (CRA, recording consent, privacy)
- [ ] Agent summarizes findings from transcripts (pain points + opportunities, no hallucination)
- [ ] Agent can generate shareable reports (one-pager or slide deck)
- [ ] Agent files research in repository with searchable tags (OKRs, teams, topics)

### Long-term Success Metrics
- **Efficiency**: 50% reduction in time spent on research planning and administration
- **Quality**: 90% of research plans meet quality standards (comprehensive goals, clear hypotheses, appropriate methodology)
- **Compliance**: 100% of studies have required CRA agreements and follow best practices
- **Impact**: 3x increase in research insights shared across teams

## Core Features

### 1. Research Plan Development

**User Story**: As a researcher, I want to quickly develop a comprehensive research plan so that I can ensure my study is well-structured and aligned with business goals.

**Capabilities**:
- Guide users through structured planning conversation
- Generate research plans with the following sections:
  - **Research Goals**: What questions are we trying to answer?
  - **Hypothesis**: What do we believe and want to validate?
  - **Methodology**: What research methods will we use? (interviews, surveys, usability tests, etc.)
  - **Participants**: Who should we talk to? (personas, sample size, recruitment criteria)
  - **Timeline**: When will research be conducted?
  - **Success Criteria**: How will we know if the research was successful?

**Inputs**:
- Project context and background
- Business objectives
- Target user segments
- Research constraints (timeline, budget, access)

**Outputs**:
- Structured research plan document (markdown format)
- Saved to `memory/research-plans/[project-name]-research-plan.md`

---

### 2. Research Script Generation

**User Story**: As a researcher, I want to generate interview/study scripts based on my research plan so that my sessions are consistent and comprehensive.

**Capabilities**:
- Automatically generate research scripts from the research plan
- Include:
  - **Introduction**: Welcome and consent
  - **Warm-up Questions**: Build rapport
  - **Core Questions**: Address research goals and hypothesis
  - **Task Scenarios**: For usability testing (if applicable)
  - **Follow-up Probes**: Dig deeper into responses
  - **Closing**: Thank participant, next steps
- Customize script based on methodology (interview vs usability test vs survey)
- Align questions with research goals and hypothesis
- **Identify and eliminate leading questions**:
  - Scan generated questions for bias or leading language
  - Flag questions that suggest desired answers
  - Suggest neutral alternatives
  - Example: "Don't you think X is confusing?" → "What are your thoughts on X?"
  - Helps non-researchers avoid common pitfalls

**Inputs**:
- Research plan (from Feature 1)
- Methodology type
- Session duration

**Outputs**:
- Research script document (markdown format)
- Saved to `memory/research-scripts/[project-name]-script.md`

---

### 3. Screener Questions & Participant Recruitment Automation

**User Story**: As a researcher, I want to create screener questions and automate participant recruitment so that I conduct research with high-quality, relevant users who match my target personas.

**Capabilities**:

**Phase 1: Screener Question Generation**
- Generate screener questions based on research goals and target participants
- Help identify qualifying vs. disqualifying criteria
- Examples:
  - **Looking for churned users?** Screen out active users who still use the product
  - **Looking for specific persona?** Filter by job role, experience level, tools used
  - **Looking for specific behaviors?** Screen for users who have encountered specific pain points
- Create recruitment criteria document with:
  - Sample size needed (qualitative vs quantitative)
  - Required demographics
  - Must-have vs nice-to-have criteria
  - Disqualifying criteria

**Phase 2: Recruitment Automation**
- **Integration with booking systems** (Calendly, Microsoft Bookings, internal tools)
- Automatically apply screener questions when participants sign up
- Filter participants based on screener responses:
  - **Qualify**: Participant meets criteria → allow booking
  - **Disqualify**: Participant doesn't meet criteria → block booking or send rejection
- Track recruitment status:
  - How many participants qualified?
  - How many sessions booked?
  - Target sample size reached?
- Send automated communications:
  - Confirmation emails to qualified participants
  - Include CRA agreement for signing
  - Session reminders

**Why This Matters**:
- **Qualitative research doesn't need statistical significance** - it needs the *right* users
- Current problem: Teams don't use screener questions, so they get wrong participants (e.g., active users when researching churn)
- Wrong participants = low-quality insights = bad product decisions
- Manual recruitment is time-consuming and error-prone
- Automated filtering ensures only qualified participants book sessions

**Inputs**:
- Research plan (goals, hypothesis, target participants)
- Persona descriptions
- Specific qualifying/disqualifying criteria
- Sample size needed
- Booking system integration details (optional for hackathon)

**Outputs**:
- Screener questions document (markdown format)
- Saved to `memory/screener-questions/[project-name]-screener.md`
- Integration-ready format for booking systems (Calendly, etc.)
- Recruitment tracking dashboard (showing qualified vs disqualified participants)

---

### 4. Compliance & Best Practices Validation

**User Story**: As a researcher, I want to ensure my study complies with Autodesk and industry standards so that I can avoid legal issues and maintain participant trust.

**Capabilities**:
- Validate research plan against compliance checklist:
  - **CRA Agreement**: Ensure participants will sign Customer Research Agreement
  - **Privacy Requirements**: Verify PII handling procedures
  - **Recording Consent**: Confirm consent for audio/video recording
  - **Data Storage**: Validate secure storage practices
  - **Incentive Compliance**: Check incentive policies
  - **Accessibility**: Ensure inclusive participant recruitment
- Generate compliance checklist for each study
- Flag missing or incomplete compliance items
- Provide templates for required documents (CRA, consent forms)

**Inputs**:
- Research plan
- Study methodology
- Participant information

**Outputs**:
- Compliance checklist document
- Saved to `memory/compliance/[project-name]-compliance.md`
- Links to required agreement templates

**Compliance Requirements**:
- All participants must sign CRA before participating
- PII must be stored securely and anonymized in reports
- Recording consent must be explicit and documented
- Research data retention follows Autodesk policies

---

### 5. Findings Summarization

**User Story**: As a researcher, I want to quickly synthesize my research transcripts into actionable pain points and opportunities so that I can hand off clear, evidence-based recommendations to product teams.

**Capabilities**:
- Analyze research session transcripts and recordings
- **CRITICAL: Avoid Hallucination** - Extract pain points and opportunities ONLY from provided transcripts, never infer or create findings
- Generate structured findings summary:
  - **Top Pain Points**: Key user problems identified across participants
    - Quote/evidence from participants
    - Video clip references (timestamp and participant ID for Dovetail integration)
    - Affected product area
  - **Opportunity Areas**: Actionable opportunities derived from each pain point
    - What could be improved?
    - Expected impact on user experience
    - Priority/severity
  - **Hypothesis Validation**: Did findings support or refute the hypothesis?
  - **Participant Overview**: Demographics and recruitment summary (anonymized)
  - **Deep Dives**: Detailed analysis of each major pain point with supporting evidence
- Tag findings by:
  - Theme/category
  - Product area
  - OKR linkage (which OKRs does this research support?)
  - Team (which team should act on this?)
- Link findings back to original research goals

**Why This Matters**:
- Stakeholders need video evidence - they won't believe findings without seeing users say it
- Pain points alone aren't actionable - need clear opportunity areas
- Proper hand-off to product/design teams requires clear recommendations

**Inputs**:
- Research transcripts and recordings (uploaded by user)
- Research plan (for context and hypothesis)
- Session metadata (participant IDs, dates)
- OKRs to link research to business goals

**Outputs**:
- Findings summary document (markdown format)
- Saved to `memory/findings/[project-name]-findings.md`
- Includes video clip references for evidence

---

### 6. Knowledge Sharing & Repository Management

**User Story**: As a researcher, I want to automatically share and file my research insights so that colleagues across the organization can discover and learn from past research.

**Capabilities**:
- Generate shareable research reports in multiple formats:
  - **One-Pager**: Single page summary with top pain points and opportunities
  - **Slide Deck**: Formatted for stakeholder presentations
    - Top pain points with evidence
    - Opportunities for each pain point
    - Deep dive slides for each major pain point
    - Video clip references
    - Recommendations and next steps
  - **Detailed Report**: Full findings with all evidence and recommendations
- Share research outputs:
  - **Slack**: Automatically post research summary to relevant channels
  - **PDF Export**: For broader distribution
  - **Shareable links**: For internal wikis or collaboration tools
- **Research Repository Management**:
  - Automatically file research artifacts into repository folders
  - Tag research by:
    - **OKRs**: Which business objectives does this research support?
    - **Teams**: Which teams should care about these findings?
    - **Topics**: Product areas, user types, features
    - **Date**: When research was conducted
  - **Searchable Index**: Enable queries like "Find all research about churned users" or "Show research supporting OKR #3"
  - List all completed studies with quick access to findings

**Why This Matters**:
- Avoid duplicated research efforts - teams can find existing research before starting new studies
- Stakeholders need different formats (leadership wants one-pagers, product teams want detailed reports)
- Repository becomes organizational knowledge base - searchable across all historical research

**Inputs**:
- Findings summary (from Feature 5)
- Target audience (leadership, product team, design team)
- Desired format (one-pager, slide deck, detailed report)
- OKR tags
- Team tags
- Topic tags

**Outputs**:
- Formatted research report in requested format
- Saved to `memory/reports/[project-name]-report.md`
- Updated research repository index at `memory/README.md`
- Slack notification (if enabled)
- Repository automatically organized by tags

---

## User Workflows

### Workflow 1: Complete Research Study Lifecycle (For Non-Researchers)

```
1. User: "I need to do research on [topic]"
   ↓
2. Agent: "Do you have a research plan?" (Yes/No)
   ↓
3. If No → Agent guides through planning conversation:
   - What are your goals?
   - What's your hypothesis?
   - What methodology? (interviews, usability tests, surveys)
   - Who are your target participants?
   ↓
4. Agent generates research plan using Autodesk template
   ↓
5. User reviews and refines plan
   ↓
6. Agent: "Would you like me to create an interview script?"
   ↓
7. Agent generates script aligned with research goals and hypothesis
   ↓
8. Agent: "Let me create screener questions to help you recruit the right participants"
   ↓
9. Agent generates screener questions to filter for target personas
   ↓
10. Agent validates compliance:
    - CRA agreement required? ✓
    - Recording consent documented? ✓
    - PII handling procedures? ✓
    - Flags any missing items
   ↓
11. User conducts research sessions (manual)
    ↓
12. User uploads transcripts and recordings
    ↓
13. Agent: "Let me synthesize your findings - I'll extract pain points and opportunities ONLY from your transcripts"
    ↓
14. Agent generates findings summary:
    - Top pain points with video clip references
    - Opportunity areas for each pain point
    - Hypothesis validation
    - Recommendations for teams
   ↓
15. User reviews findings
    ↓
16. Agent: "Would you like a one-pager or slide deck to share these findings?"
    ↓
17. Agent generates shareable report in requested format
    ↓
18. Agent: "Should I share this to Slack and file it in the repository?"
    ↓
19. Agent tags research by OKRs, teams, topics
    ↓
20. Agent files research in repository and updates index
    ↓
21. Research is now searchable by other teams
```

### Workflow 2: Quick Compliance Check

```
1. User provides existing research plan
   ↓
2. Agent validates against compliance checklist
   ↓
3. Agent flags missing items
   ↓
4. Agent provides templates for required documents
   ↓
5. User addresses compliance gaps
```

### Workflow 3: Findings-Only Workflow

```
1. User has completed research sessions
   ↓
2. User provides session notes
   ↓
3. Agent asks for research context (goals, hypothesis)
   ↓
4. Agent generates findings summary
   ↓
5. Agent creates shareable report
```

---

## Technical Requirements

### Memory Structure

```
research-assistant-agent/
├── CLAUDE.md                       # Agent system prompt
├── memory/
│   ├── README.md                   # Research repository index (searchable by OKR, team, topic)
│   ├── research-plans/             # All research plans
│   │   └── [project-name]-research-plan.md
│   ├── research-scripts/           # Generated scripts
│   │   └── [project-name]-script.md
│   ├── screener-questions/         # Recruitment screener questions
│   │   └── [project-name]-screener.md
│   ├── compliance/                 # Compliance checklists
│   │   └── [project-name]-compliance.md
│   ├── session-notes/              # Raw research notes/transcripts
│   │   └── [project-name]/
│   │       ├── participant-01.md
│   │       └── participant-02.md
│   ├── findings/                   # Synthesized findings (pain points + opportunities)
│   │   └── [project-name]-findings.md
│   └── reports/                    # Shareable reports (one-pagers, slide decks)
│       └── [project-name]-report.md
└── templates/
    ├── research-plan-template.md
    ├── research-script-template.md
    ├── screener-questions-template.md
    ├── compliance-checklist-template.md
    ├── session-notes-template.md
    ├── findings-template.md
    ├── report-one-pager-template.md
    └── report-slide-deck-template.md
```

### Agent Commands

```
/plan_research             # Start research planning workflow (asks: "Do you have a research plan?")
/generate_script           # Create interview/study script from research plan (identifies leading questions)
/review_questions          # Review existing questions and identify leading/biased language
/create_screener           # Generate screener questions for participant recruitment
/check_compliance          # Validate compliance requirements (CRA, privacy, etc.)
/add_session_notes         # Add transcripts/notes from research session
/summarize_findings        # Generate findings summary (pain points + opportunities)
/create_report             # Generate shareable report (one-pager or slide deck)
/share_research            # Share research to Slack and file in repository
/search_repository         # Search past research by OKR, team, topic, or keyword
/list_studies              # Show all research studies in repository
/link_to_okr               # Tag research with relevant OKRs
```

### Integration Points

- **File System**: Read/write markdown files to memory structure
- **Git**: Track changes to research artifacts
- **Export Tools**: Convert markdown to PDF (future: integrate with Confluence, Notion, etc.)

### Data & Privacy Considerations

- All participant data must be anonymized in findings and reports
- PII should only exist in session notes (stored securely)
- CRA agreements must be tracked and verified
- Agent should remind users to follow data retention policies

---

## Non-Functional Requirements

### Performance
- Research plan generation: < 2 minutes
- Script generation: < 1 minute
- Findings summarization: < 5 minutes (for 5-10 session notes)
- Report generation: < 1 minute

### Usability
- Conversational interface (natural language commands)
- Clear prompts and guidance throughout workflows
- Ability to edit and refine generated documents

### Reliability
- Validate all file operations (read/write)
- Handle missing or incomplete inputs gracefully
- Provide clear error messages

### Security
- Follow Autodesk data handling policies
- Ensure secure storage of participant information
- Comply with GDPR/CCPA requirements

---

## Out of Scope (For Hackathon)

- Live transcription during sessions
- Advanced analytics (sentiment analysis, quantitative analysis)
- Dovetail integration for video clip management
- Full Slack bot integration (can do manual sharing for hackathon)
- Integration with external tools (Confluence, Jira, Notion)
- Multi-language support
- Automated video/audio analysis (can reference timestamps manually)
- Calendar integration for automated scheduling

---

## Future Enhancements

### Phase 2: Automation
- Automated participant recruitment via integration with research panels
- Calendar integration for session scheduling
- Real-time transcription and note-taking during sessions

### Phase 3: Advanced Analysis
- Sentiment analysis on participant feedback
- Quantitative data analysis for survey results
- Longitudinal trend analysis across multiple studies

### Phase 4: Collaboration
- Multi-user collaboration on research plans
- Real-time updates and notifications
- Integration with Autodesk design/product tools

### Phase 5: AI-Powered Insights
- Predictive recommendations for research methodologies
- Auto-tagging of findings across studies
- Research insight search engine across all historical studies

---

## Appendix: Autodesk Research Best Practices

### CRA (Customer Research Agreement) Requirements
- **CRA is like an NDA** - protects Autodesk confidential information from being shared by participants
- **Absolutely required** - All external participants must sign CRA before research begins
- **Enforced by Research Ops** - If Research Ops discovers you're not using CRAs, you will get in trouble and research may be invalidated
- **Low friction** - It's a simple form, participants sign it without issues
- CRA covers:
  - Consent to participate
  - Recording consent (audio/video)
  - Data usage and privacy
  - Confidentiality (participants can't share what they learn)
  - Compensation/incentives
- **When required**: Any research with external participants (not just Autodesk employees)

### Participant Privacy
- Use participant IDs (P01, P02) instead of names in notes and reports
- Store PII separately from research findings
- Obtain explicit consent for any recording
- Follow data retention policies (typically 2-3 years)

### Research Quality Standards
- Clear research goals tied to business objectives
- Testable hypotheses
- Appropriate sample size (typically 5-8 for qualitative, 30+ for quantitative)
- Diverse participant recruitment (avoid bias)
- Structured interview guides
- Triangulation of findings across multiple participants

### Common Research Methodologies at Autodesk
- **User Interviews**: 1-on-1 conversations to understand user needs, behaviors, pain points
- **Usability Testing**: Observing users complete tasks with prototypes or products
- **Surveys**: Quantitative data collection from larger sample sizes
- **Field Studies**: Observing users in their natural environment
- **Diary Studies**: Participants document experiences over time
- **Card Sorting**: Understanding information architecture and mental models

---

## Risks & Mitigations

| Risk | Impact | Likelihood | Mitigation |
|------|--------|------------|------------|
| Compliance gaps in generated plans | High | Medium | Build comprehensive compliance checklist; validate against ADSK policies |
| Poor quality findings summaries | Medium | Medium | Provide clear structure and examples; allow user refinement |
| Data privacy violations | High | Low | Enforce anonymization; provide clear guidance on PII handling |
| Low adoption due to complexity | Medium | Medium | Design simple, intuitive workflows; provide examples and templates |
| Integration challenges with existing tools | Low | Medium | Start with standalone tool; plan integrations for Phase 2+ |

---

## Success Criteria for Hackathon Demo

At the end of the hackathon, the team should be able to demonstrate:

1. **Research Planning**: Generate a complete research plan from conversational input
2. **Script Generation**: Create an interview script aligned with the research plan
3. **Screener Questions & Recruitment**: Generate screener questions and show recruitment automation flow
4. **Compliance Check**: Validate a research plan for compliance and flag missing items
5. **Findings Summary**: Synthesize 3-5 mock session notes/transcripts into a findings document with pain points and opportunities
6. **Report Sharing**: Generate a shareable report (one-pager or slide deck) from findings
7. **Repository Management**: File research in repository with OKR/team/topic tags

**Demo Flow**:
```
1. "I need to plan research about churned users"
2. Agent guides through planning questions (goals, hypothesis, methodology, participants)
3. Shows generated research plan using Autodesk template
4. Agent creates interview script aligned with goals
5. Agent generates screener questions to filter for churned users (not active users)
6. Agent shows recruitment automation integration (booking system with screener filtering)
7. Agent validates compliance (CRA required? ✓, Recording consent? ✓, shows checklist)
8. User uploads 3-5 mock transcripts
9. Agent generates findings summary:
   - Top pain points with evidence
   - Opportunity areas
   - Video clip references
   - Recommendations
10. Agent creates shareable slide deck
11. Agent tags research by OKRs, teams, topics
12. Agent files in repository
13. Shows research repository index (searchable by tags)
```

---

## Team Responsibilities (Hackathon)

- **Person 1**: Memory structure, file management, templates
- **Person 2**: Research planning & script generation workflows
- **Person 3**: Compliance validation & best practices integration
- **Person 4**: Findings summarization & reporting workflows

---

## References

- Autodesk Research Operations Guidelines (internal)
- CRA Agreement Template (internal)
- UXPA Research Standards
- Nielsen Norman Group Research Best Practices
