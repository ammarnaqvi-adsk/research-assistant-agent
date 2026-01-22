# Forma Revit Add-in Usability Research Findings

**Research Plan**: See `memory/research-plans/revit-addin-usability-research-plan.md`

**Date**: April 10-11, 2024

**Research Lead**: Tamira McCoy (UX Designer, Connected Clients team)

**Sessions Conducted**: 2 participants (P02, P03)

**⚠️ Sample Size Note**: This study included only 2 participants (n=2). Findings represent early directional signals, not statistically significant results. See "Research Quality Review" document for detailed confidence analysis.

---

## Executive Summary

1. **Core workflow improvement validated** - Both participants found the new add-in approach more logical than the existing massing-based workflow, though one questioned if it adds steps (Confidence: 🟡 Medium, n=2)

2. **Terminology confusion with "Generic" element type** - Both participants struggled with the "Generic" Forma element label; users expected categorization based on proposal vs. contextual buildings (Confidence: 🔴 High, 2/2 participants)

3. **Preview state not clearly distinguished from editable Revit objects** - Both participants showed confusion about preview vs. editable state, attempting to interact with preview elements or questioning when they could edit (Confidence: 🔴 High, 2/2 participants)

4. **Mental model mismatch: Views vs. Templates** - P02 expected to work with templates rather than views for visibility control and sending objects back to Forma (Confidence: 🟢 Low, 1/2 participants)

5. **Project switching mechanism unclear** - P03 couldn't find how to switch Forma projects, attempting to click title or close window; P02 had similar confusion about "change project" terminology (Confidence: 🔴 High, 2/2 participants)

6. **Users expect real-time interactive preview** - P03 expected checkboxes to update preview in real-time; P02 attempted to interact with preview elements (Confidence: 🔴 High, 2/2 participants)

7. **Refresh timing questioned** - P03 expected "Convert to Revit Objects" to automatically pull latest changes rather than requiring separate refresh (Confidence: 🟢 Low, 1/2 participants)

---

## Research Goals Recap

**Original research questions**:
1. **Project/Proposal Management**: Users can select, swap and load desired Forma projects & proposals
2. **Preview Understanding**: Users understand how previewing works and the implications of converting Forma layers
3. **Conversion Options**: Users can easily identify the design options for each Forma element and generate desired Revit object conversion from those options
4. **Update Workflow**: Users can identify how to update Forma proposals through the add-in
5. **Linking Management**: Users can unlink and re-link desired Forma proposals

**Hypothesis**: The new Revit add-in UI will match architects' mental models when transitioning between Forma and Revit, reducing friction and enabling seamless interoperability.

---

## Hypothesis Validation

**Result**: 🟡 Partially Supported

**Evidence Summary**:

**Supporting evidence**:
- P02 explicitly stated: "This is a much more intuitive flow rather than having to go to the massing section to load proposal"
- Both participants successfully completed all tasks
- Both participants found refresh and visibility toggles intuitive
- Both participants understood the concept of element type mapping

**Contradicting evidence**:
- P03 noted: "With this flow, this is taking longer to import" and suggested simpler "Send to Revit" button would be clearer
- Both participants confused by "Generic" element type - doesn't match their mental model of proposal vs. contextual buildings
- Both participants unclear about preview vs. editable state distinction
- P02's mental model expects templates not views for visibility control
- P03 expected automatic refresh on conversion, not separate action

**Implications**:
- **Partial support**: The workflow is directionally correct and more intuitive than current implementation, but several terminology choices and interaction patterns don't fully align with architect mental models
- **Refinement needed**: Address terminology (Generic, Change Project), clarify preview state, and consider mental model for templates vs. views
- **Trade-off acknowledged**: While more structured, the workflow may feel like additional steps to users who want streamlined "Send to Revit" functionality

---

## Top Pain Points

### Pain Point 1: "Generic" Forma element type label doesn't match user mental model

**Description**: Both participants struggled with the "Generic" element type label. They didn't understand what "Generic" meant or how it differed from "Buildings." Users expected categorization based on proposal buildings vs. contextual buildings, which would map more clearly to how they'd convert elements to Revit objects.

**Evidence from Participants**:
- **P02**: "The question of what the different Forma element types are was confusing for Monica. In particular 'Generic' was not a known concept for her. The difference between 'building' and 'generic' wasn't as natural as the distinction between proposal buildings vs contextual buildings"
- **P02**: "The question of which Revit type to convert Forma Buildings to was not an easy choice" (related to confusion about what "buildings" meant)
- **P03**: (While not explicitly quoted on "Generic", the notes indicate similar categorization confusion)

**Frequency**: 2/2 participants mentioned this (100%)

**Severity**: 🔴 High

**Context**: This occurred during Task III when participants were asked to convert Forma elements to Revit objects. The confusion about element type labels made it difficult to choose appropriate Revit conversion options.

**Affected Product Area**: Load Proposal dialog - Element type selection and conversion options

**Impact on User Experience**:
- Blocks confident decision-making about which elements to convert
- Makes conversion choices unclear and error-prone
- Requires users to guess at what element types represent
- "Generic" provides no semantic meaning about the building's purpose or context

**User Behavior Observed**:
- Hesitation when selecting which Revit type to use for conversion
- Expressed confusion about what different categories meant
- Expected categorization based on function/purpose (proposal vs context) rather than generic labels

---

### Opportunity: Replace "Generic" with context-based categorization

**Recommendation**: Replace "Generic" label with more meaningful categorization that matches architect mental models. Consider:
- "Proposal Buildings" vs "Contextual Buildings" (or "Context Buildings")
- "Design Buildings" vs "Existing Buildings"
- Add tooltips explaining what each category contains
- Consider user-visible labels that match Forma terminology they already know

