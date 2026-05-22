# GitHub Profile README Redesign — Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the template-heavy profile README with a hand-crafted terminal/neon/dark-academia design, and remove the snake animation workflow.

**Architecture:** Single-file Markdown rewrite with Unicode/ASCII terminal art. Zero external image dependencies. Monospace-first typography with `#00D4FF` (cyan) and `#CC7832` (amber) accent colors on `#0a0a0a` canvas. No stats cards, no shields.io badges, no snake animation.

**Tech Stack:** GitHub Flavored Markdown, Unicode box-drawing characters, HTML `<pre>` / code blocks for monospace preservation

---

### Task 1: Remove Snake Animation Workflow

**Files:**
- Delete: `.github/workflows/snake.yml`

- [ ] **Step 1: Delete the workflow file**

```bash
rm .github/workflows/snake.yml
```

- [ ] **Step 2: Verify removal**

```bash
ls .github/workflows/ 2>&1 || echo "directory empty or removed"
```

Expected: directory empty or removed

- [ ] **Step 3: Commit**

```bash
git add .github/workflows/snake.yml
git commit -m "chore: remove snake animation workflow"
```

---

### Task 2: Rewrite README.md — Terminal Header + §1 THE SIGNAL

**Files:**
- Modify: `README.md` (complete rewrite in staged tasks)

The README will be built in sections. This task writes the header and "who am I" prose.

- [ ] **Step 1: Write the header section**

```markdown
<div align="center">

<pre style="font-family: 'SF Mono', 'Fira Code', 'JetBrains Mono', monospace; color: #c9d1d9; background: #0a0a0a; line-height: 1.6;">

╔══════════════════════════════════════════════════════════════╗
║                                                              ║
║   <span style="color: #CC7832;">root</span>@<span style="color: #00D4FF; font-weight: bold;">forest-isle</span>:<span style="color: #CC7832;">~</span># whoami                ║
║   <span style="color: #00D4FF; font-size: 2em; font-weight: bold;">Forest Isle</span>                                          ║
║                                                              ║
║   <span style="color: #CC7832;">root</span>@<span style="color: #00D4FF; font-weight: bold;">forest-isle</span>:<span style="color: #CC7832;">~</span># cat /etc/motd               ║
║   the stack is deep. i live between the kernel              ║
║   and the void. building things that think.                  ║
║   breaking things that defend.                               ║
║                                                              ║
╚══════════════════════════════════════════════════════════════╝

</pre>

</div>

<br/>
```

- [ ] **Step 2: Write §1 THE SIGNAL (self-description prose)**

```markdown
---

<br/>

<div align="center">

<pre style="font-family: 'SF Mono', 'Fira Code', 'JetBrains Mono', monospace; color: #c9d1d9; background: transparent; line-height: 1.8; text-align: left; display: inline-block; max-width: 720px; white-space: pre-wrap;">

<span style="color: #CC7832;">// §1 — THE SIGNAL</span>

  deep in the stack, between CUDA kernels and Win32 syscalls,
  where LLMs meet evasions and Rust rewrites C++ nightmares.

  i build things that think, break things that defend,
  and occasionally write assembly for fun.

  low-level by choice. high-impact by design.
  not a job title — an obsession.

</pre>

</div>

<br/>
```

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: rewrite README with terminal header and signal section"
```

---

### Task 3: Write §2 THE STACK (Skills as Terminal Tree)

**Files:**
- Modify: `README.md` (append after §1)

- [ ] **Step 1: Write the skills as a box-drawn terminal tree**

```markdown
---

<br/>

<div align="center">

<pre style="font-family: 'SF Mono', 'Fira Code', 'JetBrains Mono', monospace; color: #c9d1d9; background: transparent; line-height: 1.6; text-align: left; display: inline-block;">

<span style="color: #CC7832;">// §2 — THE STACK</span>
<span style="color: #CC7832;">root</span>@<span style="color: #00D4FF;">forest-isle</span>:<span style="color: #CC7832;">~</span># tree /arsenal

<span style="color: #CC7832;">/arsenal</span>
├── <span style="color: #CC7832;">languages/</span>
│   ├── cpp      <span style="color: #6e7681;">[primary blade]</span>
│   ├── rust     <span style="color: #6e7681;">[the rewrite]</span>
│   ├── python   <span style="color: #6e7681;">[the glue]</span>
│   ├── go       <span style="color: #6e7681;">[the dispatch]</span>
│   ├── c        <span style="color: #6e7681;">[the root]</span>
│   ├── ts       <span style="color: #6e7681;">[the interface]</span>
│   ├── bash     <span style="color: #6e7681;">[the stitch]</span>
│   └── x86_64   <span style="color: #6e7681;">[the truth]</span>
├── <span style="color: #CC7832;">ai-ml/</span>
│   ├── pytorch
│   ├── cuda
│   ├── transformers
│   ├── langchain
│   ├── vllm
│   ├── ollama
│   └── jax
├── <span style="color: #CC7832;">offensive/</span>
│   ├── reverse-engineering
│   ├── malware-analysis
│   ├── red-team-ops
│   ├── exploit-dev
│   ├── win32-api
│   ├── pwntools
│   ├── ida-pro
│   └── edr-evasion
└── <span style="color: #CC7832;">infra/</span>
    ├── arch
    ├── kali
    ├── docker
    ├── k8s
    ├── neovim
    ├── git
    ├── cmake
    └── gdb

