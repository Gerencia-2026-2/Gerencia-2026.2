# Plano do Projeto

# SubTracker

**Gestão Inteligente de Assinaturas, Detecção por Extrato e Otimização de Recorrências**

| | |
|---|---|
| **Versão** | 4.0 |
| **Data de Início** | 03/08/2026 (Gestão) e 04/08/2026 (Desenvolvimento) |
| **Patrocinador** | Diogo Silveira Mendonça |
| **Gerência do projeto** | Davi Luiz Rodrigues da Conceição, João Henrique Lima Gualberto, Michael Patrick Ferreira da Silva Borba e Vinicius da Silva Mendes |
| **Equipe de desenvolvimento** | Ronald Teixeira de Assis, Rodrigo Américo Nascimento D'Icarahy e Thiago Souza da Silva |
| **Repositório** | https://github.com/SouzTH/SubTracker |
| **Documentos que este plano consolida** | Business Case v2.1, Termo de Abertura v1.2, EAP e Dicionário da EAP v2.1 |

> **Como ler este plano.** O Plano integra e aponta a fonte dos documentos-base. A EAP e o Dicionário definem o trabalho; o Business Case define a justificativa e os objetivos; este Plano define como tudo isso é gerenciado (prazo, custo, recursos, partes interessadas, riscos, controle).
>
> Itens marcados com [confirmar] dependem de validação da equipe. As decisões consolidadas estão no Anexo A.

---

# Sumário

1. Introdução
2. Escopo do Projeto
3. Estrutura Analítica do Projeto (EAP)
4. Dicionário da EAP (resumo)
5. Cronograma
6. Rede de Atividades
7. Orçamento (esforço e custo)
8. Recursos do Projeto
9. Partes Interessadas
10. Plano de Engajamento
11. Plano de Comunicação (Cadência)
12. Gerenciamento de Riscos
13. Controle e Monitoramento
14. Encerramento do Projeto

Anexo A. Decisões consolidadas do projeto

---

# 1. Introdução

## 1.1 Objetivo do Plano

Descrever como o projeto SubTracker será planejado, executado, monitorado e encerrado, integrando em um único plano o escopo, o prazo, o esforço e custo, os recursos, as partes interessadas e os riscos.

## 1.2 Visão Geral do Projeto

**Problema.** A proliferação de serviços por assinatura fragmenta as cobranças ao longo do mês. O usuário perde a visão do total comprometido e é surpreendido por débitos recorrentes de serviços que quase não usa.

**Proposta de valor.** O SubTracker unifica as assinaturas em uma visão cronológica e previsível e passa a:
- **Detectar assinaturas por extrato:** lê extratos em CSV e cruza as descrições com o catálogo de provedores.
- **Controlar tetos orçamentários:** metas de gasto por categoria, com barras de progresso.
- **Facilitar o cancelamento:** link direto para cancelar na plataforma do provedor.
- **Emitir relatório de impacto:** distribuição por categoria, ranking, projeção mensal e custo anual.

**Produto.** Aplicação web responsiva (mobile-first) com 5 entidades de domínio, 13 casos de uso ativos e 2 perfis de acesso.

**Situação atual e marcos.** O projeto teve seu kickoff em 03/08/2026 (Gestão) e 04/08/2026 (Desenvolvimento). O período de agosto a setembro foi dedicado ao levantamento de requisitos, prototipagem e planejamento. Os marcos de entrega são:
- **Marco 1:** 05/10/2026 (Documentos de gerência)
- **Marco 2:** 06/10/2026 (Frontend + json-server)
- **Marco 3:** 07 a 11/12/2026 (Integração Backend Real + Frontend)
- **Status Reports:** SR1 (12/10), SR2 (02/11), SR3 (16/11), SR4 (Data e escopo a definir).

## 1.3 Abordagem e Ciclo de Vida

**Abordagem híbrida**:
- **Preditiva** no que é estável: escopo, EAP, esforço por pacote, marcos e a data da entrega final.
- **Adaptativa** no desenvolvimento: cada módulo é construído e demonstrado em incrementos, com refinamento a partir do retorno da equipe.

## 1.4 Premissas Gerais

| # | Premissa | Fonte | Se for falsa, vira o risco |
|---|----------|-------|----------------------------|
| P1 | Há extratos de teste sintéticos em CSV, de pelo menos 3 layouts diferentes e com 10 ou mais lançamentos, disponíveis desde o início de 1.3.5 e 1.4.5. | Business Case (O2) | R1 |
| P2 | A dedicação é de **4 h por semana por pessoa** (3 desenvolvedores e 4 gerentes), sem considerar feriados. | Dicionário | R2 |
| P3 | O modelo de dados é congelado ao final de 1.4.1; mudanças posteriores passam por controle de mudanças. | Plano | R7 |
| P4 | Para contar dias úteis (DU), o Plano desconta sábados, domingos e feriados nacionais. | Plano | R7 |
| P5 | A infraestrutura é local e sem custo de produção (caixa é R$ 0,00). | Dicionário; Business Case | Orçamento |
| P6 | O Marco 2 usa `json-server` como protótipo. O Marco 3 exige o backend real (Express/Prisma/PostgreSQL) integrado. | Dicionário | R4 |
| P7 | A linha de base de importação de extratos é **CSV**. Leitura de OFX está fora do escopo. | Dicionário; Business Case | R1, R6 |
| P8 | As estimativas de esforço são por julgamento, sem base histórica. | Business Case | R2, R7 |
| P9 | Matheus não integra o desenvolvimento; a equipe é a descrita no cabeçalho. | Dicionário | R3 |

