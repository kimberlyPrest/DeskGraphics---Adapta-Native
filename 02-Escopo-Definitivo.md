# DeskGraphics — Escopo Definitivo v1.1
## Central de Inteligência Comercial On-Time

**Cliente:** Deskgraphics Realize Tecnologia (Rio de Janeiro, ~60 funcionários, parceira Autodesk, segmento AECO)
**Consultora técnica:** Kim · **Gerente:** Erik
**Versão:** 1.1 — Emenda 01/2026 (06/10): Fase 1 reescopada para fundação + interface sem integrações; integrações e baseline → Fase 2. APROVADO (consultora + cliente/CSM em 06/10/2026)
**Fontes:** 1ª Consultoria 17/09 (tl;dv `6aac1c86d1e2410013ab3ab4`), briefing oficial `desk.pdf`, análise crítica 17/09, escopo base 14/09

---

## 0. Como ler este documento

Este é o contrato executável do projeto. As seções 1–3 fixam objetivo e métricas; 4–7 descrevem recorte, atores, fluxo e arquitetura; 8–9 definem fases e gates; 10–12 registram decisões, riscos e a cláusula de salvamento. O Anexo A traz as perguntas de validação da 2ª consultoria (06/10) — **as respostas geram emendas na v1.2**.

Status: **APROVADO** — consultora + cliente/CSM em 06/10/2026.

**Emenda 01/2026 (06/10):** a Fase 1 foi redefinida para NÃO depender de integrações — fundação de dados + interface (login, sidebar, design moderno, dashboards sobre fixture). Credenciais, ingestões, baseline e dados reais movidos para a Fase 2.

---

## 1. Resultado de negócio (objetivo)

Centralizar e tornar **on-time** a inteligência do funil comercial DeskGraphics — da captura do lead (Meta Ads, RD Station, CREA, site) à qualificação (SDR), passagem para o pipeline comercial (HubSpot) até o fechamento — com:

1. **Dashboards on-time** de campanhas e funil (hoje o Ronaldo recebe o resultado só no fim do mês);
2. **Workflows e cadências automatizadas dentro do HubSpot** (hoje: zero configuração — a única automação existente é RD→HubSpot);
3. **Loops de valor** de melhoria contínua (roteiros, cadências, CPA);
4. **Relatório trimestral Autodesk** gerado a partir dos dados centralizados.

Palavra do cliente na 1ª consultoria (Flávio): *"capturar todos os dados que envolvem a entrada do lead, a qualificação do lead e a entrada dele no nosso pipeline até o fechamento, de forma on-time"* e *"o nosso processo seja sempre evolutivo"*.

---

## 2. Critérios de sucesso (KPIs)

### 2.1 KPIs do contrato (briefing oficial `desk.pdf`)

| # | KPI | Meta | Baseline | Definição operacional | Anti-gameação |
|---|-----|------|----------|----------------------|---------------|
| K1 | Conversão SQL→Venda | **+20%** | 90 dias congelados | (vendas fechadas no período) ÷ (SQLs criadas no período), por cohort de entrada | SQL só muda de estágio com critério homologado (GATE-03); motivo de perda obrigatório |
| K2 | Ciclo SQL→Venda | **−20%** | 90 dias congelados | mediana dos dias entre criação da SQL e data de fechamento (ganho ou perda) | mediana, não média (outliers); relógio para na perda |
| K3 | Receita por SQL | **+20%** | 90 dias congelados | soma do valor fechado ÷ nº de SQLs do período | valor = contrato assinado, não forecast |

**⚠️ Tensão registrada (AC-001 da análise crítica):** os KPIs do briefing medem **SQL→Venda**, mas a conversa da 1ª consultoria cobriu o funil inteiro (captura→fechamento). Proposta de resolução: **K1–K3 são os KPIs do contrato**; o funil completo é a infraestrutura que os habilita (não se pode melhorar SQL→Venda sem ver o que acontece antes e depois). Confirmar na call de hoje.

