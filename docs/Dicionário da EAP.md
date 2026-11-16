# Dicionário da EAP - SubTracker

**Versão:** 2.1  
**Data:** 03/10/2026

## 1. Finalidade

Este documento detalha os pacotes de trabalho da EAP do SubTracker, com foco em entregas, responsáveis, estimativas de esforço, dependências, riscos e critérios de aceite observáveis.

## 2. Visão Geral da EAP

| Código | Elemento                                    | Nível  | Responsável             | Origem (UC/requisito)     |
| ------ | ------------------------------------------- | ------ | ----------------------- | ------------------------- |
| 1.1.1  | Documentação e acompanhamento do projeto    | Pacote | Gerência                | Gestão                    |
| 1.1.2  | Monitoramento, riscos e comunicação         | Pacote | Gerência                | Gestão e riscos           |
| 1.2.1  | Levantamento, priorização e rastreabilidade | Pacote | Ronald, Rodrigo, Thiago | UCs Ativos                |
| 1.2.2  | Prototipagem e matrizes de requisitos       | Pacote | Ronald, Rodrigo, Thiago | Prototipagem e requisitos |
| 1.3.1  | Estrutura de front-end e rotas              | Pacote | Ronald                  | UCs Ativos                |
| 1.3.2  | Assinaturas e dashboard                     | Pacote | Ronald                  | UC01–UC04                 |
| 1.3.3  | Serviços e cancelamento                     | Pacote | Thiago                  | UC06, UC18                |
| 1.3.4  | Tetos e consumo orçamentário                | Pacote | Thiago                  | UC09–UC12                 |
| 1.3.5  | Extratos e conciliação                      | Pacote | Rodrigo                 | UC13, UC14                |
| 1.3.6  | Relatório e tutorial                        | Pacote | Ronald e Thiago         | UC17, UC18                |
| 1.4.1  | Estrutura da API e modelagem do banco       | Pacote | Rodrigo                 | Requisito de alto nível   |
| 1.4.2  | API de Assinaturas                          | Pacote | Ronald                  | UC01–UC04                 |
| 1.4.3  | API de Serviços e Links                     | Pacote | Thiago                  | UC06, UC18                |
| 1.4.4  | API de Tetos                                | Pacote | Thiago                  | UC09–UC12                 |
| 1.4.5  | Importação de extratos e conciliação        | Pacote | Rodrigo                 | UC13, UC14                |
| 1.4.6  | Relatório, projeção e acesso                | Pacote | Ronald e Thiago         | UC17, UC18                |
| 1.5.1  | Integração front-end/back-end               | Pacote | Ronald, Rodrigo, Thiago | Integridade do sistema    |
| 1.5.2  | Testes de validação funcional               | Pacote | Ronald, Rodrigo, Thiago | UCs Ativos                |
| 1.5.3  | Ajustes e validação final                   | Pacote | Ronald, Rodrigo, Thiago | Critérios de sucesso      |
| 1.6.1  | Documentação final e entrega                | Pacote | Gerência + equipe       | Encerramento do projeto   |

## 3. Dicionário dos Elementos

### 3.1 Código 1.1.1 - Documentação e acompanhamento do projeto

| Campo                      | Descrição                                                                                                                    |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Descrição do trabalho      | Planejar, acompanhar e documentar o progresso do projeto, incluindo entregáveis de gestão, cronograma e comunicação interna. |
| Entregas                   | Business Case, Termo de Abertura, Plano do Projeto, EAP e Dicionário da EAP, registros de acompanhamento.                    |
| Responsável                | Gerência (Davi, João, Michael, Vinicius).                                                                                    |
| Início e término previstos | 03/08/2026 a 05/10/2026                                                                                                      |
| Marco relacionado          | Marco 1                                                                                                                      |
| Critérios de aceitação     | Documentos revisados e consistentes com o escopo da versão 1; aprovação do patrocinador/gerência.                            |
| Dependências               | Nenhuma                                                                                                                      |
| Recursos necessários       | Repositório GitHub, documentos de contexto, comunicação por reunião e arquivo de controle.                                   |
| Custo estimado             | 20 horas de esforço                                                                                                          |
| Premissas e restrições     | A capacidade de gestão foi informada como 4 h/semana por gerente. O escopo foi consolidado conforme os documentos base.      |
| Riscos associados          | Atraso no desenvolvimento; mudanças nos requisitos; dificuldades de comunicação; baixa participação dos integrantes.         |