---

# 2. Escopo do Projeto

## 2.1 Objetivo

Entregar, até a segunda semana de dezembro de 2026 (Marco 3, 07 a 11/12/2026), um sistema web mobile-first que detecta assinaturas via CSV, centraliza o acompanhamento, monitora tetos e leva o usuário à página de cancelamento do provedor, com backend real integrado e documentação completa.

## 2.2 Requisitos

| ID | Requisito (necessidade) | Tipo | Origem | Objetivo (BC) | Pacotes (EAP) | Prioridade |
|----|-------------------------|------|--------|:-------------:|---------------|------------|
| RQ01 | Ver, em uma só tela, o total gasto no mês, as próximas cobranças em ordem de vencimento e o consumo frente às metas. | Negócio / Usuário | UC02 | O3 | 1.3.2, 1.3.4 | Média |
| RQ02 | Identificar assinaturas recorrentes a partir do extrato bancário, sem digitar uma a uma, e confirmar a conciliação. | Funcional | UC13, UC14 | O2 | 1.3.5, 1.4.5 | **Máxima** |
| RQ03 | Cadastrar uma assinatura manualmente, consultá-la com o histórico, pausá-la, editá-la ou excluí-la. O histórico pertence à Assinatura. | Funcional | UC01, UC03, UC04 | O1 | 1.3.2, 1.4.2 | Média / Básica |
| RQ04 | Definir um teto de gasto por categoria e acompanhar o quanto já foi consumido. | Funcional | UC09, UC10, UC11, UC12 | O1 | 1.3.4, 1.4.4 | Média / Básica |
| RQ05 | Chegar à página de cancelamento do provedor a partir da assinatura (consulta de catálogo). | Funcional | UC06, UC18 | O1 | 1.3.3, 1.4.3, 1.3.6 | **Máxima** / Básica |
| RQ06 | Entender o impacto financeiro das assinaturas: distribuição por categoria, ranking, projeção e custo anual. | Funcional | UC17 | O3 | 1.3.6, 1.4.6 | **Máxima** |
| RQ07 | Usabilidade no celular, com fluxos em etapas curtas, e perfis de acesso distintos. | Não funcional | Protótipo | O1, O3 | 1.3.1, 1.4.6 | Média |
| RQ08 | Aceitar apenas extratos em CSV (baseline), sem processar pagamentos ou conectar diretamente a bancos. | Restrição | UC13; exclusões de escopo | — | 1.3.5, 1.4.5 | — |

## 2.3 Declaração do Escopo

**Escopo do produto.** Cadastro e acompanhamento de assinaturas, importação e conciliação de extratos CSV, consulta ao catálogo de provedores com atalho de cancelamento, tetos orçamentários e relatório de impacto financeiro.

**Escopo do projeto.** Gerenciamento, prototipagem e requisitos, client-side, server-side, integração, testes e validação, e encerramento.

**Entregas principais**
1. **Gerenciamento (1.1):** Documentos, registro de riscos, plano de comunicação e 4 Status Reports.
2. **Prototipagem e requisitos (1.2):** Matriz de priorização, protótipo de 7 telas e matrizes.
3. **Client-side (1.3) e server-side (1.4):** Sistema SubTracker com os módulos e a estrutura de API real e banco de dados.
4. **Integração, testes e validação (1.5):** Fluxo integrado, checklist de testes manuais e sistema ajustado.
5. **Encerramento (1.6):** Documentação final e entrega.

## 2.4 Exclusões de Escopo

- Integração bancária direta e integração com cartões.
- Leitura de arquivos OFX.
- Processamento de pagamentos e dados de cartão.
- Cancelamento automático em nome do usuário.
- CRUD de catálogo (UCs 05, 07, 08) e histórico/descarte de extratos (UCs 15, 16).
- Aplicativo móvel nativo.
- Monetização do SubTracker.

## 2.5 Critérios de Aceite Gerais

| # | Critério | Objetivo (BC) | Pacote que verifica |
|---|----------|:-------------:|---------------------|
| 1 | **Importação:** em extrato CSV com 10+ lançamentos, reconhecer 80%+ das assinaturas; layout incompatível é rejeitado. | O2 | 1.3.5, 1.4.5, 1.5.2 |
| 2 | **Painel:** exibe total do mês, próximas cobranças e barras de consumo frente ao teto. | O1 | 1.3.2, 1.3.4, 1.5.2 |
| 3 | **Cancelamento:** botão "Cancelar no Provedor" abre a página cadastrada. | O1 | 1.3.3, 1.3.6, 1.5.2 |
| 4 | **Relatório:** custo anual coerente e distribuição por categoria somando 100%. | O1 | 1.3.6, 1.4.6, 1.5.2 |
| 5 | **Clareza:** 4 de 5 usuários encontram total mensal e projeção anual em até 30s. | O3 | 1.5.2 |
| 6 | **Integração:** os UCs ativos funcionam de ponta a ponta entre frontend, **API real (PostgreSQL)** e dados. | O1 | 1.5.1, 1.5.2 |
| 7 | **Esforço e custo:** esforço dentro da linha de base e caixa de R$ 0,00. | O4 | 1.1.2 |
| 8 | **Testes Manuais:** checklist de validação funcional e isolamento de dados entre usuários validados pela equipe. | O1 | 1.4.2, 1.5.2 |

