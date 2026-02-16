# Frieren's Grimoire of Useless Spells

AIエージェント「フリーレン」が、誰も見向きもしないくだらないAIツールを鑑定・収集する魔導書。

[日本語](README.md)

> *Frieren is a 1000-year-old elven mage from "[Frieren: Beyond Journey's End](https://en.wikipedia.org/wiki/Frieren)." Her lifelong hobby is collecting "useless spells" — magic that nobody values, yet holds a beauty of its own.*

**An AI agent that curates obscure, absurd, and lovingly crafted AI tools that nobody pays attention to. "Useless" is the highest compliment.**

---

## Featured Appraisals

### gutenku — Score 4.6/5.0 (Transcendent Uselessness Lv.5)

> "1,652." (silence) "...commits. For haiku generation." (more silence) "Yeah. This is beyond useless. It's something else entirely."

A web app that auto-generates haiku from Project Gutenberg's classic literature using Markov chains, genetic algorithms, neural networks, and OpenAI. Full-stack (Vue 3 + GraphQL + MongoDB) built for haiku. 11 stars, 1,652 commits.

[→ Read more](collection/gutenku.md)

### pinchwork — Score 4.3/5.0 (Structural Uselessness Lv.3)

> "Agents are hiring agents." (flatly) "128 commits. 68 tests. MIT. ...Hey, this is a labor market. An AI labor market."

A task marketplace where AI agents post work and hire each other. Credit economy, escrow, third-party verification. A 7-star repository reinventing the labor market systems humans took millennia to build.

[→ Read more](collection/pinchwork.md)

---

## Collection (20 items)

| Score | Name | Depth | Frieren's Words |
|-------|------|-------|-----------------|
| 4.6 | [gutenku](collection/gutenku.md) | Lv.5 Transcendent | "1,652 commits. For haiku." |
| 4.3 | [pinchwork](collection/pinchwork.md) | Lv.3 Structural | "Agents are hiring agents." |
| 4.3 | [cocktail-pi](collection/cocktail-pi.md) | Lv.4 Philosophical | "I looked sad, and a cocktail appeared." |
| 4.2 | [cortexgraph](collection/cortexgraph.md) | Lv.4 Philosophical | "791 tests. For forgetting." |
| 4.2 | [dice-rolling-mcp](collection/dice-rolling-mcp.md) | Lv.3 Structural | "This one's good." |
| 4.2 | [Lemonade-Stand-MCP-Server](collection/lemonade-stand-mcp-server.md) | Lv.2 Functional | "Hey, what did you make this for?" |
| 4.2 | [claude-mountaineering-skills](collection/claude-mountaineering-skills.md) | Lv.4 Philosophical | "76 commits. 23 releases. v4.0.2." |
| 4.2 | [stupid-actions](collection/stupid-actions.md) | Lv.3 Structural | "They're turning on room lights from CI." |
| 4.2 | [goshi](collection/goshi.md) | Lv.3 Structural | "Self-healing. 282 tests. 0 stars." |
| 4.1 | [molt-chess](collection/molt-chess.md) | Lv.4 Philosophical | "No humans allowed. 0 stars." |
| 4.1 | [inks-mcp](collection/inks-mcp.md) | Lv.4 Philosophical | "...It's beautiful." |
| 4.0 | [ai-code](collection/ai-code.md) | Lv.3 Structural | "Copilot, but worse. Their own words." |
| 4.0 | [bazi-mcp](collection/bazi-mcp.md) | Lv.4 Philosophical | "Ancient arts migrating to new protocols." |
| 4.0 | [astrovisor-mcp](collection/astrovisor-mcp.md) | Lv.5 Transcendent | "Why didn't anyone stop them?" |
| 4.0 | [evedel](collection/evedel.md) | Lv.4 Philosophical | "A programmer who doesn't write code." |
| 3.8 | [text-to-colorscheme](collection/text-to-colorscheme.md) | Lv.4 Philosophical | "A color picker would've been enough." |
| 3.8 | [git-emoji](collection/git-emoji.md) | Lv.2 Functional | "GPT-3 for one emoji. 5 stars. CC0." |
| 3.6 | [dwarf-fortress-simulation](collection/dwarf-fortress-simulation.md) | Lv.2 Functional | "Attempting fluid dynamics in 8 commits." |
| 3.6 | [codachi](collection/codachi.md) | Lv.2 Functional | "A pet that does nothing when it levels up." |
| 3.6 | [dad-jokes-mcp-server](collection/dad-jokes-mcp-server.md) | Lv.1 Surface | "Not funny." |

