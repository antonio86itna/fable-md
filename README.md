# FABLE.md

**A single-file operating standard for Claude Code — and most other coding agents.**

FABLE.md does not make the model smarter. Capabilities live in the weights, not in
prompts (that's literally section 0 of the file). What it does is encode the
*working discipline* that separates excellent output from mediocre output on the
same model:

- **Honesty & pushback** — "it should work" is banned: tested, or declared
  untested. Disagreeing with a flawed request *before* executing is mandatory.
- **Anti-hallucination** — every API/flag/version verified before it lands in
  delivered code; every number needs a traceable origin.
- **Calibrated autonomy** — a hard list of actions that always require asking
  first: spending money, deploys, deletions, irreversible operations, scope
  changes.
- **Reasoning discipline** — plans proportional to task size, treated as
  contracts; edge cases considered by default; alternatives noted for structural
  decisions.
- **Project memory** — STATUS.md updated at session end, so the next session
  restarts from a file, not from vibes.
- Plus: code quality rules, source hierarchy for research, communication format,
  and an end-of-work self-check.

## How to use it

1. Drop `FABLE.md` into your project root.
2. Reference it from your project's `CLAUDE.md`:

   ```
   Read FABLE.md in full at the start of every session and treat its rules
   as hard constraints.
   ```

   Or paste its content directly into `CLAUDE.md` / `AGENTS.md` if you prefer a
   single file — the content is tool-agnostic apart from a few Claude Code
   conventions.
3. Customize the **USER PROFILE** block in section 1 (name, experience, stack,
   communication language). This is what lets the model calibrate depth and
   pushback to *you*.
4. Priority on conflict: model safety policies > FABLE.md > project CLAUDE.md >
   model defaults.

## What it is not

- Not a jailbreak, not a "model upgrade", not magic. If a rules file promises to
  turn one model into a better one, it's lying to you.
- Not a new idea. Instruction files for coding agents are an established
  practice (`CLAUDE.md`, the open `AGENTS.md` standard). FABLE.md is a distilled,
  opinionated version focused on *working discipline* rather than project
  context — the two complement each other.
- Not affiliated with Anthropic. Claude is Anthropic's product; the name FABLE
  is a nod to their model naming. This is an independent, unofficial project.

## Files

| File          | Description                          |
|---------------|--------------------------------------|
| `FABLE.md`    | English version                      |
| `FABLE.it.md` | Italian version (the original)       |

## Origin

Distilled from months of daily production use of Claude Code across web agency,
hosting and product development work. First shared on r/ClaudeAI.

## Contributing

It's a v1.0. If a rule doesn't work in practice, is missing, or conflicts with
how a specific model behaves, open an issue or a PR.

## License

MIT — see [LICENSE](LICENSE).

Maintained by **[ReviewMost4463](https://www.reddit.com/user/ReviewMost4463/)** — [[website / GitHub / X links here]](https://github.com/antonio86itna).
