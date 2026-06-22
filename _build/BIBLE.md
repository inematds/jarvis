# BIBLE — Curso "Jarvis: Seu Sistema Operacional de IA" (INEMA.CLUB, formato-curso-v2)

Fonte única de verdade para construir CADA página. courseId = `jarvis`. Emoji = 🤖. Público = **LEIGOS** (PT-BR). Tom = direto, caloroso, didático; **define cada termo técnico na 1ª vez** (estilo "Novo aqui?"). Dark premium INEMA. Tudo self-contained (Tailwind CDN + learn.css/js por caminho relativo).

---

## 0. COMO MONTAR UMA PÁGINA (regra de ouro — não negociável)

Toda página de trilha/módulo = **HEAD-inner.html** (do `_build/`) + seu `<main id="conteudo">…</main>` + **FOOT.html** (do `_build/`, troque `{{REL}}` por `../../`).

1. Copie `_build/HEAD-inner.html` VERBATIM. Troque `{{TITLE}}` e `{{DESC}}`. ATIVE a trilha desta página (instrução no topo do arquivo — só a sua trilha vira ativa).
2. Escreva o `<main id="conteudo"> … </main>`.
3. Cole `_build/FOOT.html`, trocando `{{REL}}` por `../../`.

**Exemplar GOLD (clonar a estrutura/qualidade):** `/home/nmaldaner/projetos/agentehermeslocal/curso/trilha1/modulo-1-1.html` (módulo) e `/home/nmaldaner/projetos/agentehermeslocal/curso/trilha1/index.html` (índice de trilha). Leia-os e copie os PADRÕES (não o conteúdo).

### Regras v2 que NÃO podem ser violadas (checklist resumido)
- Botões `justify-start` (esquerda). Tópicos com **número em círculo**, nunca seta.
- Índice de trilha: header com badge+stats; **"Mapa da trilha"** (grid de cards-âncora `#modulo-X-Y`, header `justify-between` X.Y/duração, emoji, subtítulo PUNCHY 3-5 palavras); h2 `Conteudo detalhado`; cards de módulo com **6 tópicos expansíveis** (cada um com 3 seções: "O que é / Por que aprender / Conceitos-chave") + botões `Ver em Modal` (iframe) e `Ver Completo`. Cada card de módulo tem `id="modulo-X-Y"` e `data-inema-module="X-Y" data-inema-track="N"`.
- Módulo: breadcrumb; header (badge MODULO X.Y + título `text-3xl/4xl` + stats); **6 `<section id="topico-N" data-inema-topic="modulo-X-Y#topico-N">`**, cada uma: número em círculo grande (w-12 h-12) + h2 `text-2xl`; parágrafos com `data-inema-block="mX-Y-tN-pK"`; **VARIEDADE** de boxes (conceito gradiente, dados azul, dica primary, grid ✓/✗ emerald/red, timeline, alerta red, "Novo aqui?" glossário); termina com grid "Conceitos-chave" (4 mini-cards) + **botão marcar-como-lido** (copie verbatim do exemplar). Resumo final com checklist + próximo módulo + CTAs.
- **≥1 SVG futurista inline por módulo** (cor da trilha + ciano, defs com id prefixado `mXY-…`, `role="img"`+`aria-label`, painel `rounded-2xl border border-COR-500/30 bg-dark-900/40`, legenda que ENSINA). Use mais de 1 quando ajudar. Índice de trilha: **1 hero SVG**.
- **Visual-first:** cada conceito-chave ganha apoio visual + legenda. Módulos práticos: **≥1 exemplo copy-run REAL** (code box `font-mono`, com objetivo + bloco colável + como verificar; parta variável = `<isto-voce-troca>`).
- 500–800 linhas por módulo, sem template repetido 6×.

### Cores por trilha
T1 Fundamentos=**emerald** 🌱 · T2 Panorama=**blue** 🗺️ · T3 Anatomia=**purple** 🧬 · T4 Construir=**amber** 🛠️ · T5 Celular=**teal** 📱 · T6 Crianças=**rose** 🧸.
SVG: primária=cor da trilha; secundária=ciano `#38bdf8`. Paleta SVG por trilha — emerald `#34d399`/`#10b981`/fill`#0e2018`; blue `#60a5fa`/`#3b82f6`/`#0e1622`; purple `#c084fc`/`#a855f7`/`#1a1230`; amber `#fbbf24`/`#f59e0b`/`#1f1604`; teal `#2dd4bf`/`#14b8a6`/`#0c1f1c`; rose `#fb7185`/`#f43f5e`/`#2a0f16`. Glow `feGaussianBlur stdDeviation="1.8"` só na caixa-foco; `stroke-width="2"`; títulos `font-weight="600"`.

---

## 1. AS 6 TRILHAS (descrição p/ a landing + header de cada índice)

