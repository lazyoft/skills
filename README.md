# Skills

Reusable agent skills by Fabrizio Chignoli, available in English and Italian.

Each skill contains instructions and supporting material that an agent can use in a conversation.

## Available skills

| Skill | What it does | English | Italiano |
| --- | --- | --- | --- |
| Spec it out | Interviews you about a feature and produces a specification with requirements, checks, and tasks. | [Read the skill](en/spec-it-out/SKILL.md) | [Leggi lo skill](it/spec-it-out/SKILL.md) |

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

The specification is the output. Implementation follows as a separate step when you request it.

The writing instructions use practical principles from [ASD-STE100 Simplified Technical English](https://www.asd-ste100.org/STE_faq.html): short sentences, active voice, consistent terms, and concrete behavior.
The Italian version adapts these principles to Italian.

## Use a skill

Choose the language you want for the interview and the document. Copy the complete `spec-it-out` folder into your agent's skills directory.
Keep `reference/spec-format.md` alongside `SKILL.md`. Both language versions use the same skill name, so install the version you want to use.

Ask your agent to use the skill with your request. For example:

> Use the spec-it-out skill to interview me about this feature: an offline app for arranging comic pages from existing images.

In Italian:

> Usa lo skill spec-it-out per intervistarmi su questa idea: un'app offline per impaginare un fumetto con immagini già disponibili.

If your agent does not support skill discovery, give it `SKILL.md` and the referenced specification format directly.

## Repository layout

```text
en/spec-it-out/
  SKILL.md
  reference/spec-format.md
it/spec-it-out/
  SKILL.md
  reference/spec-format.md
```

## License

[MIT](LICENSE). You can use, modify, and redistribute these files under its terms.
