# Skill X9 2.0 — Apresentações V4

Skill de IA que transforma um briefing ou um arquivo consolidado de cliente em uma apresentação estratégica no padrão visual V4/Genspark, com duas saídas:

- **HTML de alta fidelidade**, para revisar a narrativa e aprovar o visual rápido;
- **Google Slides ou PPTX editável**, construído com elementos nativos (caixas, textos, formas, cards), pronto para o time ajustar.

Funciona no Claude Code, no Claude.ai, no ChatGPT, no Gemini e em outros modelos: cada um tem o seu ponto de entrada.

## Como usar

| Onde você está | Comece por |
|---|---|
| Claude Code (com terminal e arquivos) | [`SKILL.md`](./SKILL.md) |
| Claude.ai ou API, sem terminal | [`PROMPT_CLAUDE.md`](./PROMPT_CLAUDE.md) |
| ChatGPT | [`PROMPT_GPT.md`](./PROMPT_GPT.md) |
| Gemini | [`PROMPT_GEMINI.md`](./PROMPT_GEMINI.md) |
| Outro modelo | [`PROMPT_UNIVERSAL.md`](./PROMPT_UNIVERSAL.md) |

## Como funciona

1. O pedido vira um roteiro: tese central, capítulos, métricas, gargalos e próximos passos.
2. O roteiro vira um arquivo intermediário, o **X9 Deck IR** (JSON validado por [`schemas/x9-deck-ir.schema.json`](./schemas/x9-deck-ir.schema.json)).
3. A partir do mesmo IR saem o HTML, o PPTX e o Google Slides, sempre com o mesmo conteúdo.
4. Antes de entregar, roda a revisão de qualidade visual e estrutural.

## Estrutura

| Pasta | Conteúdo |
|---|---|
| `references/` | Manual da skill: arquitetura, design system, layouts, Google Slides editável, contrato do HTML, revisão de qualidade e biblioteca de padrões visuais |
| `schemas/` | Esquema JSON do X9 Deck IR |
| `scripts/` | Geradores de HTML, PPTX e Google Slides a partir do IR, login no Google e envio ao Drive |
| `templates/` | IR de exemplo |
| `assets/` | HTML de exemplo gerado pela skill |
| `testes-formatos/` | Comparações de formatos e referências visuais usadas para calibrar o estilo |

## Requisitos

```bash
npm install   # googleapis e pptxgenjs
```

Para criar decks direto no Google Slides, siga [`references/10-setup-google-slides-mcp.md`](./references/10-setup-google-slides-mcp.md) no primeiro uso.

## Repositório

Repositório oficial desde 20/10/2026: <https://github.com/edervasconcelos/skill-x9-apresentacoes-v4>. O antigo `edervasconcelosv4/skill-x9-apresentacoes-v4` está congelado.

Mantido por Eder Vasconcelos (V4 Company).