### 3.2 Código 1.1.2 - Monitoramento, riscos e comunicação

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Registrar riscos, indicadores de progresso, elaborar os Status Reports (SR1 a SR4) e garantir a comunicação interna para manter o projeto dentro do cronograma e do escopo previsto. |
| Entregas | Registro de riscos, plano de comunicação, indicadores de acompanhamento, Status Reports (SR1 a SR4) e ações de replanejamento. |
| Responsável | Gerência. |
| Início e término previstos | 05/10/2026 a 11/12/2026 |
| Marco relacionado | Marcos 1, 2 e 3 |
| Critérios de aceitação | Riscos atualizados, acompanhamento do cronograma, comunicação registrada e Status Reports entregues nos prazos. |
| Dependências | 1.1.1 |
| Recursos necessários | Repositório GitHub, reuniões, registros de acompanhamento e documentos de gestão. |
| Custo estimado | 26 horas de esforço |
| Premissas e restrições | A gestão funciona com 4 h/semana por gerente e sem orçamento financeiro formal. |
| Riscos associados | Atraso no desenvolvimento; ausência de integrantes; mudanças nos requisitos; dificuldades de comunicação. |

### 3.3 Código 1.2.1 - Levantamento, priorização e rastreabilidade

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Consolidar os requisitos da versão 1, confirmar as prioridades e manter a rastreabilidade entre requisitos, UC e entregas de produto. |
| Entregas | Matriz de priorização, matriz UC x requisito, lista de requisitos e rastreabilidade do escopo. |
| Responsável | Ronald, Rodrigo e Thiago. |
| Início e término previstos | 03/08/2026 a 05/10/2026 |
| Marco relacionado | Marco 1 |
| Critérios de aceitação | Todos os UCs ativos estão mapeados e a priorização foi confirmada pela equipe. |
| Dependências | 1.1.1 |
| Recursos necessários | Termo de Abertura, prototipagem e documentação do repositório. |
| Custo estimado | 10 horas de esforço |
| Premissas e restrições | O escopo principal foi definido pelos documentos base; não há promessa de implementação de módulos fora do escopo. |
| Riscos associados | Mudanças nos requisitos; baixa participação dos integrantes; dificuldades de comunicação. |

### 3.4 Código 1.2.2 - Prototipagem e matrizes de requisitos

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Validar o fluxo do sistema por meio do protótipo e das matrizes de CRUD, perfil x funcionalidade e priorização das telas. |
| Entregas | Protótipo das 7 telas, matrizes CRUD e perfil x funcionalidade, priorização do escopo. |
| Responsável | Ronald, Rodrigo e Thiago. |
| Início e término previstos | 03/08/2026 a 05/10/2026 |
| Marco relacionado | Marco 1 |
| Critérios de aceitação | Prototipagem concluída e consistente com o fluxo de usuário e com os casos de uso da versão 1. |
| Dependências | 1.2.1 |
| Recursos necessários | Repositório, prototipagem e material de requisitos. |
| Custo estimado | 14 horas de esforço |
| Premissas e restrições | O protótipo foi tratado como concluído no repositório e como base para a implementação da versão 1. |
| Riscos associados | Mudanças nos requisitos; dificuldades de comunicação; atraso no desenvolvimento. |

