# Tasks — Fase 1 (Fundação e Interface, sem integrações)

**Status geral:** 0/8 concluídas · 4 levas · NENHUMA task depende de API (Emenda 01, 06/10)

| ID | Task | SPEC | Leva | Dono | Status | Dependências |
|----|------|------|------|------|--------|--------------|
| T1.1 | Fixture sintética de funil (leads, SQLs, campanhas, estágios) | 1-004 | A | Kim | ☐ | — |
| T1.2 | Modelo de dados centralizado (leads/campanhas/estágios) | 1-004 | A | Kim | ☐ | — |
| T1.3 | App Shell: sidebar, topbar, design moderno, rotas protegidas | 1-003 | B | Kim | ☐ | T1.2 |
| T1.4 | Dashboard v1: visão de funil (estágios, conversão por etapa) — dados sintéticos | 1-004 | C | Kim | ☐ | T1.1, T1.3 |
| T1.5 | Dashboard v1: visão de campanhas (origem, custo, CPA) — dados sintéticos | 1-004 | C | Kim | ☐ | T1.1, T1.3 |
| T1.6 | Lista de oportunidades (tela) com critérios versionados — dados sintéticos | 1-004 | D | Kim | ☐ | T1.4 |
| T1.7 | Política LGPD: base legal, opt-out, retenção | 1-005 | B | Kim | ☐ | — |
| T1.8 | Distribuição das 5 licenças Skip + plano de aculturamento | 1-006 | B | Ronaldo | ☐ | — |

## Levas

| Leva | Tasks | Elegível quando |
|---|---|---|
| A | T1.1, T1.2 | agora |
| B | T1.3, T1.7, T1.8 | T1.3 após T1.2 |
| C | T1.4, T1.5 | após T1.1+T1.3 |
| D | T1.6 | após T1.4 |

## Movidas para a Fase 2 (Emenda 01)
Testes de conectividade das 6 APIs, extração/congelamento do baseline 90d, ingestões reais HubSpot/Meta, dashboards com dados reais.
