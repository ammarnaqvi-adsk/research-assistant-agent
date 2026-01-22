# Session Notes: P02

**Project**: Forma Add-in for Revit Usability Testing

**Research Plan**: See `memory/research-plans/revit-addin-usability-research-plan.md`

**Participant ID**: P02 *(Monica Pereira Da Silva)*

**Date**: April 10, 2024

**Facilitator**: Tamira McCoy

**Notetaker**: Nicholas Ragonese

**Session Duration**: ~45-60 minutes

---

## ⚠️ Privacy Reminder

**USE PARTICIPANT IDs ONLY** - Never include real names, emails, or other PII in shared reports.

**This document may be shared** with product teams, stakeholders, and other researchers.

---

## Session Metadata

### Participant Profile *(Anonymized)*

- **ID**: P02
- **Role/Title**: Architect/Designer (specific role not documented)
- **Experience**: Has familiarity with Revit and Forma workflows
- **Product Usage**: Experienced with Forma add-in for Revit

### Session Info

- **Methodology**: Usability Testing (Figma Prototype Walkthrough)
- **Platform**: Remote with screen sharing
- **Recording**: Not documented in notes
- **Recording Consent**: Not documented in notes
- **CRA Signed**: Not documented in notes

---

## Warm-Up Summary

**Background**: P02 is an architect/designer with experience using both Forma and Revit. She has familiarity with existing Forma workflows and has used the massing section to load proposals in the past.

**Key Context**: P02 has prior experience with Forma-Revit interoperability, which provided useful comparison points between old and new workflows.

---

## Observations & Key Moments

### Task I: Download Add-in and Load Proposal

**Observation** - P02 found the extension and Revit add-in very easily
- ✅ **Success**: Located add-in download within Forma without difficulty

**Observation** - P02 found the load proposal button easily
- ✅ **Success**: Navigated to proposal loading functionality quickly

**Observation** - P02 understood the hub concept
- ⚠️ **Minor confusion**: Confused the project list for a proposal list initially
- 💡 **Note**: This might have been a verbal mistake as she understood proposal selection right away

**Observation** - P02 appreciated the improved workflow
- 💡 **Positive reaction**: "This is a much more intuitive flow rather than having to go to the massing section to load proposal"
- **Context**: Comparing new design to existing workflow

**Observation** - P02 immediately understood the concept of choosing Revit element type for each Forma element type
- ✅ **Success**: Mental model matched for element type mapping

**Observation** - P02 was slightly confused about "change project" terminology
- ⚠️ **Confusion point**: While in Revit, she assumed "change project" meant change the underlying Revit project, rather than change the Forma project being loaded into Revit
- **Resolution**: Once clarified it was about changing Forma project, she found the proposal dropdown easily
- **Note from notetaker**: Unclear how P02 would have navigated to change Forma project rather than proposal

**Success/Completion**: ✅ Completed with minor terminology confusion

**Key Takeaway**: P02 found the new workflow more intuitive than the existing massing-based approach, but terminology around "project" vs "proposal" needs clarification when working within Revit context.

---

### Task II: Refresh Proposal with New Changes

**Observation** - Refresh icon felt natural
- Quote: "When prompted to update the Forma proposal in Revit, the refresh icon felt natural to Monica"
- ✅ **Success**: Refresh functionality was discoverable and intuitive

**Observation** - P02 found it very natural to toggle visibility of different Forma element types
- ✅ **Success**: Visibility controls matched mental model

**Observation** - P02 understood the concept of "Convert to Revit Objects" as the starting point for editing
- 🟡 **Partial understanding**: P02 seemed to understand she could only use the Revit project once clicking "Convert to Revit Objects"
- ⚠️ **Confusion**: She did not immediately understand that the preview was itself not Revit elements
- **Behavior**: P02 seemed to want to interact with the elements in the preview scene
- **Note from notetaker**: This might be her tendency to click things she's familiar with, and if she had a live demo it might have been immediately clear based on UI feedback that preview elements have no interaction

