# Specification format

The specification is one Markdown document. The user reads every section. There are no appendices reserved for agents.

## Writing

Apply these basic ASD-STE100 principles:

1. One idea per sentence. Use short sentences and separate instructions with periods.
2. Use active voice. Write "The app shows the missing file".
3. Use imperatives for checks. Write "Open the project and check the images", without repeating "the verifier".
4. Describe observable behavior. Use known or agreed quantities without inventing values to make a sentence measurable.
5. Remove adjectives such as "robust" and "critical" when they do not explain behavior.

Use the same word for the same concept. Explain technical terms needed for the decision.
Aim for twenty words per instruction and twenty-five per description. Keep conditions that change the meaning.
The standard's dictionary is reference material, not a reason to block the specification.

## Sections

Use these sections in the order shown below. Problem describes what is wrong today.
Outcome describes what will become possible. Not doing preserves what you decided to exclude.
How, roughly explains how the pieces connect. Use a diagram when it makes the flow easier to understand.

Each requirement has an `R<n>` block: behavior and reason, followed by `Check:` with a concrete verification.
Each task has a `T<n>` block with `Ask:`, `Covers:`, and `Depends:`.

- `Ask:` states what to build.
- `Covers:` names the task's requirements. The task inherits their text and checks without reinterpretation.
- `Depends:` names tasks that must finish first. `Depends: none` means there are no dependencies.

Write the dependency on the task that waits. `Depends: T1` inside T2 means T2 waits for T1.
Every requirement must be covered. Use unique identifiers and keep them stable during revisions.
A task integrates a usable part of the outcome. Prefer fewer tasks and separate only genuinely independent changes.

Do not add a format version, glossary, technical appendix, or open-questions section.
Resolve decisions in the interview. Record delegated choices and their boundaries in the relevant requirement's prose.
A verification criterion describes a check to perform. Building a permanent tool for that check remains a choice to discuss within delegated authority.

## Template

```markdown
# Title

## Problem
What is wrong today.

## Outcome
What will become possible when the work is complete.

## Not doing
What we decided to exclude.

## How, roughly
How the pieces connect.

## Requirements

### R1: Requirement title
What must be true and why.
Check: How to verify the behavior.

## Tasks

### T1: Task title
Ask: What to build.
Covers: R1
Depends: none

## Sources
- Request material and references consulted.
```