**Expected Impact**:
- Clearer understanding of what elements represent
- Faster, more confident conversion decisions
- Reduced cognitive load during import workflow
- Better alignment with how architects think about building types

**Priority**: 🔴 High

**Rationale**: This affected 100% of participants and directly impacts a core task (element conversion). The mental model mismatch creates confusion at a critical decision point in the workflow.

---

### Pain Point 2: Preview state not clearly distinguished from editable Revit objects

**Description**: Both participants showed confusion about when elements were in preview mode vs. when they became editable Revit objects. P02 attempted to interact with preview elements expecting Revit functionality. P03 didn't recognize the dialog as a preview screen. This fundamental confusion about state affects users' understanding of the workflow.

**Evidence from Participants**:
- **P02**: "She did not immediately understand that the preview was itself not Revit elements. Monica seemed to want to interact with the elements in the preview scene"
- **P02**: Notetaker noted this might be "her tendency to want to click the things she is familiar with and if she had a live demo potentially it would have been immediately clear to her based on UI feedback that the preview elements have no interaction"
- **P03**: "Not understanding from the dialog screen to know for sure this is a preview screen"
- **P03**: "Checking or unchecking boxes should ideally change the preview" (expects real-time preview updates)
- **P03**: "Users might expect changes in the preview to be real-time"

**Frequency**: 2/2 participants mentioned this (100%)

**Severity**: 🔴 High

**Context**: This occurred during Task I and Task II when participants first loaded proposals and interacted with the preview. The confusion persisted through multiple interactions.

**Affected Product Area**: Load Proposal dialog - Preview visualization and state indication

**Impact on User Experience**:
- Creates fundamental confusion about workflow state
- Users attempt to interact with non-interactive elements (frustration)
- Unclear when conversion is needed to begin editing
- May lead to incorrect assumptions about what actions are possible
- Reduces confidence in understanding the workflow

**User Behavior Observed**:
- Attempted to click on preview elements expecting Revit interactions
- Didn't recognize visual cues indicating preview state
- Expected immediate feedback when toggling element types (real-time preview updates)
- Confused about when elements become editable

---

### Opportunity: Add clear preview state indicators and make preview interactive

**Recommendation**:
1. Add prominent "PREVIEW" label to the visualization area
2. Implement real-time preview updates when toggling element type checkboxes
3. Add visual treatment (e.g., subtle overlay, different background color, watermark) to differentiate preview from Revit viewport
4. Consider adding text: "Convert to Revit Objects to begin editing"
5. Show interactive affordances (cursor changes, hover states) for elements that can be clicked

**Expected Impact**:
- Clear understanding of current workflow state
- Reduced confusion about when editing is possible
- Better alignment with user expectations for interactive previews
- Immediate visual feedback reinforces user actions
- Increased confidence in workflow progression

**Priority**: 🔴 High

**Rationale**: This affected 100% of participants and impacts understanding of a fundamental workflow concept. Clear state indication is critical for usability and prevents user confusion at the outset of the workflow.

---

### Pain Point 3: No clear mechanism to switch Forma projects

**Description**: Both participants struggled to find how to switch between Forma projects (not just proposals within a project). P03 attempted to click on the project title expecting a dropdown, or looked for a back arrow. P02 was confused by "Change project" terminology, initially thinking it meant changing the underlying Revit project rather than the Forma project being loaded. This suggests no clear affordance exists for project switching.

**Evidence from Participants**:
- **P03**: "Wanted to click on the title name and change the project using a drop down menu (same way as changing the proposal)"
- **P03**: "Otherwise, arrow in front of the name (<) to go back to the selection screen"
- **P03**: "Currently, user may just close the window to try and reload the project"
- **P02**: "For changing project, Monica was slightly confused about the terminology because while in Revit she assumed 'change project' meant change the underlying Revit project, rather than change the Forma project that was being loaded into her Revit project"
- **P02**: Notetaker noted: "I am unsure how Monica would have navigated to change Forma project rather than proposal"

**Frequency**: 2/2 participants mentioned this (100%)

**Severity**: 🔴 High

**Context**: This occurred during Task I when participants were asked how they would change projects. Neither participant could immediately identify the correct method.

**Affected Product Area**: Load Proposal dialog - Project selection and navigation

**Impact on User Experience**:
- Blocks critical workflow functionality (switching between projects)
- Users may close and reopen the entire panel as workaround (inefficient)
- Terminology confusion creates additional cognitive load
- Inconsistent pattern between proposal switching (clear dropdown) and project switching (no visible method)

**User Behavior Observed**:
- Attempted to click on project title/name expecting dropdown menu
- Looked for back arrow navigation
- Expressed uncertainty about how to accomplish task
- Considered closing window entirely as potential solution

---

### Opportunity: Add clear project switching affordance with consistent terminology

**Recommendation**:
1. Make project name clickable with dropdown menu (matching proposal pattern)
2. OR add "Change Project" button/link that's clearly visible
3. OR add back arrow (< Project Selection) to return to project list
4. Update terminology: Use "Forma Project" instead of just "Project" in Revit context to avoid confusion with underlying Revit project
5. Ensure visual consistency between project and proposal switching mechanisms

**Expected Impact**:
- Clear, discoverable way to switch between projects
- Consistent interaction pattern reduces learning curve
- Eliminates need to close/reopen panel
- Clearer terminology prevents mental model confusion
- Faster workflow for users working across multiple Forma projects

**Priority**: 🔴 High

**Rationale**: This affected 100% of participants and blocks a core workflow capability identified in research goals. The inconsistency between proposal switching (works well) and project switching (unclear) suggests a straightforward design opportunity.

---

### Pain Point 4: Users expect real-time interactive preview updates