**Observation** - Confusion about Forma element types
- ⚠️ **Confusion**: "The question of what the different Forma element types are was confusing for Monica. In particular 'Generic' was not a known concept for her"
- **Details**: The difference between "building" and "generic" wasn't as natural as the distinction between proposal buildings vs contextual buildings
- **Context**: That categorization would map more clearly to how she would want to convert them into Revit objects
- **Note**: Otherwise there was no other categorization she was uncomfortable with

**Observation** - Difficulty choosing which Revit type to convert buildings to
- ⚠️ **Difficulty**: The question of which Revit type to convert Forma Buildings to was not an easy choice
- **Note from notetaker**: This is likely related to not being clear what "buildings" she was supposed to think about converting

**Observation** - When refreshing load proposal after new elements were added in Forma
- ✅ **Success**: There was no confusion about which elements in the preview were new vs already imported into Revit

**Success/Completion**: ⚠️ Completed with confusion around preview vs. editable Revit objects, and Forma element type categorization

**Key Takeaway**: While refresh and visibility controls worked well, the distinction between preview mode and editable Revit objects was unclear, and Forma element type labels (especially "Generic") didn't match P02's mental model.

---

### Task III: Convert Forma Elements to Revit Objects

**Observation** - P02 wasn't clear on what she can do now with the new Revit objects
- ⚠️ **Limitation noted**: Given P02's familiarity, the notetaker assumes this is largely a limitation of the demo where she only had the option to click through pre-planned paths
- **Context**: She wasn't getting feedback from Revit UI when clicking things as she is used to

**Observation** - P02 was not clear on what would happen to Revit objects being sent back to Forma
- ⚠️ **Confusion**: Question around which elements will be interpreted - just ones in her view or all of them
- 💡 **Tooltip helped**: The tooltip provided some clarity
- **Mental model mismatch**: Using purely views was somewhat confusing
- Quote: "Monica clarified that potentially using the concept of template rather than a view since that is the more base concept, and then within that the visibility settings are set for what shows up in the view"
- **Details**: "In general it seems because she sets the visibility settings on the template it made more sense for her to filter based on template. The gap seems to be that the specification of 3D view is required for us, but for a Revit user that is just a specific view mode and their visibility toggling is more based on templates, which can sometimes be on 3D views"

**Success/Completion**: ⚠️ Completed with confusion around view vs template concept for sending back to Forma

**Key Takeaway**: The mental model for sending Revit objects back to Forma doesn't align with how P02 thinks about visibility settings - she expects to work with templates rather than views.

---

## Key Quotes *(with timestamps for video clips)*

These quotes stood out as particularly insightful or representative:

1. **Task I** - P02: "This is a much more intuitive flow rather than having to go to the massing section to load proposal"
   - **Context**: Comparing new workflow to existing approach
   - **Why it matters**: Validates that the new workflow is an improvement over current implementation

2. **Task II** - (Paraphrased): "In particular 'Generic' was not a known concept for her"
   - **Context**: Discussing Forma element type labels
   - **Why it matters**: Reveals terminology mismatch between system labels and user understanding

3. **Task III** - P02: "Monica clarified that potentially using the concept of template rather than a view since that is the more base concept"
   - **Context**: Discussing how to send Revit objects back to Forma
   - **Why it matters**: Shows fundamental mental model mismatch - users think in templates, system thinks in views

---

## Pain Points Observed

| # | Pain Point | Evidence | Severity |
|---|------------|----------|----------|
| 1 | "Generic" element type label unclear | "In particular 'Generic' was not a known concept for her. The difference between 'building' and 'generic' wasn't as natural as the distinction between proposal buildings vs contextual buildings" | 🟡 Medium |
| 2 | Preview vs. editable Revit objects unclear | "She did not immediately understand that the preview was itself not Revit elements. P02 seemed to want to interact with the elements in the preview scene" | 🟡 Medium |
| 3 | "Change project" terminology ambiguous in Revit context | "While in Revit she assumed 'change project' meant change the underlying Revit project, rather than change the Forma project being loaded" | 🟡 Medium |
| 4 | View vs. Template mental model mismatch | "Using purely views was somewhat confusing... because she sets visibility settings on the template it made more sense to filter based on template" | 🟡 Medium |
| 5 | Difficult to choose which Revit type for Buildings conversion | "The question of which Revit type to convert Forma Buildings to was not an easy choice" (related to Generic confusion) | 🟡 Medium |
| 6 | Unclear what happens when sending Revit objects back to Forma | "Her question was around which elements will be interpreted, especially if it is just ones in her view or all of them" | 🟢 Low |