### 3.5 Código 1.3.1 - Estrutura de front-end e rotas

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Definir a estrutura de interface do front-end, incluindo layout, organização dos módulos e rotas da aplicação web responsiva. |
| Entregas | Estrutura inicial do projeto React/Vite/TypeScript, rotas e layout base. |
| Responsável | Ronald. |
| Início e término previstos | 05/10/2026 a 06/10/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | Rotas e estrutura organizadas e navegáveis, com layout base estável para os módulos do sistema. |
| Dependências | 1.2.2 |
| Recursos necessários | React 19 + Vite + TypeScript, Tailwind CSS, react-router-dom. |
| Custo estimado | 16 horas de esforço |
| Premissas e restrições | O estado real do repositório já possui front-end React + Vite + TypeScript. |
| Riscos associados | Atraso no desenvolvimento; dificuldades de comunicação; mudanças nos requisitos. |

### 3.6 Código 1.3.2 - Assinaturas e dashboard

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Implementar a gestão de assinaturas, incluindo cadastro, edição, ativação/pausa, exclusão e as telas de painel e dashboard relacionadas. |
| Entregas | Tela de painel, formulário de assinatura, listagem, edição e detalhamento de assinatura. |
| Responsável | Ronald. |
| Início e término previstos | 05/10/2026 a 06/10/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | UC01–UC04 operacionais no front-end e consistentes com os dados de teste e a lógica da aplicação. |
| Dependências | 1.3.1 |
| Recursos necessários | React, Tailwind, react-hook-form, zod, react-query. |
| Custo estimado | 20 horas de esforço |
| Premissas e restrições | O histórico de cobranças é parte da assinatura; não há tabela de cobrança separada no escopo da versão 1. |
| Riscos associados | Atraso no desenvolvimento; mudanças nos requisitos; dificuldade de comunicação. |

### 3.7 Código 1.3.3 - Serviços e cancelamento

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Desenvolver a consulta ao catálogo de serviços e as orientações/links de cancelamento. |
| Entregas | Consulta de serviços, visualização de links de cancelamento e orientações. |
| Responsável | Thiago. |
| Início e término previstos | 05/10/2026 a 06/10/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | UC06 e UC18 disponíveis na interface com fluxo de cancelamento informado. |
| Dependências | 1.3.1 |
| Recursos necessários | React, rotas, formulário e dados de serviço. |
| Custo estimado | 8 horas de esforço |
| Premissas e restrições | O cancelamento é orientativo e não automático; o sistema não integra com provedores externos. |
| Riscos associados | Mudanças nos requisitos; atraso no desenvolvimento; dificuldades de comunicação. |

### 3.8 Código 1.3.4 - Tetos e consumo orçamentário

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Implementar a gestão de tetos orçamentários, permitindo cadastro, consulta e acompanhamento do consumo por categoria. |
| Entregas | Formulário de tetos, visão de consumo e indicadores de orçamento por categoria. |
| Responsável | Thiago. |
| Início e término previstos | 05/10/2026 a 06/10/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | UC09–UC12 operacionais, com indicadores de consumo e atualização de valores orçamentários. |
| Dependências | 1.3.1 |
| Recursos necessários | React, Tailwind, estado local e dados de categoria. |
| Custo estimado | 12 horas de esforço |
| Premissas e restrições | Categoria é domínio-base com seed populado, sem manutenção independente. |
| Riscos associados | Atraso no desenvolvimento; mudanças nos requisitos; baixa participação dos integrantes. |

### 3.9 Código 1.3.5 - Extratos e conciliação

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Permitir o upload de extratos em CSV e a identificação de lançamentos recorrentes. |
| Entregas | Tela de importação e função de conciliação de extratos. |
| Responsável | Rodrigo. |
| Início e término previstos | 05/10/2026 a 06/10/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | UC13 e UC14 funcionais; importação aceita CSV e rejeita layouts incompatíveis. |
| Dependências | 1.3.1 |
| Recursos necessários | React, biblioteca de leitura de CSV, controles de upload e lógica de filtro. |
| Custo estimado | 12 horas de esforço |
| Premissas e restrições | O repositório já possui importação em CSV. |
| Riscos associados | Atraso no desenvolvimento; mudanças nos requisitos; falha na importação de extratos. |

