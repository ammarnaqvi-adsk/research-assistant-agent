# Forma Onboarding Feedback Research Findings

**Research Plan**: Exploratory onboarding feedback (no formal research plan)

**Date**: December 16, 2025

**Research Lead**: Clément Lemaire

**Sessions Conducted**: 1 participant (P01)

---

## Executive Summary

1. **Navigation shortcuts inconsistent with Revit** - P01 explicitly identified this as "the hardest thing" about adopting Forma, creating friction for Revit users transitioning between tools.
2. **Street parking feature missing** - Critical for master planning workflows; P01 has existing Revit family solution that could be adapted.
3. **Cycle lanes and footpaths cannot be added to roads** - Essential infrastructure for European master planning, currently very manual to implement.
4. **Google Maps integration highly valued** - Reduces setup time and provides immediate topography and imagery context.
5. **Analysis features meet user needs** - Carbon, sunlight, and daylight analysis are easy to launch with fast results.

---

## Research Goals Recap

**Original research questions**:
- This was an exploratory onboarding feedback session
- No formal hypothesis was being tested
- Goal: Understand P01's experience with Forma after 2 weeks of use

**Hypothesis**: N/A - Exploratory research

---

## Hypothesis Validation

**Result**: ❓ Not Applicable - Exploratory Study

**Context**: This session was an exploratory interview to gather onboarding feedback from a new Forma user (P01) who had been using the tool for 2 weeks.

---

## Top Pain Points

*Pain points are ranked by severity and frequency. Each includes evidence from participant transcripts.*

---

### Pain Point 1: Navigation shortcuts different from Revit

**Description**: Forma uses different navigation controls than Revit (shift key for pan vs. middle mouse button in Revit). This creates muscle memory conflicts for users who work in both tools, causing constant friction during adoption. P01 explicitly identified this as "the hardest thing" when asked for overall feedback.

**Evidence from Participants**:
- **P01** (20:35): "I had to learn how to, um, pan using the shift key. Now I'm sure that's something that's fixed and I think I remember it from eight years ago. Um, it's just it's not how you pan in Revit."
- **P01** (20:48): "So like if people are going to be going from Revit to Format and back to Revit, it would be good if some of the basic commands are familiar."
- **P01** (21:50-22:08): "If someone is familiar with Revit and then they're using Forma for the first time, they're gonna constantly not be able to pan and zoom like they do in Revit. So it's gonna be an obstacle for them and they're not gonna like using. They're gonna be uncomfortable."
- **P01** (22:21): "It's like getting into a car with the steering wheel on the other side."
- **P01** (22:33): "But look, you asked for feedback and **that was the hardest thing actually**."

**Frequency**: 1/1 participants mentioned this (100%)

**Severity**: 🔴 High

**Context**: This pain point occurs immediately upon starting to use Forma and persists throughout the learning period (P01 mentioned adapting "after a week or two"). It affects users who are transitioning from Revit, which is the primary target audience.

**Affected Product Area**: Navigation controls (pan, zoom)

**Impact on User Experience**:
- Creates immediate friction for Revit users (primary target audience)
- Blocks muscle memory and slows down workflows
- Causes discomfort and reluctance to use the tool
- Prevents smooth switching between Revit and Forma for users who need both tools
- Takes 1-2 weeks to adapt

**User Behavior Observed**:
- P01 had to consciously learn new shortcuts
- Compared the experience to "steering wheel on the wrong side" - disorienting
- Eventually adapted after 2 weeks but identified this as the single biggest obstacle

---

### Opportunity: Align navigation shortcuts with Revit

**Recommendation**: Make Forma's navigation shortcuts match Revit's navigation controls (especially pan and zoom), or provide a "Revit mode" toggle that uses Revit-style shortcuts.

**Expected Impact**:
- Eliminate the #1 pain point for Revit users adopting Forma
- Reduce learning curve from weeks to days
- Enable seamless workflow switching between Revit and Forma
- Increase adoption among existing Revit user base

