# Forma Revit Add-in Usability: One-Page Summary

**Date**: April 10-11, 2024 | **Research Lead**: Tamira McCoy | **Participants**: 2 users (P02, P03)

**⚠️ Note**: Small sample size (n=2) - findings are directional signals, not conclusive. Recommend 3-6 additional sessions.

---

## 🎯 Research Goal

**We wanted to learn**: Does the new Revit add-in UI match architects' mental models when transitioning between Forma and Revit?

**Why it matters**: The Forma-Revit integration is critical for Q1 interoperability goals. We need to validate designs before development to ensure seamless workflows and adoption.

---

## 🔬 Methodology

**What we did**: Conducted 2 remote usability tests with Figma prototype walkthrough

**Who we talked to**: Experienced architects/designers (P02, P03) familiar with both Forma and Revit workflows. Both have used existing Forma-Revit integration via massing section.

**Tasks tested**: (1) Download add-in and load proposal, (2) Refresh proposal with changes, (3) Convert Forma elements to Revit objects

---

## ✅ Key Finding: Hypothesis Result

**Our hypothesis**: The new Revit add-in UI will match architects' mental models when transitioning between Forma and Revit, reducing friction and enabling seamless interoperability.

**Result**: 🟡 Partially Supported

**What this means**: The core workflow is directionally correct and more intuitive than the existing massing-based approach, but several terminology choices and interaction patterns need refinement to fully align with architect mental models.

---

## 🔴 Top 3 Pain Points

### 1. "Generic" Element Type Label Doesn't Match Mental Model

**What we heard**: "In particular 'Generic' was not a known concept for her. The difference between 'building' and 'generic' wasn't as natural as the distinction between proposal buildings vs contextual buildings" - P02

**How common**: 2/2 participants (100%)

**Impact**: Makes conversion choices unclear; users can't confidently select which Revit element type to use

**💡 Opportunity**: Replace "Generic" with meaningful categorization like "Proposal Buildings" vs. "Contextual Buildings" that maps to how architects think about building purpose and context

---

### 2. Preview State Not Clearly Distinguished from Editable Revit Objects

**What we heard**: "Not understanding from the dialog screen to know for sure this is a preview screen" - P03 | "She did not immediately understand that the preview was itself not Revit elements" - P02

**How common**: 2/2 participants (100%)

**Impact**: Fundamental confusion about workflow state; users attempt to interact with non-interactive elements; unclear when conversion is needed to begin editing

**💡 Opportunity**: Add prominent "PREVIEW" label, implement real-time preview updates when toggling checkboxes, use visual treatment to differentiate preview from Revit viewport

---

### 3. No Clear Way to Switch Between Forma Projects

**What we heard**: "Wanted to click on the title name and change the project using a drop down menu... Currently, user may just close the window to try and reload the project" - P03 | "Monica was slightly confused about the terminology because while in Revit she assumed 'change project' meant change the underlying Revit project" - P02

**How common**: 2/2 participants (100%)

**Impact**: Blocks critical workflow functionality; users resort to closing/reopening panel as workaround; terminology confusion adds cognitive load

**💡 Opportunity**: Make project name clickable with dropdown (matching proposal pattern) OR add clear "Change Forma Project" button OR add back arrow to project selection. Use "Forma Project" terminology to avoid confusion with Revit project.

---

## ⚡ Quick Wins

*Easy improvements that could have immediate impact*

1. **Add "PREVIEW" label to visualization area** - Clarifies workflow state at a glance
2. **Replace "Generic" with "Contextual Buildings"** - Uses terminology architects already understand
3. **Add project dropdown/button with "Forma Project" terminology** - Provides missing functionality and prevents confusion

---

## 🎁 What Users Loved

*Don't forget the positive findings!*

- **More intuitive than existing workflow**: "This is a much more intuitive flow rather than having to go to the massing section to load proposal" - P02
- **Refresh icon natural**: "The refresh icon felt natural to Monica" - P02 | "User would click on the refresh button" - P03
- **Visibility toggles natural**: "Monica found it very natural to toggle visibility of different Forma element types" - P02
- **Element mapping concept clear**: "Monica immediately understood the concept of choosing the Revit element type for each Forma element type" - P02
- **Preview concept valued**: "Like the idea of the preview" - P03
- **Icon consistency appreciated**: "Great to have the same symbols associated with each icon in Forma" - P03

**Keep these strengths** as we iterate on the design.

---

## 📊 Additional Findings

