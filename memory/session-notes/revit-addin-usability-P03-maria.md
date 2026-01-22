# Session Notes: P03

**Project**: Forma Add-in for Revit Usability Testing

**Research Plan**: See `memory/research-plans/revit-addin-usability-research-plan.md`

**Participant ID**: P03 *(Maria Johansson)*

**Date**: April 11, 2024

**Facilitator**: Tamira McCoy

**Notetaker**: Zhou Fang

**Session Duration**: ~45-60 minutes

---

## ⚠️ Privacy Reminder

**USE PARTICIPANT IDs ONLY** - Never include real names, emails, or other PII in shared reports.

**This document may be shared** with product teams, stakeholders, and other researchers.

---

## Session Metadata

### Participant Profile *(Anonymized)*

- **ID**: P03
- **Role/Title**: Architect/Designer (specific role not documented)
- **Experience**: Has experience with Revit and Forma workflows
- **Product Usage**: Experienced with Forma-Revit interoperability

### Session Info

- **Methodology**: Usability Testing (Figma Prototype Walkthrough)
- **Platform**: Remote with screen sharing
- **Recording**: Not documented in notes
- **Recording Consent**: Not documented in notes
- **CRA Signed**: Not documented in notes

---

## Warm-Up Summary

**Background**: P03 is an architect/designer with experience using both Forma and Revit. Has working knowledge of the existing Forma-Revit workflow.

**Key Context**: P03 had clear expectations about how the workflow should function and provided specific suggestions for improvements throughout the session.

---

## Observations & Key Moments

### Task I: Download Add-in and Load Proposal

**Where to go and download add-in:**
- ⚠️ **Confusion**: P03 looked in multiple places:
  - "Go to the dots (besides proposal) to download it"
  - "Preferably to see a Revit Icon on the navigation bar or the analysis bar"
  - "Look for logo for Revit within Forma"
- **Takeaway**: Download location not immediately obvious - P03 expected to see Revit branding/icon

**Q1: Difficulty rating (1-5 scale)**
- ⚠️ **Difficulty finding the icon to download**
- **Note**: Didn't give an actual score

**Q2: Loading Proposal A from Revit**
- ✅ **Success**: "Go to add-in and load proposal (instead of going to Massing & Site)"
- 💡 **Positive reaction**: "The presentation seems logical"

**Observation** - Hub/Project list scalability concern
- **Suggestion**: "(If there are folders in the hub, it would be logical to see the folder in the hub instead of showing every project in the list as the list can get very long)"
- **Alternative suggestion**: "Otherwise, a search bar to search for the name of the project would be helpful"

**Observation** - Proposal lock/status indicator request
- **Suggestion**: "Some visual on Forma side beside the proposal imported to Revit would also help remind users not to edit this proposal in Forma anymore"
- **Context**: Concern about keeping Forma and Revit in sync

**Q3: Describe what you see (Preview screen)**
- ⚠️ **Confusion**: "Before the load, the file is created without being able to select what can be loaded. (During the preview screen)"
- ⚠️ **Confusion**: "Not understanding from the dialog screen to know for sure this is a preview screen"
- 💡 **Positive reaction**: "Like the idea of the preview"
- **Expectation mismatch**: "Checking or unchecking boxes should ideally change the preview"
- 💡 **Positive reaction**: "Great to have the same symbols associated with each icon in Forma"
- **Takeaway**: P03 likes the preview concept but expects it to be interactive (checkboxes update preview in real-time)

**Q4: How to change the project**
- ⚠️ **Confusion**: "Wanted to click on the title name and change the project using a drop down menu (same way as changing the proposal)"
- **Alternative expectation**: "Otherwise, arrow in front of the name (<) to go back to the selection screen"
- **Risk**: "Currently, user may just close the window to try and reload the project"
- **Takeaway**: No clear affordance for changing projects - users expect dropdown or back button

**Q5: How to change from Proposal A to Proposal C**
- ✅ **Success**: "User selected proposal C as expected in the drop down menu"

**Success/Completion**: ⚠️ Completed with difficulty finding download location and confusion about project selection

**Key Takeaway**: Core proposal selection worked well, but download discoverability was poor and project switching mechanism was unclear. P03 expects interactive preview and better visual indicators.

---

### Task II: Refresh Proposal with New Changes

**Observation** - Refresh button location
- ✅ **Success**: "User would click on the refresh button that's currently available in the design to bring in the latest proposal"
- **Discoverability**: P03 found the refresh button as expected

**Q1: Was this the behavior you expected when clicking refresh?**
- ❌ **Expectation mismatch**: "Not particularly, as the IE would expect you shouldn't be able to change the Forma proposal after importing to Revit"
- **Use case identified**: "The button can be useful during iterative design process. I.E client asks the main building to split into two smaller buildings"
- ⚠️ **Confusion**: "Finding the refresh to be a little confusing"
- **Alternative expectation**: "However, as a user, the expectation is that clicking on Convert to Revit Objects should bring in the latest proposal"
- **Takeaway**: P03 didn't expect separate refresh - thought conversion should auto-pull latest