### 2.2 KPIs operacionais (acordados na 1ª consultoria)

| # | KPI | Meta | Dono |
|---|-----|------|------|
| K4 | Rastreabilidade de origem | 100% dos leads com campanha/peça identificada no dashboard | Flávio |
| K5 | Dashboard on-time | dados de campanha/funil atualizados com defasagem ≤ 24h (a definir) | Ronaldo |
| K6 | Relatório trimestral Autodesk | gerado a partir da fonte centralizada, sem montagem manual | Ronaldo |
| K7 | Lista diária de oportunidades | SDR recebe toda manhã a lista priorizada (ex.: lead parado + entrou em treinamento = quente) | SDR/Flávio |

---

## 3. Recorte

### 3.1 Entra
- Funil comercial completo: captura → qualificação (SDR) → SQL → pipeline comercial → fechamento/perda
- Inteligência de campanhas (Meta Ads) com dashboard on-time
- Workflows/cadências **dentro do HubSpot** (e-mail, WhatsApp, nutrição no pipeline comercial)
- Visibilidade das conversas de WhatsApp (nível de atendimento por SDR/vendedor/closer)
- Análise de calls (Read.ai) e participação em treinamentos (Vimeo/DeskHub → campo no HubSpot)
- Lista diária de melhores oportunidades para o SDR
- Relatório trimestral Autodesk
- Métrica de participação em treinamento (formulário → campo no HubSpot → % de quem comprou e participou)

### 3.2 Não entra (1º ciclo)
- **DeskHub** (plataforma EAD, 2–3 mil profissionais): integração profunda fica para fase futura — Ronaldo foi explícito ("não agora"); entra só o dado de participação em treinamento
- **PMO Vision** (contratos de serviço) e **Partner Center** (licenças): futuro (Prieto)
- Substituir HubSpot, RD Station ou qualquer ferramenta atual
- Agente de IA autônomo em contato com cliente (IA sempre assistiva, humano no loop)
- Geração de demanda (novas campanhas/criativos) — escopo de marketing, não de sistema
- CRIA parceria com Autodesk (campanha em andamento, meta de outubro) — o sistema **mede**, não executa

---

## 4. Atores e papéis

| Ator | Papel no projeto |
|------|-----------------|
| **Ronaldo Chaves** | Champion / gerente de entrega; dono do dashboard on-time e do relatório Autodesk |
| **Flávio Bordalo** | Gerente de marketing; dono de campanhas, cadências e roteiros |
| **José Chaves** | Gerente de negócios e serviços; visão comercial |
| **Marcos Prieto** | Diretor de serviços; visão de contratos (PMO Vision, futuro) |
| **Antônio Chaves** | Desenvolvedor principal; apoio técnico e integrações |
| **Michel** | Detentor dos acessos/tokens das APIs (Meta, HubSpot, RD, WhatsApp, Read.ai, Vimeo) |
| **SDRs / Inside Sales / pré-venda** | Usuários do funil; fonte dos dados de qualificação |
| **Kim** | Consultora técnica; desenha, implementa e valida |
| **Erik** | Gerente do projeto (Adapta) |

---

## 5. Fluxo de valor (10 passos)

1. **Lead chega** — Meta Ads, RD Station, CREA, site, indicação (origem/campanha/peça registrada)
2. **RD Station captura** e empurra para o HubSpot (automação existente, confirmada na call)
3. **SDR qualifica** — roteiro de abordagem; call/mensagem registrada
4. **SQL definida** — critério homologado (GATE-03); lead vira oportunidade
5. **Passagem para o pipeline comercial** — handoff SDR→Inside Sales/closer
6. **Atuação comercial** — reunião de diagnóstico online (Read.ai grava); pré-venda técnica quando a oportunidade exige ganho técnico
7. **Fechamento ou perda** — motivo de perda obrigatório; valor real no fechamento
8. **Dados alimentam os dashboards on-time** — campanhas, funil, conversão por etapa
9. **Loops de valor** — cadências disparam (lead parado, pós-treinamento, pós-diagnóstico); agente analisa e sugere melhoria de roteiro/cadência; CPA monitorado
10. **Relatório trimestral Autodesk** — consolidado da fonte centralizada (impressões, views, posts, resultados, vendas)

