# video-gen

> Generate AI video from text or images using fal.ai models (Kling, Veo, LTX, Wan). Smart router picks the best model by video type.

**Free. Apache 2.0. Bring-your-own-Claude.**

## What this is

A Claude skill bundle — a sanitized, attributed, downloadable subject-matter expert that runs inside Claude Code, Claude Desktop, or any Claude-API workflow. Drop it in, invoke it, get answers grounded in real practitioner content rather than generic LLM consensus.

Use when generating AI video from text prompts or image-to-video, picking a model per video type (cinematic, animated, talking-head, action).

## Install

```bash
# Claude Code plugin install (one-line)
claude plugin install video-gen --from https://fadaly.net/downloads/skills/video-gen.zip
```

Or clone this repo into your Claude skills directory:

```bash
git clone https://github.com/MomoFadaly/video-gen.git ~/.claude/skills/video-gen
```

Or download the zip from [fadaly.net/skills/video-gen](https://fadaly.net/skills/video-gen) (the per-skill landing page on fadaly.net) and extract into `~/.claude/skills/`.

## What's in the bundle

| File | Size |
|---|---|
| `SKILL.md` | 1KB |
| `thumb.png` | 1.75MB |

Total: 1.75MB

## Sources

This SME's canon was built from these practitioners. Every claim in the canon is attributed.

- fal.ai (fal.ai) — model gateway
- Kling · Veo · LTX · Wan — underlying video models

Primary sources (official documentation, peer-reviewed research) take priority over practitioner consensus, which takes priority over single-source claims. Confidence tiers are tagged inline.

## How it works

Claude reads `SKILL.md` as the system instructions for the skill. Supporting files (`canon.md`, `mental-models.md`, etc.) are loaded as reference material when the skill needs to answer off the cuff or cite a specific source.

When you ask a question this SME covers, Claude pulls the relevant canon entry, names its source, tags its confidence level, and pushes back if your question contradicts canon.

## Confidence levels

- **Verified** — primary source + practitioner corroboration. Treat as fact.
- **Confirmed** — practitioner consensus across credible voices, no primary contradiction. Defended best-practice.
- **Plausible** — single-source or thin evidence. Working hypothesis until validated.
- **Disputed** — credible voices disagree. The SME names the camps and gives you the lens to decide.
- **Stale** — once true, contradicted by current docs/data. Flagged for refresh.

## License

Apache License 2.0. See [LICENSE](LICENSE).

You are free to use, modify, redistribute, and build on this skill. Attribution to the original practitioners (named in `sources.md` or `SKILL.md`) is morally required even if not legally; their work made the canon possible.

## Built by

[Mo Fadaly](https://fadaly.net) — AI intrapreneur, runs Claude skills in production.

This is one of a series. See the [full catalog at fadaly.net/work](https://fadaly.net/work).
