# Fase 1 — Fundação e Interface (sem integrações)

**Status:** Publicada (06/10/2026) — Emenda 01/2026 do escopo: F1 NÃO depende de APIs
**Duração estimada:** 2–3 semanas
**Objetivo:** fundação de dados (modelo central + fixture sintética) + interface completa (App Shell com sidebar, design moderno, dashboards v1 com dados sintéticos) + LGPD documentada + licenças distribuídas.

## Tasks

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

## Critérios de saída da fase
- [ ] Modelo + fixture carregando (CA-1-12/13)
- [ ] App Shell no ar (CA-1-19..22)
- [ ] Dashboards v1 com dados sintéticos (CA-1-16..18)
- [ ] LGPD documentada (CA-1-27..30)
- [ ] Licenças distribuídas (CA-1-31/32)

## Integrações (movidas para a Fase 2 — Emenda 01)
Testes de conectividade, baseline 90d, ingestões reais e dashboards com dados reais. Referência em `03_documentos/fase-2-referencia/` (SPEC-F2-001 APIs, SPEC-F2-002 baseline); as SPECs oficiais da F2 serão geradas na liberação da fase.
