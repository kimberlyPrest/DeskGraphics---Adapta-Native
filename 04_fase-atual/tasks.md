# Tasks — Fase 1 (Fundação e Interface)

**Status geral:** 0/12 concluídas · 4 levas · **sem dependência de integrações** (Emenda 01, 06/10)

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
| B | T1.4, T1.5, T1.9, T1.10, T1.11 | agora |
| C | T1.6, T1.7, T1.8 | após A e B |
| D | T1.12 | após T1.3 |