- **T1 · Fundamentos** 🌱 (emerald) — "Do zero: o que é, afinal, um Jarvis?" Sem nenhum pré-requisito. Define LLM, contexto, ferramenta, agente, SO de IA. 3 módulos · 18 tópicos · ~2h30 · Iniciante.
- **T2 · O Panorama** 🗺️ (blue) — "Os sistemas que existem e qual é o caminho." Compara OpenClaw, GravityClaw, Hermes, Intelecto, Antidote + os de fora (AIOS, MemGPT, Open Interpreter, Operator). 3 módulos · 18 tópicos · ~2h30 · Iniciante.
- **T3 · Anatomia** 🧬 (purple) — "As 6 camadas que viram um chat num assistente que vê, lembra e age." Canais, Identidade, Ferramentas, Skills, Agentes, Cérebros — uma por módulo. 6 módulos · 36 tópicos · ~5h · Intermediário.
- **T4 · Construir um Jarvis eficaz** 🛠️ (amber) — "Do primeiro tijolo à solução robusta." A receita mínima, a arquitetura das 4 camadas (Context·Connections·Capabilities·Cadence) e como operar. 3 módulos · 18 tópicos · ~3h · Intermediário.
- **T5 · Jarvis no celular** 📱 (teal) — "Seu assistente no bolso, sem app de loja." Canais (Telegram/WhatsApp), voz (STT/TTS) e on-device. 3 módulos · 18 tópicos · ~2h30 · Intermediário.
- **T6 · Jarvis para crianças** 🧸 (rose) — "Um tutor socrático que ensina perguntando — e seguro." Método socrático, persona/voz/boneco, e a segurança inegociável. 3 módulos · 18 tópicos · ~2h30 · Iniciante.

Curso total: **21 módulos · 126 tópicos · ~18h**.

---

## 2. BRIEFS POR MÓDULO (6 tópicos cada — título do tópico + semente de conteúdo)

> Cada tópico vira uma `<section>` com 3 boxes variados + Conceitos-chave + marcar-lido. Defina os termos em negrito na 1ª vez. Os "→" são as sementes; expanda com a substância da §3.

### T1 — FUNDAMENTOS (emerald)

**1-1 · O que é um "Jarvis" — da ficção à sua casa** 🤖 (Goal: entender o conceito sem nenhum jargão)
1. Da ficção ao real → Jarvis do Homem de Ferro = a fantasia de um assistente que conversa, lembra e FAZ. Hoje isso é construível. "Jarvis" no curso = um **assistente de IA pessoal**.
2. Chatbot ≠ Jarvis → ChatGPT responde; um Jarvis AGE (manda email, lê sua agenda, roda tarefa sozinho). A diferença é AÇÃO no mundo.
3. "Sistema operacional de IA" em 1 frase → assim como o Windows organiza programas/memória/periféricos, um **SO de IA** organiza modelo + memória + ferramentas + canais para o assistente viver.
4. Por que agora → modelos bons o bastante + hardware pessoal + padrões abertos (MCP). A onda está no começo.
5. O que dá pra fazer hoje (e o que não dá) → expectativa realista: ótimo p/ texto, busca, agenda, rascunhos, automação; ainda falha em tarefas longas sem supervisão, e "alucina".
6. O mapa do curso → as 6 trilhas em 1 parágrafo cada; convite a seguir T1→T6.
SVG: fan-out simples "você → (modelo+memória+ferramentas+canais) → ações". Glossário: LLM, agente, SO de IA.

**1-2 · O cérebro da coisa: o que é um LLM (sem jargão)** 🧠 (Goal: desmistificar o modelo)
1. O que é um LLM → "Modelo de Linguagem Grande": um programa treinado em MUITO texto que prevê a próxima palavra; é o que roda atrás do ChatGPT/Claude. É o **cérebro** que pensa em texto.
2. Como ele "pensa" → não é busca nem banco de dados; é previsão estatística treinada. Por isso é criativo E às vezes erra com confiança (**alucinação**).
3. Contexto = a memória de trabalho → a **janela de contexto** é tudo que o modelo "está vendo agora" (sua conversa + instruções + arquivos). É como a RAM: limitada, esvazia ao fechar.
4. Tokens → o modelo lê/escreve em **tokens** (pedaços de palavra). Nuvem cobra por token; contexto se mede em tokens.
5. Modelo local vs nuvem → nuvem (Claude/GPT, potentes, pagam por uso) vs local (Ollama, grátis, privado, exige hardware). Mesmo papel: ser o cérebro.
6. Limites e como contornar → alucina, não sabe de coisas pós-treino, esquece fora do contexto → ferramentas e memória (T3) resolvem.
SVG: "LLM como kernel" — caixa central LLM, contexto=RAM, ferramentas=periféricos. Glossário: LLM, token, janela de contexto, alucinação, Ollama.

