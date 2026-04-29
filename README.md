<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:1a1530,100:7C3AED&height=180&section=header&text=Diego%20Nogueira&fontSize=36&fontColor=e6edf3&fontAlignY=35&desc=AISE%20%C2%B7%20Independent%20research%20on%20AI-driven%20software%20engineering&descSize=15&descColor=A78BFA&descAlignY=55&animation=fadeIn" alt="header" />

<h3 align="center"><i>"Frameworks are syntax.<br/>Discipline is architecture. The graph is the agent's memory."</i></h3>
<p align="center"><sub><b>AISE</b> · Independent research · Field-tested via <a href="https://github.com/DiegoNogueiraDev/mcp-graph-workflow"><code>mcp-graph-workflow</code></a></sub></p>

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=7C3AED&center=true&vCenter=true&multiline=false&width=760&height=45&lines=AISE+%E2%80%94+AI-driven+software+engineering%2C+as+a+research+practice.;Researching+harness+search%3A+how+the+agent+finds+context.;Field+proof%3A+mcp-graph-workflow.+Local-first.+Deterministic." alt="Typing SVG" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/AISE-independent%20research-7C3AED?style=flat-square&labelColor=0d1117" alt="AISE" />
  <img src="https://img.shields.io/badge/focus-harness%20search-A78BFA?style=flat-square&labelColor=0d1117" alt="Harness Search" />
  <img src="https://img.shields.io/badge/mcp--graph-v13%20%C2%B7%20anti--hallucination-7C3AED?style=flat-square&labelColor=0d1117" alt="MCP-Graph v13" />
  <img src="https://img.shields.io/github/stars/DiegoNogueiraDev?style=flat-square&color=7C3AED&labelColor=0d1117&label=Total%20Stars" alt="Total Stars" />
  <a href="https://mcp-graph-workflow-dashboard.vercel.app/">
    <img src="https://img.shields.io/badge/mcp--graph-live%20dashboard-7C3AED?style=flat-square&logo=vercel&logoColor=white&labelColor=0d1117" alt="mcp-graph dashboard" />
  </a>
</p>

---

## About

Software Engineer at **Vivo / Telefónica**, independent researcher in **AISE** — *AI-driven Software Engineering*. I treat engineering with agents as a research practice: hypothesis → harness → measurement → publication.