</pre>

</div>

<br/>
```

- [ ] **Step 2: Commit**

```bash
git add README.md
git commit -m "feat: add terminal tree skills section"
```

---

### Task 4: Write §3 THE ARSENAL (Projects)

**Files:**
- Modify: `README.md` (append after §2)

- [ ] **Step 1: Write the project blocks**

```markdown
---

<br/>

<div align="center">

<pre style="font-family: 'SF Mono', 'Fira Code', 'JetBrains Mono', monospace; color: #c9d1d9; background: transparent; line-height: 1.5; text-align: left; display: inline-block;">

<span style="color: #CC7832;">// §3 — THE ARSENAL</span>
<span style="color: #CC7832;">root</span>@<span style="color: #00D4FF;">forest-isle</span>:<span style="color: #CC7832;">~</span># ls -la /ops

</pre>

</div>

<br/>

<!-- CHIMERA -->
<div align="center">

<pre style="font-family: 'SF Mono', 'Fira Code', 'JetBrains Mono', monospace; color: #c9d1d9; background: transparent; line-height: 1.5; text-align: left; display: inline-block;">

┌─[ <a href="https://github.com/Forest-Isle/chimera" style="color: #DC143C;">chimera</a> ]─────────────────────────────────────────────────────┐
│  EDR evasion through syscall proxying and memory manipulation.    │
│  The ghost in the machine that the scanner never sees.            │
│                                                                   │
│  <span style="color: #CC7832;">:: deps</span>   C++  ·  Win32  ·  x64 asm                              │
│  <span style="color: #CC7832;">:: status</span>  active                                               │
└───────────────────────────────────────────────────────────────────┘

</pre>

</div>

<br/>

<!-- SYNAPSE -->
<div align="center">

<pre style="font-family: 'SF Mono', 'Fira Code', 'JetBrains Mono', monospace; color: #c9d1d9; background: transparent; line-height: 1.5; text-align: left; display: inline-block;">

┌─[ <a href="https://github.com/Forest-Isle/synapse" style="color: #00D4FF;">synapse</a> ]─────────────────────────────────────────────────────┐
│  Multi-agent AI framework with MCP integration.                   │
│  Autonomous task execution. Swarms that finish each other's        │
│  sentences.                                                       │
│                                                                   │
│  <span style="color: #CC7832;">:: deps</span>   Python  ·  MCP  ·  LLMs                                 │
│  <span style="color: #CC7832;">:: status</span>  active                                               │
└───────────────────────────────────────────────────────────────────┘

</pre>

</div>

<br/>

<!-- IRONCLAW -->
<div align="center">

<pre style="font-family: 'SF Mono', 'Fira Code', 'JetBrains Mono', monospace; color: #c9d1d9; background: transparent; line-height: 1.5; text-align: left; display: inline-block;">

┌─[ <a href="https://github.com/Forest-Isle/IronClaw" style="color: #8B0000;">IronClaw</a> ]─────────────────────────────────────────────────────┐
│  Rust-based C2 infrastructure with gRPC transport.                │
│  Modular implants. Your network, my rules.                         │
│                                                                   │
│  <span style="color: #CC7832;">:: deps</span>   Rust  ·  gRPC  ·  TLS                                     │
│  <span style="color: #CC7832;">:: status</span>  active                                               │
└───────────────────────────────────────────────────────────────────┘

</pre>

</div>

<br/>

<!-- ARGON -->
<div align="center">

<pre style="font-family: 'SF Mono', 'Fira Code', 'JetBrains Mono', monospace; color: #c9d1d9; background: transparent; line-height: 1.5; text-align: left; display: inline-block;">

┌─[ <a href="https://github.com/Forest-Isle/argon" style="color: #76B900;">argon</a> ]─────────────────────────────────────────────────────────┐
│  GPU inference optimization with CUDA kernels and TensorRT.        │
│  Every wasted cycle is an insult.                                  │
│                                                                   │
│  <span style="color: #CC7832;">:: deps</span>   CUDA  ·  PyTorch  ·  TensorRT                               │
│  <span style="color: #CC7832;">:: status</span>  active                                               │
└───────────────────────────────────────────────────────────────────┘