**Users expect real-time interactive preview** (2/2 participants):
- "Checking or unchecking boxes should ideally change the preview" - P03
- P02 attempted to interact with preview elements expecting Revit functionality
- **Impact**: Static preview doesn't meet modern software expectations

**Mental model mismatch: Templates vs. Views** (1/2 participants):
- P02 expects to work with templates rather than views for visibility control
- "Because she sets visibility settings on the template it made more sense to filter based on template" - P02
- **Impact**: Advanced users' workflows may not align with view-based model

**Refresh timing questioned** (1/2 participants):
- "The expectation is that clicking on Convert to Revit Objects should bring in the latest proposal" - P03
- P03 found refresh button but questioned need for separate action
- **Impact**: Extra step users question; potential for stale content errors

---

## 📊 Recommendations (Prioritized)

| Priority | Recommendation | Impact | Owner |
|----------|---------------|--------|-------|
| 🔴 High | Replace "Generic" with context-based categorization (Proposal/Contextual Buildings) | Faster, confident conversion decisions | UX Design + Product |
| 🔴 High | Add clear preview state indicators + real-time preview updates | Clear workflow understanding, meets modern expectations | UX Design + Engineering |
| 🔴 High | Add project switching mechanism with "Forma Project" terminology | Enables critical functionality, prevents confusion | UX Design + Product |
| 🟡 Medium | Investigate templates vs. views mental model (validate with more users) | Better alignment for advanced users | UX Research + Engineering |
| 🟡 Medium | Clarify refresh behavior or integrate with conversion | Reduced steps, fewer errors | Product + UX Design |
| 🟡 Medium | Improve add-in download discoverability with Revit branding | Faster onboarding, better first impression | Forma Product + UX |

---

## 🔮 Next Steps

1. **Conduct 3-6 additional usability sessions** - Research Team by end of Q2 2024
   - Rationale: n=2 insufficient for conclusive findings; need minimum 5-8 participants
   - Include broader range of Revit expertise and Forma experience levels

2. **Iterate designs addressing high-priority issues** - UX Design by mid-Q2 2024
   - Focus on: Generic label, preview state, project switching
   - Prepare refined designs for testing in additional sessions

3. **Test with functional prototype or beta** - Engineering + Research by Q3 2024
   - Validate that preview confusion and interaction issues resolve with real Revit feedback
   - Separate Figma prototype artifacts from genuine design issues

4. **Resolve compliance documentation** - Research Ops immediately
   - Confirm CRA status for P02 and P03 (critical if external participants)
   - Document recording consent and data storage procedures

---

## ⚠️ Important Caveats

**Sample Size Limitation**: This study included only 2 participants (n=2), below the recommended 5-8 for qualitative usability testing. Findings represent directional signals and should be validated with additional research before making final product decisions.

**Prototype Limitations**: Figma prototype constraints may have masked or exaggerated some issues. Follow-up testing with functional prototype recommended.

**Participant Diversity**: Both participants appeared experienced with Revit and Forma. Missing perspective from novice users, different firm sizes, and varying experience levels.

**Use This Research For**:
- ✅ Design iteration and refinement
- ✅ Hypothesis generation for further testing
- ✅ Prioritization of improvements (with caveats)
- ✅ Stakeholder alignment on design direction

**Don't Use This Research For**:
- ❌ Final go/no-go decision on development
- ❌ Conclusive validation of hypothesis
- ❌ Comprehensive usability assessment
- ❌ Quantitative claims without additional validation

---

## 📚 Learn More

- **Full findings**: See `memory/findings/revit-addin-usability-findings.md`
- **Research quality review**: See `memory/findings/revit-addin-usability-QUALITY-REVIEW.md`
- **Session notes**: See `memory/session-notes/revit-addin-usability-P02-monica.md` and `P03-maria.md`
- **Research plan**: See `memory/research-plans/revit-addin-usability-research-plan.md`
- **Questions?** Contact Tamira McCoy (Connected Clients team)

---

## 🏷️ Tags

**OKRs**: Connected Clients Interoperability, Forma Adoption, Revit Integration Q1 Goals | **Teams**: Connected Clients, Forma Product, Revit Product | **Topics**: [usability-testing], [revit-integration], [forma-add-in], [interoperability], [mental-models], [pilot-study]

---

_Research conducted by Tamira McCoy (Connected Clients team) | Generated by Research Assistant Agent | April 2024_

**Summary**: While sample size is limited (n=2), this research provides valuable direction for design improvements. The core workflow is validated as more intuitive than existing approach, but terminology, state indication, and interaction patterns need refinement. Recommend completing 3-6 additional sessions before finalizing designs for development.