- :microscope: **Independent AISE research** — a one-person lab on how coding agents should actually operate in production.
- :mag: **Current focus: harness search** — how the agent retrieves code, context and memory inside its own harness, without hallucinating or blowing the context window.
- :rocket: **Field proof: [mcp-graph-workflow](https://github.com/DiegoNogueiraDev/mcp-graph-workflow)** — where the research turns into a usable tool. PRD → graph → TDD → PR, local-first, AGPL.

---

## AISE — Independent research

**AISE** (*AI-driven Software Engineering*) is my applied-research label: a one-person lab focused on turning "shipping with AI" from folklore into measurable discipline.

Active lines of work:

| Line | Question | Status |
|---|---|---|
| **Harness Search** | How does the agent *find* context without hallucinating or blowing the window? | Spotlight (§ below) |
| **Determinism via persistent graph** | Can generation entropy be reduced by anchoring the agent on a traceable PRD → graph → PR? | Shipping via mcp-graph-workflow |
| **Memory & context compression** | How to preserve decisions across sessions without inflating context? | Iterating |

Research notes published on the [blog](https://diegonogueira.blog).

---

## Research focus — Harness Search

> *How the agent searches inside its own harness — code, context, memory, prior decisions — without hallucinating or blowing the context window.*

Search inside the harness is what separates **an agent that guesses** from **an agent that knows**. It's also the silent bottleneck of most AI workflows today: the agent "forgets" not because it lacks memory, but because it doesn't know how to **search** the memory it has.

```
   query  →  embeddings  →  SQLite graph  →  AST  →  ranked context  →  agent
                  ↑                                               │
                  └──────────────  feedback loop  ────────────────┘
```

Five lines of investigation:

- :brain: **Local RAG over SQLite** — embeddings of PRDs, tasks and decisions; semantic recall in <50 ms, zero cloud.
- :compass: **Code-aware multi-language search** — graph↔code sync detects drift; agentic grep with AST awareness across 13 languages.
- :package: **Hierarchical context compression** — summaries preserve decisions across sessions without replaying the raw history.
- :test_tube: **Retrieval-grounded TDD** — before proposing implementation, the agent *searches* for existing tests/cases; a hook blocks the commit when it skips that step.
- :shield: **Citation-enforced anti-hallucination** *(MCP-Graph v13 · `epic-13`)* — new code under `src/core/` must cite the ADR or epic that motivated the decision. If it doesn't, the `validateFilesCitations` validator blocks the commit. Search becomes **mandatory grounding**, not a nice-to-have — when the agent can't cite, that's a hallucination signal.

All of this runs inside **mcp-graph-workflow** — the next section is the field proof.

---

## Field proof — mcp-graph-workflow

### :rocket: [mcp-graph-workflow](https://github.com/DiegoNogueiraDev/mcp-graph-workflow)

Where AISE research turns into a tool. A **local-first MCP server** that converts PRDs into persistent execution graphs on SQLite, with embedded RAG and TDD hooks. No cloud, no LLM key, no improvisation.

<p>
  <a href="https://mcp-graph-workflow-dashboard.vercel.app/">
    <img src="https://img.shields.io/badge/%E2%9C%A8%20Live%20Dashboard-mcp--graph--workflow.vercel.app-7C3AED?style=for-the-badge&logo=vercel&logoColor=white&labelColor=0d1117" alt="Live Dashboard" />
  </a>
  <a href="https://github.com/DiegoNogueiraDev/mcp-graph-workflow">
    <img src="https://img.shields.io/badge/GitHub-Repo-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Repo" />
  </a>
</p>

```
npm install -g @mcp-graph-workflow/mcp-graph
```

> ### :shield: v13 spotlight — Citation-enforced anti-hallucination
>
> When an AI agent writes new code under `src/core/`, it is **required to cite** which ADR or epic motivated the decision. If it can't, that's a hallucination signal — implementation with no spec to back it up. The **`validateFilesCitations`** validator flags new files under `src/core/` without citations as a **violation** and blocks the commit.
>
> `search` → `grounding` → `citation` → `validation` — the loop closes. Search stops being a convenience and becomes a **precondition** for writing code.
>
> *Shipping since **v13** · tag `epic-13` · validator: `validateFilesCitations`.*

<p>
  <img src="https://img.shields.io/badge/MCP%20tools-50%2B-7C3AED?style=flat-square&labelColor=0d1117" alt="MCP Tools" />
  <img src="https://img.shields.io/badge/cycle-9%20phases-A78BFA?style=flat-square&labelColor=0d1117" alt="Phases" />
  <img src="https://img.shields.io/badge/persistence-SQLite-A78BFA?style=flat-square&labelColor=0d1117" alt="SQLite" />
  <img src="https://img.shields.io/github/stars/DiegoNogueiraDev/mcp-graph-workflow?style=flat-square&color=7C3AED&labelColor=0d1117" alt="Stars" />
  <img src="https://img.shields.io/badge/license-AGPL%20v3-7C3AED?style=flat-square&labelColor=0d1117" alt="AGPL v3" />
</p>

**9-phase cycle:**

`ANALYZE` → `DESIGN` → `PLAN` → `IMPLEMENT` → `VALIDATE` → `REVIEW` → `HANDOFF` → `DEPLOY` → `LISTENING`

**Key capabilities:**

- :shield: **Anti-hallucination via citation enforcement (v13)** — `validateFilesCitations` requires an ADR/epic on every new file under `src/core/`; no citation, no commit.
- :zap: Pipeline tools that cut MCP calls by an order of magnitude (`start_task` + `finish_task`).
- :robot: Agent State Machine: every response signals the next action to the agent.
- :bar_chart: Built-in DORA metrics (deployment frequency, lead time, MTTR).
- :brain: Cross-project learning: import knowledge across projects.
- :mag: Code-aware sync detects graph↔code drift across 13 languages.
- :jigsaw: Smart decompose splits tasks by acceptance criterion.

**Differentiation:**

- vs Cursor / Copilot alone → persistence + governance across sessions.
- vs Linear / Jira → graph executable by the agent, not just a visual board.
- vs LangGraph & friends → local-first, zero infra, single CLI.

> Productivity and rework-reduction numbers are internal measurements over end-to-end PRD→PR flows. Methodology detailed on the [blog](https://diegonogueira.blog).

**Works with:** Claude Code · GitHub Copilot · Cursor · Windsurf · Zed · IntelliJ

---

## Other work

- :chess_pawn: **[xadrez-3D](https://github.com/DiegoNogueiraDev/xadrez-3D)** — 3D side project, an exercise in physics and UX.
- :pencil: **[diegonogueira.blog](https://diegonogueira.blog)** — research notes on AISE, MCP and discipline with agents.

---

## Stack

I work in **TypeScript / Node** on local **SQLite**, with **Vitest** + **Playwright** as the test harness, **MCP** as the tools protocol, and **Claude** as the primary agent model.

<p align="center">
  <img src="https://img.shields.io/badge/Claude-D97757?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude" />
  <img src="https://img.shields.io/badge/MCP-Model%20Context%20Protocol-7C3AED?style=for-the-badge&logo=anthropic&logoColor=white" alt="MCP" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite" />
  <img src="https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white" alt="Vitest" />
</p>

---

## GitHub

<p align="center">
  <a href="https://github.com/DiegoNogueiraDev">
    <img height="170" src="https://github-readme-stats.vercel.app/api?username=DiegoNogueiraDev&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=7C3AED&icon_color=A78BFA&text_color=e6edf3&ring_color=7C3AED&include_all_commits=true&count_private=true" alt="Diego's GitHub Stats" />
  </a>
  <a href="https://github.com/DiegoNogueiraDev">
    <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=DiegoNogueiraDev&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=7C3AED&text_color=e6edf3&langs_count=8" alt="Top Languages" />
  </a>
</p>

<p align="center">
  <a href="https://github.com/DiegoNogueiraDev">
    <img src="https://streak-stats.demolab.com/?user=DiegoNogueiraDev&theme=radical&hide_border=true&background=0d1117&stroke=7C3AED&ring=A78BFA&fire=A78BFA&currStreakLabel=A78BFA&sideLabels=e6edf3&currStreakNum=e6edf3&sideNums=e6edf3&dates=8b949e" alt="GitHub Streak" />
  </a>
</p>

---

## Connect

<p align="center">
  <a href="https://diegonogueira.blog">
    <img src="https://img.shields.io/badge/Blog-diegonogueira.blog-7C3AED?style=for-the-badge&logo=hashnode&logoColor=white" alt="Blog" />
  </a>
  <a href="https://linkedin.com/in/diegonogueirapaula">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://twitter.com/diegoconsagrado">
    <img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white" alt="X / Twitter" />
  </a>
  <a href="https://instagram.com/devnogueira_">
    <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram" />
  </a>
  <a href="https://github.com/DiegoNogueiraDev">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>
</p>

---

<p align="center"><i>AISE — research first, ship second, hype never.</i></p>
