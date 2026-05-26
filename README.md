# Write and Humanize

A skill for AI coding agents to write, draft, revise, and humanize nonfiction content with genuine voice and clarity.

## Overview

This skill combines two capabilities:

- **Nonfiction Writing** — based on *On Writing Well* by William Zinsser and *Storyworthy* by Matthew Dicks. Covers essays, memoirs, op-eds, profiles, travel writing, science/tech writing, business writing, and long-form journalism.
- **Humanizer** — based on Wikipedia's "Signs of AI writing" guide (WikiProject AI Cleanup). Strips inflated language, AI vocabulary, rule-of-three, em dash overuse, vague attributions, sycophantic tone, negative parallelisms, and 20+ other telltale AI patterns.

Use either capability on its own or both together.

---

## Installation

### OpenCode (OhMyOpenCode)

Copy the skill to your OpenCode skills directory:

```bash
mkdir -p ~/.config/opencode/skills/write-well
cp SKILL.md ~/.config/opencode/skills/write-well/SKILL.md
```

Then load the skill by name in tasks:

```js
task(
  category="writing",
  load_skills=["write-and-humanize"],
  prompt="Write a personal essay about..."
)
```

The skill is also available as the `/write-and-humanize` slash command.

### Claude Code (Anthropic)

Place the `SKILL.md` file in your project's `.claude/skills/` directory:

```bash
mkdir -p .claude/skills/write-well
cp SKILL.md .claude/skills/write-well/SKILL.md
```

Reference it in your `.claude/CLAUDE.md` project instructions:

```
Always load the write-and-humanize skill when the user asks to write, revise, or humanize any piece of writing.
```

### Cline (VS Code Extension)

Copy `SKILL.md` into your Cline custom instructions directory, or add its contents to your `.clinerules` file:

```bash
cat SKILL.md >> .clinerules
```

### GitHub Copilot / Other Chat Agents

Include the relevant sections of `SKILL.md` in your custom instructions or agent prompt context. The key sections are:

- **Part One: Nonfiction Writing** — for drafting new content
- **Part Two: Humanizer — Remove AI Writing Patterns** — for editing existing drafts
- **Process sections** — for step-by-step workflows

---

## Quick Start

**Writing something new:** Load the skill and say "Write a personal essay about [topic]." The agent applies the five-second moment framework, unity table, clutter test, and voice principles from Zinsser and Dicks.

**Humanizing existing text:** Load the skill and say "Humanize this: [text]." The agent strips AI patterns and injects genuine voice.

**Revising an AI draft:** Say "Revise this draft: [text]." The agent applies nonfiction craft first, then humanizer patterns.

---

## What It Covers

| Capability | What It Does |
|---|---|
| Five-Second Moment | Find the one transformative instant your piece revolves around |
| Unity Table | Choose voice, tone, stance, scope, tense before writing |
| Lead + Ending | Craft openings that hook and endings that stick |
| Clutter Test | Strip adverbs, redundancy, passive voice, throat-clearing |
| Voice & Vulnerability | Write like a human, not a brochure |
| 24 AI Pattern Detectors | Catch and fix every common AI writing tic (em dashes, synonym cycling, false ranges, etc.) |
| Form-Specific Guides | Essays, profiles, travel, science, business, op-eds |

---

## Credits

This skill draws directly from three sources:

- **William Zinsser** — *On Writing Well* (1976). The definitive guide to clarity, simplicity, and voice in nonfiction. The Clutter Test, Unity Table, and much of the craft guidance originate here.
- **Matthew Dicks** — *Storyworthy* (2018). The five-second moment, transformation arc, and "but/therefore" story structure come from Dicks's approach to finding and telling compelling stories.
- **Wikipedia contributors** — "Signs of AI writing" (WikiProject AI Cleanup). The comprehensive catalog of AI-generated writing patterns — from em dash overuse to synonym cycling to false ranges — that forms the Humanizer half of this skill.

---

## License

Apache 2.0. See [LICENSE](LICENSE).
