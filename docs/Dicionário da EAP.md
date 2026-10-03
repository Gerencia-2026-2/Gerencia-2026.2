# Dicionário da EAP - SubTracker

**Versão:** 3.0  
**Data:** 03/10/2026

## 1. Finalidade

Este documento descreve cada pacote de trabalho da Estrutura Analítica do Projeto (EAP) do SubTracker: trabalho a realizar, responsável, entregas, datas, dependências, esforço, riscos e critérios de aceitação. O estado considerado é o do repositório em 03/10/2026 (`documentacao/Cronograma.md`, `Refinamento_da_Prototipagem_SubTracker.md` e `README.md`).

Marcos: **Marco 1** = AV1, 05/10/2026 às 18:30; **Marco 2** = 17/11/2026 (conforme Termo de Abertura, a confirmar); **Marco 3** = entrega final, 07/12/2026 a 11/12/2026.

**Validação:** salvo indicação contrária, os critérios de aceitação são validados pelos gerentes (Davi, João, Michael e Vinicius) e pelo patrocinador, conforme o Termo de Abertura.

## 2. Visão Geral da EAP

| Código | Elemento | Nível | Responsável | Origem (UC/requisito) |
| ------ | -------- | ----- | ----------- | --------------------- |
| 1 | SubTracker | Projeto | Davi, João, Michael e Vinicius (gerentes) | UC01–UC18 conforme Refinamento, seção 4 |
| 1.1 | Gerenciamento do Projeto | Entrega | Davi, João, Michael e Vinicius | Enunciado da AV1 |
| 1.1.1 | Artefatos de gerência da AV1 | Pacote de trabalho | Davi, João, Michael e Vinicius | Enunciado da AV1 |
| 1.1.2 | Monitoramento, riscos e comunicação | Pacote de trabalho | Davi, João, Michael e Vinicius | Gestão e riscos |
| 1.2 | Prototipagem e Requisitos | Entrega | Ronald, Rodrigo e Thiago | UC01–UC18 |
| 1.2.1 | Levantamento, priorização e rastreabilidade | Pacote de trabalho | Ronald, Rodrigo e Thiago | UC01–UC18 |
| 1.2.2 | Protótipo e matrizes de requisitos | Pacote de trabalho | Ronald, Rodrigo e Thiago | Prototipagem e Refinamento, seções 1 e 2 |
| 1.3 | Client-Side (front-end) | Entrega | Ronald, Rodrigo e Thiago | UC01–UC04, UC06, UC09–UC11, UC13–UC14, UC17–UC18 |
| 1.3.1 | Estrutura, rotas e autenticação simulada | Pacote de trabalho | Ronald, Rodrigo e Thiago | Telas de autenticação (suporte) |
| 1.3.2 | Assinaturas e dashboard | Pacote de trabalho | Ronald | UC01–UC04 |
| 1.3.3 | Catálogo de serviços e cancelamento | Pacote de trabalho | Thiago | UC06, UC18 |
| 1.3.4 | Metas por categoria (Meu Perfil) | Pacote de trabalho | Ronald, Rodrigo e Thiago | UC09–UC11 (UC12 reinterpretado) |
| 1.3.5 | Importação de extrato CSV e conciliação | Pacote de trabalho | Rodrigo | UC13, UC14 |
| 1.3.6 | Relatório de projeção e impacto | Pacote de trabalho | Ronald | UC17 |
| 1.3.7 | Acabamento e conferência final do front-end | Pacote de trabalho | Ronald | Cronograma, conferência final |
| 1.4 | Server-Side (back-end real) | Entrega | Ronald, Rodrigo e Thiago | Limitações atuais (README) e etapa posterior (Cronograma) |
| 1.4.1 | Arquitetura do back-end e modelagem do banco | Pacote de trabalho | Rodrigo | Limitações atuais (README) |
| 1.4.2 | Autenticação e controle de acesso | Pacote de trabalho | Thiago | Telas de autenticação; perfis Usuário e Administrador |
| 1.4.3 | API de assinaturas, pagamentos e metas | Pacote de trabalho | Ronald | UC01–UC04, UC09–UC11 |
| 1.4.4 | API de extratos e conciliação | Pacote de trabalho | Rodrigo | UC13, UC14 |
| 1.4.5 | API de relatórios e catálogo de serviços | Pacote de trabalho | Rodrigo | UC06, UC17, UC18 |
| 1.4.6 | Publicação em ambiente gratuito | Pacote de trabalho | Thiago | Disponibilidade do sistema |
| 1.5 | Integração, Testes e Validação | Entrega | Ronald, Rodrigo e Thiago (execução); gerentes (validação) | Integridade do sistema |
| 1.5.1 | Integração front-end/back-end | Pacote de trabalho | Ronald | Substituição do json-server |
| 1.5.2 | Testes funcionais e de segurança básica | Pacote de trabalho | Rodrigo | UC implementados |
| 1.5.3 | Validação com patrocinador e gerentes | Pacote de trabalho | Davi, João, Michael e Vinicius | Critérios de aceite dos pacotes |
| 1.6 | Encerramento | Entrega | Davi, João, Michael e Vinicius | Encerramento do projeto |
| 1.6.1 | Documentação final e entrega | Pacote de trabalho | Davi, João, Michael e Vinicius | Encerramento do projeto |

