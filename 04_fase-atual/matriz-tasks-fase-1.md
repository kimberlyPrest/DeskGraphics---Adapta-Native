# Matriz de Rastreabilidade — Fase 1 (Emenda 01)

| Ref (escopo) | Requisito | SPEC | CAs | Tasks |
|---|---|---|---|---|
| §5, §6.3 | Modelo central + fixture + auth/perfis | 1-001 | CA-1-01..06 | T1.1, T1.2, T1.3, T1.12 |
| §6.3 | Interface: shell, sidebar, design system, 3 telas | 1-002 | CA-1-07..14 | T1.4, T1.5, T1.6, T1.7, T1.8 |
| §2.1, AC-004 | Definição operacional de SQL | 1-003 | CA-1-15..17 | T1.9 |
| RN-01, DEC-08 | LGPD: base legal, opt-out, retenção | 1-004 | CA-1-18..21 | T1.10 |
| GATE-06 | Licenças + aculturamento | 1-005 | CA-1-22..23 | T1.11 |
| §6.2, §8-F2 | Integrações, baseline e dados reais (**Fase 2**) | 1-006 | CA-1-24..27 | — (F2) |

## Levas

| Leva | Tasks | Independência |
|---|---|---|
| A | T1.1, T1.2, T1.3 | independentes |
| B | T1.4, T1.5, T1.9, T1.10, T1.11 | T1.5 depende de T1.4 (sequência intra-leva declarada) |
| C | T1.6, T1.7, T1.8 | dependem de A+B (levas anteriores) |
| D | T1.12 | depende de T1.3 (leva anterior) |

**Totais:** 27 CAs únicos · 12 tasks · 4 levas · 0 dependência de integração na F1.