**Q2: How to remove Forma elements you don't want to see?**
- ✅ **Success**: "Unchecking the box"
- **Enhancement suggestion**: "Perhaps clicking on individual buildings to be able to exclude in the preview would be nice"

**Q3: What actions would you take next?**
- **Workflow suggestion**: "If a site has multiple buildings in Forma, Revit should give an option to load an individual building to be loaded in Revit"
- **Preview expectation**: "Users might expect changes in the preview to be real-time"

**Success/Completion**: ✅ Completed but with confusion about refresh timing and expectation that conversion should auto-update

**Key Takeaway**: Refresh functionality was discoverable, but P03 questioned why refresh is separate from conversion - expected "Convert to Revit Objects" to automatically pull latest changes. Also wants individual building selection.

---

### Task III: Convert Forma Elements to Revit Objects

**Observation** - Converting Buildings to Walls/Roofs/Floors
- ✅ **Success**: "User selected the correct drop down"

**Enhancement suggestion**
- **Request**: "Also, it would be nice to select the Revit families that exist during import process. (for example, external wall should belong to one family and floor would be another family)"
- **Qualifier**: "Not completely necessary to do so, because user can change it within Revit as well"

**Q2: Send Revit edits back to Forma for analysis**
- **Terminology feedback**: "Change the name of 'Load proposal' to 'Interoperability with Forma'"
- **Clarity feedback**: "'Update Proposal' should be more specific such as 'Sync proposals to Forma'"
- **Multi-view scenario**: "If there are multiple 3D views, be able to select which 3D view to send to Forma"

**Success/Completion**: ✅ Completed successfully with terminology improvement suggestions

**Key Takeaway**: Core conversion functionality worked, but terminology could be clearer and more specific about what actions are being performed.

---

## Concluding Remarks

**Overall feedback**:
- Quote: "With this flow, this is taking longer to import. (Send to Revit) on proposal would be a little clearer during the import process to the user if the user has many projects to know which project to import"
- **Takeaway**: P03 feels the new flow adds steps compared to a simpler "Send to Revit" button on proposals

---

## Key Quotes *(with timestamps for video clips)*

These quotes stood out as particularly insightful or representative:

1. **Task I** - P03: "Preferably to see a Revit Icon on the navigation bar or the analysis bar"
   - **Context**: Looking for where to download the add-in
   - **Why it matters**: Reveals expectation for clear Revit branding/iconography

2. **Task I** - P03: "Not understanding from the dialog screen to know for sure this is a preview screen"
   - **Context**: Looking at the Load Proposal preview
   - **Why it matters**: Preview state needs clearer labeling or visual differentiation

3. **Task I** - P03: "Checking or unchecking boxes should ideally change the preview"
   - **Context**: Interacting with element type checkboxes
   - **Why it matters**: Users expect real-time preview updates based on selections

4. **Task II** - P03: "Not particularly, as the IE would expect you shouldn't be able to change the Forma proposal after importing to Revit"
   - **Context**: Asked if refresh behavior matched expectations
   - **Why it matters**: Questions the need for separate refresh functionality

5. **Task II** - P03: "However, as a user, the expectation is that clicking on Convert to Revit Objects should bring in the latest proposal"
   - **Context**: Discussing refresh vs. convert behavior
   - **Why it matters**: Suggests combining refresh into conversion action

6. **Task III** - P03: "Change the name of 'Load proposal' to 'Interoperability with Forma'"
   - **Context**: Overall panel naming
   - **Why it matters**: Current name doesn't reflect bidirectional workflow

7. **Task III** - P03: "'Update Proposal' should be more specific such as 'Sync proposals to Forma'"
   - **Context**: Sending Revit objects back to Forma
   - **Why it matters**: Terminology should be clearer about sync action

8. **Concluding** - P03: "With this flow, this is taking longer to import"
   - **Context**: Overall impression of new workflow
   - **Why it matters**: Suggests new flow adds friction compared to simpler alternatives

---

## Pain Points Observed