## 3. Dicionário dos Elementos

### 3.1 Código 1.1.1 - Artefatos de gerência da AV1

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Produzir e revisar o Business Case, o Termo de Abertura, o Plano do Projeto e a EAP com o Dicionário, conforme o enunciado da AV1, alinhados ao escopo atualizado e ao estado real do repositório. |
| Entregas | Quatro artefatos em `docs/` do repositório e o link postado na atividade da AV1. |
| Responsável | Davi, João, Michael e Vinicius. |
| Início e término previstos | 03/10/2026 a 05/10/2026 |
| Marco relacionado | Marco 1 (AV1, 05/10/2026 às 18:30) |
| Critérios de aceitação | Os quatro artefatos existem no repositório, sem campos `[ ]` ou `[DD/MM]` restantes; EAP e Dicionário têm códigos idênticos; link entregue até 05/10/2026 às 18:30. Validação: os quatro gerentes. |
| Dependências | Nenhuma |
| Recursos necessários | Repositório GitHub, aulas 1 a 7 de GTI, documentação de PSW em `documentacao/`. |
| Custo estimado | 16 horas de esforço |
| Premissas e restrições | O enunciado não admite entrega em atraso. As 16 h correspondem à capacidade semanal total dos quatro gerentes (4 h cada). |
| Riscos associados | Atraso na entrega (prazo apertado); mudanças nos requisitos; dificuldades de comunicação. |

### 3.2 Código 1.1.2 - Monitoramento, riscos e comunicação

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Acompanhar semanalmente o avanço da programação, atualizar o registro de riscos e manter a comunicação com a equipe de PSW e com o patrocinador até o encerramento. |
| Entregas | Registro de riscos atualizado, status semanal resumido e registro de decisões (escopo, OFX, back-end). |
| Responsável | Davi, João, Michael e Vinicius. |
| Início e término previstos | 06/10/2026 a 11/12/2026 |
| Marco relacionado | Marcos 2 e 3 |
| Critérios de aceitação | Registro de riscos revisado em cada marco, status semanal registrado e decisões pendentes da seção "Registro de uso de IA" do `EAP.md` respondidas pelo grupo. Validação: gerentes. |
| Dependências | 1.1.1 |
| Recursos necessários | Repositório GitHub, reuniões do grupo e arquivo de controle. |
| Custo estimado | 20 horas de esforço (cerca de 2 h por semana do grupo de gerentes) |
| Premissas e restrições | Capacidade de 4 h por semana por gerente; sem orçamento financeiro; feriados e provas não considerados. |
| Riscos associados | Ausência de integrantes (um integrante de PSW já trancou a matrícula, `Refinamento`, seção 3); baixa participação; dificuldades de comunicação. |

