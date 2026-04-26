<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:238636&height=180&section=header&text=Diego%20Nogueira&fontSize=36&fontColor=e6edf3&fontAlignY=35&desc=PRD%20%E2%86%92%20grafo%20%E2%86%92%20TDD%20%E2%86%92%20produ%C3%A7%C3%A3o.%20Zero%20vibe-coding.&descSize=16&descColor=8b949e&descAlignY=55&animation=fadeIn" alt="header" />

<h3 align="center"><i>"Frameworks são sintaxe.<br/>Disciplina é arquitetura. O grafo é a memória."</i></h3>
<p align="center"><sub>Anti-vibe-coding por padrão. Estrutura antes do código.<br/>Tudo local, tudo rastreado, zero improviso.</sub></p>

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=238636&center=true&vCenter=true&multiline=false&width=720&height=45&lines=PRD+%E2%86%92+grafo+persistente+%E2%86%92+TDD+obrigat%C3%B3rio+%E2%86%92+PR+pronto.;Anti-vibe-coding+por+padr%C3%A3o.+Local-first.+Determin%C3%ADstico.;Creator+of+mcp-graph-workflow.+Made+in+Brazil." alt="Typing SVG" />
  </a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=DiegoNogueiraDev&label=Profile%20Views&color=238636&style=flat-square" alt="Profile views" />
  <img src="https://img.shields.io/github/stars/DiegoNogueiraDev?style=flat-square&color=238636&label=Total%20Stars" alt="Total Stars" />
  <img src="https://img.shields.io/badge/PRO-member-238636?style=flat-square&logo=github" alt="Pro" />
</p>

---

## About Me

Sou **Diego Nogueira**, Software Engineer na **Vivo / Telefonica**, Brasil.

A cena que motiva tudo o que construo: 6 prompts soltos no Claude, código que não compila, o agente esquecendo o que foi combinado, PRD virando parede de texto que ninguém relê. É o estado padrão de "fazer ship com IA" em 2026, e é exatamente isso que recuso.

Por isso criei o **[mcp-graph-workflow](https://github.com/DiegoNogueiraDev/mcp-graph-workflow)** — o sistema operacional para fazer ship com IA sem perder o controle. PRD vira grafo persistente. Grafo vira tasks atômicas com critérios de aceite. Tasks vira PR com testes. Tudo local, tudo rastreado, zero vibe-coding.

Quando não estou construindo, escrevo sobre engenharia no [blog](https://diegonogueira.blog) e exploro ideias em side projects como um [jogo de xadrez 3D](https://github.com/DiegoNogueiraDev/xadrez-3D).

- :dart: **Estrutura antes do código** — PRD vira grafo persistente em SQLite, zero trabalho não-rastreado
- :test_tube: **TDD não-negociável** — toda task tem teste antes da implementação. O agente recusa pular
- :brain: **Memória que sobrevive ao reload** — contexto comprimido, RAG local, 52 ferramentas MCP

---

## Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000" alt="JavaScript" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite" />
  <img src="https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white" alt="Vitest" />
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white" alt="Playwright" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions" />
</p>

---

## Featured Project

<table align="center">
<tr>
<td>

### :rocket: [mcp-graph-workflow](https://github.com/DiegoNogueiraDev/mcp-graph-workflow)

**O sistema operacional para fazer ship com IA sem perder o controle.**

PRD → grafo → TDD → produção. Servidor MCP local-first que transforma documentos de requisitos em grafos de execução persistentes em SQLite. Sem cloud, sem chave de LLM, sem improviso.

```
npm install -g @mcp-graph-workflow/mcp-graph
```

<p>
  <img src="https://img.shields.io/badge/productivity-12x-238636?style=flat-square" alt="12x productivity" />
  <img src="https://img.shields.io/badge/tests-5111+-238636?style=flat-square" alt="Tests" />
  <img src="https://img.shields.io/badge/MCP%20tools-52-blue?style=flat-square" alt="MCP Tools" />
  <img src="https://img.shields.io/badge/analyze%20modes-48-blue?style=flat-square" alt="Analyze Modes" />
  <img src="https://img.shields.io/badge/engineering%20skills-30-blue?style=flat-square" alt="Skills" />
  <img src="https://img.shields.io/github/stars/DiegoNogueiraDev/mcp-graph-workflow?style=flat-square&color=238636" alt="Stars" />
  <img src="https://img.shields.io/github/license/DiegoNogueiraDev/mcp-graph-workflow?style=flat-square" alt="License" />
</p>

<sub>**12x menos retrabalho** vs prompting solto — medição interna em fluxos PRD→PR completos.</sub>

**Antes vs depois:**

| Sem mcp-graph | Com mcp-graph |
|---|---|
| 6 prompts soltos, código que não compila | Grafo persistente, PR pronto |
| Agente esquece entre sessões | SQLite local, contexto comprimido |
| TDD opcional, depende do humor do agente | Hook bloqueia commit sem teste primeiro |
| "Tá pronto?" → adivinhação | `mcp-graph status` em 200 ms |

**Ciclo de 9 fases:**

`ANALYZE` > `DESIGN` > `PLAN` > `IMPLEMENT` > `VALIDATE` > `REVIEW` > `HANDOFF` > `DEPLOY` > `LISTENING`

**Capacidades-chave:**
- :zap: Pipeline tools que cortam **67%** das chamadas (`start_task` + `finish_task`)
- :robot: Agent State Machine: cada resposta indica a próxima ação ao agente
- :bar_chart: Métricas DORA (deployment frequency, lead time, MTTR)
- :brain: Cross-project learning: importe conhecimento entre projetos
- :mag: Code-aware sync: detecta drift grafo↔código em 13 linguagens
- :jigsaw: Smart decompose: quebra tasks por critério de aceite

**Diferenciação:**
- vs Cursor / Copilot puros → persistência + governança
- vs Linear / Jira → executável pelo agente, não só visual
- vs LangGraph & cia → local-first, zero infra, CLI única

**Works with:** GitHub Copilot · Claude Code · Cursor · IntelliJ · Windsurf · Zed

</td>
</tr>
</table>

---

## GitHub Stats

<p align="center">
  <a href="https://github.com/DiegoNogueiraDev">
    <img height="170" src="https://github-readme-stats.vercel.app/api?username=DiegoNogueiraDev&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=238636&icon_color=238636&text_color=e6edf3&ring_color=238636&include_all_commits=true&count_private=true" alt="Diego's GitHub Stats" />
  </a>
  <a href="https://github.com/DiegoNogueiraDev">
    <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=DiegoNogueiraDev&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=238636&text_color=e6edf3&langs_count=8" alt="Top Languages" />
  </a>
</p>

<p align="center">
  <a href="https://github.com/DiegoNogueiraDev">
    <img src="https://streak-stats.demolab.com/?user=DiegoNogueiraDev&theme=github-dark-blue&hide_border=true&background=0d1117&stroke=238636&ring=238636&fire=238636&currStreakLabel=238636&sideLabels=e6edf3&currStreakNum=e6edf3&sideNums=e6edf3&dates=8b949e" alt="GitHub Streak" />
  </a>
</p>

---

## Blog & Connect

<p align="center">
  <a href="https://diegonogueira.blog">
    <img src="https://img.shields.io/badge/Blog-diegonogueira.blog-238636?style=for-the-badge&logo=hashnode&logoColor=white" alt="Blog" />
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

<p align="center">
  <i>"Disciplina de principal engineer, embutida no agente. Anti-vibe-coding por padrão."</i>
</p>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:238636&height=100&section=footer" alt="footer" />
