# Matriz de Rastreabilidade — Fase 1

| Ref (escopo) | Requisito | SPEC | CAs | Tasks |
|---|---|---|---|---|
| §6.2 | 6 integrações testadas e documentadas | 1-001 | CA-1-01..04 | T1.2 |
| §2.1, RN-07 | Baseline 90d congelado | 1-002 | CA-1-05..08 | T1.3, T1.5 |
| §2.1, AC-004 | Definição operacional de SQL | 1-003 | CA-1-09..11 | T1.4 |
| §5, §6.3 | Modelo central + ingestões + dashboard v1 | 1-004 | CA-1-12..18 | T1.1, T1.6, T1.7, T1.8, T1.9, T1.10 |
| RN-01, DEC-08 | LGPD: base legal, opt-out, retenção | 1-005 | CA-1-19..22 | T1.11 |
| GATE-06 | Licenças + aculturamento | 1-006 | CA-1-23..24 | T1.12 |

## Levas

| Leva | Tasks | Independência |
|---|---|---|
| A | T1.1, T1.2 | independentes |
| B | T1.3, T1.4, T1.11, T1.12 | T1.3 depende de T1.2 (leva anterior) |
| C | T1.5, T1.6 | T1.5 depende de T1.3 (leva anterior) |
| D | T1.7, T1.8 | T1.7 depende T1.2+T1.6; T1.8 depende T1.2 (levas anteriores) |
| E | T1.9, T1.10 | T1.9 depende T1.7; T1.10 depende T1.8 (levas anteriores) |

**Totais:** 24 CAs únicos · 12 tasks · 5 levas · 0 dependência intra-leva.
