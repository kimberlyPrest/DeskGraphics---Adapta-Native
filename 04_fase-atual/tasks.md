# Tasks — Fase 1 (Fundação e Baseline)

**Status geral:** 0/12 concluídas · 5 levas · execução inicia após GATE-01

| ID | Task | SPEC | Leva | Dono | Status | Dependências |
|----|------|------|------|------|--------|--------------|
| T1.1 | Fixture sintética de funil (leads, SQLs, campanhas, estágios) | 1-004 | A | Kim | ☐ | — |
| T1.2 | Teste de conectividade das 6 APIs (Meta, HubSpot, RD, WhatsApp/Huug, Read.ai, Vimeo) | 1-001 | A | Kim | ☐ | GATE-01 |
| T1.3 | Extração do baseline 90d do HubSpot | 1-002 | B | Kim | ☐ | T1.2 |
| T1.4 | Documento de definição operacional de SQL p/ homologação | 1-003 | B | Kim | ☐ | — |
| T1.5 | Congelamento do baseline + documento assinado | 1-002 | C | Kim | ☐ | T1.3 |
| T1.6 | Modelo de dados centralizado (leads/campanhas/estágios) | 1-004 | C | Kim | ☐ | — |
| T1.7 | Ingestão HubSpot → modelo central | 1-004 | D | Kim | ☐ | T1.2, T1.6 |
| T1.8 | Ingestão Meta Ads → modelo central | 1-004 | D | Kim | ☐ | T1.2 |
| T1.9 | Dashboard v1: visão de funil (estágios, conversão por etapa) | 1-004 | E | Kim | ☐ | T1.7 |
| T1.10 | Dashboard v1: visão de campanhas (origem, custo, CPA) | 1-004 | E | Kim | ☐ | T1.8 |
| T1.11 | Política LGPD: base legal, opt-out, retenção | 1-005 | B | Kim | ☐ | — |
| T1.12 | Distribuição das 5 licenças Skip + plano de aculturamento | 1-006 | B | Ronaldo | ☐ | — |

## Levas

| Leva | Tasks | Elegível quando |
|---|---|---|
| A | T1.1, T1.2 | agora (T1.2 depende de GATE-01) |
| B | T1.3, T1.4, T1.11, T1.12 | T1.3 após T1.2 |
| C | T1.5, T1.6 | T1.5 após T1.3 |
| D | T1.7, T1.8 | após T1.2 e T1.6 |
| E | T1.9, T1.10 | após T1.7 / T1.8 |