---

## 6. Arquitetura e integrações

### 6.1 Princípios
- **HubSpot = fonte de verdade do funil** (CRM central confirmado na call; pipeline SDR integrado ao comercial)
- **Workflows rodam dentro do HubSpot** — não construir sistema paralelo de automação
- **Skip/Maestro = camada de construção e análise** (dashboards, agente de análise de campanhas, relatório Autodesk)
- **IA assistiva sempre** — nenhuma IA contata cliente sem humano no loop (1º ciclo)

### 6.2 Integrações (todas pendentes de credencial — GATE-01)

| Integração | Uso | Status |
|-----------|-----|--------|
| **HubSpot API** | ler/escrever funil, criar workflows, campos de participação | pedida 17/09; com Michel |
| **RD Station API** | confirmar automação RD→HubSpot e dados de captura | automação confirmada verbalmente; API a validar |
| **Meta Ads API** | campanhas, conjuntos, peças, custo, CPA | pedida; com Michel |
| **WhatsApp API** | visibilidade de conversas + disparos de cadência | Huug chegando na semana da call — confirmar se entrou no ar e qual API expõe |
| **Read.ai API** | transcrições/análise de calls de diagnóstico | pedida; com Michel |
| **Vimeo API** | webinários/podcasts (participação e consumo) | pedida; com Michel |
| **DeskHub** | só o dado de participação em treinamento (fase futura: integração profunda) | fora do 1º ciclo |
| **Formulário de inscrição** | fluxo de inscrição em treinamento → campo no HubSpot | fluxo a mapear (Zoom na Adapta; aqui: confirmar ferramenta) |

### 6.3 Onde roda o quê
- **Dashboards**: construídos no Skip (App Builder), lendo as APIs
- **Agente de análise de campanhas**: Maestro/Skip, lendo os dados centralizados, sugerindo (nunca alterando campanha sem aprovação do Flávio)
- **Cadências**: nativas do HubSpot, criadas com apoio da IA
- **Relatório Autodesk**: gerado no Skip a partir dos dados centralizados

---

## 7. Regras de negócio (RNs)

- **RN-01** — Nenhum dado pessoal sai do ecossistema sem base legal LGPD registrada (GATE-05)
- **RN-02** — Toda cadência/workflow tem dono, critério de entrada, critério de saída e meta declarada
- **RN-03** — Motivo de perda é obrigatório para mover oportunidade para "perdida" (sem motivo = bloqueado)
- **RN-04** — SQL só é criada/mudança de estágio conforme critério homologado (GATE-03); ocultação no frontend não é prova
- **RN-05** — Dashboard on-time = defasagem máxima definida no GATE-04 (proposta: 24h para campanhas, 1h para funil)
- **RN-06** — Relatório Autodesk usa exclusivamente a fonte centralizada (nada de montagem manual paralela)
- **RN-07** — Baseline de 90 dias é congelado ANTES de qualquer mudança de processo (GATE-02); sem baseline, nenhum KPI é reportado
- **RN-08** — Lista diária de oportunidades usa critérios explícitos e versionados (ex.: parado ≥ X dias + evento de engajamento)
- **RN-09** — Toda automação nova passa por período de observação (modo sombra) antes de valer para os KPIs
- **RN-10** — Acesso às APIs por token/segregado; segredos nunca em prompt ou repositório

---

## 8. Fases

