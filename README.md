# 🤖 Jarvis — Seu Sistema Operacional de IA

Curso aberto, em português e **para leigos**, sobre Jarvis e sistemas operacionais de IA. Do "o que é, afinal?" até montar o seu — no computador, no celular e até num brinquedo educativo.

**No ar:** https://inematds.github.io/jarvis/ · Parte do **[INEMA.CLUB](https://inema.club)**.

## As 6 trilhas

| # | Trilha | O que cobre |
|---|--------|-------------|
| 🌱 T1 | **Fundamentos** | O que é um Jarvis, o que é um LLM, e quando a IA passa a agir. Sem pré-requisitos. |
| 🗺️ T2 | **O Panorama** | Os sistemas que existem — OpenClaw, GravityClaw, Hermes, Intelecto, AIOS — e qual é o caminho. |
| 🧬 T3 | **Anatomia** | As 6 camadas: canais, identidade, ferramentas, skills, agentes e cérebros (uma por módulo). |
| 🛠️ T4 | **Construir um Jarvis eficaz** | Da receita mínima à arquitetura robusta (as 4 camadas: Context · Connections · Capabilities · Cadence). |
| 📱 T5 | **Jarvis no celular** | Canais (Telegram/WhatsApp), voz (STT/TTS) e modelo local. Sem app de loja. |
| 🧸 T6 | **Jarvis para crianças** | Tutor socrático, persona, voz — e a segurança inegociável. |

**21 módulos · 126 tópicos · ~18h.**

## Como foi construído

Pesquisa estruturada (web + dezenas de projetos reais) → arquitetura → 27 páginas no **formato-curso-v2** do INEMA, com verificação por página. Tudo documentado em **[doc/metodologia.html](doc/metodologia.html)** e no `_build/BIBLE.md`.

## Estrutura

```
index.html                 landing (as 6 trilhas + progresso do curso)
doc/metodologia.html       como o curso foi pesquisado e construído (transparência)
curso/trilhaN/index.html   índice de cada trilha (mapa + módulos)
curso/trilhaN/modulo-N-M.html  os 21 módulos
assets/learn.css|js        camada de aprendizagem (progresso, jornada, temas) — self-contained
_build/                    kit de construção (templates + bible) — documentação interna
```

100% estático (Tailwind via CDN + JS inline). Abre direto no navegador, sem build nem servidor.

---

Feito com ❤️ pela comunidade **INEMA.CLUB**.
