# GitHub Profile Redesign — `root@forest-isle:~#`

## Summary

Tear down the template-heavy, badge-cluttered profile README and rebuild from zero.
The new profile speaks with Forest Isle's own voice — a terminal skeleton, neon pulses,
and dark-academia breathing room. No stats cards. No shields.io. No snake animation.
Just what matters, rendered with craft.

---

## Visual System

### Palette
- **Canvas**: `#0a0a0a` deep black, leveraging GitHub dark mode
- **Primary / Neon**: `#00D4FF` electric cyan — highlights, links, cursor pulse
- **Secondary / Amber**: `#CC7832` warm amber — section headers, category labels, terminal warning tone
- **Text**: `#c9d1d9` (GitHub default light grey) for body
- **Muted**: `#6e7681` for secondary text, timestamps, footnotes

### Typography
- **Primary**: `SF Mono`, `Fira Code`, `JetBrains Mono` — monospace stack for all terminal content
- **Accent**: system sans-serif stack for contrast labels where needed

### Spacing
- Heavy vertical whitespace between sections (60–80px equivalent)
- Each section is a self-contained visual block
- No horizontal crowding — wide gutters, narrow content column

### Principles
- Every element must look hand-placed, not template-generated
- ASCII box-drawing over HTML tables where possible
- Zero external API-dependent images (no capsure-render, no readme-stats, no typing-svg, no trophy, no streak, no activity-graph, no snake, no quote widget)
- The README must render correctly on both GitHub dark and light mode without JavaScript

---

## Layout & Content Architecture

### HEADER — Custom Terminal Window

A hand-built SVG or ASCII art block simulating a terminal frame:
```
┌──────────────────────────────────────────────────────────────┐
│  root@forest-isle:~# whoami                                  │
│  Forest Isle                                                 │
│                                                              │
│  root@forest-isle:~# cat /etc/motd                           │
│  the stack is deep. i live between the kernel and the void.  │
└──────────────────────────────────────────────────────────────┘
```

- Neon cyan `Forest Isle` name
- Below it: one-line tagline in amber, poetic, not keyword-stuffed
- No waving banner, no typing animation, no gradient capsule

### §1 — THE SIGNAL (Self-Description)

4–6 lines of prose. Dark-academia tone. Not a resume bullet list — a credo.
Written in monospace, indented like a decrypted field report.
Wide left margin. Reads like a page from a notebook found in a crashed server room.

Topics to touch:
- The space between CUDA kernels and Win32 syscalls
- Building things that think, breaking things that defend
- Low-level by choice, high-impact by design
- Not a job title — an obsession

### §2 — THE STACK (Skills as Terminal Output)

Replace all shields.io badges with a box-drawn terminal tree:

```
root@forest-isle:~# tree /arsenal --charset=utf-8

/arsenal
├── languages/
│   ├── cpp    [primary blade]
│   ├── rust   [the rewrite]
│   ├── python [the glue]
│   ├── go     [the dispatch]
│   ├── c      [the root]
│   ├── ts     [the interface]
│   ├── bash   [the stitch]
│   └── x86_64 [the truth]
├── ai-ml/
│   ├── pytorch
│   ├── cuda
│   ├── transformers
│   ├── vllm
│   └── jax
├── offensive/
│   ├── reverse-engineering
│   ├── malware-analysis
│   ├── red-team-ops
│   ├── exploit-dev
│   ├── win32-api
│   └── edr-evasion
└── infra/
    ├── arch
    ├── kali
    ├── docker
    ├── neovim
    └── gdb
```

Category labels in amber (`#CC7832`), items in text grey, bracketed annotations in muted grey.
Clean, scannable, no external image URLs.

### §3 — THE ARSENAL (Projects)

Six projects. Each formatted as a terminal block:

```
┌─[ chimera ]──────────────────────────────────────────────────┐
│  EDR evasion through syscall proxying.                       │
│  The ghost in the machine that the scanner never sees.       │
│                                                              │
│  :: deps   C++  ·  Win32  ·  x64 asm                        │
│  :: status  active                                            │
└──────────────────────────────────────────────────────────────┘
```

Six entries: Synapse, Chimera, IronClaw, Argon, AlphaForge, NyxRAT.
Each with a two-line description that has attitude, not README-speak.
Tech tags as `:: deps` line.
No shields.io badges. No HTML tables. Pure monospace terminal blocks.

### §4 — THE WIRE (Contact)

One clean block:

```
root@forest-isle:~# nc -lvp 31337
Listening on [0.0.0.0]:31337 ...

  > gh      github.com/Forest-Isle
  > mail    forest.isle@proton.me
  > key     [PGP fingerprint if available]
  > x       @<handle>
```

Minimal. No badges. No visitor counter. No Komarev hit tracker.

### §5 — FOOTER (Sign-off)

A single line in muted grey, centered:
```
// the quieter you become, the more you are able to hear
```

HTML comment block below for those who read source:
```html
<!--
    hidden in plain sight.
    If you're reading this, you know the game.
    Reach out. Let's build something that matters.
-->
```

No footer banner SVG. No quote widget.

---

## What Gets Removed

- `capsule-render.vercel.app` header and footer SVGs
- `readme-typing-svg` typing animation
- All `img.shields.io` badges (arsenal table + project badges + battle honours + comms)
- GitHub readme-stats cards (stats, top langs, streak)
- GitHub profile trophy grid
- GitHub readme-activity-graph
- Contribution grid snake animation (including the `snake.yml` workflow)
- Komarev visitor counter
- Random dev quote widget
- The animated divider GIF

---

## Implementation Notes

### File Changes
- **`README.md`**: Complete rewrite (~200–300 lines of clean markdown + ASCII art)
- **`.github/workflows/snake.yml`**: Delete (no longer needed)

### Constraints
- Pure Markdown + Unicode/ASCII art — no external image dependencies that can break
- Readable on both dark and light GitHub themes
- No JavaScript
- Monospace-preserving formatting (use code blocks with appropriate language tags)
- All links preserved, just re-styled

### Testing
- Preview on GitHub dark mode
- Preview on GitHub light mode
- Verify all links resolve
- Verify mobile rendering (narrow viewport)
