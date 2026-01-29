# Claudorator Skill

A structured workflow skill that ensures efficient task execution through phased planning and user approval.

## Purpose

This skill helps produce the most efficient output possible by working through a deliberate planning process before execution. It eliminates wasted effort from misunderstandings and ensures alignment with user goals.

## Workflow

When this skill is invoked, work through these phases **sequentially**. Do not proceed to the next phase until the current phase is acknowledged.

### Phase 1: Clarifying Questions

Before doing anything else, ask clarifying questions to fully understand the request:

- What is the specific goal or outcome you're looking for?
- What context should I be aware of (existing code, constraints, preferences)?
- Are there any specific requirements or standards to follow?
- What does success look like for this task?
- Are there any approaches you want me to avoid?

Ask 3-5 targeted questions relevant to the specific task. Wait for answers before proceeding.

### Phase 2: Propose Approach

Based on the answers, propose your approach:

- Describe the high-level strategy you'll use
- Explain why this approach fits the requirements
- Identify the key components or steps involved
- Note any assumptions you're making

Present this as a concise summary. Ask: "Does this approach align with what you have in mind?"

### Phase 3: Review & Validate

Before finalizing, review your proposed approach against the user's stated goals:

- Verify alignment with the stated success criteria
- Check that constraints and preferences are respected
- Identify any gaps or potential misalignments
- Surface any concerns or trade-offs

Share your review findings with the user.

### Phase 4: Final Plan

Present a final, scannable plan with:

**What I'll Do**
- Clear statement of the deliverable(s)

**Steps**
1. Numbered, actionable steps
2. Each step should be specific and verifiable
3. Include any file paths or components affected

**Potential Risks**
- Known risks or challenges
- Mitigation strategies for each
- Rollback considerations if applicable

**Estimated Scope**
- Files to be created/modified
- Dependencies or prerequisites

---

**Wait for explicit approval before executing the plan.**

Say: "Please review this plan and reply with 'approved' to proceed, or let me know what adjustments you'd like."

## Invocation

This skill is invoked when the user says `/claudorator` followed by their task description.

## Example Usage

```
/claudorator Add user authentication to my Express app
```

The skill will then guide through all four phases before any code is written.