### 3.3 Código 1.2.1 - Levantamento, priorização e rastreabilidade

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Levantar os 18 casos de uso, as entidades e as prioridades, vinculando cada requisito à entidade e ao responsável. Trabalho **concluído**; o status de implementação por UC foi atualizado em 01/10/2026. |
| Entregas | Lista UC01–UC18, priorização em três níveis, divisão por integrante e status por UC (`Refinamento`, seções 3 e 4). |
| Responsável | Ronald, Rodrigo e Thiago. |
| Início e término previstos | Concluído antes de 19/09/2026 (início da implementação, `Cronograma.md`); data exata não registrada. |
| Marco relacionado | Marco 1 |
| Critérios de aceitação | UC01–UC18 mapeados com entidade e prioridade; cada UC não implementado tem justificativa. Validação: gerentes. |
| Dependências | Nenhuma |
| Recursos necessários | `Prototipagem_SubTracker.md` e `Refinamento_da_Prototipagem_SubTracker.md`. |
| Custo estimado | 0 horas restantes (esforço realizado não registrado) |
| Premissas e restrições | O PDF de prototipagem diz "17 casos de uso" mas lista 18; adota-se 18, como no `.md` do repositório. |
| Riscos associados | Mudanças nos requisitos (a saída de um integrante já reduziu o escopo). |

### 3.4 Código 1.2.2 - Protótipo e matrizes de requisitos

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Prototipar as telas mobile-first e validar o escopo com a matriz CRUD (5 entidades x 18 UC) e a matriz Perfil x Funcionalidade. Trabalho **concluído**. |
| Entregas | Protótipo de 8 telas mais telas de autenticação de suporte (`Prototipagem_SubTracker.md`) e matrizes (`Refinamento`, seções 1 e 2). |
| Responsável | Ronald, Rodrigo e Thiago. |
| Início e término previstos | Concluído antes de 19/09/2026; data exata não registrada. |
| Marco relacionado | Marco 1 |
| Critérios de aceitação | Telas e matrizes consistentes com os UC01–UC18. Validação: gerentes. |
| Dependências | 1.2.1 |
| Recursos necessários | Documentos de prototipagem do repositório. |
| Custo estimado | 0 horas restantes (esforço realizado não registrado) |
| Premissas e restrições | A prototipagem foi majoritariamente feita pelo integrante que trancou a matrícula (`Refinamento`, seção 3). |
| Riscos associados | Mudanças nos requisitos; dificuldades de comunicação. |

### 3.5 Código 1.3.1 - Estrutura, rotas e autenticação simulada

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Estrutura do front-end em React 19, Vite e TypeScript, com rotas, login, registro e recuperação de senha simulados no `json-server`, navegação responsiva e padronização com Tailwind, react-hook-form, Zod e TanStack Query. Trabalho **concluído**. |
| Entregas | Aplicação navegável com rotas `/`, `/cadastro`, `/esqueci-senha` e `/painel`. |
| Responsável | Ronald, Rodrigo e Thiago. |
| Início e término previstos | 19/09/2026 a 01/10/2026 (`Cronograma.md`) |
| Marco relacionado | Marco 1 |
| Critérios de aceitação | `npm run server` e `npm run dev` iniciam o sistema; navegação responsiva em desktop e celular. Validação: gerentes. |
| Dependências | 1.2.2 |
| Recursos necessários | React 19, Vite, TypeScript, Tailwind CSS, react-router-dom, `json-server`. |
| Custo estimado | 0 horas restantes (esforço realizado não registrado) |
| Premissas e restrições | Autenticação simulada em `localStorage`; senhas em texto puro no `db.json` (`README`, limitações). Padronização técnica de 28/09 a 01/10 sobreposta aos demais pacotes. |
| Riscos associados | Segurança fraca de credenciais (tratada em 1.4.2); mudanças nos requisitos. |

### 3.6 Código 1.3.2 - Assinaturas e dashboard

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Cadastro em dois passos, edição, exclusão, pausa e reativação de assinaturas, confirmação de pagamento com histórico e dashboard com metas e próximas cobranças. Trabalho **concluído**. |
| Entregas | Telas Dashboard, Nova e Editar Assinatura e Detalhes da Assinatura. |
| Responsável | Ronald. |
| Início e término previstos | 22/09/2026 a 26/09/2026 (`Cronograma.md`) |
| Marco relacionado | Marco 1 |
| Critérios de aceitação | UC01–UC04 implementados (`Refinamento`, seção 4), com recálculo imediato dos totais após qualquer alteração. Validação: gerentes. |
| Dependências | 1.3.1 |
| Recursos necessários | React, react-hook-form, Zod, TanStack Query, `json-server`. |
| Custo estimado | 0 horas restantes (esforço realizado não registrado) |
| Premissas e restrições | Histórico de cobranças é parte da assinatura (campo `history`), sem tabela própria. "Confirmar pagamento" foi acrescentado durante o desenvolvimento. |
| Riscos associados | Cálculo de dias restantes ainda "a confirmar" (`Cronograma.md`). |

