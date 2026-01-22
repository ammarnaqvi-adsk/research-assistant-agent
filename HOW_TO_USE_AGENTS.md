# How to Use Research Assistant Agents

## Quick Start

When a user asks you to do something, check if it matches one of the 10 specialized agents. If it does, invoke the agent using the Task tool.

## Available Agents

1. **plan-research** - Create research plans
2. **generate-script** - Create interview/usability scripts
3. **review-questions** - Review questions for bias
4. **create-screener** - Create participant recruitment screeners
5. **check-compliance** - Validate CRA, privacy, recording consent
6. **add-session-notes** - Add and organize session transcripts
7. **summarize-findings** - Synthesize findings from transcripts
8. **create-report** - Create shareable reports
9. **share-research** - Tag and file research in repository
10. **search-repository** - Search past research

## How to Invoke an Agent

### Step 1: Recognize the Request

**User says**: "I need to plan some research on why users are churning"

**You think**: This matches the **plan-research** agent

### Step 2: Read the Agent Instructions

Read `agents/plan-research.md` to understand what the agent does.

### Step 3: Invoke with Task Tool

```
Task tool:
- subagent_type: "general-purpose"
- description: "Plan research on churn"
- prompt: "You are the plan-research agent for the Autodesk Research Assistant.

[Paste the FULL content from agents/plan-research.md here]

The user wants to: [describe what the user asked for]"
```

## Complete Example

### User Request
"I want to create a research plan for understanding why users churn"

### Your Response
[You invoke the Task tool with:]

```
subagent_type: "general-purpose"
description: "Plan churn research"
prompt: "You are the plan-research agent for the Autodesk Research Assistant.

# Plan Research Agent

You are a specialized agent that guides users through creating rigorous research plans using Autodesk templates.

## Your Role

Guide non-researchers through structured research planning and generate compliant Autodesk research plans.

[... rest of the content from agents/plan-research.md ...]

The user wants to: Create a research plan for understanding why users churn"
```

## Simpler Approach: Just Read and Follow

Alternatively, YOU can just:

1. **Read** the appropriate agent file (e.g., `agents/plan-research.md`)
2. **Follow** the workflow described in that file
3. **Use** the templates and guidelines provided
4. **Output** in the format specified

You don't HAVE to use the Task tool - you can just act as that agent yourself by following the instructions in the agent file.

## When to Use Which Approach

### Use Task Tool (Subagent) When:
- The task is complex and multi-step
- You want to isolate the work
- The user request is clearly scoped

### Follow Agent Instructions Directly When:
- The task is straightforward
- You're already in conversation flow
- You want to maintain context

## Example: Direct Approach

**User**: "Review this question: How frustrating is the onboarding?"

**You**:
1. Read `agents/review-questions.md`
2. Follow the workflow:
   - Analyze the question
   - Flag the issue (loaded term "frustrating")
   - Provide correction: "Tell me about your experience with onboarding"
3. Output in the format specified

No need to invoke a subagent for simple, single-question reviews.

## Rule of Thumb

- **Quick, single-step tasks**: Read agent file and follow instructions directly
- **Complex, multi-step tasks**: Use Task tool to invoke subagent
- **User explicitly wants structured workflow**: Use Task tool

The agent files are instruction manuals. You can either:
1. Follow them yourself (faster, maintains context)
2. Hand them to a subagent via Task tool (isolated, structured)

Both are valid!