### Fase 1 — Fundação e Interface, sem integrações (2–3 semanas) — Emenda 01
- [ ] Modelo de dados central + fixture sintética carregando
- [ ] App Shell: sidebar, topbar, design moderno, rotas protegidas
- [ ] Dashboard v1: funil e campanhas com dados sintéticos (banner "dados de demonstração")
- [ ] LGPD: base legal, opt-out, política de dados (GATE-05)
- [ ] Distribuição das 5 licenças Skip (GATE-06)

### Fase 2 — Integrações e Baseline (2 semanas) — destravada por GATE-01
- [ ] Credenciais das 6 APIs entregues e testadas (GATE-01)
- [ ] Extração e congelamento do baseline de 90 dias (GATE-02)
- [ ] Definição operacional de SQL homologada (GATE-03)
- [ ] Defasagem do dashboard definida (GATE-04)
- [ ] Ingestões reais HubSpot + Meta Ads → modelo central
- [ ] Dashboards v1 com dados reais (sem banner demo)

### Fase 3 — Workflows e cadências (3–4 semanas)
- [ ] Primeiras 3 cadências aprovadas pelo Flávio (ex.: lead parado 3 dias; pós-treinamento; reativação de SQL fria)
- [ ] Nutrição no pipeline comercial (comportamento → ação automática)
- [ ] Campo de participação em treinamento + fluxo de inscrição → HubSpot
- [ ] Modo sombra de cada cadência antes de valer para KPI (RN-09)

### Fase 4 — Loops de valor (3 semanas)
- [ ] Agente de análise de campanhas (CPA, o que melhorou/piorou, sugestões)
- [ ] Loop de melhoria de roteiros (análise de calls Read.ai + objeções)
- [ ] Relatório trimestral Autodesk automatizado (K6)
- [ ] Revisão de cadências com base nos dados (o que converte, o que morre)

### Fase 5 — Medição e consolidação (2 semanas)
- [ ] Medição K1–K3 vs baseline congelado
- [ ] Consolidação do relatório de resultado do ciclo
- [ ] Decisão de expansão (DeskHub, PMO Vision, Partner Center)

---

## 9. Gates (dono + fase bloqueada)

| Gate | O quê | Dono | Bloqueia |
|------|-------|------|----------|
| GATE-01 | Credenciais das 6 APIs (Meta, HubSpot, RD, WhatsApp, Read.ai, Vimeo) | Michel | F2 inteira |
| GATE-02 | Baseline 90d extraído e congelado | Kim + Flávio | Relatório de KPIs (F5) e qualquer otimização |
| GATE-03 | Definição operacional de SQL | Flávio + José | F2 e K1–K3 |
| GATE-04 | Defasagem aceitável do dashboard on-time | Ronaldo | F2 |
| GATE-05 | LGPD: base legal, opt-out, retenção | Kim + cliente | F3 (cadências) |
| GATE-06 | 5 licenças Skip distribuídas | Ronaldo | Aculturamento (não bloqueia F1 técnica) |
| GATE-07 | Aprovação das primeiras cadências | Flávio | F3 |
| GATE-08 | Campos exatos do relatório Autodesk | Ronaldo | F4 (relatório) |

---

## 10. Decisões (DEC)

- **DEC-01** — HubSpot é a fonte de verdade do funil; não construir CRM próprio
- **DEC-02** — Workflows/cadências nativos do HubSpot; nenhum motor paralelo de automação
- **DEC-03** — Skip/Maestro como camada de construção (dashboards, agente, relatório)
- **DEC-04** — DeskHub fora do 1º ciclo (só o dado de participação em treinamento)
- **DEC-05** — IA assistiva; nenhuma IA contata cliente sem humano no loop no 1º ciclo
- **DEC-06** — Baseline-first: sem baseline congelado, nenhum KPI é reportado
- **DEC-07** — K1–K3 (SQL→Venda) são os KPIs do contrato; o funil completo é infraestrutura (a confirmar na call)
- **DEC-08** — LGPD como pré-condição de cadências, não como retrabalho posterior
- **DEC-09** — Interface dark/glass moderna (referência AUROVIA): fundação e interface construídas na F1 sem depender de integração; ajustável à marca do cliente

