# Elements of Style

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill that applies the writing principles from William Strunk Jr.'s *The Elements of Style* (1918) to any prose.

Distilled from the [public domain original](https://www.gutenberg.org/files/37134/37134-h/37134-h.htm) into a concise, actionable reference that fits in an LLM's context window.

## What it does

When triggered, the skill reads a compact principle reference and applies Strunk's 18 rules to your writing. It works for new drafts and revisions alike.

The revision workflow follows a specific order: **Sharpen** (add specificity) → **Cut** (remove filler) → **Activate** (use active voice, positive form) → **Structure** (paragraphs, parallel form, emphasis) → **Polish** (punctuation, word choice).

Key editorial decisions baked in:
- **Specificity beats conciseness.** Rule 12 outranks Rule 13. Never cut words that add specific meaning in the name of brevity.
- **Em dashes are flagged.** Rule 5 is updated to "Do not join independent clauses by a comma *or an em dash*." LLMs overuse em dashes; this skill treats them as a writing tell to correct.

## Install

Copy the skill folder into your Claude Code skills directory:

```bash
mkdir -p ~/.claude/skills/elements-of-style
cp SKILL.md elements-of-style.md ~/.claude/skills/elements-of-style/
```

The skill will trigger automatically when you use phrases like "elements of style," "tighten this," "edit for clarity," "make this concise," or "improve the writing."

## Files

- **`SKILL.md`** — Trigger configuration, usage instructions, and the revision workflow
- **`elements-of-style.md`** — The distilled principle reference (~4KB, all 18 rules plus word usage guidance)

## Source

Based on William Strunk Jr., *The Elements of Style* (1918). The original text is in the public domain.

## License

MIT
