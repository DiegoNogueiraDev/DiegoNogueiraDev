# Diego Nogueira

Software Engineer · independent research on AI-driven Software Engineering (AISE).

---

## About

Software Engineer at **Vivo / Telefónica**. Independent researcher in **AISE** — *AI-driven Software Engineering* — treating engineering with agents as a research practice: hypothesis → harness → measurement → publication.

Current focus: **harness search** (how an agent retrieves code, context and memory inside its own harness without hallucinating) and **determinism via persistent graph** (anchoring generation on a traceable PRD → graph → PR).

Research notes published on [diegonogueira.blog](https://diegonogueira.blog).

---

## mcp-graph-workflow

A **local-first MCP server** that converts PRDs into persistent execution graphs on SQLite, with embedded RAG and TDD hooks. Anti-hallucination via citation enforcement: new code under `src/core/` must cite an ADR or epic, otherwise the commit is blocked.

```
npm install -g @mcp-graph-workflow/mcp-graph@13.27.0
```

**Status — community-pinned at v13.27.0.** mcp-graph remains active and installable on npm; the community release is frozen at `v13.27.0` and will not break. Further development moves into a private master's-research track — the public repository will be archived and the hosted dashboard may go offline, but the npm package is unaffected.

- Repository — [github.com/DiegoNogueiraDev/mcp-graph-workflow](https://github.com/DiegoNogueiraDev/mcp-graph-workflow) *(archived going forward)*
- Live dashboard — [mcp-graph-workflow-dashboard.vercel.app](https://mcp-graph-workflow-dashboard.vercel.app/) *(may go offline)*

---

## Stack

TypeScript / Node · SQLite · Vitest · Playwright · MCP · Claude.

<p>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite" />
  <img src="https://img.shields.io/badge/MCP-7C3AED?style=flat-square&logoColor=white" alt="MCP" />
  <img src="https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=anthropic&logoColor=white" alt="Claude" />
</p>

---

## Connect

- Blog — [diegonogueira.blog](https://diegonogueira.blog)
- LinkedIn — [/in/diegonogueirapaula](https://linkedin.com/in/diegonogueirapaula)
- X — [@diegoconsagrado](https://twitter.com/diegoconsagrado)
- GitHub — [@DiegoNogueiraDev](https://github.com/DiegoNogueiraDev)