### 3.10 Código 1.3.6 - Relatório e tutorial

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Exibir o relatório financeiro e disponibilizar o tutorial de uso e instruções de cancelamento. |
| Entregas | Tela de relatório, projeção de impacto e tutorial. |
| Responsável | Ronald e Thiago. |
| Início e término previstos | 05/10/2026 a 06/10/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | UC17 e UC18 acessíveis na aplicação e com informações que apoiam a tomada de decisão do usuário. |
| Dependências | 1.3.2, 1.3.3, 1.3.4, 1.3.5 |
| Recursos necessários | React, gráficos e navegação por telas. |
| Custo estimado | 8 horas de esforço |
| Premissas e restrições | O relatório é de projeção e impacto financeiro; não há operação financeira real. |
| Riscos associados | Atraso no desenvolvimento; mudanças nos requisitos; dificuldades de comunicação. |

### 3.11 Código 1.4.1 - Estrutura da API e modelagem do banco

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Definir a estrutura da API real e a modelagem do banco de dados com as entidades do domínio. |
| Entregas | Estrutura da API, diagrama/descrição de entidades e configuração do banco. |
| Responsável | Rodrigo. |
| Início e término previstos | 06/10/2026 a 12/10/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | Estrutura de dados e API alinhadas com os casos de uso e com o modelo real. |
| Dependências | 1.2.1 |
| Recursos necessários | Node.js, Express, Prisma, PostgreSQL. |
| Custo estimado | 10 horas de esforço |
| Premissas e restrições | O backend real será a base para o Marco 3. |
| Riscos associados | Atraso no desenvolvimento; dificuldades de comunicação; mudanças nos requisitos. |

### 3.12 Código 1.4.2 - API de Assinaturas

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Implementar endpoints e regras de negócio para cadastro, consulta, atualização e remoção de assinaturas, além de controles de status. |
| Entregas | API de assinaturas, regras de edição e eventos de status. |
| Responsável | Ronald. |
| Início e término previstos | 12/10/2026 a 31/10/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | UC01–UC04 atendidos pelos endpoints e pela persistência real. |
| Dependências | 1.4.1 |
| Recursos necessários | Express, Prisma, rotas de assinatura e validação de dados. |
| Custo estimado | 8 horas de esforço |
| Premissas e restrições | O sistema não realiza cobrança real; todas as operações são de registro e acompanhamento. |
| Riscos associados | Atraso no desenvolvimento; mudanças nos requisitos; baixa participação do time. |

### 3.13 Código 1.4.3 - API de Serviços

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Implementar a consulta ao catálogo de serviços e as operações de orientação e cancelamento. |
| Entregas | API de serviços, links de cancelamento e catálogo base. |
| Responsável | Thiago. |
| Início e término previstos | 12/10/2026 a 31/10/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | UC06 e UC18 atendidos, com acesso ao catálogo e orientação de cancelamento. |
| Dependências | 1.4.1 |
| Recursos necessários | Express, Prisma e roteamento de serviço. |
| Custo estimado | 6 horas de esforço |
| Premissas e restrições | O cancelamento é sempre conduzido pelo usuário; não há integração automática com provedores externos. |
| Riscos associados | Atraso no desenvolvimento; mudanças nos requisitos; baixa participação dos integrantes. |