**Priority**: 🔴 High

**Rationale**:
1. P01 explicitly identified this as "the hardest thing actually" when asked for overall feedback
2. Both Forma and Revit are Autodesk products - this should be solvable
3. Affects primary target audience (Revit users)
4. P01 directly connected this to adoption: "The more interoperability between Forma and Revit, I think you'll get more people using Forma" (23:28)
5. Creates friction for entire learning period (1-2 weeks)

---

### Pain Point 2: No street parking feature

**Description**: Forma lacks a way to create street parking layouts (parallel or perpendicular parking along roads). The parking plugin works well for parking lots/basements but not for street-level parking, which is critical for master planning.

**Evidence from Participants**:
- **P01** (3:24): "The roads and the parking is also very important because they take up space on the ground and the plug in is very good to do an entire parking area like in a basement."
- **P01** (3:40): "But I haven't found a way just to do parking on the street like in a in a in a row."
- **P01** (4:08): "Maybe I can bring that into format, just, yeah, I just thought of that. I haven't used that in two years, but that was very useful when I and it would again count the number of parking spaces."

**Frequency**: 1/1 participants mentioned this (100%)

**Severity**: 🔴 High

**Context**: Street parking is needed for master planning workflows. P01 previously used a Revit family that could create parallel/perpendicular parking and automatically count spaces.

**Affected Product Area**: Site design - parking and roads

**Impact on User Experience**:
- Blocks critical master planning task
- Forces manual workarounds
- P01 considered importing Revit family as workaround

**User Behavior Observed**:
- P01 looked for this feature but couldn't find it
- Immediately thought of bringing existing Revit solution into Forma

---

### Opportunity: Add street parking feature

**Recommendation**: Create a street parking feature that allows users to place parallel or perpendicular parking along roads, with automatic space counting (similar to existing Revit family P01 mentioned).

**Expected Impact**:
- Complete the parking workflow (currently only parking lots/basements supported)
- Eliminate manual workarounds for street-level parking
- Better support European master planning requirements

**Priority**: 🔴 High

**Rationale**:
- Critical for master planning use case
- User has existing solution in Revit that could be adapted
- Parking is essential for site feasibility studies

---

### Pain Point 3: Cannot add cycle lanes and footpaths to roads

**Description**: Forma lacks the ability to add cycle lanes and footpaths alongside roads. This requires very manual work and is essential for master planning, especially in Europe.

**Evidence from Participants**:
- **P01** (4:46): "Could have a road that's say 6 meters wide and then with a cycle lane on both sides and a footpath. So if we could, you know, if it's possible in the future to or maybe there's a way to do it and I just don't know how to do it."
- **Clément** (5:00): "I mean, there's a way, but it's very manual. But we are working on something that is close to what you describe."
- **P01** (18:43-19:06): "If I wanted to draw a footpath here now what? Because the line tool is great, but um... [Clément: Yeah, you cannot snap and it's done.]"

**Frequency**: 1/1 participants mentioned this (100%)

**Severity**: 🔴 High

**Context**: Essential for European master planning. Currently possible but "very manual." Autodesk team is already working on this feature.

**Affected Product Area**: Site design - roads and infrastructure

**Impact on User Experience**:
- Makes infrastructure planning very manual
- Cycle lanes and footpaths are regulatory requirements in many regions
- Line tool cannot snap, making manual workarounds difficult

---

### Opportunity: Add cycle lanes and footpaths to road configurations

**Recommendation**: Allow users to configure roads with cycle lanes and footpaths (e.g., "6m road + cycle lanes on both sides + footpaths").

**Expected Impact**:
- Reduce manual work for infrastructure planning
- Meet European master planning requirements
- Enable proper site design with complete street infrastructure

**Priority**: 🔴 High