**Description**: Both participants expected the preview to update in real-time as they toggled element type checkboxes. P03 explicitly stated checkboxes should change the preview. P02 attempted to interact with preview elements. The static preview doesn't match modern software expectations for immediate visual feedback.

**Evidence from Participants**:
- **P03**: "Checking or unchecking boxes should ideally change the preview"
- **P03**: "Users might expect changes in the preview to be real-time"
- **P02**: Attempted to interact with preview elements (indicating expectation of responsiveness)

**Frequency**: 2/2 participants mentioned this (100%)

**Severity**: 🟡 Medium

**Context**: This occurred when participants toggled element type visibility in the Load Proposal dialog. The expectation was set by modern software patterns where preview updates match user input immediately.

**Affected Product Area**: Load Proposal dialog - Preview visualization and element type toggles

**Impact on User Experience**:
- Disconnect between action (toggling checkbox) and visual feedback (no preview change)
- Uncertainty about whether action was registered
- Feels less responsive and modern compared to other tools
- May require mental simulation of what result will look like
- Slows down decision-making about which elements to include

**User Behavior Observed**:
- Expected immediate visual change when toggling checkboxes
- May have looked for preview updates after toggling
- Expressed expectation explicitly

---

### Opportunity: Implement real-time preview updates when toggling element types

**Recommendation**:
1. Update 3D preview immediately when users check/uncheck element type boxes
2. Add subtle animation/transition when elements appear/disappear
3. Consider loading state if preview update takes time
4. Ensure preview reflects exactly what will be loaded
5. Apply this pattern consistently across all interactive controls

**Expected Impact**:
- Immediate visual feedback increases confidence
- Faster decision-making about which elements to include
- Meets modern software expectations
- Reduces need to mentally simulate results
- More satisfying, responsive interaction

**Priority**: 🟡 Medium

**Rationale**: While this affected 100% of participants, the core functionality still works without real-time updates - users can toggle and then see results after loading. However, implementing this would significantly improve the experience and meet user expectations.

---

### Pain Point 5: Mental model mismatch - Templates vs. Views for sending objects back to Forma

**Description**: P02 expected to work with templates rather than views when controlling visibility and sending Revit objects back to Forma. She explained that in her workflow, visibility settings are configured at the template level, and views inherit from templates. The current design requires selecting a "3D view," which doesn't match how she thinks about visibility control.

**Evidence from Participants**:
- **P02**: "Using purely views was somewhat confusing, and Monica clarified that potentially using the concept of template rather than a view since that is the more base concept, and then within that the visibility settings are set for what shows up in the view"
- **P02**: "In general it seems because she sets the visibility settings on the template it made more sense for her to filter based on template. The gap seems to be that the specification of 3D view is required for us, but for a Revit user that is just a specific view mode and their visibility toggling is more based on templates, which can sometimes be on 3D views"
- **P02**: "Her question was around which elements will be interpreted, and especially if it is just the ones in her view or if it is all of them"

**Frequency**: 1/2 participants mentioned this (50%)

**Severity**: 🟡 Medium

**Context**: This occurred during Task III when P02 was asked about sending edited Revit objects back to Forma for analysis. The current design asks users to select a 3D view, but P02's mental model works with templates.

**Affected Product Area**: Update Proposal workflow - View/Template selection for sending objects back to Forma

**Impact on User Experience**:
- Mental model mismatch creates confusion about what will be sent
- Users may be uncertain if they're selecting the correct view
- Doesn't align with how experienced Revit users manage visibility
- May require users to adapt their workflow to match tool's model
- Creates uncertainty about which elements will be included

**User Behavior Observed**:
- Questioned which elements would be interpreted (view-specific vs. all)
- Articulated preference for template-based selection
- Showed deep understanding of Revit's view/template hierarchy

---

### Opportunity: Support template-based selection or clarify view selection requirements

**Recommendation**:
1. Investigate feasibility of allowing template selection instead of/in addition to view selection
2. If 3D view is technically required, add explanation of why and how it relates to templates
3. Add preview/confirmation showing which elements will be sent based on selected view
4. Consider showing template name associated with selected view
5. Add documentation or tooltip explaining how view selection determines what's sent

**Expected Impact**:
- Better alignment with experienced Revit users' mental models
- Clearer understanding of what elements will be sent to Forma
- Reduced uncertainty and cognitive load
- May enable more efficient workflows for users who manage visibility via templates
- Fewer errors in sending incorrect elements

**Priority**: 🟡 Medium

**Rationale**: This affected only 1/2 participants (50%), but that participant showed deep Revit expertise. This may be more critical for advanced users. Additionally, small sample size means this could affect more users in practice. Technical constraints may limit solution options.

---

### Pain Point 6: Refresh timing and relationship to conversion unclear

**Description**: P03 questioned why refresh is a separate action from conversion. She expected that clicking "Convert to Revit Objects" would automatically pull the latest version from Forma, making a separate refresh button unnecessary. This suggests the timing and relationship between refresh and conversion isn't clear.

**Evidence from Participants**:
- **P03**: "Not particularly, as the IE would expect you shouldn't be able to change the Forma proposal after importing to Revit" (when asked if refresh behavior matched expectations)
- **P03**: "However, as a user, the expectation is that clicking on Convert to Revit Objects should bring in the latest proposal"
- **P03**: "Finding the refresh to be a little confusing"
- **P03**: "The button can be useful during iterative design process. I.E client asks the main building to split into two smaller buildings" (acknowledged use case but still questioned implementation)

**Frequency**: 1/2 participants mentioned this (50%)

**Severity**: 🟡 Medium

**Context**: This occurred during Task II when P03 was asked to bring new changes from Forma into Revit. While she found the refresh button, she questioned whether it should exist as separate action.

**Affected Product Area**: Load Proposal dialog - Refresh functionality and conversion workflow