---

## 11. Riscos

| Risco | Impacto | Mitigação |
|-------|---------|-----------|
| APIs não chegarem (Michel) | F2 inteira parada | Cobrar na call; definir prazo; F1 (fundação + interface) NÃO depende e avança por completo |
| Baseline de 90d não extraível do HubSpot | K1–K3 inverificáveis | GATE-02 antes de tudo; se HubSpot não exportar, reconstruir baseline de planilhas existentes |
| "SQL" continuar indefinido | KPIs manipuláveis | GATE-03 com critério binário e auditável |
| Huug/WhatsApp sem API utilizável | Sem visibilidade de conversas | Confirmar na call o que o Huug expõe; plano B: API oficial Meta |
| Escopo inflar (DeskHub, PMO, Partner) | Ciclo de 4 meses estoura | DEC-04; expansão só na F5 |
| Campanha CREA/Autodesk com meta em outubro | Pressão por resultado antes do baseline | Sistema mede; resultado de outubro é leitura, não meta do projeto |

---

## 12. Cláusula de salvamento

Se qualquer premissa deste escopo se mostrar inviável (API indisponível, baseline inextrável, definição de SQL rejeitada), a fase afetada é reescopada em emenda registrada neste documento — o projeto não para: o que não depende do gate bloqueado continua (ex.: sem APIs, a Fase 2 aguarda enquanto a Fase 1 — fundação e interface — avança por completo).

---

## 13. Emendas

### Emenda 01/2026 (06/10) — Fase 1 reescopada
Decisão da Kim: a Fase 1 NÃO depende de integrações. F1 = fundação de dados (modelo central + fixture sintética) + interface completa (App Shell com sidebar, design moderno, dashboards v1 com dados sintéticos) + LGPD + licenças. Integrações (APIs), baseline de 90 dias, ingestões reais e dashboards com dados reais movidos para a Fase 2, destravada pelo GATE-01. Fases 3–5 inalteradas (renumeradas).

## Anexo A — Perguntas de validação para a 2ª consultoria (06/10, 17h)

1. **SQL (D3/GATE-03):** o que exatamente transforma um lead em SQL? Critério binário — quem decide: Flávio, José ou o SDR?
2. **Baseline (D2/GATE-02):** confirmar os 90 dias e quem extrai do HubSpot (precisa de acesso admin).
3. **APIs (GATE-01):** Michel entrega quando? Lista: Meta Ads, HubSpot, RD, WhatsApp/Huug, Read.ai, Vimeo.
4. **Recorte (D1/DEC-07):** confirmar que K1–K3 (SQL→Venda) são os KPIs do contrato e o funil completo é infraestrutura.
5. **Cadências (GATE-07):** quais as primeiras 3? Quem aprova? (sugestão: lead parado 3 dias; pós-treinamento; SQL fria)
6. **WhatsApp/Huug:** o Huug entrou no ar? Que API ele expõe (visibilidade de conversas + disparos)?
7. **Treinamento:** qual o fluxo de inscrição hoje (formulário? qual ferramenta?) e onde mora a lista de participantes?
8. **Relatório Autodesk (GATE-08):** quais campos exatos o fabricante pede no relatório trimestral?
9. **LGPD (GATE-05):** base legal para cadências por e-mail/WhatsApp; quem responde pela política?
10. **Licenças Skip (GATE-06):** quem são os 5? (Ronaldo sugeriu: Antônio, José, Maria + 2; Prieto sugeriu alguém do back office)
11. **Competição interna de aculturamento:** Ronaldo gostou da ideia — entra no plano como ação paralela da F1?
12. **CREA/Autodesk:** a meta de outubro precisa de qual leitura do sistema? (dashboard de campanha basta?)
13. **Design (DEC-09):** dark/glass moderno serve, ou há identidade visual da marca para seguir?
