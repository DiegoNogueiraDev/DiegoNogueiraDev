<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:1a1530,100:7C3AED&height=180&section=header&text=Diego%20Nogueira&fontSize=36&fontColor=e6edf3&fontAlignY=35&desc=AISE%20%C2%B7%20Independent%20research%20on%20AI-driven%20software%20engineering&descSize=15&descColor=A78BFA&descAlignY=55&animation=fadeIn" alt="header" />

<h3 align="center"><i>"Frameworks são sintaxe.<br/>Disciplina é arquitetura. O grafo é a memória do agente."</i></h3>
<p align="center"><sub><b>AISE</b> · Independent research · Field-tested via <a href="https://github.com/DiegoNogueiraDev/mcp-graph-workflow"><code>mcp-graph-workflow</code></a></sub></p>

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=7C3AED&center=true&vCenter=true&multiline=false&width=760&height=45&lines=AISE+%E2%80%94+AI-driven+software+engineering%2C+as+a+research+practice.;Researching+harness+search%3A+how+the+agent+finds+context.;Field+proof%3A+mcp-graph-workflow.+Local-first.+Determin%C3%ADstico." alt="Typing SVG" />
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

Software Engineer na **Vivo / Telefónica**, pesquisador independente em **AISE** — *AI-driven Software Engineering*. Trato engenharia com agentes como prática de pesquisa: hipótese → harness → medição → publicação.