## 2.6 Gerenciamento do Escopo

- **Quem valida regras de negócio:** o patrocinador.
- **Quem aprova mudança de escopo:** qualquer integrante propõe; a gerência avalia o impacto; o patrocinador aprova.
- **Aceite:** por pacote da EAP, conforme o Dicionário, não por tela isolada.
- **Linha de base do escopo:** declaração + EAP + Dicionário.

---

# 3. Estrutura Analítica do Projeto (EAP)

Reprodução da EAP decomposta por entrega:

- **1 SubTracker**
  - **1.1 Gerenciamento do Projeto**
    - 1.1.1 Documentação e acompanhamento do projeto
    - 1.1.2 Monitoramento, riscos e comunicação (SR1 a SR4)
  - **1.2 Prototipagem e Requisitos**
    - 1.2.1 Levantamento, priorização e rastreabilidade
    - 1.2.2 Prototipagem e matrizes de requisitos
  - **1.3 Client-Side**
    - 1.3.1 Estrutura de front-end e rotas
    - 1.3.2 Assinaturas e dashboard
    - 1.3.3 Serviços e cancelamento (Consulta e Link)
    - 1.3.4 Tetos e consumo orçamentário
    - 1.3.5 Extratos e conciliação
    - 1.3.6 Relatório e tutorial
  - **1.4 Server-Side**
    - 1.4.1 Estrutura da API real e modelagem do banco
    - 1.4.2 API de Assinaturas
    - 1.4.3 API de Serviços e Links
    - 1.4.4 API de Tetos
    - 1.4.5 Importação de extratos e conciliação
    - 1.4.6 Relatório, projeção e acesso
  - **1.5 Integração, Testes e Validação**
    - 1.5.1 Integração front-end/back-end
    - 1.5.2 Testes de validação funcional
    - 1.5.3 Ajustes e validação final
  - **1.6 Encerramento**
    - 1.6.1 Documentação final e entrega

**Totais:** 6 entregas e 20 pacotes de trabalho.

---

# 4. Dicionário da EAP (resumo)

| Pacote | Entregas (resumo) | Critério de aceite (resumo) | Responsável | Esforço (h) | Marco |
|--------|-------------------|-----------------------------|-------------|:-----------:|:-----:|
| **1.1.1** Documentação | Business Case, Termo, Plano, EAP e Dicionário | Documentos aprovados | Gerência | 20 | 1 |
| **1.1.2** Monitoramento | Riscos, comunicação, EVM (SR1 a SR4) | Relatórios entregues nos prazos | Gerência | **26** | 1, 2, 3 |
| **1.2.1** Levantamento | Matriz de priorização e rastreabilidade | UCs mapeados e priorização confirmada | Ronald, Rodrigo, Thiago | 10 | 1 |
| **1.2.2** Prototipagem | Protótipo de 7 telas, matrizes CRUD | Prototipagem concluída e validada | Ronald, Rodrigo, Thiago | 14 | 1 |
| **1.3.1** Estrutura Front | Projeto React/Vite/TS, rotas e layout | Rotas navegáveis e layout estável | Ronald | 16 | 2 |
| **1.3.2** Assinaturas | Painel, formulário, listagem, edição | UC01, UC02, UC03, UC04 | Ronald | 20 | 2 |
| **1.3.3** Serviços/Links | Consulta de catálogo e link de cancelamento | UC06, UC18 na interface | Thiago | **8** | 2 |
| **1.3.4** Tetos | Formulário, visão de consumo, indicadores | UC09 a UC12 operacionais | Thiago | 12 | 2 |
| **1.3.5** Extratos | Importação CSV e conciliação | UC13, UC14; rejeita layouts inválidos | Rodrigo | **12** | 2 |
| **1.3.6** Relatório | Tela de relatório e tutorial | UC17 e UC18 acessíveis | Ronald e Thiago | 8 | 2 |
| **1.4.1** Estrutura API | Estrutura da API real, entidades e banco | Modelo congelado e alinhado | Rodrigo | 10 | 2 |
| **1.4.2** API Assinaturas | Endpoints de assinaturas | UC01 a UC04 atendidos | Ronald | 8 | 2 |
| **1.4.3** API Serviços | Endpoints de links | UC06, UC18 atendidos | Thiago | **6** | 2 |
| **1.4.4** API Tetos | Endpoints de tetos | UC09 a UC12 atendidos | Thiago | 6 | 2 |
| **1.4.5** API Extratos | Upload e processamento de CSV | UC13, UC14 atendidos | Rodrigo | **8** | 2 |
| **1.4.6** API Relatório | Projeção e acesso | UC17 atendidos | Ronald e Thiago | 6 | 2 |
| **1.5.1** Integração | Integração Front + API Real | CRUD e importação ponta a ponta | Ronald, Rodrigo, Thiago | 10 | 3 |
| **1.5.2** Testes Manuais | Checklist, evidências e correções | Fluxos validados sem divergências | Ronald, Rodrigo, Thiago | 12 | 3 |
| **1.5.3** Ajustes Finais | Sistema ajustado, registros de correção | Sistema estável para entrega | Ronald, Rodrigo, Thiago | 8 | 3 |
| **1.6.1** Encerramento | Documentação final e repositório atualizado | Entregas revisadas e consistentes | Gerência + equipe | 8 | 3 |
| | | | **Total** | **228** | |

---

# 5. Cronograma

## 5.1 Gerenciamento do Prazo