### 3.7 Código 1.3.3 - Catálogo de serviços e cancelamento

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Catálogo de serviços populares, opção "Outro" para serviço personalizado e atalho "Cancelar no provedor" na tela de detalhes. Trabalho **concluído**. |
| Entregas | `src/constants/catalog.ts`, seleção de serviço no cadastro e atalho de cancelamento. |
| Responsável | Thiago. |
| Início e término previstos | 23/09/2026 a 01/10/2026 (`Cronograma.md`) |
| Marco relacionado | Marco 1 |
| Critérios de aceitação | UC06 e UC18 implementados (`Refinamento`, seção 4). Validação: gerentes. |
| Dependências | 1.3.1 |
| Recursos necessários | React e a lista fixa do catálogo. |
| Custo estimado | 0 horas restantes (esforço realizado não registrado) |
| Premissas e restrições | UC05, UC07 e UC08 estão fora do escopo (`Refinamento`, seção 4); o catálogo é uma lista fixa no código; o cancelamento é orientativo. |
| Riscos associados | Links de cancelamento desatualizados; mudanças nos requisitos. |

### 3.8 Código 1.3.4 - Metas por categoria (Meu Perfil)

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Definição e ajuste de metas de gasto por categoria na tela Meu Perfil, usadas pelas barras do dashboard. Trabalho **concluído** e absorvido pela equipe após a saída do integrante responsável. |
| Entregas | Tela Meu Perfil com metas por categoria. |
| Responsável | Ronald, Rodrigo e Thiago. |
| Início e término previstos | 25/09/2026 (`Cronograma.md`) |
| Marco relacionado | Marco 1 |
| Critérios de aceitação | UC09, UC10 e UC11 implementados; UC12 atendido zerando a meta (`Refinamento`, seção 4). Validação: gerentes. |
| Dependências | 1.3.2 |
| Recursos necessários | React, react-hook-form, Zod. |
| Custo estimado | 0 horas restantes (esforço realizado não registrado) |
| Premissas e restrições | As seis categorias são fixas no domínio. |
| Riscos associados | Mudanças nos requisitos. |

### 3.9 Código 1.3.5 - Importação de extrato CSV e conciliação

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Leitura de arquivo `.csv` (`data,descricao,valor`), identificação de serviços do catálogo e confirmação de pagamento ou criação de assinatura sem duplicar. Trabalho **concluído**. |
| Entregas | Tela Importar Extrato e `teste.csv` de exemplo. |
| Responsável | Rodrigo. |
| Início e término previstos | 26/09/2026 (`Cronograma.md`) |
| Marco relacionado | Marco 1 |
| Critérios de aceitação | UC13 e UC14 implementados para CSV (`Refinamento`, seção 4). Validação: gerentes. |
| Dependências | 1.3.2, 1.3.3 |
| Recursos necessários | React e lógica de reconhecimento por palavras-chave. |
| Custo estimado | 0 horas restantes (esforço realizado não registrado) |
| Premissas e restrições | OFX não implementado e fora do escopo (desvio do UC13 e da Tela 6, a registrar); UC15 e UC16 fora do escopo. |
| Riscos associados | Falha na importação por layout de CSV diferente do fixo. |

### 3.10 Código 1.3.6 - Relatório de projeção e impacto

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Gráfico donut por categoria, ranking das três assinaturas mais caras e resumo mensal e anual. Trabalho **concluído**. |
| Entregas | Tela Relatórios. |
| Responsável | Ronald. |
| Início e término previstos | 25/09/2026 (`Cronograma.md`) |
| Marco relacionado | Marco 1 |
| Critérios de aceitação | UC17 implementado (`Refinamento`, seção 4), convertendo periodicidades para valor mensal. Validação: gerentes. |
| Dependências | 1.3.2 |
| Recursos necessários | React e componentes de gráfico. |
| Custo estimado | 0 horas restantes (esforço realizado não registrado) |
| Premissas e restrições | O cálculo usa apenas dados cadastrados, sem movimentação financeira real. |
| Riscos associados | Divergência de cálculo entre relatório e detalhes ("a confirmar" no `Cronograma.md`). |

