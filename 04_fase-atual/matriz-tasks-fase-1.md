# Matriz de Rastreabilidade — Fase 1 (Emenda 01: sem integrações)

| Ref (escopo) | Requisito | SPEC | CAs | Tasks |
|---|---|---|---|---|
| §5, §6.3 | Modelo central + fixture sintética | 1-004 | CA-1-12..15 | T1.1, T1.2 |
| §5, §6.3 | Dashboards v1 (funil + campanhas) com dados sintéticos | 1-004 | CA-1-16..18 | T1.4, T1.5, T1.6 |
| §6.3, DEC-03 | App Shell (sidebar,/design, rotas) | 1-003 | CA-1-19..22 | T1.3 |
| RN-01, DEC-08 | LGPD: base legal, opt-out, retenção | 1-005 | CA-1-27..30 | T1.7 |
| GATE-06 | Licenças + aculturamento | 1-006 | CA-1-31..32 | T1.8 |

## Levas

| Leva | Tasks | Independência |
|---|---|---|
| A | T1.1, T1.2 | independentes |
| B | T1.3, T1.7, T1.8 | T1.3 depende de T1.2 (leva anterior) |
| C | T1.4, T1.5 | dependem de T1.1+T1.3 (levas anteriores) |
| D | T1.6 | depende de T1.4 (leva anterior) |

**Totais:** 32 CAs únicos · 8 tasks · 4 levas · 0 dependência intra-leva · 0 dependência de API.

**Movidos para a Fase 2 (Emenda 01):** CA-1-01..04 (APIs, SPEC-1-001), CA-1-05..08 (baseline, SPEC-1-002), CA-1-09..11 (definição de SQL — SPEC a detalhar na F2, GATE-03).