- **Unidade:** dia útil (DU). Início em 03/08/2026.
- **Calendário:** descontados sábados, domingos e feriados nacionais.
- **Fonte das datas:** início e término previstos de cada pacote. Esforço (h) e duração são diferentes: um pacote de 16 h pode durar 6 semanas porque cada pessoa dedica 4 h por semana.
- **Base:** julgamento da equipe.
- **Mudança:** atraso acima de 3 DU no caminho crítico exige registro de mudança.
- **Acompanhamento:** revisão semanal.

## 5.2 Cronograma dos Pacotes

| Pacote | Predecessoras | Esforço (h) | Início | Fim | Duração (DU) | Folga (DU) | Marco |
|--------|---------------|:-----------:|--------|-----|:------------:|:----------:|:-----:|
| 1.1.1 Documentação | — | 20 | 03/08 | 05/10 | 1 | 0 | 1 |
| 1.1.2 Monitoramento | 1.1.1 (TI) | 26 | 05/10 | 11/12 | 47 | 0 | 1, 2, 3 |
| 1.2.1 Levantamento | 1.1.1 (II) | 10 | 03/08 | 05/10 | 1 | 0 | 1 |
| 1.2.2 Prototipagem | 1.2.1 (II) | 14 | 03/08 | 05/10 | 1 | 0 | 1 |
| 1.3.1 Estrutura Front | 1.2.2 (II) | 16 | 05/10 | 06/10 | 2 | 0 | 2 |
| 1.3.2 Assinaturas | 1.3.1 (II) | 20 | 05/10 | 06/10 | 2 | 0 | 2 |
| 1.3.3 Serviços/Links | 1.3.1 (TI) | 8 | 05/10 | 06/10 | 2 | 0 | 2 |
| 1.3.4 Tetos | 1.3.1 (TI) | 12 | 05/10 | 06/10 | 2 | 0 | 2 |
| **1.3.5 Extratos** ★ | 1.3.1 (II) | 12 | 05/10 | 06/10 | 2 | 0 | 2 |
| **1.3.6 Relatório** ★ | 1.3.2 a 1.3.5 (TI/TT) | 8 | 05/10 | 06/10 | 2 | 0 | 2 |
| 1.4.1 Estrutura API | 1.2.1 (TI) | 10 | 06/10 | 12/10 | 4 | 0 | 2 |
| 1.4.2 API Assinaturas | 1.4.1 (TI) | 8 | 12/10 | 31/10 | 14 | 5 | 2 |
| 1.4.3 API Serviços | 1.4.1 (TI) | 6 | 12/10 | 31/10 | 14 | 5 | 2 |
| 1.4.4 API Tetos | 1.4.1 (TI) | 6 | 12/10 | 31/10 | 14 | 5 | 2 |
| **1.4.5 API Extratos** ★ | 1.4.1 (II) | 8 | 06/10 | 17/11 | 29 | 0 | 2 |
| **1.4.6 API Relatório** ★ | 1.4.2 a 1.4.5 (TI/TT) | 6 | 10/11 | 17/11 | 6 | 0 | 2 |
| **1.5.1 Integração** ★ | 1.3.x e 1.4.x (TI) | 10 | 18/11 | 24/11 | 4 | 0 | 3 |
| **1.5.2 Testes** ★ | 1.5.1 (TI) | 12 | 25/11 | 03/12 | 7 | 0 | 3 |
| **1.5.3 Ajustes** ★ | 1.5.2 (TI) | 8 | 04/12 | 11/12 | 6 | 0 | 3 |
| **1.6.1 Encerramento** ★ | 1.5.3 (TT) | 8 | 07/12 | 11/12 | 5 | 0 | 3 |

★ = no caminho crítico.

## 5.3 Caminho Crítico e Folgas

- **Caminho crítico:** 1.3.5 e 1.4.5 (extratos) → 1.3.6 e 1.4.6 → 1.5.1 → 1.5.2 → 1.5.3 → 1.6.1. São os pacotes com folga zero que levam à entrega final de 11/12.
- **Folga de 5 DU** em 1.3.2, 1.3.3, 1.3.4, 1.4.2, 1.4.3 e 1.4.4: terminam em 31/10 e só são necessários em 10/11.
- **Importação de extratos (RQ02, prioridade máxima) está no caminho crítico** e concentra o risco R1 e a maior contingência.
- **Não há reserva de prazo** entre o fim de 1.5.3 e a entrega: qualquer atraso no caminho crítico atinge diretamente a entrega.

## 5.4 Marcos

| Marco | Data | O que está concluído | Pacotes |
|-------|------|----------------------|---------|
| **Marco 1** | 05/10/2026 | Documentos de gestão e levantamento de requisitos | 1.1.1, 1.2.1 |
| **Marco 2** | 06/10/2026 | Frontend com backend simulado (`json-server`) | 1.2.2, 1.3.1 a 1.3.6, 1.4.1 |
| **Marco 3** | 07 a 11/12/2026 | Integração Backend Real + Frontend, testes e entrega | 1.4.2 a 1.4.6, 1.5.1 a 1.5.3, 1.6.1 |

---

# 6. Rede de Atividades