### 3.14 Código 1.4.4 - API de Tetos

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Implementar o gerenciamento de tetos orçamentários, incluindo cadastro, consulta, atualização e consumo por categoria. |
| Entregas | Endpoints e dados para cadastro/consulta/uso de tetos orçamentários. |
| Responsável | Thiago. |
| Início e término previstos | 12/10/2026 a 31/10/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | UC09–UC12 consistentes com os valores de consumo e categoria. |
| Dependências | 1.4.1 |
| Recursos necessários | Express, Prisma e regras de cálculo do orçamento por categoria. |
| Custo estimado | 6 horas de esforço |
| Premissas e restrições | Categoria é base do domínio e não há módulo de manutenção independente. |
| Riscos associados | Mudanças nos requisitos; atraso no desenvolvimento; dificuldades de comunicação. |

### 3.15 Código 1.4.5 - Importação de extratos e conciliação

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Implementar a importação e leitura de extratos em CSV e a identificação de lançamentos recorrentes. |
| Entregas | Endpoints de upload e processamento de extratos e conciliação. |
| Responsável | Rodrigo. |
| Início e término previstos | 06/10/2026 a 17/11/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | UC13 e UC14 atendidos, com leitura de CSV. |
| Dependências | 1.4.1 |
| Recursos necessários | Express, Prisma e lógica de parser de CSV. |
| Custo estimado | 8 horas de esforço |
| Premissas e restrições | O sistema não conecta diretamente a bancos ou cartões. |
| Riscos associados | Atraso no desenvolvimento; falha na importação; mudanças nos requisitos. |

### 3.16 Código 1.4.6 - Relatório, projeção e acesso

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Gerar relatórios de impacto financeiro e disponibilizar a projeção do gasto recorrente e acesso ao tutorial de cancelamento. |
| Entregas | Métricas de projeção, relatórios e controle de acesso. |
| Responsável | Ronald e Thiago. |
| Início e término previstos | 10/11/2026 a 17/11/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | UC17 e UC18 atendidos e acessíveis a partir da interface, com projeção e links de cancelamento. |
| Dependências | 1.4.2, 1.4.3, 1.4.4, 1.4.5 |
| Recursos necessários | Express, Prisma, dados do sistema e visualização de relatório. |
| Custo estimado | 6 horas de esforço |
| Premissas e restrições | O cálculo é baseado em dados cadastrados pelo usuário e não em movimentação financeira real. |
| Riscos associados | Mudanças nos requisitos; atraso no desenvolvimento; dificuldades de comunicação. |

### 3.17 Código 1.5.1 - Integração front-end/back-end

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Integrar as telas criadas com a API real para garantir que os dados de assinaturas, serviços, tetos e extratos estejam em sincronização. |
| Entregas | Fluxo integrado de dados e comunicação funcional entre front-end e API real. |
| Responsável | Ronald, Rodrigo e Thiago. |
| Início e término previstos | 18/11/2026 a 24/11/2026 |
| Marco relacionado | Marco 3 |
| Critérios de aceitação | Operações CRUD e importação respondendo corretamente em end-to-end. |
| Dependências | 1.3.2, 1.3.3, 1.3.4, 1.3.5, 1.4.2, 1.4.3, 1.4.4, 1.4.5 |
| Recursos necessários | Front-end, API real (Express/Prisma), PostgreSQL, dados de teste e GitHub. |
| Custo estimado | 10 horas de esforço |
| Premissas e restrições | A integração usa o backend real desenvolvido até o momento. |
| Riscos associados | Atraso no desenvolvimento; dificuldades de comunicação; mudanças nos requisitos. |

### 3.18 Código 1.5.2 - Testes de validação funcional

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Validar o comportamento funcional do sistema contra os requisitos da versão 1, incluindo fluxos principais e cenários de erro. |
| Entregas | Checklist de testes manuais, evidências e correções de falhas observadas. |
| Responsável | Ronald, Rodrigo e Thiago. |
| Início e término previstos | 25/11/2026 a 03/12/2026 |
| Marco relacionado | Marco 3 |
| Critérios de aceitação | Fluxos principais e críticos concluídos e sem divergência importante com o escopo definido. |
| Dependências | 1.5.1 |
| Recursos necessários | Ambiente de teste local, dados de exemplo, repositório e documentação. |
| Custo estimado | 12 horas de esforço |
| Premissas e restrições | Os testes têm foco em integração e validação funcional manual. |
| Riscos associados | Atraso no desenvolvimento; baixa participação dos integrantes; dificuldades de comunicação. |