</pre>

</div>

<br/>

<!-- ALPHAFORGE -->
<div align="center">

<pre style="font-family: 'SF Mono', 'Fira Code', 'JetBrains Mono', monospace; color: #c9d1d9; background: transparent; line-height: 1.5; text-align: left; display: inline-block;">

┌─[ <a href="https://github.com/Forest-Isle/AlphaForge" style="color: #FF6F00;">AlphaForge</a> ]───────────────────────────────────────────────────┐
│  Autonomous coding agent with tool-use and memory.                 │
│  Self-reflection loops. It learns from its own mistakes.           │
│                                                                   │
│  <span style="color: #CC7832;">:: deps</span>   TypeScript  ·  AI SDK  ·  Tool-use                          │
│  <span style="color: #CC7832;">:: status</span>  active                                               │
└───────────────────────────────────────────────────────────────────┘

</pre>

</div>

<br/>

<!-- NYXRAT -->
<div align="center">

<pre style="font-family: 'SF Mono', 'Fira Code', 'JetBrains Mono', monospace; color: #c9d1d9; background: transparent; line-height: 1.5; text-align: left; display: inline-block;">

┌─[ <a href="https://github.com/Forest-Isle/nyxrat" style="color: #FF0000;">nyxrat</a> ]───────────────────────────────────────────────────────┐
│  Stealth post-exploitation toolkit with encrypted C2.              │
│  When you need to be in and out before anyone notices.             │
│                                                                   │
│  <span style="color: #CC7832;">:: deps</span>   C++  ·  Sockets  ·  Crypto                                    │
│  <span style="color: #CC7832;">:: status</span>  active                                               │
└───────────────────────────────────────────────────────────────────┘

</pre>

</div>

<br/>
```

- [ ] **Step 2: Commit**

```bash
git add README.md
git commit -m "feat: add terminal-style project arsenal section"
```

---

### Task 5: Write §4 THE WIRE + §5 FOOTER, Complete README

**Files:**
- Modify: `README.md` (append final sections)

- [ ] **Step 1: Write THE WIRE contact section**

```markdown
---

<br/>

<div align="center">

<pre style="font-family: 'SF Mono', 'Fira Code', 'JetBrains Mono', monospace; color: #c9d1d9; background: transparent; line-height: 1.6; text-align: left; display: inline-block;">

<span style="color: #CC7832;">// §4 — THE WIRE</span>
<span style="color: #CC7832;">root</span>@<span style="color: #00D4FF;">forest-isle</span>:<span style="color: #CC7832;">~</span># nc -lvp 31337

<span style="color: #6e7681;">Listening on [0.0.0.0]:31337 ...</span>

  <span style="color: #CC7832;">></span> <span style="color: #00D4FF;">gh</span>      <a href="https://github.com/Forest-Isle" style="color: #c9d1d9;">github.com/Forest-Isle</a>
  <span style="color: #CC7832;">></span> <span style="color: #00D4FF;">mail</span>    <a href="mailto:forest.isle@proton.me" style="color: #c9d1d9;">forest.isle@proton.me</a>

</pre>

</div>

<br/>
```

- [ ] **Step 2: Write FOOTER sign-off**

```markdown
---

<br/>

<div align="center">

<pre style="font-family: 'SF Mono', 'Fira Code', 'JetBrains Mono', monospace; color: #6e7681; background: transparent; line-height: 1.6;">

<span style="color: #6e7681;">// the quieter you become, the more you are able to hear</span>

</pre>

</div>

<br/>

<!--
    hidden in plain sight.

    If you're reading this, you know the game.
    Reach out. Let's build something that matters.
-->
```

- [ ] **Step 3: Verify the complete file is well-formed**

Read the full README.md and confirm:
- All HTML tags close properly
- All links have correct `href` attributes
- No stray template artifacts remain
- File renders cleanly (check in your head — monospace blocks aligned, colors consistent)

- [ ] **Step 4: Commit**

```bash
git add README.md
git commit -m "feat: add contact wire and footer, finalize README redesign"
```

---

### Task 6: Push and Verify

- [ ] **Step 1: Push to GitHub**

```bash
git push origin main
```

- [ ] **Step 2: Visit profile page**

Open `https://github.com/Forest-Isle` in browser and verify:
- Page renders without errors
- All links work
- Dark mode looks correct (colors visible, contrast good)
- Light mode is readable (check via GitHub appearance toggle)
- Mobile viewport looks clean

- [ ] **Step 3: Fix any rendering issues**

If colors don't render (GitHub strips inline styles from `<span>` in some contexts), fall back to using only semantic HTML tags and GitHub's native syntax highlighting. The `pre` blocks with monospace will work regardless.
