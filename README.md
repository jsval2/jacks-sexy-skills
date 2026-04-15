# Jack's Sexy Skills

A curated pack of Claude Code slash commands and skills. Thinking partners, creative engines, and research pipelines — drop them into your `~/.claude/` and invoke with `/skill-name`.

## What's in here

| Skill | Invoke | What it does |
|---|---|---|
| **Systems Thinking Partner** | `/js-systems-thinking` | Analyse any situation through systems-thinking lenses — stocks/flows, feedback loops, leverage points, archetypes. Includes the full Meadows/Senge/Forrester knowledge base as references. |
| **First Principles Partner** | `/js-first-principles` | Breaks any problem — business, technical, personal, strategic — down to irreducible fundamentals and rebuilds from the ground up. Socratic coach + knowledge engine. |
| **Sales Copy CIA** | `/sales-copy-cia` | Generates high-conversion copy using two stacked systems: a behavioural-psychology persuasion engine and master-level direct-response frameworks (Schwartz, Halbert, Hopkins, Ogilvy, Bencivenga, Carlton, Kennedy). Includes a "master directive" reference covering CIA/KUBARK psychology, fMRI neuroscience of buying, Milton Model hypnotic language, and the 12 Laws of Deep Persuasion. Use responsibly. |
| **Excalidraw Diagram Generator** | `/excalidraw` | Turns a description into a valid Excalidraw JSON file with the right diagram type, layout, and visual structure. Ships with schema docs, layout patterns, and annotated examples. |
| **Deep Research** | `/deep-research` | Executes an 8-phase research pipeline to produce comprehensive, rigorously sourced research on any topic. |
| **Skill Creator** | `/create-skill` | Meta-skill. Guides you through creating your own Claude Code slash commands with proper structure, references, and invocation patterns. Use this to build the next one. |

## Install

Clone anywhere, then copy the two folders into your Claude config:

```bash
git clone https://github.com/jsval2/jacks-sexy-skills.git
cd jacks-sexy-skills

# Copy commands (the slash-command prompts)
cp commands/*.md ~/.claude/commands/

# Copy skills (the reference knowledge bases)
cp -r skills/* ~/.claude/skills/
```

That's it. Restart Claude Code (or open a new session) and the slash commands will be available globally.

### Install only what you want

```bash
cp commands/js-systems-thinking.md ~/.claude/commands/
cp -r skills/js-systems-thinking ~/.claude/skills/
```

### Update later

```bash
cd jacks-sexy-skills && git pull
cp commands/*.md ~/.claude/commands/
cp -r skills/* ~/.claude/skills/
```

## How these skills work (for the curious)

Each skill is two pieces:

1. **`commands/<name>.md`** — the slash-command prompt. This is the "engine" Claude loads when you type `/<name>`. It defines the persona, workflow, and which reference files to read.
2. **`skills/<name>/references/*.md`** — the knowledge base. The command file stays lean; detailed frameworks, examples, and patterns live here and are pulled in on demand.

Paths inside the command files use `~/.claude/skills/...`, so as long as you install to the standard locations, everything just works.

To build your own, run `/create-skill` — it'll walk you through the structure.

## What these are NOT

- Not MCP servers. No servers to run, no auth, no env vars.
- Not a framework. Just prompts + reference docs.
- Not production-certified. These are personal tools shared as-is. Read them, tweak them, make them yours.

## License

MIT. Use them, fork them, rename them, ship them. Attribution appreciated but not required.

Built by [Jack Stephen](https://github.com/jsval2) — Valentis AI Labs.