### 3.11 Código 1.3.7 - Acabamento e conferência final do front-end

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Fechar as pendências da "Conferência final" do `Cronograma.md`: estados de lista vazia, navegação por teclado, `npm run build` sem erros, README atualizado e conferência dos commits na `main`. |
| Entregas | Front-end revisado e checklist da conferência final concluído. |
| Responsável | Ronald. |
| Início e término previstos | 03/10/2026 a 06/10/2026 |
| Marco relacionado | Entrega de PSW em 06/10/2026 (um dia após o Marco 1) |
| Critérios de aceitação | Todos os itens da conferência final marcados; build de produção sem erros. Validação: gerentes. |
| Dependências | 1.3.1, 1.3.2, 1.3.3, 1.3.4, 1.3.5, 1.3.6 |
| Recursos necessários | Node.js, repositório GitHub e `teste.csv`. |
| Custo estimado | 4 horas de esforço |
| Premissas e restrições | Prazo de entrega de PSW em 06/10/2026, com ensaio em 05/10 (`Cronograma.md`). |
| Riscos associados | Atraso no desenvolvimento; baixa participação dos integrantes. |

### 3.12 Código 1.4.1 - Arquitetura do back-end e modelagem do banco

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Decidir a tecnologia do back-end e do banco (a avaliar; não decidida) e modelar as cinco entidades a partir do `db.json` atual, em que `users` guarda as metas e `subs` guarda o histórico. Inclui o script de migração dos dados de exemplo. |
| Entregas | Registro da decisão de arquitetura, esquema do banco e script de seed e migração. |
| Responsável | Rodrigo. |
| Início e término previstos | 07/10/2026 a 23/10/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | Esquema cobre os UC implementados e o isolamento por usuário; tecnologia escolhida registrada e aceita pelo grupo. Validação: gerentes. |
| Dependências | 1.3.7 |
| Recursos necessários | `db.json`, plano gratuito do provedor escolhido e repositório. |
| Custo estimado | 12 horas de esforço |
| Premissas e restrições | A monetização não foi decidida: assume-se uso acadêmico não comercial e planos gratuitos (cenário A). Se houver monetização, rever hospedagem e custos. |
| Riscos associados | Atraso no desenvolvimento; limites e pausa de planos gratuitos; mudanças nos requisitos. |

### 3.13 Código 1.4.2 - Autenticação e controle de acesso

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Cadastro, login com senha criptografada, sessão ou token, recuperação de senha e isolamento dos dados por usuário, com perfis Usuário e Administrador. |
| Entregas | Endpoints de autenticação e controle de acesso nas rotas protegidas. |
| Responsável | Thiago. |
| Início e término previstos | 26/10/2026 a 20/11/2026 |
| Marco relacionado | Marco 3 (término três dias após o Marco 2) |
| Critérios de aceitação | Senhas guardadas apenas como hash; rota protegida sem sessão é recusada; um usuário não acessa dados de outro. Validação: gerentes. |
| Dependências | 1.4.1 |
| Recursos necessários | Banco do pacote 1.4.1, biblioteca de hash e repositório. |
| Custo estimado | 16 horas de esforço |
| Premissas e restrições | A recuperação de senha segue sem envio de e-mail real (`README`, limitações), a confirmar; o perfil Administrador terá só controle de acesso, sem área de catálogo. |
| Riscos associados | Falha de segurança em credenciais; atraso no desenvolvimento. |

