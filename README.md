# Skills

Reusable agent skills by Fabrizio Chignoli, available in English and Italian.

Each skill contains instructions and supporting material that an agent can use in a conversation.

## Available skills

| Skill | What it does | English | Italiano |
| --- | --- | --- | --- |
| Spec it out | Interviews you about a feature and produces a specification with requirements, checks, and tasks. | [Read the skill](en/spec-it-out/SKILL.md) | [Leggi lo skill](it/spec-it-out/SKILL.md) |
| Next iteration | Proposes the next iteration through risk analysis and preserves risk history; implementation follows separately. | [Read the skill](en/next-iteration/SKILL.md) | [Leggi lo skill](it/next-iteration/SKILL.md) |
| Therapist | Opens a session with you when work with an agent went wrong. | [Read the skill](en/therapist/SKILL.md) | [Leggi lo skill](it/therapist/SKILL.md) |

## Spec it out

Start with an idea, an existing plan, or a requirements document. The agent reads the available material and asks one question at a time.

The interview explores the decisions that affect the result. The agent compares reasonable alternatives against the same criteria, grounded in your needs.
It explains their consequences without recommending an alternative. You make the choice.
It also discusses how to divide the work into tasks. You review the decisions before it writes the specification.

The result is one Markdown file containing:

- The problem and intended outcome.
- What you decided to leave out.
- The overall approach.
- Requirements with concrete checks.
- Tasks linked to those requirements, with dependencies.
- The sources used during the interview.
- An appendix of assumptions and alternatives considered and rejected, when applicable.

The specification is the output. Implementation follows as a separate step when you request it.

The writing instructions use practical principles from [ASD-STE100 Simplified Technical English](https://www.asd-ste100.org/STE_faq.html): short sentences, active voice, consistent terms, and concrete behavior.
The Italian version adapts these principles to Italian.

## Next iteration

Use risk analysis to choose the next iteration of a software project. The agent reads existing code, documents, and evidence, discusses the choices with you, and records the proposed iteration and its rationale.

The skill stops at the proposal. Accepting it records an accepted proposal; it does not start implementation. Specifications and an interview follow when you request them separately, before implementation.

The analysis record in `ITERATIONS.md` keeps both the current state and the history of risks, decisions, and evidence. Later sessions revisit earlier risks instead of starting from scratch. The skill writes only its analysis record; it does not write code, prototypes, or tests.

The dialogue uses domain language and practical ASD-STE100 principles, adapted for Italian. Each language version is one self-contained `SKILL.md`.

This replaces `spiral`. Invoke `/next-iteration` in Claude Code. A running conversation that already loaded the old skill still has those old instructions; start a new session with the new skill. Preserve existing analysis notes so the new session can read them.

## Therapist

Launch it in the conversation where the work went wrong. The therapist starts from what happened there and closes the session after a few exchanges.

## Use a skill

Choose the language you want for the interview and the document. Copy the complete skill folder into your agent's skills directory.
For Spec it out, keep `reference/spec-format.md` alongside `SKILL.md`. Next iteration needs only `SKILL.md`. Both language versions use the same skill name, so install the version you want to use.

Ask your agent to use the skill with your request. For example:

> Use the spec-it-out skill to interview me about this feature: an offline app for arranging comic pages from existing images.

In Italian:

> Usa lo skill spec-it-out per intervistarmi su questa idea: un'app offline per impaginare un fumetto con immagini già disponibili.

If your agent does not support skill discovery, give it `SKILL.md` and the referenced specification format directly.

To use Next iteration:

> Use next-iteration to propose the next iteration for this project from its risks and existing evidence. Read the previous analysis record and leave the proposal ready for specifications and an interview.

In Italian:

> Usa next-iteration per proporre la prossima iterazione in base ai rischi e alle evidenze esistenti. Riprendi il registro precedente e prepara la proposta da portare a specifiche e interview.

## Repository layout

```text
en/spec-it-out/
  SKILL.md
  reference/spec-format.md
en/therapist/
  SKILL.md
en/next-iteration/
  SKILL.md
it/spec-it-out/
  SKILL.md
  reference/spec-format.md
it/therapist/
  SKILL.md
it/next-iteration/
  SKILL.md
```

## License

[MIT](LICENSE). You can use, modify, and redistribute these files under its terms.
