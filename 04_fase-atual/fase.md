# Fase 1 — Fundação e Interface

**Status:** Publicada (06/10/2026, Emenda 01) — **SEM dependência de integrações**
**Duração estimada:** 2–3 semanas
**Objetivo:** fundação do sistema (modelo de dados, fixture sintética, auth/perfis) + interface completa (shell com sidebar, design system moderno, telas de funil/campanhas/leads) operando com dados sintéticos. Integrações e dados reais ficam na **Fase 2** (SPEC-1-006).

**Decisão da Kim (06/10):** nada na Fase 1 depende de API ou credencial — o GATE-01 não bloqueia mais esta fase.

## Tasks

| ID | Task | SPEC | Leva | Dono | Status | Dependências |
|----|------|------|------|------|--------|--------------|
| T1.1 | Fixture sintética de funil (leads, SQLs, campanhas, estágios, vendas/perdas) | 1-001 | A | Kim | ☐ | — |
| T1.2 | Modelo de dados central (leads, histórico de estágios, vendas, perdas, campanhas) | 1-001 | A | Kim | ☐ | — |
| T1.3 | Auth + perfis (login, papéis admin/gestor/sdr/leitor, proteção de rotas) | 1-001 | A | Kim | ☐ | — |
| T1.4 | Design system (paleta, tipografia, componentes, dark mode) | 1-002 | B | Kim | ☐ | — |
| T1.5 | Shell da aplicação: sidebar + topbar + navegação | 1-002 | B | Kim | ☐ | T1.4 |
| T1.6 | Tela Dashboard Funil (estágios, conversão por etapa, tempo mediano) com fixture | 1-002 | C | Kim | ☐ | T1.2, T1.5 |
| T1.7 | Tela Campanhas (origem, custo, CPA) com fixture | 1-002 | C | Kim | ☐ | T1.2, T1.5 |
| T1.8 | Tela Leads (lista com busca e filtros por origem/estágio/campanha) | 1-002 | C | Kim | ☐ | T1.2, T1.5 |
| T1.9 | Documento de definição operacional de SQL p/ homologação | 1-003 | B | Kim | ☐ | — |
| T1.10 | Política LGPD: base legal, opt-out, retenção | 1-004 | B | Kim | ☐ | — |
| T1.11 | Distribuição das 5 licenças Skip + plano de aculturamento | 1-005 | B | Ronaldo | ☐ | — |
| T1.12 | Revisão de segurança da fundação (auth, segredos, PII) | 1-001 | D | Kim | ☐ | T1.3 |

## Levas

| Leva | Tasks | Elegível |
|---|---|---|
| A | T1.1, T1.2, T1.3 | agora |
| B | T1.4, T1.5, T1.9, T1.10, T1.11 | agora (T1.5 após T1.4, sequência intra-leva) |
| C | T1.6, T1.7, T1.8 | após levas A e B |
| D | T1.12 | após T1.3 |

## Critérios de saída da fase
- [ ] Sistema no ar com login, sidebar e 3 telas operando com fixture (CA-1-07..14)
- [ ] Fundação revisada em segurança (CA-1-06)
- [ ] Doc de SQL pronto p/ homologação (GATE-03)
- [ ] LGPD documentada (CA-1-18..21)
- [ ] Licenças distribuídas (GATE-06)

**Nota:** integrações (6 APIs), baseline real e dashboards com dados reais = **Fase 2** (SPEC-1-006, publicada como referência).