**1-3 · De chatbot a agente: quando a IA passa a agir** ⚙️ (Goal: o loop agêntico)
1. O salto → de "responde" para "faz". Um **agente** é um LLM que pode usar ferramentas em ciclo.
2. O loop agêntico → recebe pedido → pensa → chama ferramenta → lê resultado → chama mais → responde. Com **limite de iterações** por segurança.
3. Ferramentas (tools) → as "mãos": buscar web, rodar código, ler arquivo, mandar mensagem. Sem elas, o modelo "responde como um estranho".
4. A metáfora LLM-OS (Karpathy, 2023) → o LLM é o **kernel** de um SO novo: contexto=RAM, ferramentas=periféricos, agentes=processos. A indústria adotou esse modelo mental.
5. AIOS, Operator, Project Jarvis → a metáfora virou produto: AIOS (paper, kernel p/ agentes), OpenAI Operator, Google Project Jarvis (agente que navega o Chrome).
6. O que muda pra você → você para de "perguntar" e começa a "delegar". Ponte para a Anatomia (T3).
SVG: ciclo agêntico (loop pedido→pensa→tool→resultado→resposta). Glossário: agente, ferramenta/tool, loop agêntico, kernel.

### T2 — O PANORAMA (blue)

**2-1 · Como comparar SOs de IA + o mapa das categorias** 🗺️ (Goal: critérios de comparação)
1. A pergunta que todos os sistemas respondem → "como rodo MINHA IA (agente+memória+personalidade) sem depender de um chatbot fechado?".
2. Os 5 critérios → **privacidade** (local vs nuvem), **custo** (fixo/grátis vs por token), **controle/auditabilidade** (você lê o código?), **esforço** (clonar vs construir), **poder** (quantas integrações).
3. As 4 categorias → (a) pesquisa/kernel (AIOS, MemGPT); (b) assistentes locais/voz (Leon, OVOS, Jan, Home Assistant); (c) hardware dedicado (Rabbit R1, Humane — recepção ruim); (d) frameworks de agente (LangGraph, CrewAI, MCP) — onde a maioria é construída.
4. Local vs nuvem (o eixo-mestre) → trade-off privacidade/custo × potência/conveniência. Muitos sistemas deixam você ESCOLHER por mensagem.
5. Lean vs framework → "menos é mais" (Intelecto ~3.000 linhas, sem Docker) vs frameworks pesados. Código que você entende > código que você clona e nunca lê.
6. Como ler a tabela do próximo módulo → o que olhar em cada sistema.
SVG: escada/quadrante de categorias OU tabela-mock. Glossário: framework, auditabilidade, vendor lock-in.

**2-2 · A família em casa: OpenClaw, GravityClaw, Hermes e Intelecto** 🏠 (Goal: comparar os sistemas do ecossistema)
1. OpenClaw → o "original" (jan/2026, 250K+ estrelas): agente pessoal com canais, loop de tools, memória, voz, **700+ skills da comunidade**, heartbeat. Problemas: **web server exposto (42.665 instâncias públicas, 93,4% sem auth)**, **341 skills maliciosas**, custo $500–5K/mês, 100K+ linhas que ninguém lê.
2. GravityClaw → reimplementação LEAN e segura do OpenClaw em TypeScript: **só Telegram (long-polling, zero portas)**, **só MCP** (auditável), custo fixo ($200) ou local, código **brick-by-brick**. "Um agente pessoal lean, seguro e totalmente compreendido."
3. Intelecto → o "anti-framework": ~3.000 linhas de Python, sem Docker, sem web UI, Telegram, memória **SQLite FTS5+BM25**, personalidade por arquivos (**SOUL/AGENTS/USER**), nuvem (OpenRouter) ou local (Ollama). A tese "menos é mais".
4. Antidote → mesmo projeto/stack do Intelecto numa fase mais enxuta; gera um `.md` 100% tool-agnostic (roda em Codex/Gemini/Cursor) e TEM guia de build passo-a-passo.
5. Hermes / claude-hermes-os → Hermes = agente self-hosted "um cérebro, várias bocas" (vários modelos) com memória/personas/skills/MCP/cron, virando um "SO de IA". claude-hermes-os = painel local (só leitura) que LÊ Claude Code/Codex/OpenClaw/Obsidian/Pinecone e mostra gasto, memória 3D, skills (com auto-melhoria diária "Dream").
6. A lição de segurança → exposição e skills de terceiros foram os maiores furos; o caminho seguro = sem portas + só MCP + local-first + whitelist.
SVG: comparação OpenClaw (exposto/inchado) × GravityClaw (lean/fechado) — malha×solo ou ✓/✗. Glossário: MCP, long-polling, heartbeat, whitelist, FTS5/BM25, SOUL.md.

**2-3 · O mundo lá fora (AIOS, MemGPT, Operator…) e o caminho** 🌍 (Goal: contexto global + recomendação)
1. AIOS (paper, COLM 2025) → kernel de SO para agentes LLM (escalonador, memória, storage); 2,1× mais rápido. A metáfora LLM-OS virou sistema real.
2. MemGPT / Letta → memória **hierárquica** (core/recall/archival) inspirada em paginação de SO; captou US$10M. Ideia-chave: dar "memória infinita" ao agente.
3. Open Interpreter → deixa o LLM **rodar código na sua máquina** com confirmação. Poder bruto + responsabilidade.
4. Assistentes e hardware → Leon, OVOS, Jan, Home Assistant Assist (locais/voz); Rabbit R1 e Humane Pin (hardware dedicado, recepção morna→ruim) — lição: o problema raramente é o hardware.
5. MCP — o "USB das ferramentas de IA" → padrão da Anthropic (nov/2024) que conecta qualquer ferramenta a qualquer agente. É o que faz as peças se encaixarem.
6. O CAMINHO (recomendação honesta) → comece lean e local (Intelecto/GravityClaw, Ollama), só MCP, single-owner, memória em arquivos+SQLite; cresça por necessidade. Construa entendendo cada tijolo. Ponte para T3 (a anatomia) e T4 (construir).
SVG: fan-out "1 padrão MCP → muitos agentes/ferramentas" OU linha do tempo. Glossário: AIOS, memória hierárquica, MCP.

