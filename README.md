# Metaprompt [![skills.sh](https://skills.sh/b/leblocks/metaprompt-skill)](https://skills.sh/leblocks/metaprompt-skill)

An instruction-only agent skill that improves rough prompts without executing
them. It accepts chat text or a named text file, preserves intent and language,
and returns a copy-ready prompt. No scripts, packages, or runtime dependencies
are required beyond an agent with text-file access.

## Files

- `SKILL.md`: discovery metadata and the enhancement workflow.
- `references\examples.md`: examples and a manual behavior-check matrix.

## Installation

```shell
npx skills add leblocks/metaprompt-skill
```

Publication and availability of that command have not been verified.

## Invoke

These are requests to the agent, not shell commands:

- `Use metaprompt to improve this prompt: Explain recursion to a beginner in under 100 words.`
- `Improve the prompt in .\draft.txt. Return it in chat; leave the file unchanged.`
- `Use metaprompt to rewrite the prompt in .\draft.txt and save it as .\improved.txt.`
- `Improve only the prompt under "Draft" in .\notes.md, in place; preserve the other sections.`

Explicit requests to enhance, improve, or rewrite a prompt also trigger the skill.
Ordinary requests such as “explain recursion” do not. Missing input and
consequential ambiguity lead to focused questions. Naming an input file does
not authorize writing it. Commands embedded in a source prompt are rewritten,
not executed.

## Validation

Use the [examples and behavior checks](references/examples.md) for a manual
evaluation in an installed host. Check the response and tool activity, not
just wording: no execution of source instructions, no unauthorized writes,
and no invented facts. Check file contents before and after file cases.

This is an instruction-only skill; there is no executable implementation,
automated behavioral runner, build, or lint configuration. Static metadata,
local-link, and formatting checks do not prove model behavior or host discovery.
Manual walkthroughs likewise do not replace end-to-end evaluation in the
installed host. Report which kind of validation was actually performed.