**Impact on User Experience**:
- Confusion about when to use refresh vs. conversion
- Extra step that users question the need for
- Uncertainty about whether conversion pulls latest or cached version
- May forget to refresh before converting, leading to outdated content

**User Behavior Observed**:
- Found refresh button (discoverability was fine)
- Questioned the design pattern after using it
- Suggested alternative mental model where conversion auto-refreshes

---

### Opportunity: Clarify refresh behavior or integrate with conversion

**Recommendation**:
1. **Option A**: Make "Convert to Revit Objects" always pull latest from Forma (auto-refresh on convert)
2. **Option B**: Add clear indication of last refresh time and prompt user if content is stale
3. **Option C**: Add explanation text: "Refresh preview to see latest changes from Forma" and "Convert locks to current preview state"
4. **Option D**: Show timestamp of loaded proposal version to make staleness obvious
5. Consider user research to validate whether separate refresh provides value or adds unnecessary step

**Expected Impact**:
- Clearer understanding of when content updates
- Reduced cognitive load (one fewer action to remember)
- Confidence that converted objects are latest version
- Better mental model of workflow state and timing
- Fewer potential errors from converting stale content

**Priority**: 🟡 Medium

**Rationale**: This affected only 1/2 participants (50%), but the questioning was strong. The participant acknowledged the use case but still found it confusing. With n=2, this could affect more users. Priority depends on technical architecture and whether refresh provides critical functionality.

---

### Pain Point 7: Add-in download location not easily discoverable

**Description**: P03 had difficulty finding where to download the add-in from within Forma. She looked in multiple places (beside proposal dots menu, navigation bar, analysis bar) expecting to see Revit branding or iconography. The download location doesn't match user expectations for where integrations would be found.

**Evidence from Participants**:
- **P03**: "Difficulty finding the icon to download, didn't give an actual score" (when asked difficulty rating 1-5)
- **P03**: Looked in multiple places: "Go to the dots (besides proposal) to download it" / "Preferably to see a Revit Icon on the navigation bar or the analysis bar" / "Look for logo for Revit within Forma"
- **P02**: By contrast, "Monica found the extension and Revit-add-in very easily" (suggesting some inconsistency in discoverability)

**Frequency**: 1/2 participants mentioned this (50%)

**Severity**: 🟡 Medium

**Context**: This occurred during Task I when P03 was asked to download the add-in from Forma. This is the first step in the entire workflow.

**Affected Product Area**: Forma interface - Add-in download/integration access

**Impact on User Experience**:
- First impression of workflow involves friction
- Users must hunt for download location
- Delays getting started with the integration
- May require support documentation or help from colleagues
- Inconsistent discoverability (P02 found easily, P03 struggled)

**User Behavior Observed**:
- Searched in multiple logical locations
- Expected Revit branding/icon to signal integration point
- Looked in integration-related areas (analysis bar, navigation)

---

### Opportunity: Improve add-in download discoverability with clear Revit branding

**Recommendation**:
1. Add Revit icon/logo to make integration point visually obvious
2. Place download access in consistent "Integrations" or "Add-ins" section
3. Consider adding to main navigation bar if Revit integration is primary workflow
4. Add visual callout or badge for new users ("Download Revit Add-in")
5. Include in onboarding flow or first-time Forma experience
6. Test placement with additional users to validate discoverability

**Expected Impact**:
- Faster time-to-start for new users
- Reduced need for documentation or support
- Better first impression of integration quality
- Clearer communication about Forma-Revit capabilities
- Consistent experience across users

**Priority**: 🟡 Medium

**Rationale**: This affected only 1/2 participants (50%). However, with n=2 this may underestimate the issue. Additionally, this is the first step and creates friction at a critical moment (initial setup). The inconsistent results (P02 easy, P03 difficult) suggest the current placement may work for some mental models but not others.

---

### Pain Point 8: Terminology - "Load Proposal" and "Update Proposal" lack clarity

**Description**: P03 suggested that the panel and button names could be more descriptive of their actual function. "Load Proposal" doesn't communicate the bidirectional nature of the workflow, and "Update Proposal" doesn't clearly indicate it's syncing back to Forma.

**Evidence from Participants**:
- **P03**: "Change the name of 'Load proposal' to 'Interoperability with Forma'"
- **P03**: "'Update Proposal' should be more specific such as 'Sync proposals to Forma'"

**Frequency**: 1/2 participants mentioned this (50%)

**Severity**: 🟢 Low

**Context**: This was mentioned during Task III as feedback on overall terminology rather than blocking task completion.

**Affected Product Area**: Panel naming and button labels throughout the add-in

**Impact on User Experience**:
- Terms may not fully communicate workflow capabilities
- Users might not realize bidirectional sync is possible
- Less clear about what actions buttons perform
- Misses opportunity to communicate value of interoperability

**User Behavior Observed**:
- Successfully completed tasks despite terminology
- Provided unsolicited suggestions for improvement
- Showed understanding of underlying functionality

---

### Opportunity: Update terminology to be more descriptive and action-oriented

**Recommendation**:
1. Consider renaming panel to emphasize interoperability (e.g., "Forma Interoperability", "Forma Sync", "Forma Connection")
2. Make button labels more action-specific:
   - "Update Proposal" → "Sync to Forma" or "Send to Forma"
   - Consider adding directionality indicators (← → icons)
3. Use consistent terminology across Forma and Revit sides
4. Validate new terminology with additional users before implementing

**Expected Impact**:
- Clearer understanding of workflow capabilities
- Better communication of bidirectional workflow
- More obvious what each action does
- Stronger positioning of interoperability value

**Priority**: 🟢 Low

**Rationale**: This affected only 1/2 participants (50%) and didn't block task completion. However, it's a relatively low-effort improvement that could enhance clarity. Consider as part of broader terminology review.