A rede de dependências segue a lógica abaixo:
- **1.1.1** e **1.2.1** iniciam o projeto em 03/08.
- **1.2.2** (protótipo) depende de **1.2.1** e termina em 05/10.
- **1.3.1** (estrutura front) e **1.4.1** (estrutura API) iniciam em 05/10 e 06/10, respectivamente.
- Os módulos de frontend (**1.3.2 a 1.3.6**) e backend (**1.4.2 a 1.4.6**) são desenvolvidos em paralelo entre outubro e novembro.
- **1.5.1** (integração) depende de todos os módulos e começa em 18/11.
- **1.5.2** (testes) e **1.5.3** (ajustes) ocorrem até 11/12, quando se encerra o projeto (**1.6.1**).

---

# 7. Orçamento (esforço e custo)

## 7.1 Gerenciamento Financeiro

- **Unidade de custo:** horas de esforço.
- **Desembolso de caixa:** R$ 0,00.
- **Custo econômico:** horas valoradas a **R$ 10,00 por hora** (valor bruto, sem encargos).
- **Reserva de contingência:** 10% do esforço dos pacotes, separada e ligada a eventos de risco (seção 7.5).
- **Aprovação de estouro:** estouro acima de 10% das horas de um pacote exige registro de mudança.
- **Relatório:** horas realizadas x orçadas acompanhadas no status semanal.

## 7.2 Esforço e Custo por Pacote

| Pacote | Esforço (h) | Custo econômico (R$) |
|--------|:-----------:|---------------------:|
| 1.1.1 Documentação e acompanhamento | 20 | 200 |
| 1.1.2 Monitoramento, riscos e comunicação | 26 | 260 |
| 1.2.1 Levantamento, priorização e rastreabilidade | 10 | 100 |
| 1.2.2 Prototipagem e matrizes de requisitos | 14 | 140 |
| 1.3.1 Estrutura de front-end e rotas | 16 | 160 |
| 1.3.2 Assinaturas e dashboard | 20 | 200 |
| 1.3.3 Serviços e cancelamento | 8 | 80 |
| 1.3.4 Tetos e consumo orçamentário | 12 | 120 |
| 1.3.5 Extratos e conciliação | 12 | 120 |
| 1.3.6 Relatório e tutorial | 8 | 80 |
| 1.4.1 Estrutura da API e banco | 10 | 100 |
| 1.4.2 API de Assinaturas | 8 | 80 |
| 1.4.3 API de Serviços | 6 | 60 |
| 1.4.4 API de Tetos | 6 | 60 |
| 1.4.5 Importação de extratos | 8 | 80 |
| 1.4.6 Relatório, projeção e acesso | 6 | 60 |
| 1.5.1 Integração front-end/back-end | 10 | 100 |
| 1.5.2 Testes de validação funcional | 12 | 120 |
| 1.5.3 Ajustes e validação final | 8 | 80 |
| 1.6.1 Documentação final e entrega | 8 | 80 |
| **Subtotal dos pacotes** | **228** | **2.280** |
| Reserva de contingência (10%) | 23 | 230 |
| **Linha de base de esforço e custo** | **251** | **2.510** |
| Capacidade nominal | 252 | 2.520 |

## 7.3 Resumo por Entrega

| Entrega (EAP) | Esforço (h) | Custo econômico (R$) |
|---------------|:-----------:|---------------------:|
| 1.1 Gerenciamento | 46 | 460 |
| 1.2 Prototipagem e Requisitos | 24 | 240 |
| 1.3 Client-Side | 76 | 760 |
| 1.4 Server-Side | 44 | 440 |
| 1.5 Integração, Testes e Validação | 30 | 300 |
| 1.6 Encerramento | 8 | 80 |
| **Subtotal** | **228** | **2.280** |
| Contingência | 23 | 230 |
| **Total** | **251** | **2.510** |

## 7.4 Contingência Ligada a Eventos

| Evento | Risco | Reserva (h) | Custo (R$) |
|--------|-------|:-----------:|-----------:|
| Leitor de CSV falha em layouts diferentes | R1 | 8 | 80 |
| Integrante indisponível e cobertura | R3 | 6 | 60 |
| Dados sensíveis usados indevidamente | R5 | 3 | 30 |
| Mudança de requisito de pequeno porte | R6 | 3 | 30 |
| Integração tardia revela incompatibilidade | R7 | 3 | 30 |
| **Total** | | **23** | **230** |

Os riscos R2 (capacidade) e R4 (back-end real) não têm contingência: dependem de decisão do patrocinador.

## 7.5 Carga de Trabalho x Capacidade

O projeto teve um período de preparação de agosto a setembro para levantamento de requisitos e prototipagem. A capacidade nominal de 252h considera o período de trabalho intensivo de 9 semanas (de 05/10 a 11/12), com dedicação de 4 h/semana por pessoa.

| Grupo / pessoa | Esforço (h) | Capacidade (h) | Ocupação |
|----------------|:-----------:|:--------------:|:--------:|
| Ronald | 67,9 | 36 | 188% |
| Rodrigo | 41,3 | 36 | 114% |
| Thiago | 54,3 | 36 | 150% |
| **Desenvolvimento** | **163,5** | **108** | **151%** |
| Gerência (4) | 64,5 | 144 | 44% |
| **Total** | **228** | **252** | **90%** |

**Leitura.** A carga nos desenvolvedores ainda é alta (cerca de 6 h/semana por pessoa), mas a realocação de 14h para a Gerência aliviou o time de tecnologia, que agora tem mais tempo para focar no backend real e na integração do Marco 3. O principal risco continua sendo R2 (Capacidade) e exige acompanhamento semanal.

---

# 8. Recursos do Projeto

## 8.1 Tipos de Recurso

