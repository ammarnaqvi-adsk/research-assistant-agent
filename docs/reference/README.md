# Reference Documents

This folder contains official Autodesk research documentation and guidelines that inform the Research Assistant Agent's templates and workflows.

## Documents

### Research Plan Template.pdf
**Official Autodesk Research Plan Template** (based on Nielsen Norman research plan)

This template defines the standard structure for research plans at Autodesk and includes:

**Key Sections**:
1. **Metadata**: Squad name, leads, stakeholders, last updated
2. **Study Purpose & Context**: Objectives and what the research will inform
3. **Research Goals, Questions, Assumptions, and Hypotheses**: Structured table format
4. **Participants**:
   - Sampling method and sample size with rationale
   - Inclusion criteria (what participants must have)
   - Exclusion criteria (who to filter out)
   - Screening questionnaire
   - Demographic balance considerations
5. **Method**: Description of methodology (e.g., moderated usability test, interviews)
6. **Procedure**:
   - Session format with time breakdown
   - Initial questions
   - Tasks (with task table)
   - Closing questions
7. **Observation Guidelines**: How team members should observe sessions
8. **Schedule**: Table for scheduling sessions
9. **Notetaking**: Guidelines for effective note-taking during sessions
10. **Relevant Documents**: Links to consent forms, screener, scripts, checklists

**Usage**: The agent uses this structure when generating research plans via `/plan_research`

**Source**: Nielsen Norman Group research plan methodology, adapted for Autodesk

---

### diy-research-guide.pdf
**DIY Research Guide for Non-Researchers**

Guide for teams conducting research without formal research training. Covers best practices, common pitfalls, and step-by-step guidance.

**Usage**: Informs the agent's guidance for non-researcher users

---

### governance-autodesk-community.pdf
**Governance for Autodesk Community Participation**

Official Autodesk policies for community participation and research, including compliance requirements and ethical guidelines.

**Usage**: Ensures agent follows Autodesk governance standards

---

## How These Inform the Agent

The Research Assistant Agent uses these documents to:

1. **Generate compliant artifacts**: All templates match Autodesk standards
2. **Guide non-researchers**: Agent uses DIY guide principles when assisting beginners
3. **Enforce best practices**: Agent validates research plans against these standards
4. **Maintain consistency**: All research follows the same structure across teams

## Template Mapping

| Reference Document | Agent Template | Agent Command |
|-------------------|----------------|---------------|
| Research Plan Template.pdf | templates/research-plan-template.md | `/plan_research` |
| DIY Research Guide.pdf | AGENT_RULES.md (guidance principles) | All commands |
| Governance doc | templates/compliance-checklist-template.md | `/check_compliance` |

---

_These documents are the source of truth for Autodesk research standards. Agent templates are derived from these official sources._