### T3 — ANATOMIA (purple) — uma camada por módulo

**3-1 · Canais — por onde você fala com ele** 📡 (Goal: as portas de entrada/saída)
1. O que é um canal → a "porta" por onde você conversa com o Jarvis: Telegram, WhatsApp, voz, web, o próprio Claude Code/terminal.
2. Por que Telegram é o preferido → só um token (do @BotFather), **long-polling** (sem servidor web exposto, sem portas), grátis, multiplataforma, "já é mobile".
3. WhatsApp e o resto → WhatsApp (texto/imagem/voz, via Evolution API), e-mail, web. Multicanal: o mesmo cérebro em vários lugares.
4. Whitelist = a 1ª trava → só o SEU ID é atendido; qualquer outro é ignorado em silêncio. Segurança por padrão.
5. Texto, voz e mídia → o canal carrega texto, áudio (.ogg do Telegram), imagem. Voz é entrada/saída OPCIONAL decidida em runtime.
6. Um canal, muitos dispositivos → "o Telegram já é mobile": acessível de qualquer aparelho onde você o tem, sem app nativo.
SVG: hub "Jarvis" com raios p/ Telegram/WhatsApp/voz/web. Copy-run: criar bot no @BotFather e pegar o token (passos). Glossário: canal, token, long-polling, whitelist.

**3-2 · Identidade — memória, persona e quem ele é** 🪪 (Goal: dar caráter e memória)
1. SOUL.md — a alma → arquivo de texto com personalidade, valores, tom, prioridades do dono. Injetado SEMPRE no system prompt. "Sem o brain rewire, a arquitetura é só uma pasta."
2. AGENTS.md — o contrato → o que ele FAZ e o que NUNCA faz (listas SEMPRE/NUNCA). Regras explícitas > esperar que o modelo adivinhe.
3. USER / perfil → quem é você (nome, contexto, preferências) para ele não te tratar como estranho.
4. Memória que dura → conversa esquece ao fechar; memória persistente = arquivos `.md` + índice **SQLite FTS5/BM25** (busca por palavra) e/ou banco vetorial (busca por significado).
5. Identidade = autenticação também → whitelist de ID + secrets só no `.env`. Quem ele atende faz parte de "quem ele é".
6. Personas intercambiáveis → o mesmo Jarvis troca de modo (trabalho/estudo/historinha) trocando o SOUL/perfil ativo.
SVG: 3 camadas SOUL/AGENTS/USER alimentando o LLM. Copy-run: um `soul.md` de exemplo (nome, valores, tom) + um `AGENTS.md` SEMPRE/NUNCA. Glossário: system prompt, SOUL.md, AGENTS.md, FTS5/BM25, banco vetorial.

**3-3 · Ferramentas — as mãos do Jarvis (tools + MCP)** 🔧 (Goal: como ele age no mundo)
1. Por que ferramentas → o LLM sozinho só fala; ferramentas dão mãos e olhos (web, arquivos, e-mail, agenda, shell).
2. Tool/function-calling → o modelo "pede" uma função; o sistema executa e devolve o resultado pro loop. É o mecanismo bruto.
3. MCP — o USB das ferramentas → **Model Context Protocol** (Anthropic, nov/2024): cada integração é um **servidor MCP** separado, padronizado e auditável. Plugue Gmail/Notion/GitHub sem reescrever o agente.
4. MCP vs "skills da comunidade" → por que MCP é mais seguro que baixar skill files de terceiros (lembre das 341 maliciosas do OpenClaw).
5. Confirmação e sandbox → ações perigosas (rodar shell, apagar) pedem confirmação; rodam em sandbox. Toda entrada é potencial **prompt-injection**.
6. Conectar = sair do "estranho" → sem dados reais (agenda, e-mail) ele responde genérico; com ferramentas vira ASSISTENTE.
SVG: aninhamento "agente → [MCP: gmail | github | shell | navegador]". Copy-run: config de um servidor MCP (JSON) p/ Claude Code/host. Glossário: tool/function-calling, MCP, sandbox, prompt-injection.