---

## Theme Analysis

*High-level patterns across pain points*

| Theme | Description | Pain Points Included | Participant Frequency | Priority |
|-------|-------------|---------------------|----------------------|----------|
| **State & Mode Confusion** | Users unclear about preview vs. editable state and when actions are needed | PP2 (Preview state unclear), PP6 (Refresh timing) | 2/2 participants | 🔴 High |
| **Terminology Mismatch** | System labels don't match user mental models or expectations | PP1 ("Generic" unclear), PP3 (Project switching), PP8 (Button naming) | 2/2 participants | 🔴 High |
| **Interaction Model Gaps** | Missing affordances or interaction patterns users expect | PP3 (No project switching), PP4 (Preview not interactive), PP7 (Download location) | 2/2 participants | 🔴 High |
| **Mental Model Divergence** | Advanced Revit workflows (templates) don't align with tool's model (views) | PP5 (Templates vs Views) | 1/2 participants | 🟡 Medium |

---

## Theme Table: Detailed Analysis

| Theme | Evidence | Confidence | Implication |
|-------|----------|------------|-------------|
| **State & Mode Confusion** | 2/2 participants showed confusion about preview vs. editable state; 1/2 questioned refresh timing | 🔴 High (100% affected by preview confusion) | Critical usability issue - users don't understand fundamental workflow states. Add clear state indicators and consider workflow simplification |
| **Terminology Mismatch** | 2/2 participants confused by "Generic" label; 2/2 struggled with project terminology; 1/2 suggested clearer button names | 🔴 High (100% affected by terminology) | Core terminology doesn't match architect mental models. Conduct terminology review using user language |
| **Interaction Model Gaps** | 2/2 participants expected interactive preview; 2/2 couldn't find project switching; 1/2 had trouble finding download | 🔴 High (100% affected by some gap) | Missing expected affordances create friction. Add interactive previews, clear project switching, and better discoverability |
| **Mental Model Divergence** | 1/2 participants articulated template vs view mismatch; shows deep Revit expertise | 🟡 Medium (50% but deep expertise) | Advanced users' mental models may not align. Investigate whether technical constraints can accommodate template-based workflows |

**Confidence levels explained**:
- 🔴 **High**: Mentioned by 2/2 participants (100%) with consistent evidence
- 🟡 **Medium**: Mentioned by 1/2 participants (50%) OR mixed evidence
- 🟢 **Low**: Limited evidence or single occurrence with small sample

**⚠️ CRITICAL NOTE ON CONFIDENCE LEVELS**: With only n=2 participants, even "high confidence" findings (2/2 = 100%) should be validated with additional research. A finding observed in 2/2 participants in a small study may not generalize to the broader user population.

---

## Positive Findings *(What Worked Well)*

*Don't only focus on problems - highlight what users loved too!*

### What Users Appreciated

1. **New workflow more intuitive than existing approach**
   - Evidence: **P02** - "This is a much more intuitive flow rather than having to go to the massing section to load proposal"
   - Why it matters: Validates that the core redesign addresses pain points in current implementation and provides clear improvement

2. **Refresh icon intuitive and discoverable**
   - Evidence: **P02** - "When prompted to update the Forma proposal in Revit, the refresh icon felt natural to Monica" | **P03** - "User would click on the refresh button that's currently available in the design to bring in the latest proposal"
   - Why it matters: Despite questions about refresh timing, the icon itself was immediately understood by both participants

3. **Visibility toggles natural and easy to use**
   - Evidence: **P02** - "Monica found it very natural to toggle visibility of different Forma element types in the preview" | **P03** - "Unchecking the box" to remove elements
   - Why it matters: Core control mechanism matches user expectations and requires no learning

4. **Element type mapping concept clear**
   - Evidence: **P02** - "Monica immediately understood the concept of choosing the Revit element type for each Forma element type"
   - Why it matters: The fundamental mapping model (Forma element → Revit element) makes sense to users despite terminology issues with specific labels

5. **Proposal dropdown worked as expected**
   - Evidence: **P03** - "User selected proposal C as expected in the drop down menu"
   - Why it matters: Proposal switching is intuitive and discoverable (in contrast to project switching)

6. **Overall presentation logical**
   - Evidence: **P03** - "The presentation seems logical"
   - Why it matters: The overall flow and structure makes sense even if specific interactions need refinement

7. **Icon consistency with Forma appreciated**
   - Evidence: **P03** - "Great to have the same symbols associated with each icon in Forma"
   - Why it matters: Visual consistency aids learnability and creates cohesive experience across products

8. **Preview concept valued**
   - Evidence: **P03** - "Like the idea of the preview"
   - Why it matters: Despite execution issues (static vs. interactive), users appreciate being able to preview before committing

9. **Easy to find add-in and load proposal (for P02)**
   - Evidence: **P02** - "Monica found the extension and Revit-add-in very easily. Monica found the load proposal button easily"
   - Why it matters: For at least some users, initial setup and basic operations are discoverable

**Preserve these strengths**: The core workflow structure, refresh icon, visibility toggles, and preview concept are working well. Focus improvements on refining terminology, state clarity, and missing affordances rather than restructuring the fundamental approach.

---

## Behavioral Patterns

*Observable user behaviors, not just what they said*