| Tipo | Recurso | Observação |
|------|---------|------------|
| Humano | 3 devs e 4 gerentes | 4 h/semana por pessoa. |
| Virtual | Repositório GitHub; React 19, Vite, TypeScript, Tailwind; Node.js, Express, Prisma, PostgreSQL, JWT; `json-server` (apenas para o M2). | Custo zero. O ambiente é local. |
| Dados | Extratos de teste sintéticos em CSV (3 ou mais layouts) | Sem dados reais de usuários. |
| Físico | Dispositivos para testes em celular | Dos próprios integrantes. |

## 8.2 Matriz de Responsabilidades (RAM/RACI)

**A** = presta contas (exatamente uma pessoa/grupo); **R** = executa; **A/R** = presta contas e executa; **C** = consultado; **I** = informado; **V** = valida e aceita.

| Pacote | Ronald | Rodrigo | Thiago | Gerência | Patrocinador |
|--------|:------:|:-------:|:------:|:--------:|:------------:|
| 1.1.1 Documentação | C | C | C | **A/R** | V |
| 1.1.2 Monitoramento | C | C | C | **A/R** | I |
| 1.2.1 Levantamento | R | **A/R** | R | C | I |
| 1.2.2 Prototipagem | R | R | **A/R** | C | C |
| 1.3.1 Estrutura Front | **A/R** | C | C | I | I |
| 1.3.2 Assinaturas | **A/R** | C | C | I | I |
| 1.3.3 Serviços/Links | C | C | **A/R** | I | C |
| 1.3.4 Tetos | C | C | **A/R** | I | I |
| 1.3.5 Extratos | C | **A/R** | C | I | C |
| 1.3.6 Relatório | **A/R** | C | R | C | I |
| 1.4.1 Estrutura API | C | **A/R** | C | I | I |
| 1.4.2 API Assinaturas | **A/R** | C | C | I | I |
| 1.4.3 API Serviços | C | C | **A/R** | I | I |
| 1.4.4 API Tetos | C | C | **A/R** | I | I |
| 1.4.5 API Extratos | C | **A/R** | C | I | I |
| 1.4.6 API Relatório | **A/R** | C | R | I | I |
| 1.5.1 Integração | R | **A/R** | R | I | I |
| 1.5.2 Testes Manuais | R | R | **A/R** | C | C |
| 1.5.3 Ajustes | **A/R** | R | R | I | I |
| 1.6.1 Encerramento | R | R | R | **A/R** | V |

**Divisão da gerência** [confirmar]: Davi, 1.1.1; João, 1.1.2; Michael, 1.6.1; Vinicius, controle de mudanças e esforço.

**Cobertura entre pares** (mitigação de R3): Rodrigo cobre Ronald (Assinaturas), Thiago cobre Rodrigo (Extratos) e Ronald cobre Thiago (Serviços e Tetos).

## 8.3 Estratégia de Obtenção (Fazer ou Comprar)

**Fazer:** telas, API real e regras são feitas pela equipe; bibliotecas abertas são reutilizadas. **Comprar:** nada. Só haverá aquisição se faltar algum recurso interno, e isso entrará como risco declarado.

---

# 9. Partes Interessadas

| Parte interessada                                       | O que espera                                                        | Poder | Interesse | Impacto sofrido | Quadrante          |
| ------------------------------------------------------- | ------------------------------------------------------------------- | :---: | :-------: | :-------------: | ------------------ |
| **Patrocinador** (Diogo)                                | Valida as regras, aprova mudanças e a entrega final                 | Alto  |   Alto    |      Médio      | Gerenciar de perto |
| **Gerência** (Davi, João, Michael, Vinicius)            | Planejar, acompanhar e entregar a documentação e os SRs             | Alto  |   Alto    |      Alto       | Gerenciar de perto |
| **Equipe de desenvolvimento** (Ronald, Rodrigo, Thiago) | Construir e entregar o sistema com a carga que a capacidade permite | Alto  |   Alto    |      Alto       | Gerenciar de perto |
| **Usuários finais**                                     | Visão clara das assinaturas e controle de gastos                    | Baixo |   Alto    |      Médio      | Manter informado   |
| **Administrador do catálogo**                           | Catálogo de provedores e links corretos                             | Médio |   Alto    |      Médio      | Manter informado   |
| **Provedores de serviço** (Netflix, etc.)               | Não participam, mas controlam as páginas de cancelamento            | Baixo |   Baixo   |      Médio      | Monitorar          |
| **Instituições financeiras**                            | Não participam, mas definem o formato dos extratos                  | Baixo |   Baixo   |      Médio      | Monitorar          |

---

# 10. Plano de Engajamento

| Parte interessada | Estratégia | Ações | Responsável |
|-------------------|------------|-------|-------------|
| Patrocinador | **Gerenciar de perto** | Relatórios nos marcos e Status Reports (SR1 a SR4); demonstração nos marcos 2 e 3; aprova mudanças de escopo e uso de contingência. | Gerência (Davi) |
| Gerência | **Gerenciar de perto** | Reunião semanal; acompanhamento no GitHub; revisão de riscos e do esforço. | Gerência (João) |
| Desenvolvedores | **Gerenciar de perto** | Reunião semanal; quadro de tarefas no GitHub; relato de horas por pacote; cobertura entre pares. | Gerência (João) |
| Usuários finais | **Informar e consultar** | Teste com 5 usuários-alvo no pacote 1.5.2 para o critério O3. | Thiago |
| Administrador do catálogo | **Manter informado** | Entregar lista de verificação da curadoria de links antes de 1.5.2. | Thiago |
| Provedores de serviço | **Monitorar** | Verificar todos os links de cancelamento antes de 1.5.2 e registrar a data. | Thiago |
| Instituições financeiras | **Monitorar** | Coletar amostras sintéticas de extratos CSV (3 layouts) no início de 1.3.5. | Rodrigo |