---

## Positive Moments / What Worked Well

| # | Positive Moment | Evidence | Why It Matters |
|---|----------------|----------|----------------|
| 1 | New workflow more intuitive than existing | "This is a much more intuitive flow rather than having to go to the massing section to load proposal" | Validates core design improvement |
| 2 | Refresh functionality intuitive | "The refresh icon felt natural to Monica" | Confirms icon choice and placement work well |
| 3 | Visibility toggles natural | "P02 found it very natural to toggle visibility of different Forma element types in the preview" | Core functionality matches user expectations |
| 4 | Easy to find add-in and load proposal | "P02 found the extension and Revit add-in very easily... found the load proposal button easily" | Navigation and discoverability successful |
| 5 | Element type mapping concept clear | "P02 immediately understood the concept of choosing the Revit element type for each Forma element type" | Core workflow logic makes sense |
| 6 | Clear distinction between new/existing elements after refresh | "When refreshing load proposal after new elements were added in Forma, there was no confusion about which elements in the preview were new vs already imported" | Update workflow is clear |

---

## Behavioral Observations

- P02 showed tendency to try clicking on preview elements, expecting interaction (suggests strong existing Revit interaction patterns)
- P02 compared new workflow favorably to existing massing-based approach (indicates familiarity with pain points of current system)
- P02 had clear expectations about template-based visibility controls based on her Revit experience
- Initial confusion about project/proposal terminology was quickly resolved with clarification

---

## Other Notes from Session

**Load Proposal window size/docking**:
- P02 mentioned she would prefer if the Load Proposal window was able to be docked or smaller
- Notetaker thinks this may be related to the UI being not fully available in the demo
- Use case: She wanted to edit visibilities in the view template while keeping the Load Proposal window open

**Missing vegetation information**:
- P02 missed the vegetation hints available from a satellite view of the terrain
- This is not what you currently see in the Load Proposal preview

---

## Facilitator Notes

### Technical Issues
- Figma prototype limitations: Users couldn't interact with UI elements naturally, which may have impacted understanding of preview vs. editable objects
- Demo limitations: P02 could only click through pre-planned paths, limiting natural exploration

### Session Flow
- ✅ Followed script - All three tasks completed
- Tasks appeared to flow naturally

### Follow-Up Needed
- [ ] Clarify terminology: "Change project" vs "Change proposal" when working within Revit
- [ ] Investigate: How do experienced Revit users think about templates vs views for visibility control?
- [ ] Consider: Alternative labels for "Generic" Forma element type (or better explanation)
- [ ] Explore: How to make preview vs. editable state more obvious

---

## Quick Synthesis *(For Facilitator)*

1. **New workflow is an improvement** - P02 explicitly stated the new approach is more intuitive than the current massing-based workflow, validating the core design direction

2. **Terminology needs refinement** - Labels like "Generic" and "Change project" caused confusion due to Revit context. Consider user's existing mental models (templates vs views, proposal buildings vs contextual buildings)

3. **Preview state needs clearer affordances** - The distinction between preview mode and editable Revit objects wasn't immediately clear, though this may be partially due to Figma prototype limitations

**Hypothesis Check**: Does this session support or refute our hypothesis?
- ✅ **Supports** - P02 confirmed the new workflow better matches her mental model compared to the existing approach, though some terminology and concepts still need refinement

---

## Post-Session Checklist

- [x] Session notes completed
- [x] Participant ID assigned (P02)
- [ ] Real name removed from all shared files (needs sanitization for sharing)
- [ ] Recording saved securely (not documented)
- [ ] Transcript exported (not documented)
- [x] Key quotes documented
- [x] Pain points flagged
- [ ] Research plan schedule updated
- [x] Quick synthesis completed

---

_Session notes template - Autodesk Research Assistant Agent. Remember to use participant IDs only for shared documents._