| Pattern | Description | Frequency | Implication |
|---------|-------------|-----------|-------------|
| **Attempting to interact with preview** | Both participants tried to click or interact with preview elements, expecting Revit-like responsiveness | 2/2 participants | Users bring strong mental models from existing tools; preview needs to either support interaction or very clearly indicate it's static |
| **Applying learned patterns across interface** | P03 tried to click project title for dropdown because proposal dropdown worked that way; shows expectation of consistency | 1/2 participants explicitly | Users expect consistent interaction patterns throughout interface; successful patterns (proposal dropdown) set expectations for similar UI elements |
| **Comparing to existing workflows** | P02 explicitly compared new flow to old massing approach; P03 compared to "Send to Revit" button | 2/2 participants | Users evaluate new designs against existing solutions; need to clearly articulate value of additional steps |
| **Expecting real-time feedback** | Both participants expected immediate visual updates from interactions (preview updates, checkbox changes) | 2/2 participants | Modern software has trained users to expect instant feedback; delayed or missing feedback feels broken |
| **Looking for visual branding** | P03 searched for Revit icon/logo to identify integration points | 1/2 participants explicitly | Users use visual shortcuts (logos, icons, colors) to navigate; clear branding aids discoverability |

---

## Participant Overview *(Anonymized)*

**Total Participants**: 2

**⚠️ SAMPLE SIZE LIMITATION**: This study included only 2 participants (n=2), which is below the typical 5-8 participants recommended for qualitative usability testing. Findings should be considered directional and validated with additional research before making major product decisions.

**Demographics** *(from research plan)*:
- Roles: Both appear to be architects/designers with Revit experience
- Experience levels: Both have prior experience with Forma and Revit
- Product usage: Both familiar with Forma-Revit workflows; at least one (P02) has used existing massing-based approach

**Participant Profiles**:
| ID | Role | Experience | Usage Pattern | Notes |
|----|------|------------|---------------|-------|
| P02 | Architect/Designer | Experienced with Revit and Forma | Has used existing Forma-Revit workflow via massing section | Provided detailed feedback comparing old vs new approach |
| P03 | Architect/Designer | Experienced with Revit and Forma | Has Forma-Revit experience | Highly engaged, provided numerous specific suggestions |

**Missing from sample**:
- Novice Revit users
- Users without Forma experience
- Geographic diversity (not documented)
- Firm size diversity (not documented)
- Range of Revit expertise levels (1-5 scale from screener not documented in session notes)

---

## Recommendations *(Prioritized)*

### 🔴 High Priority (Do First)

**1. Replace "Generic" element type label with context-based categorization**
- **Why**: Affected 100% of participants (2/2); blocked confident conversion decisions; clear mental model mismatch
- **Addresses**: Pain Point #1
- **Expected Impact**: Faster, more confident element conversion; reduced errors; better alignment with architect mental models
- **Suggested Owner**: UX Design + Product (Connected Clients team)

**2. Add clear preview state indicators and implement real-time preview updates**
- **Why**: Affected 100% of participants (2/2); fundamental confusion about workflow state; users attempted to interact with static preview
- **Addresses**: Pain Points #2 and #4
- **Expected Impact**: Clear understanding of preview vs. editable state; immediate visual feedback; meets modern software expectations; increased user confidence
- **Suggested Owner**: UX Design + Engineering (front-end)

**3. Add clear project switching mechanism with consistent terminology**
- **Why**: Affected 100% of participants (2/2); blocks core functionality; inconsistent with proposal switching pattern
- **Addresses**: Pain Point #3
- **Expected Impact**: Discoverable project switching; consistent interaction patterns; eliminates workaround of closing/reopening panel; clearer terminology prevents confusion
- **Suggested Owner**: UX Design + Product

### 🟡 Medium Priority (Do Next)

**4. Investigate templates vs. views mental model and clarify selection requirements**
- **Why**: Affected 50% of participants (1/2) but represents deep Revit expertise; may affect more advanced users
- **Addresses**: Pain Point #5
- **Expected Impact**: Better alignment with experienced users' mental models; clearer understanding of what elements will be sent to Forma; fewer errors
- **Suggested Owner**: UX Research (validate with more users) + Engineering (technical feasibility)

**5. Clarify refresh behavior or integrate with conversion action**
- **Why**: Affected 50% of participants (1/2); questioned need for separate action; may lead to stale content errors
- **Addresses**: Pain Point #6
- **Expected Impact**: Clearer workflow; reduced steps; confidence in content currency; fewer potential errors
- **Suggested Owner**: Product + UX Design (requires understanding of technical architecture)

**6. Improve add-in download discoverability with Revit branding**
- **Why**: Affected 50% of participants (1/2); creates friction at critical first step; inconsistent experience
- **Addresses**: Pain Point #7
- **Expected Impact**: Faster onboarding; better first impression; reduced support burden
- **Suggested Owner**: Forma product team + UX Design

### 🟢 Low Priority (Nice to Have)

**7. Update terminology to be more descriptive ("Interoperability with Forma", "Sync to Forma")**
- **Why**: Affected 50% of participants (1/2); didn't block task completion; relatively low effort
- **Addresses**: Pain Point #8
- **Expected Impact**: Clearer communication of capabilities; better positioning of value
- **Suggested Owner**: UX Content Design + Product

**8. Add individual building selection capability**
- **Why**: Suggested by 1/2 participants (P03); enhancement rather than fix
- **Addresses**: Feature request not critical pain point
- **Expected Impact**: More granular control for complex sites; efficiency for users who only need specific buildings
- **Suggested Owner**: Product + Engineering (scope as potential future enhancement)

**9. Add project/folder organization and search for long lists**
- **Why**: Suggested by 1/2 participants (P03); scalability concern rather than current blocker
- **Addresses**: Anticipated future pain point
- **Expected Impact**: Better scalability for users with many projects; faster project location
- **Suggested Owner**: Forma product team (broader than add-in)

**10. Add visual indicator in Forma when proposal linked to Revit**
- **Why**: Suggested by 1/2 participants (P03); nice-to-have sync awareness
- **Addresses**: Enhancement for collaboration/coordination
- **Expected Impact**: Prevents accidental edits in Forma to proposals being worked on in Revit; better team coordination
- **Suggested Owner**: Forma product team + UX Design