**3-4 · Skills — habilidades empacotadas** 🧩 (Goal: receitas reutilizáveis)
1. O que é uma skill → "uma receita". Um arquivo markdown (SKILL.md) que empacota um passo-a-passo repetido. "Escreve um post de LinkedIn" → pesquisa→gráfico→copy→revisão→publica.
2. Por que empacotar → em vez de explicar 5 passos toda vez, você diz uma frase e a skill executa.
3. Carregamento progressivo → a skill custa pouco (só o frontmatter, ~100 tokens) até ser acionada — economia de contexto.
4. Skills × ferramentas → ferramenta = ação atômica; skill = procedimento que ORQUESTRA ferramentas e julgamento.
5. Portabilidade (honesta) → Agent Skills spec + **polyskill**: uma fonte roda em Claude Code E Codex. "Múltiplos modelos" aqui = portabilidade, não conselho de modelos.
6. Skills se auto-corrigem → cada run melhora a receita; a biblioteca de skills é seu acervo de capacidades.
SVG: skill como caixa que dispara um mini-fluxo de ferramentas. Copy-run: um `SKILL.md` mínimo (frontmatter name/description + passos). Glossário: skill, frontmatter, progressive disclosure, polyskill.

**3-5 · Agentes — o loop que trabalha sozinho** 🤝 (Goal: autonomia e sub-agentes)
1. Agente = loop + autonomia → revisão do loop agêntico de T1, agora como camada.
2. Sub-agentes → o agente principal **delega** tarefa pesada a um sub-agente que queima o PRÓPRIO contexto e devolve só a resposta — sessão principal fica leve.
3. Multi-agente → vários especialistas (pesquisa, escrita, revisão) coordenados; quando vale e quando complica.
4. Cadência (heartbeat/cron) → **routines/cron/heartbeat** fazem o Jarvis agir sozinho no horário (resumo das 7h, monitorar caixa) — "com o laptop fechado".
5. Limites e segurança do loop → teto de iterações, gates de aprovação, **audit log** (memória forense de cada ação).
6. Proativo vs reativo → de "responde quando chamo" para "me avisa antes de eu pedir". O salto de assistente para parceiro.
SVG: fan-out orquestrador→sub-agentes→resultado (use os nós ciano pulsando). Glossário: sub-agente, multi-agente, heartbeat/cron, audit log.

**3-6 · Cérebros — o motor que pensa e a memória organizada** 🧠 (Goal: o(s) modelo(s) + a memória como "cérebros")
> CORREÇÃO IMPORTANTE: no modelo do usuário, "cérebros" NÃO é um conselho/juiz de vários LLMs rodando juntos. É (a) o **motor LLM trocável** e (b) a **memória organizada em zonas** ("segundo cérebro" → 3 cérebros). Seja honesto sobre isso.
1. O cérebro = o motor LLM → o modelo que pensa. É **plugável/trocável** (hot-swap por `.env`: anthropic | openrouter | ollama). "Um cérebro, várias bocas."
2. Trocar de cérebro sem mexer no código → mesma interface, modelo diferente: local barato p/ tarefa simples, nuvem potente p/ tarefa difícil (decisão econômica por resposta).
3. O mito do "conselho de modelos" → não há juiz/roteador mágico de N modelos nos projetos; "múltiplos modelos" honesto = **substituição e portabilidade** (cross-runtime), não votação simultânea.
4. O "segundo cérebro" vira memória → a outra acepção de "cérebros": a MEMÓRIA do Jarvis organizada. Um amontoado de notas incha; separar dá ordem.
5. Os 3 cérebros (memória) → **Projeto** (episódico: o que rolou, decisões), **Self** (identidade: valores, dúvidas — muda devagar), **Conhecimento** (referência: fatos que só acumulam). Inbox única + skill /triagem roteia. [[wikilinks]] cruzam os três.
6. Memória = filesystem + índice → `.md` legível (a verdade) + SQLite FTS5/BM25 (busca). "Sobrevive ao hype porque é só texto." O CLAUDE.md/AGENTS.md é o ROTEADOR lido no início de cada sessão.
SVG: à esquerda motor LLM trocável; à direita 3 cérebros de memória (Projeto/Self/Conhecimento) + inbox. Copy-run: `.env` hot-swap (LLM_PROVIDER/LLM_MODEL). Glossário: hot-swap, FTS5/BM25, banco vetorial, segundo cérebro.

### T4 — CONSTRUIR UM JARVIS EFICAZ (amber)

**4-1 · Do zero ao primeiro Jarvis (a receita mínima)** 🧱 (Goal: caminho mínimo viável)
1. A receita mínima → canal (Telegram) + cérebro (1 modelo) + soul.md + loop agêntico + 1 ferramenta. O "hello world" do Jarvis.
2. Os 5 Build Levels → **Foundation → Memory → Voice → Tools/MCP → Heartbeat**. Construa e teste um tijolo antes do próximo (brick-by-brick).
3. Level 1 Foundation → bot do Telegram conectado ao modelo, respondendo. Whitelist + `.env`.
4. Level 2 Memory → soul.md + SQLite de conversa; ele passa a lembrar.
5. Construir COM uma IA → use Claude Code/Antigravity + um prompt de inicialização (CLAWS) que descreve canal/cérebro/ferramentas/segurança. (incluir o prompt colável)
6. Testar cada tijolo → como saber que funcionou antes de seguir.
SVG: escada dos 5 Build Levels. Copy-run: o **prompt de inicialização** do tipo GravityClaw (You are helping me build my personal AI agent… Telegram-only, MCP-only, agentic loop, whitelist…) — colável no Claude Code. Glossário: Build Levels, brick-by-brick, .env.