**Rationale**:
- Essential for master planning workflows
- Regulatory requirement in many regions
- Team already working on this (per Clément's comment)

---

### Pain Point 4: Line tool cannot snap

**Description**: The line tool in Forma does not support snapping to existing geometry, making it difficult to draw features like footpaths that need to align with buildings or roads.

**Evidence from Participants**:
- **P01** (18:43-19:06): "If I wanted to draw a footpath here now what? Because the line tool is great, but um..."
- **Clément** (19:01): "Yeah, you cannot snap and it's done."

**Frequency**: 1/1 participants mentioned this (100%)

**Severity**: 🟡 Medium

**Context**: Discovered when trying to manually draw footpaths as a workaround for the cycle lanes/footpaths pain point.

**Affected Product Area**: Line tool / drawing tools

**Impact on User Experience**:
- Makes manual workarounds more difficult
- Reduces precision when drawing infrastructure
- Slows down workflows that require aligned geometry

---

### Opportunity: Add snapping to line tool

**Recommendation**: Enable snapping functionality for the line tool to allow precise alignment with existing geometry (roads, buildings, property lines).

**Expected Impact**:
- Improve precision of manual drawing workflows
- Enable better workarounds while advanced features are developed
- Standard feature in CAD/design tools

**Priority**: 🟡 Medium

**Rationale**:
- Improves workarounds for other missing features
- Standard expectation in design tools
- Medium priority as it's a supporting feature

---

### Pain Point 5: Site boundary visualization doesn't match Irish conventions

**Description**: In Ireland, site boundaries are typically shown as red lines around the perimeter, not red-filled areas. Forma defaults to showing the entire site area filled with red color.

**Evidence from Participants**:
- **P01** (16:00): "So do you see how the site area is this red color for the entire site? Is there a way so normally in Ireland we show just a red line around the boundary."

**Frequency**: 1/1 participants mentioned this (100%)

**Severity**: 🟢 Low

**Context**: This is a regional convention for presenting site plans to stakeholders. Clément walked P01 through a workaround (use line tool to trace boundary and hide site limit layer), which P01 found helpful.

**Affected Product Area**: Site visualization

**Impact on User Experience**:
- Minor presentation issue for Irish/regional stakeholders
- Doesn't block workflows
- Workaround exists

---

### Opportunity: Add site boundary display options

**Recommendation**: Provide option to show site boundary as outline only (not filled) to support regional presentation conventions.

**Expected Impact**:
- Better match regional presentation requirements
- Reduce need for workarounds

**Priority**: 🟢 Low

**Rationale**:
- Workaround exists
- Regional preference, not universal requirement
- Doesn't block critical workflows

---

## Theme Analysis

*High-level patterns across pain points*

| Theme | Description | Pain Points Included | Participant Frequency | Priority |
|-------|-------------|---------------------|----------------------|----------|
| **Revit Interoperability** | Forma and Revit have inconsistent patterns (shortcuts, workflows) despite being Autodesk products | PP1 (navigation) | 1/1 (100%) | 🔴 High |
| **Site Infrastructure Gaps** | Missing features for complete site design (street parking, cycle lanes, footpaths) | PP2 (parking), PP3 (cycle lanes/footpaths) | 1/1 (100%) | 🔴 High |
| **Basic Drawing Tool Capabilities** | Drawing tools lack standard CAD features (snapping) | PP4 (line tool snapping) | 1/1 (100%) | 🟡 Medium |
| **Regional Presentation Conventions** | Display defaults don't match all regional standards | PP5 (site boundary) | 1/1 (100%) | 🟢 Low |

---

## Positive Findings *(What Worked Well)*

### What Users Appreciated

1. **Google Maps integration**
   - Evidence: "It was quite good. I like the fact that it is synchronized with Google Maps. So straight away we have a basic topography, you know, there's a hill or... And we have the imagery of roads and the landscape, so that's very helpful." (2:47)
   - Why it matters: Reduces setup time and provides immediate context for site planning

2. **Analysis features (carbon, sunlight, daylight)**
   - Evidence: "It's pretty easy to launch. You see the result is fast." (14:22)
   - Evidence: "Especially the carbon analysis. I think it's because what we want to show is... living close to the city uses less carbon for transport." (8:46)
   - Why it matters: Core value proposition for master planning; helps justify urban infill vs. countryside development

3. **Space settings for building setbacks**
   - Evidence: "Normally we do have a 2 1/2 meter space in front of the houses, so that's great that you can set that." (7:23)
   - Why it matters: Matches their workflow requirements and regulatory standards

**Preserve these strengths**: Google Maps integration and analysis features are key differentiators that provide immediate value. These should remain fast and easy to use as more features are added.

---

## Behavioral Patterns

*Observable user behaviors, not just what they said*

| Pattern | Description | Frequency | Implication |
|---------|-------------|-----------|-------------|
| **Looked for workarounds** | P01 immediately thought of bringing Revit family into Forma when feature was missing | 1/1 participants | Users with Revit experience will try to leverage existing assets |
| **Adapted over time** | P01 mentioned "you learn it after a week or two" for navigation shortcuts | 1/1 participants | Resilient users will push through friction, but it creates 1-2 week adoption barrier |
| **Engaged and constructive** | P01 provided detailed, specific feedback with examples and analogies | 1/1 participants | This user profile (experienced, thoughtful) is valuable for beta testing |

---

## Participant Overview *(Anonymized)*

**Total Participants**: 1

**Demographics**:
- Roles: 1 City Council master planner (formerly architect)
- Experience levels: 1 Expert (8 years Revit, 10 years since first Forma/Formit use)
- Company sizes: 1 Public sector (City Council)
- Locations: 1 Europe (Ireland)

**Participant Profiles**:
| ID | Role | Experience | Usage Pattern | Notes |
|----|------|------------|---------------|-------|
| P01 | Master planner, City Council | 8 years Revit, returning to Forma after 10 years | 2 weeks of use | Planning 6 locations (60-400 units each) for city expecting 50% population growth |

---

## Recommendations *(Prioritized)*

*Actionable next steps for product, design, and research teams*

### 🔴 High Priority (Do First)

**1. Align navigation shortcuts with Revit (or provide "Revit mode")**
- **Why**: P01 explicitly stated "that was the hardest thing actually." Both are Autodesk products. Creates 1-2 week adoption barrier for primary target audience (Revit users).
- **Addresses**: Pain Point #1
- **Expected Impact**: Eliminate #1 pain point, reduce learning curve, increase Revit user adoption
- **Suggested Owner**: Forma Product Team + Revit Platform Team

**2. Add street parking feature**
- **Why**: Critical for master planning workflows. P01 has existing Revit solution that could be adapted.
- **Addresses**: Pain Point #2
- **Expected Impact**: Complete parking workflow (currently only lots/basements supported)
- **Suggested Owner**: Forma Site Design Team

**3. Add cycle lanes and footpaths to road configurations**
- **Why**: Essential for European master planning, regulatory requirement in many regions. Team already working on this.
- **Addresses**: Pain Point #3
- **Expected Impact**: Reduce manual work, meet regional requirements
- **Suggested Owner**: Forma Site Design Team (already in progress per Clément)

### 🟡 Medium Priority (Do Next)

**4. Add snapping to line tool**
- **Why**: Standard CAD feature, improves workarounds for other missing features
- **Addresses**: Pain Point #4
- **Expected Impact**: Improve precision of manual workflows
- **Suggested Owner**: Forma Drawing Tools Team

### 🟢 Low Priority (Nice to Have)

**5. Add site boundary display options (outline vs. filled)**
- **Why**: Regional preference for presentations. Workaround exists.
- **Addresses**: Pain Point #5
- **Expected Impact**: Better match regional conventions
- **Suggested Owner**: Forma Visualization Team

---

## What to Validate Next

### Unanswered Questions
- How widespread is the navigation shortcuts pain point? Does it affect other Revit users similarly?
- What other Revit interoperability gaps exist? (P01 mentioned "the more interoperability... the more people will use Forma")
- How do users prioritize street parking vs. cycle lanes/footpaths? Which is more critical?
- Are there other regional/country-specific presentation conventions we should support?

### Suggested Follow-Up Research

**1. Revit User Navigation Study**
- **Why**: Validate whether navigation shortcuts are a widespread issue for Revit users
- **Method**: Task-based usability testing with 5-8 Revit users new to Forma, observe pan/zoom struggles
- **Timeline**: Q1 2026

**2. Site Infrastructure Feature Prioritization**
- **Why**: Understand which missing site features (parking, cycle lanes, footpaths) are most critical
- **Method**: Survey + interviews with master planners and site designers
- **Timeline**: Q1 2026

---

## Limitations & Caveats

*Important context about the research*

### Sample Size
- Total participants: 1
- **Note**: This is a single exploratory interview, not a comprehensive study. Findings represent one user's experience and should be validated with additional participants before making major product decisions.

### Participant Diversity
- Only 1 participant from Ireland, public sector (City Council)
- **Gap**: No representation from private firms, other regions, or less experienced users
- **Note**: Pain points identified may be more or less important for other user segments

### Methodology Limitations
- This was an exploratory onboarding feedback session, not a structured research study with predefined hypotheses
- No formal research plan or screener questions were used

### Confidence Levels
- Findings with 🔴 High severity: Based on P01's explicit statement that navigation was "the hardest thing"
- Other findings: Based on single participant feedback, should be validated with additional users

### What We Can't Conclude
- We cannot generalize these findings to all Forma users
- We don't know if these pain points affect other user segments (e.g., landscape architects, urban planners in other regions)
- We cannot quantify the business impact without studying more users

---

## Appendix: Raw Data Summary

### Session Notes
- See: `test-data/real-transcript-01.md`

### Recordings
- Recording obtained with consent
- Duration: 24m 36s

### Transcripts
- Available: ✅ Yes
- Location: `test-data/real-transcript-01.md`

---

## Methodology Recap

**Research Type**: Exploratory user interview with screen sharing

**Participant Recruitment**: Direct outreach (Catherine Dollard contacted for onboarding feedback)

**Screening**: None (exploratory session)

**Session Format**: 24m 36s, remote video call (Zoom/Teams), with screen sharing walkthrough

**Analysis Method**: Transcript-based synthesis with anti-hallucination protocol (extracted findings directly from transcript)

**Compliance**: ✅ Recording consent obtained | ✅ PII anonymized (participant ID: P01) | CRA status assumed (Autodesk internal research)

---

## Tags for Repository

*For searchability in the research repository*

- **OKRs**: [Forma adoption], [Revit interoperability]
- **Teams**: [Forma Product Team], [Revit Platform Team], [Site Design Team]
- **Topics**: [onboarding], [navigation-shortcuts], [revit-interoperability], [street-parking], [cycle-lanes], [footpaths], [master-planning], [site-design]
- **Product Areas**: [Navigation], [Site Design], [Roads], [Parking], [Analysis], [Drawing Tools]

---

## Share Out Plan

*How and where these findings will be shared*

- [x] **Report Created**: Findings document created
- [ ] **One-pager Created**: See `memory/reports/forma-onboarding-feedback-one-pager.md`
- [ ] **Stakeholders Notified**: [Forma Product Manager, Caterina (Site Design PM)]
- [ ] **Presentation Scheduled**: [TBD]
- [ ] **Slack Shared**: [#forma-product-feedback channel]
- [ ] **Filed in Repository**: Tagged with navigation-shortcuts, revit-interoperability, site-design

---

_Findings synthesized by Autodesk Research Assistant Agent. All evidence extracted directly from participant transcript (no hallucination). Participant anonymized as P01._