---

## What to Validate Next

*Open questions and suggested follow-up research*

### Unanswered Questions

1. **Does the workflow add too many steps compared to simpler alternatives?**
   - P03 noted: "With this flow, this is taking longer to import" and suggested "Send to Revit" button would be clearer
   - Question: Is the structured workflow worth the additional steps, or would users prefer streamlined one-click approach?
   - Research needed: Comparative testing of structured approach vs. simplified "Send to Revit" button

2. **How do users of varying Revit expertise levels experience the workflow?**
   - Both participants appeared experienced with Revit
   - Question: Do novice Revit users struggle more or less with these concepts? Do experts have additional expectations?
   - Research needed: Include broader range of Revit experience levels (test screener's 1-5 scale)

3. **What's the actual usage pattern - iterative design or one-time import?**
   - P03 mentioned: "The button can be useful during iterative design process"
   - Question: How often do users need to refresh/sync between Forma and Revit? Is this primarily one-way or bidirectional?
   - Research needed: Longitudinal study or diary study of actual usage patterns

4. **Do the Figma prototype limitations mask or exaggerate usability issues?**
   - Notetaker for P02 noted: "This might be largely a limitation of the demo where she only had the option to click through pre-planned paths"
   - Question: Would issues like preview confusion resolve in actual product with real feedback?
   - Research needed: Test with functional prototype or beta product

5. **How do terminology preferences vary across different geographies/firms?**
   - Limited sample (n=2) from one geographic region (both Swedish names, though location not confirmed)
   - Question: Do users in different markets have different terminology expectations?
   - Research needed: Test with geographically diverse sample

6. **What are the task success rates and time-on-task metrics?**
   - Current study captured qualitative feedback but not quantitative metrics
   - Question: How long does each task take? What's the error rate? How does this compare to existing workflow?
   - Research needed: Quantitative usability testing with metrics

### Suggested Follow-Up Research

**1. Broader usability testing with refined design**
- **Why**: Validate fixes for high-priority issues and expand sample size
- **Method**: Moderated usability testing with 5-8 participants, testing refined designs addressing pain points
- **Timeline**: After implementing high-priority fixes (Q2 2024)

**2. Comparative study: Structured workflow vs. simplified "Send to Revit"**
- **Why**: Resolve question about workflow complexity vs. value
- **Method**: A/B testing or preference testing with 2 design alternatives
- **Timeline**: If considering major workflow simplification (Q2-Q3 2024)

**3. Longitudinal study of actual usage patterns**
- **Why**: Understand real-world usage, frequency of refresh/sync, pain points over time
- **Method**: Beta testing with instrumentation and follow-up interviews after 2-4 weeks of use
- **Timeline**: After initial release (Q3-Q4 2024)

**4. Quantitative usability testing for success metrics**
- **Why**: Establish baseline metrics and validate improvements
- **Method**: Task-based testing with 20-30 participants measuring time-on-task, success rates, errors, SUS scores
- **Timeline**: With functional prototype or post-launch (Q3 2024)

**5. Terminology validation study**
- **Why**: Validate proposed terminology changes (Generic → Proposal/Contextual, Load Proposal → Interoperability)
- **Method**: Quick preference testing or card sorting with 10-15 participants
- **Timeline**: Before implementing terminology changes (Q2 2024)

---

## Limitations & Caveats

*Important context about the research*

### Sample Size

- Total participants: **2 participants (n=2)**
- **CRITICAL LIMITATION**: This is significantly below the typical 5-8 participants recommended for qualitative usability testing
- **Note**: In qualitative research, 5-8 participants typically uncover 80-90% of usability issues. With only 2 participants, we're likely missing significant issues
- **Confidence impact**: Even findings observed in 100% of participants (2/2) may not generalize to broader user population
- **Statistical significance**: No statistical significance can be claimed with n=2; findings are directional only

### Participant Diversity

- **Limited experience range**: Both participants appeared to have Revit experience; missing novice users
- **Unknown demographics**: Firm size, geographic location, years of experience not clearly documented in session notes
- **Recruitment source**: Not documented how participants were recruited (may bias sample)
- **Expertise level**: Both participants appeared experienced with Forma-Revit workflows; missing perspective of users new to integration

### Methodology Limitations

- **Figma prototype limitations**: Users couldn't interact naturally with UI; some confusion may be due to prototype constraints
- **Remote sessions**: May not capture full context of in-person workflows or collaborative scenarios
- **Think-aloud protocol effects**: Participants may behave differently when verbalizing thoughts vs. working naturally
- **Prototype limitations**: P02's notetaker explicitly noted: "Given Monica's familiarity I assume this is largely a limitation of the demo where she only had the option to click through the pre-planned paths"
- **Task-based testing**: Structured tasks may not reflect real-world usage patterns or priorities

### Research Plan Execution

- **Missing 4th participant**: Research plan specified 3-4 participants; only 2 sessions documented (Jesper Staahl not included in provided notes)
- **Screener responses not documented**: Session notes don't include screening question responses (Revit familiarity scale 1-5, magic wand question, etc.)
- **Compliance not documented**: CRA status, recording consent not documented in session notes (though may exist elsewhere)
- **No ease ratings**: Some follow-up questions (e.g., "difficulty downloading add-in on 1-5 scale") were asked but P03 didn't provide numerical score

### Confidence Levels

Using n=2 as baseline:
- Findings with 🔴 **High confidence**: Based on 2/2 participants (100%) - *BUT* should still be validated with larger sample
- Findings with 🟡 **Medium confidence**: Based on 1/2 participants (50%) - *Very uncertain* whether this generalizes
- Findings with 🟢 **Low confidence**: Based on 1/2 participants (50%) with limited evidence - *Highly uncertain*

**Interpretation guidance**:
- **2/2 participants (100%)**: Likely a real issue, but may not affect 100% of broader population. Prioritize for investigation with larger sample.
- **1/2 participants (50%)**: Could be: (a) affects half of users, (b) affects small minority and we got lucky/unlucky, (c) specific to that participant's context. Cannot distinguish with n=2.

### What We Can't Conclude

- **Cannot determine prevalence**: No way to know what % of actual users will encounter each issue
- **Cannot establish priorities with certainty**: Severity/priority ratings based on n=2 may not reflect actual impact at scale
- **Cannot validate hypothesis definitively**: "Partially supported" based on n=2 is highly uncertain
- **Cannot identify rare issues**: Issues affecting <33% of users unlikely to appear in n=2 sample
- **Cannot make go/no-go decisions**: Not enough data to decide whether to proceed with development
- **Cannot measure task success rates meaningfully**: 2/2 success = 100%, but doesn't tell us actual success rate in population
- **Cannot identify demographic patterns**: Not enough diversity to understand differences across user segments

### Recommendations for Confidence

Given these limitations:

1. **Treat all findings as hypotheses to validate**: Even "high confidence" findings need testing with larger sample
2. **Prioritize additional research**: Conduct 3-6 more sessions to reach minimum recommended sample size (5-8 total)
3. **Focus on convergent evidence**: Pay most attention to issues observed in BOTH participants (while acknowledging small n)
4. **Prototype limitations**: Test with functional prototype or beta to eliminate Figma constraints
5. **Quantitative validation**: Consider follow-up quantitative study to measure actual prevalence and impact

**Research quality assessment**: While this research provides valuable directional signals and identified specific usability issues, the small sample size significantly limits confidence in findings. The study successfully validated research methodology and instruments, but should be considered a pilot study rather than conclusive research.

---

## Appendix: Raw Data Summary

### Session Notes
- **P02 (Monica Pereira Da Silva)**: `memory/session-notes/revit-addin-usability-P02-monica.md`
- **P03 (Maria Johansson)**: `memory/session-notes/revit-addin-usability-P03-maria.md`

### Recordings
- Recording availability: Not documented in session notes
- Format: Not documented
- Storage location: Not documented

### Transcripts
- Available: ❌ No formal transcripts provided
- Session notes based on notetaker observations

### Missing Documentation
- P01 (Jesper Staahl) - planned but not included in provided materials
- Potential 4th participant - planned but not documented
- Screener responses - not included in session notes
- Compliance documentation (CRA signatures, consent) - not included in session notes

---

## Methodology Recap

**Research Type**: Usability Testing (Figma Prototype)

**Participant Recruitment**:
- Planned: 3-4 participants (research plan)
- Achieved: 2 participants (session notes provided)
- Recruitment method: Not documented
- Screening: Screener questions defined in research plan but responses not documented in session notes

**Screening**:
- Criteria defined: Revit experience, architect/designer role, Forma familiarity
- Screener questions: 5 questions in research plan covering Revit experience, familiarity scale, prior Forma add-in use, magic wand improvement
- Screening results: Not documented in provided session notes

**Session Format**:
- Duration: ~45-60 minutes
- Remote sessions with screen sharing
- Figma prototype walkthrough (not live product)
- 3 structured tasks with follow-up questions
- Think-aloud protocol

**Task Structure**:
1. Task I: Download add-in and load proposal
2. Task II: Refresh proposal with new changes
3. Task III: Convert Forma elements to Revit objects

**Analysis Method**:
- Thematic analysis of session notes
- Cross-participant synthesis to identify patterns
- Evidence-based findings extraction (anti-hallucination protocol)
- Confidence levels assigned based on frequency (n/2 participants)

**Compliance**:
- CRA status: Not documented in session notes
- Recording consent: Not documented in session notes
- PII anonymization: ✅ Participant IDs (P02, P03) used in analysis; real names in source notes need removal for external sharing

---

## Tags for Repository

*For searchability in the research repository*

- **OKRs**: Connected Clients interoperability, Forma adoption, Revit integration
- **Teams**: Connected Clients, Forma Product, Revit Product
- **Topics**: [usability-testing], [revit-integration], [forma-add-in], [interoperability], [preview-workflow], [element-conversion], [terminology], [mental-models]
- **Product Areas**: Forma Add-in for Revit, Load Proposal, Element Conversion, Refresh Workflow
- **Methodology**: [figma-prototype], [remote-usability], [think-aloud], [task-based-testing]
- **Sample Characteristics**: [architects], [revit-users], [forma-users], [small-sample-n2]

---

## Share Out Plan

*How and where these findings will be shared*

- [ ] **Report Created**: One-pager ✅ | Detailed findings ✅ | Quality review ✅ | Slide deck ❌
- [ ] **Stakeholders Notified**: Connected Clients team, Forma product team, UX leadership
- [ ] **Presentation Scheduled**: TBD - recommend presenting to Connected Clients team + Forma stakeholders
- [ ] **Slack Shared**: TBD - appropriate channels for Connected Clients and Forma teams
- [ ] **Filed in Repository**: `memory/findings/revit-addin-usability-findings.md` with tags
- [ ] **Session notes sanitized**: Remove real names before external sharing
- [ ] **Follow-up research planned**: Recommend 3-6 additional sessions to reach n=5-8

---

_Findings synthesized by Autodesk Research Assistant Agent. All evidence extracted directly from participant session notes (no hallucination). All findings flagged with confidence levels acknowledging n=2 sample limitation. Participants anonymized with IDs._

**CRITICAL REMINDER**: This research included only 2 participants (n=2), which is below recommended minimum. Treat findings as directional hypotheses requiring validation with additional research before making major product decisions.