**4-2 · Arquitetura de uma solução robusta (as 4 camadas C)** 🏗️ (Goal: o framework CLAWS)
1. As 4 C → **Context. Connections. Capabilities. Cadence.** Ordem 1-2-3-4: sem conexões não há cadência; sem contexto não há capacidade.
2. Context → identidade + memória (soul + 3 cérebros). Quem ele é e o que sabe de você. (liga a T3-2/3-6)
3. Connections → canais + ferramentas/MCP. Por onde fala e o que alcança. (T3-1/3-3)
4. Capabilities → skills + agentes/sub-agentes. O que ele consegue fazer. (T3-4/3-5)
5. Cadence → heartbeat/cron/routines. Quando ele age sozinho. (T3-5)
6. Juntando as 6 camadas → como o mapa da Anatomia vira UMA arquitetura coerente; diagrama final.
SVG: equação Context+Connections+Capabilities+Cadence = Jarvis (caixa-resultado com glow). Glossário: CLAWS, as 4 C.
> "Tools change every 6 months. The platform and foundation we're building survive."

**4-3 · Operar, medir e evoluir (confiança, custo, segurança)** 📈 (Goal: produção responsável)
1. Confiabilidade → alucinação e erro existem; gates de aprovação, confirmação p/ ações perigosas, limite de iterações.
2. Custo → local ($0/token) vs nuvem (por token); decisão econômica por resposta (modelo barato vs premium). CAPEX vs OPEX.
3. Segurança zero-trust → toda entrada é potencial ataque (**prompt-injection**); sandbox, secrets no `.env`, sem portas, **audit log** forense.
4. Privacidade & dados → local-first: dados não saem a menos que você conecte um serviço. O que pode sair, você decide.
5. Medir → o que observar (uso, gasto, erros, dúvidas) — ex.: um painel como o claude-hermes-os.
6. Evoluir sem inchar → adicionar por necessidade, manter enxuto e legível; "menos é mais" vence o hype.
SVG: fluxo de decisão de segurança (entrada→é perigoso?→sandbox/aprovação). Glossário: zero-trust, prompt-injection, audit log, CAPEX/OPEX.

### T5 — JARVIS NO CELULAR (teal)

**5-1 · Onde o Jarvis mora no celular (os canais)** 📲 (Goal: sem app de loja)
1. A virada → você não precisa de app nativo; usa um app de mensagens que JÁ roda no telefone. "O Telegram já é mobile."
2. Telegram (agentejax) → @BotFather → token → whitelist do seu user ID → agente 24/7 acessível de qualquer celular.
3. WhatsApp (agentevoz) → via **Evolution API**; atendimento multicanal com Policy Engine que decide texto/voz/humano.
4. O agente roda onde? → na nuvem (Railway) ou no SEU PC em casa; o celular é só o canal. Pode rodar 24/7.
5. Privacidade no bolso → dá pra manter o cérebro local (Ollama no PC de casa) e só o canal no celular.
6. Limitações dos assistentes nativos → Siri/Gemini são fechados; seu bot de Telegram/WhatsApp é SEU.
SVG: celular → (Telegram) → agente (nuvem/PC) → ferramentas. Copy-run: passos do @BotFather + whitelist. Glossário: Evolution API, Policy Engine, canal.

**5-2 · Voz e on-device: falar, ouvir e rodar local** 🎙️ (Goal: pipeline de voz + on-device)
1. Voz é interface, não cérebro → "voz é interface, orquestrador é cérebro; TTS é saída opcional decidida em runtime".
2. Ouvir (STT) → Telegram entrega áudio `.ogg` Opus → **ffmpeg** converte → **Whisper** transcreve (idioma pt). (atenção: chave OpenAI ≠ Anthropic).
3. Falar (TTS) → modelo de voz (ex.: tts-1, voz "nova", ou TTS local) gera o áudio de resposta.
4. Decisão por resposta → Policy Engine escolhe texto, voz ou humano — e modelo barato vs premium — para economizar.
5. On-device de verdade → **Ollama** rodando local (modelos por RAM: 3B@8GB, 8B@16GB); CPU é lento (30-60s), GPU/nuvem aceleram.
6. Tempo real (avançado) → roadmap até ligação telefônica via Twilio/LiveKit com latência <1,5s. Calibrar expectativa.
SVG: pipeline voz: áudio→ffmpeg→Whisper→LLM→TTS→áudio. Copy-run: `ffmpeg` .ogg→.wav + chamada Whisper (pseudoshell) e `.env` LLM_PROVIDER=ollama. Glossário: STT/Whisper, TTS, on-device, Ollama, latência.