---

# 11. Plano de Comunicação (Cadência)

| Comunicação | Público | Conteúdo | Frequência | Canal | Responsável |
|-------------|---------|----------|------------|-------|-------------|
| Reunião da equipe | Gerência e devs | Progresso, impedimentos, riscos e horas | Semanal | Teams | Gerência (João) |
| Atualização do GitHub | Equipe | Commits, issues e marcos | Contínua | GitHub | Cada responsável (A) |
| Revisão do cronograma | Equipe | Desvio de prazo e esforço | Semanal | Reunião da equipe | Gerência (Vinicius) |
| Status Reports | Patrocinador | Marcos, desvios, riscos e esforço realizado | SR1 (12/10), SR2 (02/11), SR3 (16/11) e SR4 (a definir) | Documento no GitHub | Gerência (Davi) |
| Demonstração | Patrocinador | Funcionalidades prontas | Marco 2 (06/10) e Marco 3 (11/12) | Demonstração ao vivo | Ronald |
| Validação com usuários | Usuários | Roteiro de aceite (critério O3) | Uma vez, em 1.5.2 (25/11 a 03/12) | Sessão de teste | Thiago |
| Pedido de mudança | Patrocinador | Impacto em escopo, prazo e esforço | Sob demanda | Registro de mudança no GitHub | Quem propõe |
| Alerta de risco | Patrocinador | Gatilho de risco atingido | Imediato | Mensagem direta | Dono do risco |

---

# 12. Gerenciamento de Riscos

## 12.1 Abordagem

- **Quando:** identificados desde o início e revistos sempre que o plano mudar; o registro (entrega de 1.1.2) é revisto na reunião semanal.
- **Análise:** qualitativa, por probabilidade (P) e impacto (I) em três níveis (Baixa=1, Média=2, Alta=3). Nível = P × I (1-2 baixo, 3-4 médio, 6-9 alto).
- **Resposta a ameaças:** evitar, mitigar, transferir, aceitar ou escalar. A oportunidades: explorar, melhorar, compartilhar, aceitar ou escalar.
- **Quem autoriza:** o patrocinador, em itens de nível alto ou que usem a contingência.
- **Origem:** riscos do Business Case, do Dicionário e das premissas da seção 1.4. Cada premissa que falhar vira risco.

## 12.2 Registro de Riscos

Cada risco é escrito como **causa → evento → consequência**.

| ID                      | Risco (causa → evento → consequência)                                                                                                      | Origem                 |  P  |  I  |     Nível     | Resposta                                                                                                                                                                                          | Dono                | Reserva / gatilho                                                                                      |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------- | :-: | :-: | :-----------: | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- | ------------------------------------------------------------------------------------------------------ |
| **R1**                  | Como os bancos exportam CSV com layouts diferentes, o leitor pode falhar e atrasar 1.3.5 e 1.4.5 (caminho crítico) e a entrega final.      | Dicionário; P1, P7     |  3  |  3  | **9 (alto)**  | **Mitigar:** construir o leitor primeiro, com amostras de 3 layouts; documentar os layouts; manter a confirmação em lote como proteção.                                                           | Rodrigo             | 8 h. Gatilho: em **27/10**, o leitor ainda não detecta as assinaturas ou falha em mais de 1 amostra.   |
| **R2**                  | Como os 3 devs têm 108 h de capacidade e os pacotes pedem 163,5 h, a carga fica em 151% e o cronograma não se sustenta com 4 h por semana. | Dicionário; BC         |  3  |  3  | **9 (alto)**  | **Escalar ao patrocinador** e escolher entre: (a) aumentar a dedicação dos devs para ~6 h/semana; (b) realocar à gerência o trabalho que não é código; (c) cortar escopo; (d) rever a data final. | Gerência (João)     | Sem contingência. Gatilho: o **primeiro status semanal (13/10)** já mostra mais de 4 h/semana por dev. |
| **R3**                  | Como a equipe é pequena e tem outras demandas, a ausência de mais um pode deixar um módulo sem dono e atrasar o pacote.                    | BC; P9                 |  2  |  3  | **6 (alto)**  | **Mitigar:** cobertura entre pares; tarefas no GitHub com histórico; reunião semanal. Se não houver cobertura, redistribuir com o patrocinador.                                                   | Gerência (João)     | 6 h. Gatilho: integrante indisponível por mais de 3 DU seguidos.                                       |
| **R4**                  | Como o Marco 3 exige o backend real (Express/Prisma/PostgreSQL) integrado ao frontend, problemas técnicos podem inviabilizar a entrega.    | Dicionário; P6         |  2  |  3  | **6 (alto)**  | **Mitigar:** congelar o modelo de dados em 1.4.1; testes de integração contínuos a partir de 18/11; acompanhamento técnico semanal.                                                               | Rodrigo             | Sem contingência. Gatilho: falha crítica de integração na semana de 18/11.                             |
| **R5**                  | Como o extrato contém dados financeiros, o uso de dados reais ou armazenamento desnecessário pode expor a privacidade e exigir retrabalho. | BC                     |  1  |  3  | **3 (médio)** | **Mitigar:** testar apenas com dados sintéticos; guardar só o necessário; isolamento por usuário validado manualmente.                                                                            | Rodrigo             | 3 h. Gatilho: dados reais usados em teste ou demonstração.                                             |
| **R6**                  | Como o escopo ainda tem pendências, decisões tardias podem alterar pacotes já em andamento.                                                | BC; Dicionário         |  3  |  2  | **6 (alto)**  | **Mitigar:** decidir as pendências até 13/10; toda inclusão passa pelo controle de mudanças com aprovação do patrocinador.                                                                        | Gerência (Vinicius) | 3 h. Gatilho: pedido de funcionalidade fora da EAP após 13/10.                                         |
| **R7**                  | Como a integração (1.5.1) só começa em 18/11, incompatibilidades aparecem tarde e deixam 3 semanas para integrar, testar e ajustar.        | Dicionário; P3, P4     |  2  |  2  | **4 (médio)** | **Mitigar:** congelar o modelo em 1.4.1 (12/10); integração frequente na branch principal em vez de esperar 1.5.1.                                                                                | Ronald              | 3 h. Gatilho: atraso acima de 3 DU no caminho crítico.                                                 |
| **R8**                  | Como a gerência e o desenvolvimento têm rotinas diferentes, falhas de comunicação podem esconder desvios até o Marco 2.                    | BC; Dicionário (1.1.2) |  2  |  2  | **4 (médio)** | **Escalar:** alertar o patrocinador; reunião semanal com horas realizadas por pacote; status no GitHub.                                                                                           | Gerência (João)     | Sem contingência. Gatilho: duas reuniões semanais sem presença de um responsável.                      |
| **R9**                  | Como as páginas de cancelamento pertencem aos provedores, um link pode mudar e levar o usuário a uma página inexistente.                   | Plano                  |  2  |  1  | **2 (baixo)** | **Mitigar / aceitar:** curadoria dos links, data da última verificação e orientações escritas como alternativa.                                                                                   | Thiago              | Sem contingência. Gatilho: link inválido na verificação de 1.5.2.                                      |
| **O1** *(oportunidade)* | Como o frontend já cobre os casos de uso e o protótipo está pronto, componentes podem ser reaproveitados, reduzindo o esforço.             | BC; Dicionário         |  2  |  2  | **4 (médio)** | **Explorar:** criar a biblioteca de componentes em 1.3.1 e reutilizá-la nos módulos.                                                                                                              | Ronald              | Ganho: possível folga adicional em 1.3.2 a 1.3.4.                                                      |

