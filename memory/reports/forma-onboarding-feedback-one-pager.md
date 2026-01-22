# Forma Onboarding Feedback Research: One-Page Summary

**Date**: December 16, 2025 | **Research Lead**: Clément Lemaire | **Participants**: 1 user (P01)

---

## 🎯 Research Goal

**We wanted to learn**: How new users experience Forma onboarding and what obstacles they encounter during their first weeks of use.

**Why it matters**: Understanding early adoption barriers helps us reduce churn and accelerate time-to-value for new Forma users, especially those coming from Revit.

---

## 🔬 Methodology

**What we did**: Conducted 1 remote interview (24m 36s) with screen sharing walkthrough of P01's actual Forma projects.

**Who we talked to**: City Council master planner with 8 years of Revit experience, who returned to Forma after first trying it 10 years ago (when it was called Formit). P01 had been using the new Forma for 2 weeks.

---

## ✅ Key Finding: Exploratory Study (No Hypothesis)

**Study type**: Exploratory onboarding feedback session

**Result**: ❓ Not Applicable - this was exploratory research, not hypothesis testing

**What this means**: Identified 5 pain points (1 critical) and 3 positive findings to inform product roadmap.

---

## 🔴 Top 3 Pain Points

### 1. Navigation Shortcuts Different from Revit (CRITICAL)

**What we heard**: "But look, you asked for feedback and **that was the hardest thing actually**." - P01 (22:33)

**How common**: 1/1 participants (100%)

**Impact**: Creates immediate friction for Revit users (primary target audience). P01 said it was "like getting into a car with the steering wheel on the other side." Takes 1-2 weeks to adapt. Blocks smooth workflow switching between Forma and Revit.

**💡 Opportunity**: Align Forma's navigation shortcuts (especially pan/zoom) with Revit, or provide a "Revit mode" toggle. P01 said: "If people are going to be going from Revit to Forma and back to Revit, it would be good if some of the basic commands are familiar." (20:48)

---

### 2. No Street Parking Feature

**What we heard**: "But I haven't found a way just to do parking on the street like in a in a in a row." - P01 (3:40)

**How common**: 1/1 participants (100%)

**Impact**: Blocks critical master planning task. Parking plugin works for lots/basements but not street-level parking with parallel/perpendicular spaces. P01 has existing Revit family solution.

**💡 Opportunity**: Create street parking feature that allows users to place parking along roads with automatic space counting (similar to existing parking lot feature).

---

### 3. Cannot Add Cycle Lanes and Footpaths to Roads

**What we heard**: "Could have a road that's say 6 meters wide and then with a cycle lane on both sides and a footpath." - P01 (4:46)

**How common**: 1/1 participants (100%)

**Impact**: Essential for European master planning. Currently "very manual" to implement. Regulatory requirement in many regions.

**💡 Opportunity**: Allow users to configure roads with cycle lanes and footpaths as integrated components. (Note: Clément mentioned team is already working on this feature.)

---

## ⚡ Quick Wins

*Easy improvements that could have immediate impact*

1. **Add snapping to line tool** - Standard CAD feature, currently missing. Makes manual workarounds (like drawing footpaths) more precise.
2. **Site boundary display options** - Allow outline-only view (not filled) to match Irish/regional presentation conventions. Workaround exists but could be easier.
3. **Better error messages for import** - When import fails, explain which formats ARE supported, not just that format is "not supported."

---

## 🎁 What Users Loved

*Don't forget the positive findings!*

- **Google Maps integration**: "I like the fact that it is synchronized with Google Maps. So straight away we have a basic topography... and imagery of roads and the landscape, so that's very helpful." - P01 (2:47)
- **Analysis features (carbon, sunlight, daylight)**: "It's pretty easy to launch. You see the result is fast." - P01 (14:22). Especially carbon analysis for proving urban infill is better than countryside development.
- **Space settings for building setbacks**: "Normally we do have a 2 1/2 meter space in front of the houses, so that's great that you can set that." - P01 (7:23)

**Keep these strengths** as we add more features - they provide immediate value and reduce setup time.

---

## 📊 Recommendations (Prioritized)

| Priority | Recommendation | Impact | Owner |
|----------|---------------|--------|-------|
| 🔴 High | Align navigation shortcuts with Revit (or add "Revit mode") | Eliminate #1 pain point, reduce learning curve from weeks to days, increase Revit user adoption | Forma Product + Revit Platform |
| 🔴 High | Add street parking feature | Complete parking workflow (currently only lots/basements) | Forma Site Design |
| 🔴 High | Add cycle lanes/footpaths to roads | Meet European master planning requirements (already in progress per Clément) | Forma Site Design |
| 🟡 Medium | Add snapping to line tool | Improve precision of manual workflows | Forma Drawing Tools |
| 🟢 Low | Site boundary display options | Match regional conventions (workaround exists) | Forma Visualization |

---

## 🔮 Next Steps

1. **Validate navigation pain point with more Revit users** - Task-based usability testing with 5-8 Revit users new to Forma (Q1 2026)
2. **Connect P01 with Caterina (site design PM)** - P01 is engaged and has valuable context for ongoing site features development
3. **Consider P01 for beta testing** - When street parking and cycle lanes/footpaths features are ready

---

## 🔑 Key Insight: Revit Interoperability is Strategic

P01 explicitly stated: "The more interoperability between Forma and Revit, I think you'll get more people using Forma." (23:28)

This aligns with the navigation shortcuts pain point - both tools are Autodesk products, so inconsistent patterns create unnecessary friction. Solving this could accelerate adoption among the existing Revit user base.

---

## 📚 Learn More

- **Full findings**: See `memory/findings/forma-onboarding-feedback-findings.md`
- **Session notes**: See `test-data/real-transcript-01.md`
- **Video clips available**: All quotes include timestamps for creating video evidence
- **Questions?** Contact Clément Lemaire

---

## 🏷️ Tags

**OKRs**: Forma adoption, Revit interoperability | **Teams**: Forma Product, Site Design, Revit Platform | **Topics**: onboarding, navigation-shortcuts, revit-interoperability, street-parking, cycle-lanes, master-planning

---

_Research conducted by Autodesk Research Team | Generated by Research Assistant Agent | Anti-hallucination protocol: All quotes extracted directly from transcript_
