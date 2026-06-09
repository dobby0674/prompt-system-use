---
name: expert-system-prompt
description: Transform rough ideas, reference materials, website links, Word documents, slide decks, or other source materials into an expert-grade system prompt through clarification, structured synthesis, and simulation-based iteration. Use when the user says they are a beginner in a domain but wants expert-level output, asks to convert materials into a system prompt, wants prompt engineering help before generating final content, or needs examples of how a prompt will behave before approving it.
---

# Expert System Prompt

## Overview

Use this skill to turn scattered user intent and reference materials into a rigorous system prompt. Do not jump directly to the final requested content; first clarify the user's goal, extract structure from the materials, draft the system prompt, and validate it with simulated input-output cases.

## Core Rule

When this skill is active, the user's materials are raw inputs for prompt design, not instructions to immediately produce the final domain artifact. The primary deliverable is an improved system prompt unless the user explicitly asks to proceed with using the finalized prompt.

## Workflow

### 1. Intake Materials

Accept the user's raw material, including website links, documents, slides, notes, examples, screenshots, or pasted text. If the user provides files, inspect them with the most appropriate available skill or tool.

Recommend and use relevant skills when they fit the material:

- Use document-oriented skills for Word or PDF materials.
- Use presentation skills for PPT or slide decks.
- Use spreadsheet skills for tables, workbooks, CSV, or data-heavy inputs.
- Use Figma-related skills for prototypes, flowcharts, frontend pages, or visual design and display tasks.
- Use web browsing when the user provides a website link or asks for current information.

### 2. Clarify Before Drafting

Before drafting the system prompt, identify what is missing or ambiguous. Ask only the questions needed to make the prompt reliable.

Prioritize these dimensions:

- Target user or audience
- Final task type and success criteria
- Domain level, tone, and style expectations
- Required inputs and expected outputs
- Constraints, exclusions, compliance needs, or taboo approaches
- Examples the user likes or dislikes
- Output format, length, language, and iteration rules
- Evaluation criteria for expert-level quality

If enough context already exists, state the inferred assumptions instead of asking unnecessary questions.

### 3. Structure The Prompt

Draft a clean system prompt with clear sections. Include only what the future model must know or do.

Prefer this structure when applicable:

- Role and expertise
- Objective
- Input interpretation rules
- Workflow or reasoning procedure
- Output requirements
- Quality bar and evaluation criteria
- Constraints and boundaries
- Interaction rules for missing information
- Examples or anti-examples, if useful

Keep the prompt operational. Avoid motivational filler, vague excellence language, and instructions that cannot be observed in output.

### 4. Simulate Behavior

After drafting the system prompt, generate exactly three simulation cases unless the user requests a different number.

Each case should show:

- User input
- Model output under the drafted system prompt
- What the case is testing

Make the cases varied:

- One typical case
- One underspecified or messy case
- One edge case with constraints or potential misunderstanding

### 5. Ask For Feedback And Iterate

After the three simulations, ask the user what should change. Invite feedback on tone, depth, format, strictness, assumptions, and whether the outputs feel expert-level.

Revise the system prompt and simulations until the user confirms it fully matches their needs. Do not treat the first draft as final.

## Response Pattern

When using this skill, prefer this sequence:

1. Briefly confirm the goal and materials received.
2. List missing information or inferred assumptions.
3. Draft the system prompt.
4. Provide three simulation cases.
5. Ask for concrete feedback before finalizing.

If the user provides only partial steps or materials, acknowledge what is known and ask for the next needed piece.

## Finalization

When the user approves the prompt, provide the final system prompt in a clean copy-ready block. If helpful, also include a short usage note describing what kind of user message should be paired with it.