**Riscos de negócio** (Business Case): baixa adoção, concorrência, monetização indefinida e restrição de hospedagem não ameaçam a entrega; ameaçam o retorno financeiro se houver cobrança. A resposta é validar a demanda e decidir a monetização só depois do Marco 3.

## 12.3 Risco Geral do Projeto e Pontos de Decisão

Os pontos de maior incerteza são R2 (capacidade) e R1 (extratos).

- **Ponto de decisão 1, até 13/10/2026:** o patrocinador decide como tratar o excesso de carga dos devs (R2) e pendências de escopo.
- **Ponto de decisão 2, em 27/10/2026:** se o leitor de CSV não detectar as assinaturas, decide entre consumir a contingência de R1, reduzir o escopo ou replanejar a data de entrega.

---

# 13. Controle e Monitoramento

## 13.1 Linhas de Base

| Linha de base | Conteúdo | Quem aprova mudança |
|---------------|----------|---------------------|
| Escopo | Declaração (2.3), EAP (3) e Dicionário (4) | Patrocinador |
| Prazo | Cronograma (5.2) e marcos (5.4) | Patrocinador |
| Esforço e custo | 228 h de pacotes + 23 h de contingência = 251 h (R$ 2.510,00; R$ 0,00 de caixa) | Patrocinador |

## 13.2 Acompanhamento

- **GitHub:** atualização contínua, com issues e marcos espelhando os pacotes.
- **Status semanal:** pacotes concluídos, desvio de prazo, **horas realizadas x orçadas**, riscos com gatilho atingido e registros de mudança.
- **Status Reports:** entrega formal nos marcos (SR1, SR2, SR3 e SR4).
- **Limites para ação:** atraso acima de 3 DU no caminho crítico ou uso de contingência geram registro de mudança e aviso ao patrocinador.

## 13.3 Controle Integrado de Mudanças

1. Qualquer integrante abre o pedido descrevendo o motivo e o impacto em escopo, prazo e esforço.
2. A gerência e a equipe avaliam.
3. O patrocinador aprova ou rejeita.
4. Se aprovada, a linha de base, o Dicionário e este plano são atualizados e a versão é registrada.

---

# 14. Encerramento do Projeto

## 14.1 Encerramento Normal

O projeto será encerrado quando o sistema estiver funcional com os módulos integrados, os critérios de aceite satisfeitos, a documentação final completa e o patrocinador aprovar a entrega final (Marco 3, 07 a 11/12/2026).

## 14.2 Encerramento Antecipado ou com Escopo Reduzido

Encerrar ou reduzir o projeto cedo pode ser a decisão correta quando o valor esperado deixar de justificar o esforço. O patrocinador deve ser consultado se R2 se confirmar e nenhuma opção for viável, se R1 se concretizar sem que o conciliador funcione, se houver perda de integrantes ou se a entrega não puder mais ser cumprida. A alternativa preferida é entregar o que estiver pronto por ordem de prioridade.