**5-3 · Montando seu Jarvis de bolso (projeto)** 🛠️ (Goal: projeto guiado fim-a-fim)
1. Visão do projeto → um bot de Telegram pessoal, com memória e 1 skill, acessível do celular.
2. Passo 1 — o bot → @BotFather, token, whitelist (reuso de 5-1).
3. Passo 2 — o cérebro → escolher nuvem ou Ollama local; `.env`.
4. Passo 3 — memória + soul → soul.md + SQLite; ele lembra de você.
5. Passo 4 — uma skill útil → ex.: "resumo do meu dia" puxando agenda via MCP.
6. Passo 5 — voz e cadência → mensagem de voz (Whisper/TTS) + um heartbeat das 7h. Como testar tudo.
SVG: arquitetura final do projeto (celular→bot→cérebro→memória/skill/heartbeat). Copy-run: sequência de comandos/setup do projeto. Glossário: recap.

### T6 — JARVIS PARA CRIANÇAS (rose)

**6-1 · O Jarvis que ensina: o método socrático** 🦉 (Goal: ensinar perguntando)
1. Por que socrático → não despejar a resposta; **perguntar** e deixar a criança chegar lá. MIT RAISE (2025): melhora matemática e competências digitais.
2. O padrão do "Professor" (Animabook) → ele pergunta, os alunos respondem/questionam, um robozinho (PIX-Z) entra com a definição na medida. Ensinar pelo diálogo.
3. O ciclo socrático do bot → pergunta → espera → valida o raciocínio → só então revela. "Explica o raciocínio, não só a resposta" (valor no SOUL.md).
4. Khanmigo na prática → tutor socrático do Khan Academy: cresceu 68 mil→700 mil usuários usando exatamente essa lógica.
5. Modos de aprendizagem → "modo historinha", "modo lição de casa" — personas intercambiáveis para idade/assunto.
6. Erro como degrau → o bom tutor normaliza o erro e guia; nunca humilha, nunca entrega tudo pronto.
SVG: ciclo socrático (pergunta→espera→valida→revela). Copy-run: trecho de SOUL.md de tutor socrático (valores + "nunca dê a resposta direta"). Glossário: método socrático, persona, scaffolding.

**6-2 · Persona, voz e o boneco: dar corpo ao tutor** 🧸 (Goal: encarnar o tutor)
1. Os 4 alicerces → PERSONA (soul.md) + GUARDRAILS (agents.md) + CANAIS/voz + MEMÓRIA. O mesmo kit da Anatomia, com cara de criança.
2. Persona amigável → nome, voz, jeito de falar apropriados; calorosa, paciente, curiosa.
3. Voz que encanta → STT/TTS para o boneco ouvir e responder falando (pipeline de T5), voz suave.
4. Memória afetiva → lembrar o nome, o que a criança gosta, onde parou a história — cria vínculo.
5. O "boneco" como canal → o brinquedo é só mais um canal (microfone+alto-falante) ligado ao mesmo cérebro/segurança.
6. O risco do vínculo → bonecos viram amigos. Lição real: o robô **Moxie** ($799) "morreu" quando a empresa faliu (dez/2024) e pais tiveram que explicar às crianças. Projete para não criar dependência emocional perigosa.
SVG: boneco (canal voz) → cérebro+memória+guardrails. Copy-run: perfil de persona infantil (soul.md "modo historinha"). Glossário: persona, vínculo, dependência emocional.

**6-3 · Segurança, guardrails e os pais (o inegociável)** 🛡️ (Goal: segurança infantil — o capítulo mais sério)
1. Por que isto vem por último e é o mais importante → perto de criança, segurança não é opcional.
2. O caso FoloToy → ursinho de IA ($99, GPT-4o) foi flagrado (nov/2025) falando de conteúdo sexual explícito, BDSM e onde achar facas/comprimidos; a OpenAI revogou o acesso. Sem guardrails, o brinquedo vira perigo.
3. AGENTS.md SEMPRE/NUNCA → contrato explícito de conteúdo (NUNCA violência/sexo/perigo; SEMPRE redirecionar e avisar). Regras explícitas > torcer pra IA inferir.
4. Camada zero-trust → anti **prompt-injection**, sandbox, gates de aprovação, **audit log** (pais podem revisar tudo).
5. Privacidade de dados de criança → COPPA e afins: minimizar coleta, local-first, transparência. Dados de criança são sagrados.
6. O papel dos pais (Character.AI como alerta) → processos em 2024-2025 mostram o custo de IA sem supervisão; controles parentais, limites de tempo, e o adulto no comando. Checklist final para um produto seguro.
SVG: fluxo de guardrail (pedido da criança → filtro SEMPRE/NUNCA → resposta segura / redireciona + log). Copy-run: AGENTS.md de segurança infantil (listas SEMPRE/NUNCA). Glossário: guardrail, COPPA, audit log, prompt-injection.

---

## 3. APÊNDICE — substância de pesquisa (use à vontade, cite com naturalidade)

**Fundamentos / LLM-OS.** Karpathy (set/2023): o LLM é o **kernel** de um SO novo — contexto=RAM, ferramentas=periféricos, agentes=processos. Virou o modelo mental da indústria ("Agentic OS"). **AIOS** (paper, COLM 2025): kernel real p/ agentes (escalonador+memória+storage), 2,1× mais rápido. **MemGPT/Letta**: memória hierárquica core/recall/archival (paginação de SO), US$10M. **Open Interpreter**: LLM roda código local com confirmação. **MCP** (Anthropic, nov/2024): "USB das ferramentas de IA". Produtos da metáfora: **OpenAI Operator/ChatGPT agent** (CUA, visão de tela), **Google Project Jarvis** (agente no Chrome, visão de DOM).

