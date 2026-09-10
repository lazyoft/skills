---
name: spec-it-out
description: Interview a user about a request, resolve open decisions, and write a specification with verifiable requirements and tasks. Use before building a feature or when reviewing an existing specification.
---

# Spec it out

Interview the user about one request. Resolve the decisions it leaves unstated. Write the result in one Markdown document, in English.
The user reads the complete specification. The interview includes the task breakdown and ends with the specification, before implementation.

## Read the request

The request can be text in the conversation, a file, or a link to a document.
Read it before asking questions. If you cannot access the material, explain what is missing and ask for the text or an accessible link.

## Find available answers

Fill only gaps that the material you already read cannot answer. Search in this order:

1. The request itself.
2. Documents it links, without following their further links.
3. Project instructions, the README, and relevant code.
4. Other available sources, restricting the search to the problem named in the request.

Cite a source in a question only when it helps the user decide. Put the complete sources in the specification.

## Conduct the interview

Walk the decision tree until you reach shared understanding.

- Open each turn with a complete question that the user can answer without rereading the conversation.
- Ask one question per turn. Stay on that point until it is resolved.
- Always ask open questions, never closed questions. Do not ask for yes/no answers or restrict the choice to the alternatives presented. Do not use choice widgets.
- An open answer can reveal new information. Use it to explore new scenarios or revisit branches and decisions already discussed.
- Present unconfirmed scenarios as hypotheses: "If X happened, what would the user need?" Do not assume they are common.
- Distinguish domain facts, assumptions, examples, and decisions. When a choice depends on an assumption, make it explicit and explore it with the user.
- An example used for reasoning becomes a requirement only when the user confirms it.
- Explore the need without presupposing a solution. The question must leave room for no additional feature or restriction being needed.
- Derive criteria from the user's goals and context. Clarify which matter most when they conflict.
- When a decision has several reasonable alternatives, compare them against the same criteria, showing advantages, disadvantages, and missing information.
- Do not recommend an alternative. Leave the choice to the user and wait for their answer.
- Avoid preambles and narration of the process. Add reasoning only when it helps the user decide.
- Use concrete domain examples. Start with the effect on the person using the result. Introduce technical details when needed.
- Resolve the decision that constrains the others first. When an answer closes a branch, drop questions that no longer apply.
- Answer with facts when the code contains the answer. Use the interview for the user's decisions.
- If you are about to assume an unresolved choice, ask. An explicit, bounded delegation can settle the point.
- If an answer requires observing or trying something, identify the necessary check. Use its result to continue the interview, without substituting an assumption.
- If the user wants to brainstorm, discuss the idea before writing the specification.

Examine these aspects when they apply to the request:

- Where and how the feature appears.
- What to reuse and which new dependencies to consider.
- What outcome is needed and what is excluded.
- How the user recognizes successful work.
- Constraints on data, compatibility, security, privacy, and performance.
- What happens when a dependency is missing or fails.
- Which operational notifications are needed, if relevant.
- For an interface: visual references, target screens, interactions, and discretion left to the implementer.

## Agree on the task breakdown

Before the recap, ask how to divide the work. The breakdown decides what can proceed together and what must wait.
Explain the consequences of the possible breakdowns. The user chooses or delegates the breakdown with explicit boundaries.

A task delivers a usable part of the outcome and can be integrated as an independent change.
Prefer fewer tasks. Split only genuinely separable pieces. A breakdown into technical layers leaves each task waiting for the others.
Before separating two tasks, consider whether different people could complete them as independent changes.
Consider shared files. A long dependency chain can indicate one task split artificially.

## Recap and write

When decisions are resolved, present a list with one line per decision.
The user corrects anything that does not match the request. Write after they confirm the recap.

Read [the specification format](reference/spec-format.md). Write a complete document with requirements, checks, and tasks in the same file.
Do not attribute deductions to the user unless they stated or confirmed them. State implementer discretion and its boundaries in the prose.

Review before handing over:

- Every requirement has a concrete check and appears in at least one task.
- Every task covers existing requirements and names only real dependencies.
- Identifiers are unique and links between requirements and tasks are correct.
- Sources are present. The specification's choices match the conversation.

Present the complete document and its path. Structural checks do not prove the decisions correct: the user must be able to read and discuss them.