| # | Pain Point | Evidence | Severity |
|---|------------|----------|----------|
| 1 | Add-in download location not discoverable | "Difficulty finding the icon to download... Preferably to see a Revit Icon on the navigation bar or the analysis bar" | 🟡 Medium |
| 2 | Preview screen not clearly labeled as preview | "Not understanding from the dialog screen to know for sure this is a preview screen" | 🟡 Medium |
| 3 | Preview not interactive/real-time | "Checking or unchecking boxes should ideally change the preview" and "Users might expect changes in the preview to be real-time" | 🟡 Medium |
| 4 | No clear way to change/switch projects | "Wanted to click on the title name and change the project using a drop down menu... Currently, user may just close the window to try and reload the project" | 🔴 High |
| 5 | Refresh vs. Convert timing unclear | "Not particularly... the expectation is that clicking on Convert to Revit Objects should bring in the latest proposal" | 🟡 Medium |
| 6 | Project list scalability concerns | "If there are folders in the hub, it would be logical to see the folder... as the list can get very long" | 🟢 Low |
| 7 | No visual indicator of linked proposals in Forma | "Some visual on Forma side beside the proposal imported to Revit would help remind users not to edit this proposal in Forma anymore" | 🟢 Low |
| 8 | Can't select individual buildings to import | "If a site has multiple buildings in Forma, Revit should give an option to load an individual building" | 🟢 Low |
| 9 | Can't select specific 3D view when sending back to Forma | "If there are multiple 3D views, be able to select which 3D view to send to Forma" | 🟢 Low |
| 10 | New workflow feels longer than simple "Send to Revit" | "With this flow, this is taking longer to import. (Send to Revit) on proposal would be clearer" | 🟡 Medium |

---

## Positive Moments / What Worked Well

| # | Positive Moment | Evidence | Why It Matters |
|---|----------------|----------|----------------|
| 1 | Logical presentation of workflow | "The presentation seems logical" | Validates overall flow structure |
| 2 | Liked preview concept | "Like the idea of the preview" | Core preview feature is valued |
| 3 | Icon consistency with Forma | "Great to have the same symbols associated with each icon in Forma" | Visual consistency helps learnability |
| 4 | Proposal dropdown worked as expected | "User selected proposal C as expected in the drop down menu" | Proposal switching is intuitive |
| 5 | Refresh button discoverable | "User would click on the refresh button that's currently available in the design" | Icon placement worked well |
| 6 | Visibility toggle via checkboxes clear | "Unchecking the box" to remove elements | Core interaction pattern understood |
| 7 | Conversion dropdown intuitive | "User selected the correct drop down" for converting Buildings | Element conversion UI works |

---

## Behavioral Observations

- P03 actively looked for Revit branding/iconography when searching for download location (expects visual consistency)
- P03 tried to interact with preview in real-time (expected immediate visual feedback from checkbox changes)
- P03 attempted to click on project title name expecting dropdown (applied learned pattern from proposal dropdown)
- P03 questioned the need for separate refresh action (prefers streamlined workflow)
- P03 provided numerous specific suggestions throughout session (indicates design thinking mindset)

---

## Facilitator Notes

### Technical Issues
- Figma prototype limitations: Real-time preview updates weren't functional, which may have contributed to confusion
- Demo constraints: Limited interaction paths may not have fully demonstrated intended behavior

### Session Flow
- ✅ Followed script - All three tasks completed
- P03 was very engaged and provided detailed feedback throughout

### Follow-Up Needed
- [ ] Improve add-in download discoverability - consider Revit icon/branding
- [ ] Make preview state more obvious - consider "Preview" label or visual treatment
- [ ] Implement real-time preview updates when toggling element types
- [ ] Add clear project switching mechanism (dropdown or back button)
- [ ] Consider combining refresh into "Convert to Revit Objects" action
- [ ] Explore search/folder organization for long project lists
- [ ] Consider visual indicator in Forma when proposal is linked to Revit
- [ ] Evaluate terminology: "Load Proposal" → "Interoperability with Forma", "Update Proposal" → "Sync to Forma"

---

## Quick Synthesis *(For Facilitator)*

1. **Core workflow logic validated** - P03 found the overall flow logical and successfully completed all tasks, confirming the basic interaction model works

2. **Discoverability and clarity issues** - Download location, preview state, and project switching mechanisms need better affordances and clearer labeling

3. **Expectations for real-time interaction** - P03 expected interactive preview, automatic updates on conversion, and more granular control (individual buildings, specific views) - suggests users want more responsive, detailed control

**Hypothesis Check**: Does this session support or refute our hypothesis?
- 🟡 **Partially Supports** - The workflow matches mental models in some ways (proposal selection, conversion options), but P03 questioned whether it's an improvement over simpler alternatives, noting it "takes longer to import"

---

## Post-Session Checklist

- [x] Session notes completed
- [x] Participant ID assigned (P03)
- [ ] Real name removed from all shared files (needs sanitization for sharing)
- [ ] Recording saved securely (not documented)
- [ ] Transcript exported (not documented)
- [x] Key quotes documented
- [x] Pain points flagged
- [ ] Research plan schedule updated
- [x] Quick synthesis completed

---

_Session notes template - Autodesk Research Assistant Agent. Remember to use participant IDs only for shared documents._