### 3.14 Código 1.4.3 - API de assinaturas, pagamentos e metas

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Endpoints para UC01–UC04 (cadastro, consulta, edição, exclusão, pausa, reativação, confirmação de pagamento e histórico) e UC09–UC11 (metas por categoria, com zerar meta no lugar de UC12). |
| Entregas | API de assinaturas, pagamentos e metas. |
| Responsável | Ronald. |
| Início e término previstos | 26/10/2026 a 13/11/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | Operações dos UC01–UC04 e UC09–UC11 respondem corretamente e só para o usuário dono. Validação: gerentes. |
| Dependências | 1.4.1 |
| Recursos necessários | Banco e esquema do pacote 1.4.1, repositório. |
| Custo estimado | 12 horas de esforço |
| Premissas e restrições | Reaproveita as rotas hoje atendidas pelo `json-server`, já centralizadas em `src/lib/api.ts`, para reduzir o trabalho no front. |
| Riscos associados | Atraso no desenvolvimento; mudanças nos requisitos. |

### 3.15 Código 1.4.4 - API de extratos e conciliação

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Receber o CSV (`data,descricao,valor`), reconhecer serviços do catálogo e confirmar pagamento ou criar assinatura sem duplicar (UC13 e UC14). |
| Entregas | API de importação e conciliação. |
| Responsável | Rodrigo. |
| Início e término previstos | 26/10/2026 a 06/11/2026 |
| Marco relacionado | Marco 2 |
| Critérios de aceitação | Importar `teste.csv` produz o mesmo resultado do front atual; layout inválido é rejeitado com mensagem. Validação: gerentes. |
| Dependências | 1.4.1 |
| Recursos necessários | Banco do pacote 1.4.1, `teste.csv`. |
| Custo estimado | 8 horas de esforço |
| Premissas e restrições | OFX fora do escopo; UC15 e UC16 fora do escopo. |
| Riscos associados | Falha na importação; atraso no desenvolvimento. |

### 3.16 Código 1.4.5 - API de relatórios e catálogo de serviços

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Servir o catálogo e o serviço "Outro" (UC06), calcular as agregações mensal e anual por categoria e o ranking (UC17) e fornecer os links de cancelamento (UC18). |
| Entregas | API de relatórios e de catálogo. |
| Responsável | Rodrigo. |
| Início e término previstos | 09/11/2026 a 20/11/2026 |
| Marco relacionado | Marco 3 |
| Critérios de aceitação | Totais do relatório batem com os do front atual para os mesmos dados. Validação: gerentes. |
| Dependências | 1.4.1; mesmo responsável de 1.4.4, que termina antes (06/11/2026). |
| Recursos necessários | Banco do pacote 1.4.1, repositório. |
| Custo estimado | 8 horas de esforço |
| Premissas e restrições | O catálogo continua uma lista fixa (seed), sem área administrativa. |
| Riscos associados | Divergência de cálculo entre front e API; atraso no desenvolvimento. |

### 3.17 Código 1.4.6 - Publicação em ambiente gratuito

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Publicar o front-end e a API com banco em plano gratuito, configurar variáveis de ambiente e documentar o passo a passo no README. |
| Entregas | Sistema acessível por endereço público e instruções de publicação. |
| Responsável | Thiago. |
| Início e término previstos | 23/11/2026 a 04/12/2026 |
| Marco relacionado | Marco 3 |
| Critérios de aceitação | Sistema responde no endereço público com os dados de teste; instruções reproduzíveis pelos gerentes. Validação: gerentes. |
| Dependências | 1.4.2, 1.4.3, 1.4.4, 1.4.5 |
| Recursos necessários | Contas em planos gratuitos de hospedagem e banco, repositório. |
| Custo estimado | 8 horas de esforço |
| Premissas e restrições | Cenário A (acadêmico, uso não comercial, custo financeiro R$ 0,00, sem domínio próprio). Serviços gratuitos podem pausar por inatividade. |
| Riscos associados | Pausa ou limite dos planos gratuitos; monetização ainda não decidida. |

### 3.18 Código 1.5.1 - Integração front-end/back-end

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Substituir o `json-server` pela API real no front, ajustando autenticação, chaves de cache por usuário e tratamento de erros. |
| Entregas | Front-end funcionando contra a API real. |
| Responsável | Ronald. |
| Início e término previstos | 16/11/2026 a 04/12/2026 |
| Marco relacionado | Marco 3 |
| Critérios de aceitação | Os 13 UC implementados funcionam sem o `json-server` em execução; dados isolados por usuário. Validação: gerentes. |
| Dependências | 1.4.3 (término-início); 1.4.2, 1.4.4 e 1.4.5 de forma incremental, podendo terminar até 20/11/2026. |
| Recursos necessários | Front-end atual, API dos pacotes 1.4.x, repositório. |
| Custo estimado | 12 horas de esforço |
| Premissas e restrições | Integração módulo a módulo, conforme cada API fica pronta. |
| Riscos associados | Atraso das APIs; incompatibilidade de contratos; mudanças nos requisitos. |

