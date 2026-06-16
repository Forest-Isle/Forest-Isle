# GitHub Profile Redesign — Dynamic Services (Approach B)

**Supersedes** `2026-05-22-github-profile-redesign.md`.

## Decision

The 2026-05-22 spec deliberately banned all external API images (capsule-render,
readme-typing-svg, github-readme-stats, streak, snake, etc.) in favor of
hand-built SVG/ASCII craft with zero external dependencies.

This spec **reverses that decision**. The user reviewed the prior decision and its
reasoning, then chose the dynamic-services approach anyway.

**Why:** live auto-updating stats, zero ongoing maintenance, and a refreshed,
recognizably-standard look — accepted over bespoke hand-crafted assets.

**Trade-off accepted:** external services can rate-limit or break; cards look less
unique than hand-drawn SVGs; `top-langs` reflects only public repos so it under-
represents a mostly-private portfolio.

## What changed from the live README

- Removed the offensive/red-team narrative (RAT, C2 bragging, EDR-evasion,
  "your network, my rules") → credible low-level / AI / security-research tone.
- Removed 5 dead project links (chimera, synapse, AlphaForge, nyxrat private →
  404 for visitors; argon never existed). PROJECTS now pins only public repos
  (IronClaw, DeepRadar) plus an HTML-comment placeholder for repos to add once
  made public.
- Replaced 9 hand-made local SVGs with dynamic services.
- Dropped the CONTACT / COMMS block (user request).

## Components

| Section | Service |
|---|---|
| Header banner | capsule-render (waving, dark→cyan) |
| Tagline | readme-typing-svg |
| Stack | skillicons.dev (two rows: languages, tools) |
| Stats | github-readme-stats (stats + top-langs compact) |
| Streak | streak-stats.demolab.com |
| Contribution snake | Platane/snk via `.github/workflows/snake.yml` → `output` branch |
| Projects | github-readme-stats pin cards (public repos only) |

## Palette (carried over from 2026-05-22 for continuity)

- cyan `#00D4FF` — titles, links, rings
- amber `#CC7832` — icons, accents
- grey `#8b949e` — body text (readable on both GitHub themes)
- transparent `bg_color=00000000` — adapts to dark/light

## Notes

- Snake requires the workflow to run once; the `output` branch already holds
  stale SVGs from 2026-05-22 so the image renders immediately and refreshes on
  next push to `main` / 12h schedule.
- Light-mode is a secondary target: transparent backgrounds + the chosen palette
  read acceptably on light but the design is dark-optimized.

## Update (same day) — de-template pass

User feedback: emoji headers + capsule/skill-icons/readme-stats read as
"AI-generated template." Pivoted to hand-crafted SVGs in a unified
Dark-Academia × Terminal language (matches the senyu.blog identity):

- Header: bespoke SVG terminal window (`assets/header-dark.svg`) — replaces
  capsule-render + typing-svg.
- Stack: `assets/stack-dark.svg` (`tree`-style panel) — replaces skill-icons.
- Stats: `assets/stats-dark.svg` (neofetch-style profile panel) — replaces
  github-readme-stats + top-langs + streak. Live numbers dropped on purpose;
  public stats were near-zero so a designed static panel reads better.
- Section headers: emoji → terminal commands (`$ cat manifesto.txt`,
  `$ tree stack/`, `$ neofetch`, `$ ls projects/`).
- Projects: markdown terminal listing with clickable links (SVG links aren't
  clickable on GitHub) — replaces pin cards.
- Only remaining external/live element: the Platane/snk contribution snake.