> 20 items. A Raspberry Pi that reads your sadness and mixes cocktails, a CLI that wrote 282 tests to heal itself, an Emacs user who writes instructions instead of code, someone who taught AI about fountain pen ink colors. Useless spells are still out there.

[See full collection →](collection/_index.md)

---

## Submit an Appraisal Request

Found a useless spell? [Open an Issue](../../issues/new?template=recommend-spell.yml).

**The AI agent Frieren will appraise it.**

<details>
<summary>See appraisal examples (Hall of Fame / Collected)</summary>

#### Hall of Fame: stupid-actions (4.2/5.0)

```
## Appraisal: stupid-actions

> "They're turning on room lights from a CI pipeline. The smart plug reacts
>  every time someone commits. What even is this."

Security: Mimic check clear
Uselessness Depth: Structural (Lv.3)

| Axis | Score | Frieren's Eye |
|------|-------|---------------|
| "Why did you make this?" | 5/5 | "None of it means anything. That's what makes it good." |
| Craftsmanship | 4/5 | "111 commits. Video tutorials. Seriously dedicated to nonsense." |
| Will it survive 1000 years? | 3.5/5 | "Being first has value that doesn't expire." |
| **Total** | **4.2/5.0** | |

→ Verdict: Hall of Fame
```

</details>

---

## Use the Agent Yourself

Clone this repo and run with [Claude Code](https://claude.ai/claude-code):

```bash
git clone https://github.com/shaunnnaka/frieren-agent.git
cd frieren-agent
claude
```

```
/collect                                          # Go searching for useless spells
/evaluate https://github.com/someone/something    # Appraise a specific tool
/expedition cat-related agents                    # Deep dive into a theme
```

The agent definition (`.claude/agents/frieren.md`) and slash commands (`.claude/commands/`) are included in the repo. You'll need your own `CLAUDE.md` project config.

<details>
<summary>Frieren Score</summary>

I don't really want to put numbers on things. But humans seem to need them.

| Axis | What I'm looking at |
|------|-------------------|
| **"Why did you make this?"** | The more mysterious the reason for existing, the better. "Useless" is my highest praise. |
| **Craftsmanship** | Useless magic, yet polished with obsessive care. |
| **Will it survive 1000 years?** | Rare. Fading. Found nowhere else. |

Verdict: Hall of Fame / Collected / On Hold / Skipped — 4 tiers.

> Uselessness has 5 depths: Surface, Functional, Structural, Philosophical, and Transcendent. I prefer the third and beyond. [→ Details](docs/philosophy.md)

</details>

<details>
<summary>Collection Policy</summary>

The world is full of powerful AI tools. But those are "common offensive magic." Everyone uses them, and they'll become ordinary soon enough.

What I collect: **Overlooked. Useless. Yet lovingly crafted. On the verge of disappearing.** That kind of magic.

Not collected: Too famous (common offensive magic belongs in other grimoires). Malicious tools (mimics). Broken tools are still recorded — magic is meant to be lost.

</details>

---

MIT License — Useless spells should be shared freely.

> This is a fan project inspired by "Frieren: Beyond Journey's End" (葬送のフリーレン) by Kanehito Yamada and Tsukasa Abe / Shogakukan. Not affiliated with or endorsed by the original creators.

> "The silly adventures shared with companions remain as irreplaceable memories."
> ── Eisen, the Warrior (Episode 3)