### 3.19 Código 1.5.3 - Ajustes e validação final

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Corrigir falhas identificadas nos testes, finalizar fluxos críticos e ajustar a apresentação e a documentação para entrega final. |
| Entregas | Sistema ajustado, registros de correção e versão pronta para a entrega. |
| Responsável | Ronald, Rodrigo e Thiago. |
| Início e término previstos | 04/12/2026 a 11/12/2026 |
| Marco relacionado | Marco 3 |
| Critérios de aceitação | Sistema estável para a entrega final e documentação suficientemente alinhada ao projeto entregue. |
| Dependências | 1.5.2 |
| Recursos necessários | Repositório, ambiente local, documentação e ajustes finais. |
| Custo estimado | 8 horas de esforço |
| Premissas e restrições | O cronograma final é 07/12/2026 a 11/12/2026, com validação interna e sem operação financeira real. |
| Riscos associados | Atraso no desenvolvimento; mudanças nos requisitos; baixa participação dos integrantes. |

### 3.20 Código 1.6.1 - Documentação final e entrega

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Encerrar o projeto com documentação final, revisão de artefatos e entrega para o patrocinador. |
| Entregas | Documentação final do projeto, EAP e Dicionário finalizados e artefatos atualizados no repositório. |
| Responsável | Gerência + equipe. |
| Início e término previstos | 07/12/2026 a 11/12/2026 |
| Marco relacionado | Marco 3 |
| Critérios de aceitação | Entregas finais revisadas, repostadas e consistentes com a documentação e a versão entregue. |
| Dependências | 1.5.3 |
| Recursos necessários | Repositório, documentos finais, Git e feedback dos stakeholders. |
| Custo estimado | 8 horas de esforço |
| Premissas e restrições | O projeto encerra na segunda semana de dezembro de 2026, conforme o cronograma planejado. |
| Riscos associados | Atraso no desenvolvimento; ausência de integrantes; dificuldades de comunicação. |

## 4. Observações

- O custo estimado foi tratado em horas de esforço; não há valor/hora oficial, salário ou orçamento real definido para a equipe.
- A infraestrutura é local, sem custo de produção.
- A capacidade total estimada é de 252 horas, calculada como: 3 programadores × 4 h/semana × 9 semanas + 4 gerentes × 4 h/semana × 9 semanas.
- O esforço total estimado da EAP somou 228 horas. A reserva de contingência, separada dos pacotes, equivale a 10% do esforço total, ou seja, 23 horas.
- Em termos de linha de base: esforço total + contingência = 251 horas, dentro da capacidade nominal de 252 horas.

## 5. Premissas confirmadas pelo usuário e lacunas relevantes

| Item | Confirmação |
| ---- | ----------- |
| Programação | Ronald, Rodrigo e Thiago |
| Dedicação | 4 h/semana por pessoa, sem considerar feriados |
| Marcos | M1 = 05/10/2026; M2 = 06/10/2026; M3 = 07 a 11/12/2026 |
| Escopo | UCs 05, 07, 08, 15 e 16 removidos. Escopo ativo: UC01-UC04, UC06, UC09-UC14, UC17, UC18 |
| Cobranças | Vinculada à Assinatura; sem tabela própria |
| Infraestrutura | Local, sem custo real de produção |
| Custo | Em horas de esforço e sem valores financeiros reais |
| Reserva | 10% do esforço total, separada dos pacotes |

- O backend real (Express + Prisma + PostgreSQL) é a base para o Marco 3. O `json-server` foi usado apenas como protótipo no Marco 2.