- :microscope: **Pesquisa independente em AISE** — laboratório pessoal sobre como agentes de código deveriam realmente operar em produção.
- :mag: **Foco atual: harness search** — como o agente busca código, contexto e memória dentro do próprio harness, sem alucinar nem estourar contexto.
- :rocket: **Field proof: [mcp-graph-workflow](https://github.com/DiegoNogueiraDev/mcp-graph-workflow)** — onde a pesquisa vira ferramenta usável. PRD → grafo → TDD → PR, local-first, AGPL.

---

## AISE — Independent research

**AISE** (*AI-driven Software Engineering*) é meu selo de pesquisa aplicada: um lab de uma pessoa só, focado em transformar "fazer ship com IA" de prática folclórica em disciplina mensurável.

Linhas ativas:

| Linha | Pergunta | Status |
|---|---|---|
| **Harness Search** | Como o agente *encontra* contexto sem alucinar nem estourar a janela? | Em destaque (§ abaixo) |
| **Determinismo via grafo persistente** | Pode-se reduzir entropia de geração ancorando o agente em PRD→grafo→PR rastreável? | Em produção via mcp-graph-workflow |
| **Memory & context compression** | Como preservar decisões através de sessões sem inflar contexto? | Em iteração |

Notas de pesquisa publicadas no [blog](https://diegonogueira.blog).

---

## Research focus — Harness Search

> *Como o agente busca dentro do próprio harness — código, contexto, memória, decisões prévias — sem alucinar e sem estourar contexto.*

Search dentro do harness é o que separa **agente que adivinha** de **agente que sabe**. É também o gargalo silencioso da maioria dos workflows com IA hoje: o agente "esquece" não porque não tem memória, mas porque não sabe **buscar** a memória que tem.

```
   query  →  embeddings  →  grafo SQLite  →  AST  →  ranked context  →  agente
                  ↑                                              │
                  └──────────────  feedback loop  ───────────────┘
```

Cinco frentes de investigação:

- :brain: **Local RAG sobre SQLite** — embeddings de PRD, tasks e decisões; recall semântico em <50 ms, zero cloud.
- :compass: **Code-aware search multi-linguagem** — sync grafo↔código detecta drift; grep agentic com awareness de AST em 13 linguagens.
- :package: **Context compression hierárquica** — resumos preservam decisões através de sessões sem replay do histórico cru.
- :test_tube: **Retrieval-grounded TDD** — antes de propor implementação, o agente *busca* testes/casos existentes; hook bloqueia quando não busca.
- :shield: **Citation-enforced anti-hallucination** *(MCP-Graph v13 · `epic-13`)* — código novo em `src/core/` precisa citar o ADR ou epic que motivou a decisão. Sem citation, o validator `validateFilesCitations` bloqueia o commit. Search vira **grounding obrigatório**, não opcional — se o agente não cita, é sinal de que está alucinando.

Tudo isso roda dentro do **mcp-graph-workflow** — a próxima seção é a prova de campo.

---

## Field proof — mcp-graph-workflow

### :rocket: [mcp-graph-workflow](https://github.com/DiegoNogueiraDev/mcp-graph-workflow)

Onde a pesquisa AISE vira ferramenta. **Servidor MCP local-first** que transforma PRDs em grafos de execução persistentes em SQLite, com RAG embarcado e hooks de TDD. Sem cloud, sem chave de LLM, sem improviso.

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
> Quando um agente AI escreve código novo em `src/core/`, ele é **obrigado a citar** qual ADR ou epic motivou a decisão. Se não consegue citar, é sinal de que está alucinando — implementando sem base no spec. O validator **`validateFilesCitations`** flagra arquivos novos em `src/core/` sem citation como **violation** e bloqueia o commit.
>
> `search` → `grounding` → `citation` → `validation` — o loop fecha. Search deixa de ser conveniência e vira **pré-condição** pra escrever código.
>
> *Disponível desde a **v13** · tag `epic-13` · validator: `validateFilesCitations`.*

<p>
  <img src="https://img.shields.io/badge/MCP%20tools-50%2B-7C3AED?style=flat-square&labelColor=0d1117" alt="MCP Tools" />
  <img src="https://img.shields.io/badge/cycle-9%20phases-A78BFA?style=flat-square&labelColor=0d1117" alt="Phases" />
  <img src="https://img.shields.io/badge/persistence-SQLite-A78BFA?style=flat-square&labelColor=0d1117" alt="SQLite" />
  <img src="https://img.shields.io/github/stars/DiegoNogueiraDev/mcp-graph-workflow?style=flat-square&color=7C3AED&labelColor=0d1117" alt="Stars" />
  <img src="https://img.shields.io/badge/license-AGPL%20v3-7C3AED?style=flat-square&labelColor=0d1117" alt="AGPL v3" />
</p>

**Ciclo de 9 fases:**

`ANALYZE` → `DESIGN` → `PLAN` → `IMPLEMENT` → `VALIDATE` → `REVIEW` → `HANDOFF` → `DEPLOY` → `LISTENING`

**Capacidades-chave:**

- :shield: **Anti-hallucination via citation enforcement (v13)** — `validateFilesCitations` exige ADR/epic em todo arquivo novo de `src/core/`; sem citation, sem commit.
- :zap: Pipeline tools que reduzem chamadas MCP em ordem de grandeza (`start_task` + `finish_task`).
- :robot: Agent State Machine: cada resposta indica a próxima ação ao agente.
- :bar_chart: Métricas DORA (deployment frequency, lead time, MTTR) embutidas.
- :brain: Cross-project learning: importa conhecimento entre projetos.
- :mag: Code-aware sync detecta drift grafo↔código em 13 linguagens.
- :jigsaw: Smart decompose quebra tasks por critério de aceite.

**Diferenciação:**

- vs Cursor / Copilot puros → persistência + governança entre sessões.
- vs Linear / Jira → grafo executável pelo agente, não só visual.
- vs LangGraph & cia → local-first, zero infra, CLI única.

> Métricas de produtividade e redução de retrabalho são medições internas em fluxos PRD→PR completos. Metodologia detalhada no [blog](https://diegonogueira.blog).

**Works with:** Claude Code · GitHub Copilot · Cursor · Windsurf · Zed · IntelliJ

---

## Other work

- :chess_pawn: **[xadrez-3D](https://github.com/DiegoNogueiraDev/xadrez-3D)** — side project em 3D, exercício de física e UX.
- :pencil: **[diegonogueira.blog](https://diegonogueira.blog)** — research notes em AISE, MCP e disciplina com agentes.

---

## Stack

Trabalho em **TypeScript / Node** sobre **SQLite** local, com **Vitest** + **Playwright** pra harness de testes, **MCP** como protocolo de tools e **Claude** como modelo principal de agente.

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