### 3.19 Código 1.5.2 - Testes funcionais e de segurança básica

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Executar o checklist dos UC implementados, o isolamento entre contas, o armazenamento de senhas em hash, a importação de CSV inválido e as listas vazias, registrando evidências. |
| Entregas | Checklist executado, evidências e lista de defeitos. |
| Responsável | Rodrigo. |
| Início e término previstos | 23/11/2026 a 04/12/2026 |
| Marco relacionado | Marco 3 |
| Critérios de aceitação | Fluxos principais sem defeito crítico aberto; defeitos restantes registrados. Validação: gerentes. |
| Dependências | 1.5.1 (início-início com defasagem de uma semana; cada módulo é testado após integrado). |
| Recursos necessários | Ambiente de teste, dados de exemplo e `teste.csv`. |
| Custo estimado | 8 horas de esforço |
| Premissas e restrições | Correção de defeitos na semana final é coberta pela reserva de contingência. |
| Riscos associados | Defeitos tardios; baixa participação dos integrantes. |

### 3.20 Código 1.5.3 - Validação com patrocinador e gerentes

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Conferir os critérios de aceitação de cada pacote e do sistema como um todo, registrando a aprovação. |
| Entregas | Ata de validação e lista de pendências. |
| Responsável | Davi, João, Michael e Vinicius. |
| Início e término previstos | 07/12/2026 a 09/12/2026 |
| Marco relacionado | Marco 3 |
| Critérios de aceitação | Todos os pacotes conferidos e ata assinada pelos gerentes e pelo patrocinador. |
| Dependências | 1.5.2 |
| Recursos necessários | Sistema publicado, checklist e Dicionário da EAP. |
| Custo estimado | 6 horas de esforço |
| Premissas e restrições | Disponibilidade do patrocinador na segunda semana de dezembro. |
| Riscos associados | Ausência do patrocinador; defeitos encontrados na validação. |

### 3.21 Código 1.6.1 - Documentação final e entrega

| Campo | Descrição |
| ----- | --------- |
| Descrição do trabalho | Atualizar README, Manual, Cronograma, Refinamento (status final), EAP, Dicionário e Plano com os valores reais e fazer a entrega final. |
| Entregas | Documentação final no repositório e entrega do projeto. |
| Responsável | Davi, João, Michael e Vinicius. |
| Início e término previstos | 07/12/2026 a 11/12/2026 |
| Marco relacionado | Marco 3 |
| Critérios de aceitação | Documentos consistentes com a versão entregue e entrega registrada até 11/12/2026. Validação: gerentes e patrocinador. |
| Dependências | 1.5.2 |
| Recursos necessários | Repositório e todos os artefatos do projeto. |
| Custo estimado | 8 horas de esforço |
| Premissas e restrições | O projeto encerra na segunda semana de dezembro de 2026. |
| Riscos associados | Ausência de integrantes; atraso na documentação. |

## 4. Exemplo Preenchido

Todos os pacotes estão preenchidos na seção 3; o pacote 1.4.3 (seção 3.14) serve de referência de formato.

## 5. Observações

- O dicionário descreve apenas os pacotes de trabalho, que são o último nível da EAP. Todo elemento aqui existe no `EAP.md` e vice-versa.
- Custos estão em horas de esforço; não há valor/hora nem orçamento financeiro definido. Infraestrutura no cenário A: R$ 0,00.
- Esforço total dos pacotes: 138 h (programação 88 h, gestão 50 h). Capacidade, reserva de contingência e linhas de base estão no Plano do Projeto (trecho "Capacidade e Reserva").
- Datas coerentes com os marcos: Marco 1 em 05/10/2026, Marco 2 em 17/11/2026 (a confirmar) e Marco 3 de 07/12/2026 a 11/12/2026.