**Ecossistema do usuário.** OpenClaw (original, jan/2026, 250K+ estrelas; furos: 42.665 instâncias expostas/93,4% sem auth, 341 skills maliciosas, $500–5K/mês, 100K+ linhas). GravityClaw (reimplementação TS lean: Telegram long-polling/zero portas, MCP-only, $200 fixo ou local, brick-by-brick; stack grammy+@anthropic-ai/sdk+better-sqlite3/FTS5+Supabase/pgvector; deploy Railway/Docker; voz Whisper+ElevenLabs; heartbeat node-cron; também "feature store" que gera CLAUDE.md/prompt). Intelecto (Python ~3.000 linhas, anti-framework, Telegram, SQLite FTS5/BM25, SOUL/AGENTS/USER, OpenRouter+Ollama). Antidote (igual Intelecto, tema terminal/hacker, output .md tool-agnostic, TEM guia de build). Hermes (self-hosted, "um cérebro várias bocas", memória/personas/skills/MCP/cron/sub-agentes/segurança → "SO de IA"). claude-hermes-os ("Claude OS": painel local read-only de Claude Code/Codex/OpenClaw/Obsidian/Pinecone → gasto, memória 3D, skills, "Dream" diário). OpenClaw+Ollama (Docker compose, lab local: portas 18789/18790/11434; modelos por RAM: llama3.2 3B@8GB, 8b@16GB; CPU 30-60s/resp).

**Anatomia (6 camadas).** IDENTIDADE base (soul.md/CLAUDE.md = ficha de personagem; "sem o brain rewire é só uma pasta"). CANAIS (Telegram token+whitelist preferido por não ter servidor web; WhatsApp; Claude Code). FERRAMENTAS/Connections (dados reais via MCP="USB", API, navegador; "sem isso responde como estranho"). SKILLS/Capabilities (SKILL.md = receita; carrega só frontmatter ~100 tokens até acionar; auto-corrige). AGENTES (sub-agente queima o próprio contexto e devolve só a resposta; cadência=cron/routines/heartbeat "com laptop fechado"). CÉREBROS = motor LLM trocável **+** memória organizada.

**CÉREBROS — correção (crítico).** NÃO é conselho/juiz/roteador de vários LLMs. É (1) o motor LLM **plugável** (hot-swap `.env` LLM_PROVIDER=anthropic|openrouter|ollama) e (2) a memória em **3 cérebros**: Projeto (episódico), Self (identidade, muda devagar), Conhecimento (referência, acumula) + inbox + skill /triagem; [[wikilinks]] cruzam. Memória = filesystem .md + SQLite FTS5/BM25. CLAUDE.md/AGENTS.md = roteador lido no início da sessão. "Múltiplos modelos" honesto = substituição/portabilidade (Agent Skills + polyskill cross-runtime), não votação simultânea.

**CLAWS / 4 C.** Context · Connections · Capabilities · Cadence (ordem 1-2-3-4). Build Levels: Foundation→Memory→Voice→Tools/MCP→Heartbeat. Segurança não-negociável: whitelist, secrets no .env, limite de iterações, confirmação p/ shell perigoso, local-first, audit log.

**Mobile/voz.** agentejax (TS, Telegram, @BotFather, whitelist, 24/7; voz no Step 16: .ogg→ffmpeg→Whisper STT, TTS tts-1 voz "nova"; OPENAI_API_KEY≠ANTHROPIC_API_KEY). agentevoz (Python/FastAPI, WhatsApp via Evolution API, Policy Engine decide texto/voz/humano + barato vs premium; roadmap v1 texto→v2 voz assíncrona Whisper+TTS→v3 ligação Twilio/LiveKit <1,5s). "Voz é interface, orquestrador é cérebro." Nenhum cria app nativo: "Telegram já é mobile". On-device via Ollama.

**Crianças.** 4 alicerces: PERSONA (soul.md, perfis intercambiáveis "modo historinha"/"lição de casa") + GUARDRAILS (agents.md SEMPRE/NUNCA + zero-trust: anti prompt-injection, sandbox, gates, audit log) + CANAIS/voz + MEMÓRIA. Animabook: "Professor" ensina por diálogo socrático (alunos Lumi/Caio/Valen + robô PIX-Z dá definições). Socrático = perguntar→esperar→validar→revelar; "explica o raciocínio, não só a resposta". Khanmigo (Khan Academy): 68k→700k usuários. MIT RAISE 2025: socrático melhora matemática/digital. PERIGOS REAIS (use como alerta): FoloToy (ursinho $99 GPT-4o, nov/2025: conteúdo sexual/BDSM/facas — OpenAI revogou); Moxie (Embodied $799, "morreu" dez/2024 quando a empresa faliu — pais explicaram às crianças); Character.AI (processos 2024-2025). COPPA / privacidade de criança.
