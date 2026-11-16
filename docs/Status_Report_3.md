# Status Report 3 — SubTracker

Monitoramento e controle: engajamento, comunicação, riscos e resposta a mudanças · Grupo de gerência (GPTI): Davi Luiz Rodrigues da Conceição, João Henrique Lima Gualberto, Michael Patrick Ferreira da Silva Borba e Vinicius da Silva Mendes

**Como ler este relatório.** NI significa «não informado»: o dado não foi fornecido ao grupo até a data de status e nenhum valor foi estimado. **[confirmar]** marca uma dedução feita a partir dos documentos e do repositório, que o grupo ainda precisa validar. A linha de base vem do Plano do Projeto v3.0, da EAP e do Dicionário (AV1). Os resultados anteriores vêm do Status Report 1 (SR1) e do Status Report 2 (SR2).

## 1. Data de status e período coberto

| Item | Conteúdo |
| --- | --- |
| Data de status | 15/11/2026 |
| Período coberto | 03/11/2026 (dia seguinte ao corte do SR2) a 15/11/2026 |
| Marco 2 | 17/11/2026, conforme o Plano. Restam 2 dias úteis (16 e 17/11). A separação Marco 1 (front-end) e Marco 2 (API própria) proposta no SR1 (Q-15) não foi formalizada; este relatório usa o Plano |
| Evidência usada | (1) histórico completo dos repositórios `SubTracker` (branches `main`, `develop` e `feature/refresh-tokens-openapi-tests`) e `Gerencia-2026.2` (4 branches), lidos em 15/11; (2) relatos de horas de Ronald, Rodrigo e Thiago; (3) mensagens no Teams pedindo os relatos (prints a anexar, ver seção 4); (4) ata das reuniões de 13 e 14/11 (seção 4.4); (5) relatório de testes do back-end e do front-end de 16/11 (seção 5.6) |
| Limites | O relatório de testes de 16/11 informa testes do back-end e do front-end, mas não detalha os erros nem os resultados por caso de uso, e por isso não substitui o reteste dos critérios do Dicionário. Os relatos de horas chegaram depois das semanas relatadas e são tratados como reconstituídos. A data do commit é a do autor e só aparece trabalho enviado ao repositório |
| Taxa de valoração | R$ 10,00 por hora, igual para todos (Plano, seção 7.1); índices em horas e em R$ coincidem |
| Versão | Revisada em 15/11/2026. Restaura as seções do SR2 que estavam resumidas (cronograma completo, valor agregado por atividade, recursos, registro de mudanças com impacto), responde as perguntas de controle do escopo do SR1 e acrescenta os limites de ação, o ponto de decisão 2 e os critérios de encerramento antecipado do Plano (seções 12.3, 13.2 e 14.2). **Revisão de 16/11/2026:** incorpora a ata das reuniões de 13 e 14/11, o relatório de testes de 16/11 e os cálculos de valor agregado, previsão e capacidade (seções 4.4, 5.6, 6.2, 7 e 11.1), e acrescenta como executar a aplicação (seção 13). A data de corte das medições continua 15/11 |

## 2. Situação geral de escopo, prazo, custo e participação

**VERMELHO — o Marco 2 de 17/11 não está sustentado pelas evidências.**

| Dimensão | Cor | Justificativa |
| --- | --- | --- |
| Escopo | **VERMELHO** | 1 de 6 pacotes de front-end com critério verificado (SR1). O software mudou desde o SR2 (front-end ligado à API real) e **não foi retestado**. Importação de extratos, serviços, relatório e tutorial não têm código novo. O back-end real (Express, Prisma e PostgreSQL) foi construído **sem aprovação** do patrocinador (CHG-06). O relatório de testes de 16/11 informa back-end funcionando, com poucos erros pontuais ainda a detalhar, e front-end com correções em andamento (seção 5.6) |
| Prazo | **VERMELHO** | Os pacotes do caminho crítico (1.3.5 e 1.4.5, planejados até 17/11) **não têm nenhum commit**. Não há código de importação de extratos no back-end. O IDP é de 0,16, deprimido pela falta de verificação, e por isso não serve como tendência (seção 7.2). Pela capacidade nominal, os 42 h de 1.3.5, 1.4.5, 1.3.6 e 1.4.6 terminam por volta de 10/12, e não em 17/11 (seção 6.2) |
| Custo | **Em risco (indicativo)** | CR parcial de 35,5 h (32,5 h se a dupla contagem de 19/10 se confirmar), apontado por 3 de 7 integrantes; VA de 29,2 h pela regra 20/80 do SR2 (16 h no critério estrito). IDC de 0,82 a 0,90 e ENT de 231 h a 277 h, contra 251 h de limite com contingência (seção 7.2). Como o CR é parcial, o IDC está inflado e o ENT subestimado: o número é indicativo |
| Participação e comunicação | **VERMELHO** | A reunião semanal e a revisão semanal do cronograma, previstas no Plano, não ocorreram no formato previsto. A ata registra duas reuniões por chat no Teams (13 e 14/11, cerca de 20 min cada), com Ronald, Thiago, Davi e Michael; Rodrigo, João e Vinicius não constam. Nenhum integrante da gerência tem commit depois de 19/10. Rodrigo tem 1 commit desde 07/10 |

### 2.1 Evolução em relação ao SR1 e ao SR2

| Indicador | SR1 (06/10) | SR2 (02/11) | SR3 (15/11) |
| --- | --- | --- | --- |
| Escopo | VERMELHO | VERMELHO | VERMELHO |
| Prazo | Fora do SR1 | Não determinada | **VERMELHO** (caminho crítico sem commit) |
| Custo | Fora do SR1 | Não determinada | Não determinada |
| Participação e comunicação | Não avaliada | NI (Q-16) | **VERMELHO** (0 de 5 reuniões semanais; 2 reuniões por chat em 13 e 14/11) |
| Pacotes de front-end com critério verificado | 1 de 6 | 1 de 6 | 1 de 6 (sem reteste) |
| Software | Marco 1, com json-server | «Inalterado desde o SR1» | **Mudou:** front-end ligado à API real e back-end real na `develop` (06/11 a 11/11) |
| VP | — | 158,2 h | 178,6 h |
| VA | — | 16 h | 16 h (estrito); **29,2 h** (adotado, regra 20/80) |
| CR (parcial) | — | 14 h (2 de 7 pessoas) | **35,5 h** (3 de 7 pessoas; 32,5 h se Q-19 se confirmar) |
| IDC e ENT (indicativos) | — | Não calculados | IDC 0,82 a 0,90; ENT 231 h a 277 h (limite com contingência: 251 h) |
| Commits no `SubTracker` no período | 25 (até 06/10) | 5 (07/10 a 02/11) | 7 (03/11 a 15/11) |
| Commits da gerência (`Gerencia-2026.2`) | 17 | 0 | 0 |
| Decisões pedidas ao patrocinador | CHG-01 a CHG-05 | CHG-01 a CHG-06 e D1 a D5 | Mesmas, **sem decisão**; adiadas para a entrega final |
| Questões abertas | Q-01 a Q-15 | Q-01 a Q-18 | Q-01 a Q-28 (nenhuma encerrada; ver seção 10) |

**O que melhorou:** Rodrigo e Thiago enviaram relatos de horas; os desenvolvedores têm commits recentes; o back-end real passou a existir e o relatório de testes de 16/11 o descreve como funcionando; houve duas reuniões por chat em 13 e 14/11, com ata. **O que não mudou ou piorou:** o escopo do SR1 segue aberto, o caminho crítico não tem commit e as reuniões e decisões previstas não ocorreram.

### 2.2 As três perguntas do SR2, hoje

1. **O caminho crítico ainda entrega o Marco 2 em 17/11?** As evidências não sustentam. 1.3.5 e 1.4.5 seguem sem commit e restam 2 dias úteis (SR2: não era possível responder). Pela capacidade nominal, 1.3.5, 1.4.5, 1.3.6 e 1.4.6 (42 h) terminam por volta de 10/12 (seção 6.2). O que já está pronto e testado (autenticação, assinaturas e orçamentos) pode ser demonstrado em 17/11, sem importação, relatório, tutorial e serviços (seção 6.3).
2. **O valor agregado mostra trabalho feito no ritmo e no custo planejados?** Não. O VP é 178,6 h e o VA adotado é 29,2 h, o que dá IDP de 0,16. O IDC é de 0,82 a 0,90, abaixo de 1, e é indicativo porque o CR é parcial. O relatório de testes não eleva o VA, porque os erros do back-end não foram detalhados e o critério dos pacotes não foi verificado (seção 7).
3. **As horas que faltam cabem na capacidade que resta até o Marco 2?** Provavelmente não. Só os pacotes 1.3.5, 1.4.5, 1.3.6 e 1.4.6 somam 42 h planejadas (16 + 12 + 8 + 6), e a capacidade nominal de 16 a 17/11 é de 1,6 h por pessoa, ou 4,8 h para os 3 desenvolvedores. Até 11/12, os 62 h do caminho crítico que faltam (1.3.5, 1.4.5, 1.3.6, 1.4.6, 1.5.2 e 1.5.3) superam em 16,4 h a capacidade nominal de 45,6 h dos desenvolvedores (seção 6.2). O esforço restante real continua NI.

## 3. Engajamento das partes interessadas

### 3.1 Matriz de engajamento (planejado × observado)

Níveis: **D** desconhecedor · **R** resistente · **N** neutro · **A** apoiador · **L** líder. O nível desejado é proposta do grupo, derivada da estratégia do Plano (seção 10). O nível atual será fechado na reunião de acompanhamento de 16/11 e ainda não foi registrado.

| Parte interessada | Estratégia (Plano) | Desejado | Evidência no período | Indício frente ao esperado | Atual |
| --- | --- | :-: | --- | --- | :-: |
| Patrocinador (Diogo Silveira Mendonça) | Gerenciar de perto | L | Decisões D1 a D5 e CHG-01 a CHG-06 sem resposta; informado que decide na entrega final | Abaixo | NI |
| Gerência (Davi, João, Michael, Vinicius) | Gerenciar de perto | L | Nenhum commit depois de 19/10; horas NI (ver 3.3). Davi conduziu e Michael participou das reuniões por chat de 13 e 14/11 (ata); João e Vinicius não constam | Abaixo | NI |
| Ronald (desenvolvimento) | Gerenciar de perto | A | 2 commits no período (11/11); relato de 10 a 13/11; presente nas reuniões de 13 e 14/11 (ata) | Dentro | NI |
| Thiago (desenvolvimento) | Gerenciar de perto | A | 4 commits em 08/11; relato de 6 h para 03 a 09/11 pela ata (enviado primeiro ao chat de outro projeto e reenviado); presente nas reuniões | Dentro | NI |
| Rodrigo (desenvolvimento) | Gerenciar de perto | A | 1 commit (06/11); relato de ~10 h em quatro semanas; nenhum commit em 1.3.5 ou 1.4.5; não consta nas reuniões de 13 e 14/11 (ata) | Abaixo | NI |
| Usuários finais | Informar e consultar | A | Teste com 5 usuários previsto em 1.5.2 (25/11 a 03/12); ainda não iniciado | Dentro do planejado | NI |
| Administrador do catálogo | Manter informado | A | Lista de verificação de provedores prevista antes de 1.5.2; sem evidência. UC05, UC07 e UC08 não implementados | NI | NI |
| Provedores de serviço | Monitorar | N | Verificação dos links prevista antes de 1.5.2; sem evidência | NI | NI |
| Instituições financeiras | Monitorar | N | Amostras de CSV de pelo menos 3 layouts previstas no início de 1.3.5 e 1.4.5; sem evidência (Q-09) | Abaixo | NI |

### 3.2 Equipe de desenvolvimento

| Pessoa | Contas no GitHub | Commits (total) | No período | Último commit | Relato de horas | Leitura |
| --- | --- | :-: | :-: | --- | --- | --- |
| Ronald | TeTeuTX, Ronald Teixeira de Assis | 24 | 2 | 11/11 | 6 h (19 a 23/10) e ~5,5 h (10 a 13/11) | Ativo; o trabalho de 11/11 está só em branch de feature, fora da `develop` |
| Thiago | SouzTH, Thiago Souza da Silva | 9 | 4 | 08/11 | 14 h (8 h até 02/11, com 0 h em 26 a 30/10; 6 h em 03 a 09/11, pela ata) | Ativo; as 6 h de 03 a 09/11 provavelmente cobrem os 4 commits de 08/11 [confirmar] |
| Rodrigo | Ramerico11, Rodrigo | 3 | 1 | 06/11 | ~10 h em quatro semanas, sem divisão por semana | Abaixo do esperado; dono de 1.3.5 e 1.4.5, sem commit nesses pacotes |

### 3.3 Frequência de trabalho da gerência

| Pessoa | Commits (`Gerencia-2026.2` e `SubTracker`) | Último commit | Horas apontadas | Presença em reunião |
| --- | :-: | --- | --- | --- |
| Davi | 4 | 04/10 | NI | Conduziu as reuniões por chat de 13 e 14/11 (ata) |
| João | 0 | — | NI | Não consta na ata |
| Michael | 10 | 19/10 (Status Report 1) | NI | Participou das reuniões por chat de 13 e 14/11 (ata) |
| Vinicius | 4 | 04/10 | NI | Não consta na ata |

Commits medem presença no repositório e não todo o trabalho da gerência (reuniões, análises e documentos nem sempre passam pelo Git). As horas e a presença em reunião estão NI porque não foram fornecidas.

### 3.4 Commits por semana desde o corte do SR1

| Semana | Commits | Quem |
| --- | :-: | --- |
| 06 a 12/10 | 0 | ninguém |
| 13 a 18/10 | 0 | ninguém |
| 19 a 25/10 | 4 | Ronald 2, Michael 1, Thiago 1 |
| 26 a 31/10 | 0 | ninguém |
| 02 a 08/11 | 6 | Thiago 5, Rodrigo 1 |
| 09 a 15/11 | 2 | Ronald 2 |

### 3.5 Plano de ação para o engajamento abaixo do esperado

Prazos propostos pela gerência; o grupo confirma.

| Ação | Quem | Responsável | Prazo |
| --- | --- | --- | --- |
| Reunião de acompanhamento no Teams (30 min), com resumo ou transcrição como ata e rodada de participação de 1 min por pessoa | Todos | João | 16/11 |
| Conversa individual com quem não comparecer ou não responder (Rodrigo e a gerência, em primeiro lugar) | Rodrigo, Davi, João, Michael, Vinicius | Davi | 18/11 |
| Relato padronizado no canal do projeto: pacote da EAP, semana, horas, link do commit e impedimentos | Todos | Vinicius (cobrança) | 18/11 |
| Cobertura entre pares para 1.3.5 e 1.4.5 (risco R3), se Rodrigo não confirmar disponibilidade | Ronald e Thiago | João | 16/11 |
| Alerta formal ao patrocinador (risco R8), se não houver retorno até o prazo | Gerência | Davi | 19/11 |

## 4. Comunicações planejadas e evidências

### 4.1 Plano de Comunicação (seção 11) × o que ocorreu

| Comunicação planejada | Frequência | Ocorreu? | Evidência |
| --- | --- | --- | --- |
| Reunião da equipe (gerência e desenvolvimento) | Semanal, a partir de 13/10 (primeiro status semanal, Plano seção 12.3) | **Parcial**: 0 de 5 reuniões semanais formais previstas até a data de status (13/10, 20/10, 27/10, 03/11 e 10/11) (informado pelo grupo); duas reuniões por chat no Teams, de cerca de 20 min, em 13/11 e 14/11 | Ata (seção 4.4). Rodrigo, João e Vinicius não constam. Desvio registrado; ver risco R8 |
| Revisão do cronograma e do caminho crítico | Semanal | **Não** | A ata trata de entregas e riscos e não revisa o caminho crítico |
| Atualização do GitHub (commits, issues, marcos) | Contínua | Parcial | 12 commits desde 07/10; semanas sem nenhum commit: 06 a 18/10 e 26 a 31/10 |
| Relatório de status ao patrocinador | Marcos 1, 2 e 3 | Parcial | SR1 commitado em 19/10 (`SubTracker`, `main`). SR2 recebido, sem commit; envio ao patrocinador: NI |
| Demonstração do sistema | Marco 2 (17/11) e Marco 3 (11/12) | Ainda não | Marco 2 em 2 dias úteis; roteiro e responsável (Ronald, pelo Plano) a confirmar; ver seção 6.3 |
| Validação com usuários | Uma vez, em 1.5.2 (25/11 a 03/12) | Ainda não | Futuro |
| Pedido de mudança | Sob demanda | Parcial | CHG-01 a CHG-06 registrados nos SR1 e SR2; sem registro no GitHub; sem decisão |
| Alerta de risco ao patrocinador | Imediato | NI | Nenhuma evidência de alerta enviado |
| Pedido de relato de atividades (mensagens no Teams) | Não previsto no plano | **Sim** | Mensagens no Teams (informado pelo grupo) e ata das reuniões de 13 e 14/11 (seção 4.4); prints a anexar. Nelas, o grupo informou que a API de assinaturas está concluída e que faltam os testes finais e a integração do front-end com o back-end; que a branch a ser testada é a `feature/refresh-tokens-openapi-tests`; que, no final, as branches serão mescladas na `main` e as demais apagadas; e foi pedido que o relatório explique como rodar a aplicação, principalmente o back-end |

### 4.2 Relatos de horas recebidos no período

| Pessoa | Relato | Chegou |
| --- | --- | --- |
| Ronald | 10 a 13/11, ~5,5 h: refresh tokens com cookies HttpOnly e logout, recuperação de senha por e-mail com token de 20 min, tabelas de sessão (Prisma), Swagger/OpenAPI, testes de autenticação e de isolamento por usuário, Docker na porta 5433 | Depois da semana relatada; a ata registra o relato como feito «com auxílio» [confirmar o tipo de auxílio] |
| Rodrigo | ~10 h em quatro semanas: telas ligadas à API real na porta 3001, autenticação, cadastro, rotas protegidas, perfil, orçamento e CRUD de assinaturas; branch `feature/frontend-api` | Depois do período; sem divisão por semana |
| Thiago | 03 a 09/11, 6 h: autenticação com Passport e redefinição de senha (3h30); atualização dos arquivos JSON da API e integração à versão principal de desenvolvimento (1 h); correção de vulnerabilidades nas dependências e formatação do controller de autenticação (1h30); remoção das branches de trabalho desnecessárias | Depois da semana relatada; enviado primeiro por engano ao chat de outro projeto e reenviado (ata) |
| Gerência | Nenhum relato | — |

### 4.2.1 Início da medição de horas por pessoa

Pedido do SR2 (ação 1). As semanas abaixo são as que constam nos relatos; todas são reconstituídas, porque os relatos chegaram depois das semanas relatadas.

| Pessoa | Primeira semana com relato | Semanas sem relato | Situação |
| --- | --- | --- | --- |
| Ronald | 19 a 23/10 | 07 a 16/10; 26/10 a 09/11 (NI) | Reconstituído |
| Thiago | 19/10 | 07 a 16/10 (NI); 26 a 30/10 consta 0 h; 03 a 09/11 relatadas (6 h, pela ata); 10 a 15/11 NI | Reconstituído |
| Rodrigo | NI: relato de ~10 h em quatro semanas, sem divisão por semana | NI | Reconstituído; semanas NI |
| Davi, João, Michael e Vinicius | NI | Todas | Sem relato |

### 4.3 Leitura

As comunicações que ocorreram foram o pedido de relato por mensagem no Teams e duas reuniões por chat em 13 e 14/11, que geraram a ata. As reuniões semanais previstas não aconteceram no formato do Plano e os relatos chegaram tarde ou incompletos. O gatilho do risco R8 foi atingido; as reuniões por chat reduzem o problema sem eliminá-lo, porque só 4 dos 7 integrantes constam na ata. A gerência corrige com a reunião de 16/11 (seção 3.5), com relato padronizado e com o uso do canal do projeto no Teams, para que a comunicação tenha registro institucional.

### 4.4 Ata das reuniões de 13 e 14/11

Duas reuniões de cerca de 20 minutos, no chat do Microsoft Teams, sobre os relatórios das semanas de 03 a 09/11 e de 10 a 13/11. Participantes: Ronald e Thiago (back-end/API), Davi (condução e recolhimento dos relatórios) e Michael. Pauta: engajamento (entregas realizadas) e riscos. Prazo para relatórios adicionais: 18:10.

| Tema | O que a ata registra | Onde entra neste relatório |
| --- | --- | --- |
| Entregas de Ronald (10 a 13/11, ~5h30, com auxílio) | Refresh token com cookies HttpOnly e logout; recuperação de senha por e-mail com token de 20 min e invalidação das sessões anteriores; controle de sessões no banco (tabelas e migrações do Prisma); Swagger/OpenAPI; testes automatizados de autenticação, rotas protegidas e isolamento por usuário; Docker na porta 5433 | 4.2, 5.1 e 7 |
| Entregas de Thiago (03 a 09/11, 6 h) | Autenticação com Passport e redefinição de senha (3h30); JSON da API alinhados ao front-end e integração à versão principal de desenvolvimento (1 h); correção de vulnerabilidades e formatação do controller (1h30); remoção de branches de trabalho | 4.2 e 7 |
| APIs de assinatura | Davi perguntou se estavam concluídas e a resposta foi que sim. Michael perguntou o que faltava; Thiago respondeu que, até onde sabe, está feito, mas faltam os testes finais. Esclareceu-se que a pendência é a integração do front-end com o back-end | 5.1 e 5.6 |
| Branches | Além da `main`, há duas branches em uso. O merge na `main` será feito ao final, apagando as demais. Decisão: testar a mais recente, `feature/refresh-tokens-openapi-tests` | 5.3, R10 e ação 21 |
| Riscos | Davi informou que algumas entregas estão em vermelho. Considerando a possibilidade de reavaliação, a situação ainda é reversível | Seção 2 |

**Encaminhamentos da ata e onde estão neste relatório:** atualizar o relatório explicando como rodar a aplicação, principalmente o back-end (seção 13 e ação 10); realizar os testes finais das APIs de assinatura (ação 20); integrar o front-end com o back-end (ação 20 e pacote 1.5.1); fazer o merge das branches na `main` e apagar as demais (ações 2 e 21); enviar relatórios adicionais até as 18:10 (Q-16 e ação 5). Os relatórios recolhidos entram no relatório geral, e todos os integrantes devem reportar o que fizeram.

**O que a ata não traz:** horas da gerência, presença de Rodrigo, João e Vinicius, nem revisão do caminho crítico.

## 5. Escopo desde o Status Report 2

### 5.1 Pacotes

O front-end foi ligado à API real e o SR2 afirmava que o software não havia mudado. **Os resultados de 1.3.2 a 1.3.6 não foram retestados** e valem como no SR1 até o reteste.

| Pacote | Resultado verificado | Desde o SR2 |
| --- | --- | --- |
| 1.3.1 Estrutura de front-end e rotas | Passou (SR1) | Sem reteste |
| 1.3.2 Assinaturas e dashboard | Falhou (SR1) | Telas ligadas à API real (06/11). O relatório de testes de 16/11 diz que os erros do front-end estão sendo corrigidos, sem listá-los. **Não retestado** |
| 1.3.3 Serviços e cancelamento | Falhou (SR1) | Sem avanço |
| 1.3.4 Tetos e consumo | Falhou (SR1) | Tela de orçamento ligada à API (relato de Rodrigo). Correções do front-end em andamento (relatório de testes). **Não retestado** |
| 1.3.5 Extratos e conciliação ★ | Falhou (SR1) | **Sem commit** |
| 1.3.6 Relatório e tutorial ★ | Falhou (SR1) | Início planejado 10/11; **sem commit** |
| 1.4.1 Estrutura da API e banco | Não verificado | Base criada em 19/10 (Ronald) e integrada em 23/10 (Thiago); autenticação em 02/11 (Thiago) e 11/11 (Ronald, branch de feature). Schema com 2 das 5 entidades do Dicionário: Assinatura e Teto (faltam Serviço, Categoria e Extrato Importado). O relatório de testes de 16/11 informa PostgreSQL no Docker (porta 5433), migrações do Prisma e seed do usuário de teste, sem tratar das três entidades que faltam. Critério não verificado |
| 1.4.2 API de Assinaturas | Não verificado | Controller criado em 19/10; testes de isolamento por usuário só na branch de feature. A ata registra a API como concluída, faltando os testes finais, e o relatório de testes lista listar, consultar (com histórico de pagamentos), criar, editar e excluir, sempre isoladas por usuário, como funcionando, com poucos erros a detalhar. O critério do Dicionário (UC01 a UC04 em json-server) pressupõe json-server, e a persistência é em PostgreSQL (CHG-06, sem decisão) |
| 1.4.3 API de Serviços | Não verificado | Sem código |
| 1.4.4 API de Tetos | Não verificado | Controller de orçamentos criado em 19/10; dono do pacote ainda não definido (D5). O relatório de testes cobre consulta e atualização parcial; o critério pede UC09 a UC12 e não há rota de exclusão (UC12, Q-05), então o critério não é atendido |
| 1.4.5 Importação de extratos ★ | Não verificado | **Sem código** |
| 1.4.6 Relatório, projeção e acesso ★ | Não verificado | **Sem código** |
| 1.5.1 Integração front-end/back-end ★ | Não verificado | Iniciada em 06/11 (planejada para 18 a 24/11); depende de pacotes ainda não prontos. A ata e o relatório de testes mantêm a integração e os testes finais como pendência |
| 1.1.1 Documentação e acompanhamento | Fora do SR1 | NI. SR1 commitado em 19/10; SR2 sem commit. Este pacote soma 20 h de VP sem VA creditado |
| 1.2.1 Levantamento e rastreabilidade | Fora do SR1 | NI. Sem relato nem commit identificado com o pacote. 10 h de VP sem VA |
| 1.2.2 Prototipagem e matrizes | Fora do SR1 | NI. Sem relato nem commit identificado com o pacote. 14 h de VP sem VA |
| 1.5.2 Testes de validação funcional ★ | Fora do SR1 | Futuro (25/11 a 03/12) |
| 1.5.3 Ajustes e validação final ★ | Fora do SR1 | Futuro (04/12 a 11/12) |
| 1.6.1 Documentação final e entrega ★ | Fora do SR1 | Futuro (07/12 a 11/12) |

★ caminho crítico.

**Verificados:** 1.3.1 (SR1). **Pendentes:** UC05, UC07, UC08, UC12, UC15, UC16 e tutorial (SR1); a leitura do código em 15/11 não mostra correção de nenhum deles (seção 10.1). **Não demonstrados:** abertura da página externa do link de cancelamento e uso do fluxo principal só com teclado (SR1, Q-02); o software mudou, mas ainda não houve reteste.

**Mapeamento dos relatos aos pacotes [confirmar].** Nenhum relato nomeia o pacote da EAP; o mapeamento foi deduzido do Dicionário e dos commits.

| Trabalho | Pacote | Autor |
| --- | --- | --- |
| Setup, migration e seed (19/10); merge da base (23/10) | 1.4.1 | Ronald (commits de 19/10); Thiago (23/10) |
| Autenticação Passport/JWT e redefinição de senha (02/11); correções de 08/11 | 1.4.1 | Thiago |
| Refresh token, recuperação de senha por e-mail, Swagger, testes (11/11) | 1.4.1, com os testes de isolamento em 1.4.2 | Ronald |
| Telas ligadas à API real (06/11) | 1.5.1, tocando 1.3.2 e 1.3.4 | Rodrigo |

### 5.2 Fora da linha de base

Autenticação com refresh token, recuperação de senha por e-mail, tela de perfil, Swagger, Docker, Prisma e PostgreSQL não constam em nenhum pacote do Dicionário. Estão ligados a CHG-05 e CHG-06 e **seguem sem decisão do patrocinador**.

### 5.3 Estado do repositório (15/11)

- A `develop` está 13 commits à frente da `main` e a `main` tem 4 commits que a `develop` não tem (Status Report 1, Business Case e README, todos de documentação). A fusão automática falha por conflito.
- Os commits de 11/11 de Ronald (refresh token e recuperação de senha) estão só na branch `feature/refresh-tokens-openapi-tests`, fora da `develop`. Os testes automatizados (`api.test.ts` e `jwt.test.ts`) estão só nessa branch.
- O README da `develop` ainda descreve o sistema com json-server e diz que o back-end «não está ligado ao front-end», o que contradiz os commits de 06/11 e 08/11.
- A ata de 13 e 14/11 decidiu testar a branch `feature/refresh-tokens-openapi-tests` e, ao final, fazer o merge na `main` e apagar as demais. Falta resolver o conflito com a `develop` (Q-21) antes disso.

### 5.4 Requisitos do Marco 1 (SR1, seção 4)

Sem reteste, a situação do SR1 é mantida. A coluna «Mudança no código» vem da leitura da `develop` em 15/11.

| Requisito | Situação no SR1 | Mudança no código desde o SR1 |
| --- | --- | --- |
| RQ01 Total mensal, próximas cobranças e consumo | Parcial | Painel sem alteração; o rótulo «Em N dias» continua para cobrança vencida (Q-01) |
| RQ02 Extratos recorrentes e confirmação em lote | Parcial | Importação sem alteração; sem rejeição de layout, histórico ou descarte |
| RQ03 Cadastrar, consultar, editar, pausar e excluir assinatura | Operações atendidas | Agora via API real (06/11); sem reteste |
| RQ04 Teto por categoria e consumo | Parcial | Orçamento via API (PUT /api/budgets); sem exclusão de teto |
| RQ05 Cancelamento do provedor e catálogo (administrador) | Parcial | Sem mudança: catálogo fixo, sem perfil de administrador e sem tutorial |
| RQ06 Distribuição, ranking, projeção e custo anual | Funções atendidas | Sem alteração relevante; falta o tutorial |
| RQ07 Usabilidade móvel e perfis distintos | Parcial | Login, cadastro e rotas protegidas agora contra a API real; perfis distintos continuam inexistentes |
| RQ08 CSV como formato, sem pagamento nem conexão a bancos | Parcial | Sem mudança; validação do formato CSV continua deficiente |

Nenhum dos oito requisitos está integralmente atendido.

### 5.5 As três perguntas do controle do escopo (SR1), hoje

1. **O que está na EAP deste marco foi entregue? Não integralmente.** Continuam sem entrega UC05, UC07, UC08 (serviços), UC12 (exclusão de teto), UC15 e UC16 (histórico e descarte de extratos) e o tutorial. Os pacotes 1.3.5, 1.3.6, 1.4.3, 1.4.5 e 1.4.6 não têm código novo.
2. **O que foi entregue está na EAP? Em parte.** Há trabalho fora da EAP: back-end real (Express, Prisma e PostgreSQL), refresh token, recuperação de senha por e-mail, perfil, Swagger e Docker (CHG-05 e CHG-06), além de «Confirmar Pagamento» (CHG-04). Nenhum foi aprovado.
3. **O que foi entregue atende ao aceite do Dicionário? Não demonstrado.** 1 de 6 pacotes de front-end tem critério verificado (SR1); nenhum pacote 1.4.x tem critério verificado; nenhum aceite formal foi dado.

### 5.6 Relatório de testes de 16/11 (back-end e front-end)

Autoria: Davi. O relatório resume a situação de cada camada e não traz resultados por caso de uso nem lista os erros.

| Camada | Situação informada | O que o relatório cobre | Leitura frente ao Dicionário |
| --- | --- | --- | --- |
| Back-end (API) | Funcionando, com poucos erros pontuais ainda a detalhar | Autenticação (cadastro, login com token de 1 h, refresh token rotacionado em cookie HttpOnly por até 7 dias, logout, rotas protegidas); recuperação de senha por e-mail (token de 20 min, sessões anteriores invalidadas); assinaturas (listar, consultar com histórico, criar, editar, excluir, isoladas por usuário); orçamentos por categoria (consulta e atualização parcial); validação com Zod e resposta 400 com detalhes; Swagger em `/api-docs`; PostgreSQL no Docker (porta 5433), migrações do Prisma e seed; testes automatizados (`npm test`) | Atende em parte 1.4.1 e 1.4.2. Não cobre serviços (1.4.3), importação de extratos (1.4.5), relatório, projeção e acesso (1.4.6), exclusão de teto (UC12) nem as entidades Serviço, Categoria e Extrato Importado |
| Front-end | Pronto, com as correções dos erros encontrados em andamento | Não lista telas nem casos de uso | Não permite refazer o resultado de 1.3.2 a 1.3.6, que falharam no SR1 e seguem sem reteste |

**Pendências do próprio relatório:** detalhar e corrigir os erros pontuais do back-end; concluir as correções do front-end; executar os testes finais de integração entre front-end e back-end (Q-26 e Q-27, ação 20).

**Leitura para o valor agregado.** O relatório e a ata sustentam que 1.4.1, 1.4.2 e 1.4.4 começaram e têm código funcionando, o que justifica o crédito de 20% da regra do SR2. Não sustentam 100%: os erros do back-end não foram descritos, os testes finais das APIs não foram feitos, 1.4.1 tem 2 das 5 entidades e 1.4.4 não tem UC12. O único pacote que poderia chegar a 100% é 1.4.2, e só se o patrocinador aceitar PostgreSQL no lugar do json-server (CHG-06).

## 6. Cronograma, caminho crítico e Marco 2

### 6.1 Cronograma completo (20 atividades)

★ = caminho crítico. NI = não informado. Datas planejadas da linha de base (Plano, seção 5.2).

| ID | Atividade | Responsável (Dicionário) | Início plan. | Fim plan. | Início real | Fim real | Duração restante | Situação |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1.1.1 | Documentação e acompanhamento | Gerência | 03/10 | 05/10 | NI | NI | NI | NI; fim planejado já passou. SR1 commitado em 19/10 |
| 1.1.2 | Monitoramento, riscos e comunicação | Gerência | 05/10 | 11/12 | NI | NI | NI | Em andamento pelo plano; reunião semanal e revisão do cronograma não ocorreram |
| 1.2.1 | Levantamento e rastreabilidade | Ronald, Rodrigo, Thiago | 03/10 | 05/10 | NI | NI | NI | NI; fim planejado já passou |
| 1.2.2 | Prototipagem e matrizes | Ronald, Rodrigo, Thiago | 03/10 | 10/10 | NI | NI | NI | NI; fim planejado já passou |
| 1.3.1 | Estrutura de front-end e rotas | Ronald | 06/10 | 12/10 | NI | NI | 0 | Concluída; critério verificado no SR1; sem reteste |
| 1.3.2 | Assinaturas e dashboard | Ronald | 06/10 | 31/10 | NI | NI | NI | Telas ligadas à API (06/11); correções do front-end em andamento (relatório de testes); falhou no SR1; não retestado |
| 1.3.3 | Serviços e cancelamento | Thiago | 12/10 | 31/10 | NI | NI | NI | Sem avanço; falhou no SR1 |
| 1.3.4 | Tetos e consumo orçamentário | Equipe de desenvolvimento\* | 12/10 | 31/10 | NI | NI | NI | Tela ligada à API (relato de Rodrigo); falhou no SR1; não retestado |
| 1.3.5 ★ | Extratos, histórico e conciliação | Rodrigo | 06/10 | 17/11 | NI | NI | NI | **Sem commit**; falhou no SR1 |
| 1.3.6 ★ | Relatório e tutorial | Ronald e Thiago | 10/11 | 17/11 | NI | NI | NI | **Sem commit**; início planejado já passou |
| 1.4.1 | Estrutura da API e modelagem do banco | Rodrigo | 06/10 | 12/10 | 19/10 | NI | NI | Começou 13 dias corridos depois do planejado; critério não verificado; 2 das 5 entidades |
| 1.4.2 | API de Assinaturas | Ronald | 12/10 | 31/10 | 19/10 | NI | NI | Controller criado em 19/10; testes de isolamento só na branch de feature; ata: concluída, faltam testes finais; relatório de testes: funcionando, com poucos erros a detalhar |
| 1.4.3 | API de Serviços | Thiago | 12/10 | 31/10 | NI | NI | NI | Sem código |
| 1.4.4 | API de Tetos | Equipe de desenvolvimento\* | 12/10 | 31/10 | 19/10 | NI | NI | Controller de orçamentos criado em 19/10; dono não definido (D5); consulta e atualização testadas, sem exclusão (UC12) |
| 1.4.5 ★ | Importação de extratos e conciliação | Rodrigo | 06/10 | 17/11 | NI | NI | NI | **Sem código** |
| 1.4.6 ★ | Relatório, projeção e acesso | Ronald e Thiago | 10/11 | 17/11 | NI | NI | NI | **Sem código**; início planejado já passou |
| 1.5.1 ★ | Integração front-end/back-end | Ronald, Rodrigo, Thiago | 18/11 | 24/11 | 06/11 | NI | NI | Antecipada; dependências ainda abertas; testes finais de integração pendentes (ata e relatório de testes) |
| 1.5.2 ★ | Testes de validação funcional | Ronald, Rodrigo, Thiago | 25/11 | 03/12 | NI | NI | NI | Futuro |
| 1.5.3 ★ | Ajustes e validação final | Ronald, Rodrigo, Thiago | 04/12 | 11/12 | NI | NI | NI | Futuro |
| 1.6.1 ★ | Documentação final e entrega | Gerência | 07/12 | 11/12 | NI | NI | NI | Futuro |

\*O Dicionário não nomeia a pessoa; a decisão D5 do Plano (responsável pelos Tetos) segue sem resposta.

**Leitura.** Pela linha de base, 11 pacotes (136 h) tinham término planejado até 31/10. Só 1 (1.3.1, 16 h) tem critério verificado; os outros 10 (120 h) seguem sem verificação (Q-18).

### 6.2 Caminho crítico, desvio e folga

- **Caminho crítico da linha de base (Plano, seção 5.3):** 1.3.5 e 1.4.5 (06/10 a 17/11), depois 1.3.6 e 1.4.6 (término em 17/11), depois 1.5.1, 1.5.2, 1.5.3 e 1.6.1 (entrega final em 11/12).
- **Caminho crítico atualizado:** 1.3.5 e 1.4.5 seguem sem evidência de início. Se não começarem agora, o Marco 2 (17/11) não será cumprido, e 1.5.1, 1.5.2, 1.5.3 e 1.6.1 (entrega final em 11/12) são atingidos em cadeia.
- **Desvio de prazo no caminho crítico, em dias úteis (indicador do Plano, seção 13.2):** pela distribuição linear do VP, 1.3.5 e 1.4.5 deveriam ter 27 dos 29 dias úteis de trabalho decorridos (93%) e não têm commit; 1.3.6 e 1.4.6 deveriam ter 4 dos 6 dias úteis decorridos e também não têm. O desvio equivalente é de cerca de 27 dias úteis em 1.3.5 e 1.4.5 e de 4 dias úteis em 1.3.6 e 1.4.6, contra o limite de 3 dias úteis (seção 8.1). É um desvio medido contra a linha de base, não uma data prevista de término.
- **Folga:** a folga de 5 dias úteis de 1.3.2 a 1.3.4 e de 1.4.2 a 1.4.4 terminava em 10/11 e foi consumida sem verificação do critério.
- **Sem reserva de prazo** entre 1.5.3 e a entrega (Plano, seção 5.3).
- **Data prevista do Marco 2 e do fim, por capacidade (estimativa).** O esforço restante real continua NI, então a conta usa o esforço planejado como limite superior, já que não há commit nesses pacotes. 1.3.5, 1.4.5, 1.3.6 e 1.4.6 somam 42 h (16 + 12 + 8 + 6). A capacidade nominal dos 3 desenvolvedores é de 2,4 h por dia útil (3 × 4 h por semana ÷ 5), e 42 ÷ 2,4 = 17,5 dias úteis. Contando de 16/11, com o feriado de 20/11, isso termina por volta de **10/12**. Sobra cerca de um dia para 1.5.2 e 1.5.3 (20 h), que não cabem. A data de 17/11 só vale para o escopo já pronto (seção 6.3).
- **Capacidade até 11/12.** Os pacotes do caminho crítico que faltam somam **62 h** (1.3.5 com 16, 1.4.5 com 12, 1.3.6 com 8, 1.4.6 com 6, 1.5.2 com 12 e 1.5.3 com 8), contra 45,6 h de capacidade nominal dos desenvolvedores: faltam **16,4 h**. 1.5.1 fica fora da conta porque já tem ~10 h apontadas [confirmar]. Se 1.3.3 e 1.4.3 (20 h, fora do caminho crítico) forem mantidos, são 82 h e faltam 36,4 h. A conta não inclui as correções do back-end e do front-end citadas no relatório de testes.
- **Prazo pelo índice:** não se aplica. Com IDP de 0,16, a conta «duração planejada ÷ IDP» da aula dá um número sem sentido, porque o VA está baixo por falta de verificação, não por ritmo de trabalho.

### 6.3 Demonstração do Marco 2 (17/11)

Prevista no Plano (seção 11), com Ronald como responsável. Faltam 2 dias úteis.

| Item | Situação em 15/11 |
| --- | --- |
| Pode ser demonstrado (na `develop`, sem reteste) [confirmar] | Login, cadastro e rotas protegidas contra a API real; CRUD de assinaturas; orçamento via API (consulta e atualização); recuperação de senha por e-mail e refresh token, que estão só na branch de feature e foram descritos como funcionando no relatório de testes |
| Não pode ser demonstrado | Importação de extratos (1.3.5 e 1.4.5), relatório e tutorial (1.3.6 e 1.4.6), manutenção de serviços (1.3.3 e 1.4.3) |
| Risco para a demonstração | Refresh token, recuperação de senha por e-mail e testes estão só na branch `feature/refresh-tokens-openapi-tests` (Q-20); `develop` e `main` em conflito (Q-21) |
| Pendente | Roteiro da demonstração e confirmação de quem a conduz (ação 12 da seção 12); correção dos erros pontuais do back-end e do front-end (ações 18 e 19); testes finais das APIs de assinatura e de integração (ação 20) |

## 7. Valor agregado e custo

Regra de crédito do SR2 (20/80: 20% ao começar, com início real comprovado, e 100% quando o critério é verificado e aceito) e distribuição linear do VP pelos dias úteis do Plano, até 13/11 (15/11 é domingo).

| Total | Valor | De onde saiu |
| --- | --- | --- |
| VP | **178,6 h** (R$ 1.786) | 136 h dos 11 pacotes com fim planejado até 15/11 + 42,6 h pela distribuição linear: 1.1.2 (7,15), 1.3.5 (14,90), 1.4.5 (11,17), 1.3.6 (5,33) e 1.4.6 (4,00) |
| VA | **29,2 h** (adotado); 16 h no critério estrito | 16 h de 1.3.1 (verificado no SR1) + 20% do esforço dos pacotes com início comprovado e critério não verificado: 1.3.2, 1.3.4, 1.4.1, 1.4.2, 1.4.4 e 1.5.1 (13,2 h). Ver 7.1 |
| CR | **35,5 h** (parcial; 3 de 7 integrantes) | Ronald 11,5 h (6 + 5,5), Thiago 14 h (8 + 6 da ata) e Rodrigo ~10 h |

**Horas por pacote, pelo mapeamento da seção 5 [confirmar].** 1.4.1 recebeu ~25,5 h (Ronald 11,5 h e Thiago 14 h, incluindo as 6 h da ata) contra 10 h planejadas, ou 255%. 1.5.1 recebeu ~10 h, igual ao planejado. O Dicionário nomeia Rodrigo como responsável por 1.4.1.

**Possível dupla contagem.** Os commits de 19/10 (setup, migration e seed) são da conta de Ronald, e Thiago relata 3 h nas mesmas atividades no mesmo dia. Se forem o mesmo trabalho, o CR cai para 32,5 h (Q-19).

### 7.1 Valor agregado por atividade

Regra de crédito 20/80 (SR2). Fórmula do VP: esforço × dias úteis decorridos até 13/11 ÷ duração planejada em dias úteis. Atividade com fim planejado até 13/11 entra com o esforço inteiro; com início planejado depois de 13/11, com 0.

| ID | Esforço planejado (h) | VP em 13/11 (h) | Horas gastas | Esforço restante | Regra de crédito | VA (h) |
| --- | --- | --- | --- | --- | --- | --- |
| 1.1.1 | 20 | 20 | NI | NI | 20/80; critério NI | NI |
| 1.1.2 | 12 | 7,15 (12 × 28 ÷ 47) | NI | NI | 20/80; início NI | NI |
| 1.2.1 | 10 | 10 | NI | NI | 20/80; critério NI | NI |
| 1.2.2 | 14 | 14 | NI | NI | 20/80; critério NI | NI |
| 1.3.1 | 16 | 16 | NI | 0 | Concluída; critério verificado no SR1 (100%) | 16 |
| 1.3.2 | 20 | 20 | NI | NI | 20/80; início pelos commits de 06/11 [confirmar]; critério falhou no SR1; sem reteste | 4,0 |
| 1.3.3 | 12 | 12 | NI | NI | 20/80; início NI; critério falhou no SR1 | NI |
| 1.3.4 | 12 | 12 | NI | NI | 20/80; início pelos commits de 06/11 [confirmar]; critério falhou no SR1; sem reteste | 2,4 |
| 1.3.5 | 16 | 14,90 (16 × 27 ÷ 29) | NI | NI | 20/80; sem início comprovado | NI |
| 1.3.6 | 8 | 5,33 (8 × 4 ÷ 6) | NI | NI | 20/80; sem início comprovado | NI |
| 1.4.1 | 10 | 10 | ~25,5 (Ronald 11,5 e Thiago 14) [confirmar] | NI | 20/80; início em 19/10; critério não verificado; CHG-06 sem decisão | 2,0 |
| 1.4.2 | 8 | 8 | NI | NI | 20/80; início em 19/10; critério não verificado | 1,6 |
| 1.4.3 | 8 | 8 | NI | NI | Sem código | NI |
| 1.4.4 | 6 | 6 | NI | NI | 20/80; início em 19/10; critério não verificado | 1,2 |
| 1.4.5 | 12 | 11,17 (12 × 27 ÷ 29) | NI | NI | Sem código | NI |
| 1.4.6 | 6 | 4,00 (6 × 4 ÷ 6) | NI | NI | Sem código | NI |
| 1.5.1 | 10 | 0 | ~10 (Rodrigo) [confirmar] | NI | 20/80; início em 06/11; critério não verificado | 2,0 |
| 1.5.2 | 12 | 0 | NI | NI | Futuro | NI |
| 1.5.3 | 8 | 0 | NI | NI | Futuro | NI |
| 1.6.1 | 8 | 0 | NI | NI | Futuro | NI |
| **Total** | **228** | **178,55** | **35,5 (parcial)** | NI |  | **29,2** (adotado) |

As horas gastas por pacote seguem o mapeamento da seção 5.1 e dependem de confirmação (Q-25). NI na coluna de VA significa sem crédito (0 h).

**Cenários de VA.**

| Cenário | VA | Critério | Uso |
| --- | --- | --- | --- |
| Estrito (SR3) | 16 h | Só 1.3.1, verificado no SR1 | Piso |
| **Adotado** | **29,2 h** | 16 h + 20% de 1.3.2, 1.3.4, 1.4.1, 1.4.2, 1.4.4 e 1.5.1 | Base dos índices desta versão |
| Teto | 35,6 h | Como o adotado, mas 1.4.2 aceito a 100% (8 h em vez de 1,6 h) | Só se o patrocinador aceitar PostgreSQL (CHG-06) e os erros do back-end forem corrigidos. 1.4.4 fica fora porque não tem UC12 |

### 7.2 Variações e índices

| Medida | Fórmula | Conta (VA 29,2 h) | Valor |
| --- | --- | --- | --- |
| VPr | VA − VP | 29,2 − 178,6 | −149,4 h |
| VC | VA − CR | 29,2 − 35,5 (ou 32,5) | −6,3 h (ou −3,3 h) |
| IDP | VA ÷ VP | 29,2 ÷ 178,6 | 0,16 |
| IDC | VA ÷ CR | 29,2 ÷ 35,5 (ou 32,5) | 0,82 (ou 0,90) |

**Leitura.** O IDP de 0,16 mostra, sobretudo, pacotes sem verificação: o VA só credita 20% de seis pacotes. Por isso ele não serve para prever prazo, que vem do caminho crítico e da capacidade (seção 6.2). O IDC abaixo de 1 é indicativo. O CR é parcial (3 de 7 integrantes, sem as 36 h planejadas da gerência) e o apontamento é tardio, o que infla o IDC e subestima o ENT. No cenário-teto (VA de 35,6 h) o IDC seria 1,00, com a mesma limitação do CR parcial.

**Previsão (ONT = 228 h; limite com contingência = 251 h).** Premissa declarada: o desvio de custo continua (ENT = ONT ÷ IDC), porque os pacotes críticos ainda não começaram e a causa do excesso (back-end real, CHG-06) pode se repetir na integração. Como limite inferior, vale a premissa de desvio pontual (ENT = CR + ONT − VA).

| CR | IDC | ENT = ONT ÷ IDC | EPT = ENT − CR | VNT = ONT − ENT | IDPT = (ONT − VA) ÷ (ONT − CR) | ENT pontual |
| --- | --- | --- | --- | --- | --- | --- |
| 32,5 h | 0,90 | 253,8 h | 221,3 h | −25,8 h | 1,02 | 231,3 h |
| 35,5 h | 0,82 | 277,2 h | 241,7 h | −49,2 h | 1,03 | 234,3 h |

O IDPT de 1,02 a 1,03 fica abaixo de 1,1, acima do qual o orçamento original raramente se sustenta. Então o ONT de 228 h ainda não está perdido, mas exige eficiência acima dos 0,82 a 0,90 atuais. Na premissa de desvio contínuo, o ENT passa dos 251 h em 2,8 h a 26,2 h; na premissa pontual, fica dentro. Enquanto o patrocinador não decidir CHG-06, a gerência trabalha com a faixa de 231 h a 277 h. **Uso da contingência de 23 h:** nenhum registro de uso e nenhuma aprovação do patrocinador localizada.

**Capacidade (R2).** Os desenvolvedores têm 192 h de esforço para 108 h de capacidade nominal (84 h acima). O CR dos desenvolvedores é de 35,5 h até a data de status. Para o que falta no caminho crítico, ver seção 6.2 (62 h contra 45,6 h).

### 7.3 Recursos

Planejado conforme o Plano, seção 7.6. Capacidade da linha de base: 4 h por semana por pessoa. De 16/11 a 17/11 restam 2 dias úteis (0,4 semana, 1,6 h por pessoa); de 16/11 a 11/12 restam 19 dias úteis (3,8 semanas, 15,2 h por pessoa), descontado o feriado de 20/11. É capacidade nominal; a disponibilidade real (provas, outras disciplinas) é NI.

| Pessoa | Disciplina | Planejado (h) | Apontado (h) | Capacidade nominal até 17/11 | Capacidade nominal até 11/12 |
| --- | --- | --- | --- | --- | --- |
| Ronald | PSW | 70,3 | 11,5 (6 + 5,5; pacote a confirmar) | 1,6 h | 15,2 h |
| Rodrigo | PSW | 57,3 | ~10 (sem divisão por semana) | 1,6 h | 15,2 h |
| Thiago | PSW | 64,3 | 14 (8 até 02/11, com 0 h em 26 a 30/10; 6 em 03 a 09/11) | 1,6 h | 15,2 h |
| Davi | GPTI | 9 | NI | 1,6 h | 15,2 h |
| João | GPTI | 9 | NI | 1,6 h | 15,2 h |
| Michael | GPTI | 9 | NI | 1,6 h | 15,2 h |
| Vinicius | GPTI | 9 | NI | 1,6 h | 15,2 h |
| **Total PSW** |  | 192 | 35,5 (parcial) | 4,8 h | 45,6 h |
| **Total GPTI** |  | 36 | NI | 6,4 h | 60,8 h |

**Referência, não previsão.** Das 192 h planejadas para os desenvolvedores, 156,5 h ainda não têm apontamento (192 − 35,5), contra 45,6 h de capacidade nominal até 11/12. A gerência tem 36 h planejadas e 60,8 h de capacidade nominal restante, mas nenhuma hora apontada. O esforço restante real continua NI.

## 8. Riscos

Registro do Plano (seção 12.2), atualizado. «Atingido» considera o gatilho do próprio Plano e a evidência do repositório.

| ID | Risco | Nível | Gatilho previsto | Gatilho atingido? | Resposta aplicada | Eficaz? |
| --- | --- | :-: | --- | --- | --- | --- |
| R1 | Layouts de CSV e leitor de extratos (1.3.5 e 1.4.5) | 9 alto | 27/10: leitor falha em mais de 1 das 3 amostras | **Sim** [confirmar]: sem commit do leitor; no SR1, CSV com colunas diferentes e PDF foram aceitos como «Analisado» com zero resultados | Mitigar (construir o leitor primeiro, 3 layouts): sem evidência de execução | Não |
| R2 | Capacidade: 192 h para 108 h | 9 alto | 13/10: mais de 4 h por semana por desenvolvedor | NI: horas por semana incompletas | Escalado ao patrocinador (D4) no SR1 e no SR2; sem decisão | Não |
| R3 | Ausência de integrante deixa módulo sem dono | 6 alto | Integrante indisponível por mais de 3 dias úteis | **Sim**: Thiago 0 h em 26 a 30/10; nenhum commit em 06 a 18/10 | Cobertura entre pares: sem evidência de aplicação | Não |
| R4 | Back-end real exigido tarde | 6 alto | D1 não decidida até 13/10 | **Sim e ocorreu**: back-end real construído sem decisão | Evitar (decidir D1): não decidida; o patrocinador decide na entrega final | Não |
| R5 | Dados financeiros pessoais | 3 médio | Dados reais em teste ou demonstração | NI | Extratos sintéticos (`teste.csv`) | NI |
| R6 | Pendências de escopo e mudança de requisitos | 6 alto | Pedido fora da EAP ou UC pendente após 13/10 | **Sim**: UC pendentes sem decisão e trabalho fora da EAP (seção 5.2) | Controle de mudanças: CHG sem decisão | Parcial |
| R7 | Integração tardia e incompatibilidades | 4 médio | Mudança de esquema após 12/10 ou atraso acima de 3 dias úteis | **Sim**: schema criado em 19/10 e ampliado em 11/11 (sessões e tokens de redefinição); `develop` e `main` em conflito | Integração frequente: sem evidência | Não |
| R8 | Falha de comunicação ou baixa participação | 4 médio | Duas reuniões semanais seguidas sem presença | **Sim**: nenhuma reunião semanal formal ocorreu; as reuniões por chat de 13 e 14/11 tiveram 4 dos 7 integrantes | Escalar: reunião de 16/11 e alerta ao patrocinador (seção 3.5) | Em andamento |
| R9 | Link de cancelamento inválido | 2 baixo | Link inválido em 1.5.2 | Ainda não (1.5.2 futuro) | — | — |
| O1 | Reaproveitamento de componentes de front-end | 4 médio | — | NI | — | NI |

**Novos riscos propostos**

| ID | Risco (causa → evento → consequência) | P | I | Nível | Resposta | Dono |
| --- | --- | :-: | :-: | :-: | --- | --- |
| R10 | Como o trabalho está em branches separadas, a `develop` e a `main` estão em conflito e os commits de 11/11 não foram para a `develop`, a entrega do Marco 2 pode não refletir o que foi feito | 3 | 3 | 9 alto | **Mitigar:** resolver o conflito, mesclar a branch de Ronald na `develop` e definir qual branch será a entrega (a ata de 13 e 14/11 decidiu testar a `feature/refresh-tokens-openapi-tests` e fazer o merge na `main` no final, apagando as demais; falta resolver o conflito com a `develop`) | Ronald e Thiago |
| R11 | Como os relatos de horas são tardios, sem pacote nem semana, e há atividades relatadas por duas pessoas, o CR e o VA podem ficar errados e o relatório perde confiabilidade | 3 | 2 | 6 alto | **Mitigar:** relato padronizado (pacote, semana, horas e link do commit) | Vinicius |

**Reserva de contingência (23 h):** uso registrado de 0 h. Nenhum risco teve aprovação do patrocinador para usar a reserva.

### 8.1 Limites para ação (Plano, seção 13.2)

O Plano manda abrir registro de mudança e avisar o patrocinador quando um destes limites for ultrapassado.

| Limite | Medida em 15/11 | Atingido? | Consequência exigida |
| --- | --- | :-: | --- |
| Atraso acima de 3 dias úteis no caminho crítico | 1.3.5 e 1.4.5: ~27 dias úteis de desvio pelo VP, sem commit. 1.3.6 e 1.4.6: 4 dias úteis, sem commit (seção 6.2) | **Sim** | Registro de mudança e aviso ao patrocinador |
| Estouro acima de 10% das horas de um pacote | 1.4.1: ~25,5 h contra 10 h (255%) [confirmar o mapeamento]; os demais pacotes têm horas NI | **Sim** [confirmar] | Registro de mudança e aviso ao patrocinador |
| Qualquer uso de contingência | 0 h usadas | Não | Não se aplica |

A previsão de custo (ENT de 231 h a 277 h, contra 251 h com contingência) não é um limite do Plano, mas indica que a contingência pode não bastar na premissa de desvio contínuo (seção 7.2). Este relatório é o aviso ao patrocinador. O registro de mudança ainda não foi aberto no GitHub (ação 11 da seção 12).

### 8.2 Ponto de decisão 2 do Plano (seção 12.3), vencido em 27/10

O gatilho do R1 foi atingido (seção 8, tabela de riscos): o leitor de CSV não existe. O Plano prevê que o patrocinador decida entre:

| Opção | Efeito |
| --- | --- |
| (a) Consumir a contingência do R1 | Até 8 h da reserva (Plano, R1); não cria o leitor sozinha |
| (b) Reduzir 1.3.5 e 1.4.5 ao que for possível com um único layout e registrar o restante como evolução futura | Reduz o escopo de pacotes de 16 h e 12 h; o Plano (seção 14.2) só admite reduzir a importação depois de esgotadas as outras opções |
| (c) Replanejar a data de entrega | Altera o Marco 3 (11/12), que depende do patrocinador (Termo de Abertura) |

A decisão está pedida na seção 11. Até agora não houve decisão nem pedido formal.

### 8.3 Critérios de encerramento antecipado ou com escopo reduzido (Plano, seção 14.2)

O Plano manda consultar o patrocinador se algum destes critérios se confirmar.

| Critério | Situação em 15/11 |
| --- | --- |
| R2 se confirma e nenhuma das opções (a) a (d) é viável | Não avaliável: as opções foram escaladas (D4) e não houve decisão |
| R1 se concretiza e a contingência acaba sem que o conciliador funcione | **Em risco:** gatilho atingido e sem leitor; a contingência está intacta (23 h) |
| Perda de integrantes que a cobertura entre pares não absorve | Sem saída formal; a gerência está sem commit e sem horas (Q-24) e Rodrigo, dono do caminho crítico, tem 1 commit desde 07/10 |
| A entrega de 11/12 não pode mais ser cumprida | **Em risco:** nenhum commit nos pacotes do caminho crítico; a avaliação é do patrocinador (seção 11) |

A gerência recomenda a consulta ao patrocinador. Não declara o encerramento antecipado.

## 9. Mudanças e decisões de escopo

Pelo Plano (seção 13.3), cada pedido de mudança descreve o impacto em escopo, prazo e esforço. As colunas abaixo trazem o que se sabe; onde não há estimativa, está NI. Nenhuma das mudanças tem registro no GitHub (ação 11 da seção 12).

| ID | Mudança | Escopo | Prazo | Esforço e custo | Situação em 15/11 |
| --- | --- | --- | --- | --- | --- |
| CHG-01 | Reduzir 1.3.3 (UC05, UC07, UC08) | Remove cadastro, edição e exclusão de serviço de 1.3.3; pode afetar 1.4.3 | 1.3.3 e 1.4.3 estão fora do caminho crítico | Teto de 12 h (1.3.3); 1.4.3 (8 h) pode ser afetado; redução não estimada | Sem decisão |
| CHG-02 | Reduzir 1.3.5 (UC15, UC16) | Remove histórico de arquivos e descarte persistente | Caminho crítico: reduz o trabalho de 1.3.5 | Teto de 16 h (1.3.5); 1.4.5 (12 h) pode ser afetado; redução não estimada | Sem decisão |
| CHG-03 | UC12: exclusão real do teto ou definir zero | 1.3.4 e 1.4.4; sem rota DELETE na API | Fora do caminho crítico | NI | Sem decisão |
| CHG-04 | Ação «Confirmar Pagamento», fora da EAP | Já implementada no front-end | Sem efeito | NI; horas já gastas | Sem decisão |
| CHG-05 | Telas «Criar Conta» e «Esqueceu a senha?» | Já implementadas; agora ligadas ao back-end real | Sem efeito direto | Parte das ~35,5 h de CR; só 20% de VA (regra do SR2) | Sem decisão; agora ligadas ao back-end real |
| CHG-06 | Back-end real (Express, Prisma e PostgreSQL), no lugar do json-server | **Ampliada:** inclui refresh token, recuperação de senha por e-mail, perfil, Swagger e Docker; refaz 1.4.x e 1.5.1 sobre outro back-end | 1.4.1 começou 13 dias corridos depois do planejado; `develop` e `main` em conflito (Q-21) | ~25,5 h em 1.4.1 (255% de 10 h) e ~10 h em 1.5.1 [confirmar]; as ~35,5 h entram no CR, com VA de 20% pela regra do SR2; esforço novo de 1.4.x e 1.5.1 NI | Sem decisão |

**Efeito do adiamento.** O patrocinador informou que decidirá na entrega final. Até lá vale a linha de base original (json-server). Se ele mantiver o json-server, as ~35,5 h e o retrabalho ficam sem valor agregado. A gerência registra esse risco como aceito, dentro de R4, e pede a confirmação por escrito no Teams.

## 10. Questões

### 10.1 Itens herdados do SR1 e do SR2

Situação em 15/11 por **leitura do código da `develop`**, que não substitui um reteste em execução. O reteste é a ação 4 da seção 12. Todos os prazos originais já venceram; a última coluna traz um novo prazo **proposto pela gerência, a confirmar pelo grupo**. Os itens que dependem de decisão do patrocinador seguem a decisão.

| ID | Resumo | Dono | Prazo original | Situação em 15/11 | Novo prazo (proposto) |
| --- | --- | --- | --- | --- | --- |
| Q-01 | Cobrança vencida exibida como «Em -N dias» | Ronald | 19/10 | **Aberta.** `Dashboard.tsx` sem alteração desde 02/10; o texto «Em N dias» ainda é gerado para dias negativos | 24/11 |
| Q-02 | Link externo de cancelamento e uso só com teclado não demonstrados | Gerência | 16/10 | Aberta; sem reteste | 19/11 (junto da ação 4) |
| Q-03 | Sem cadastro, edição e exclusão de serviço | Thiago | 19/10 | **Aberta.** Catálogo continua fixo (`constants/catalog.ts`) e não há tela de serviços | Depende de CHG-01; sem decisão, 24/11 |
| Q-04 | Sem perfil Administrador | Ronald | 19/10 | **Aberta.** Nenhum perfil de administrador no front-end nem no schema | Depende de D3; sem decisão, 24/11 |
| Q-05 | Sem exclusão de teto | Equipe (a nomear) | 19/10 | **Aberta.** Sem exclusão no front-end e sem rota DELETE de orçamentos na API | Depende de CHG-03 e D5; 24/11 |
| Q-06 | Sem histórico de importações nem descarte persistente | Rodrigo | 19/10 | **Aberta.** Nenhum código nem tabela para isso | Depende de CHG-02; 24/11 |
| Q-07 | Importação aceita CSV incompatível; arquivo vazio sem mensagem | Rodrigo | 19/10 | **Aberta.** A leitura continua dividindo por vírgula, sem validar o cabeçalho; só há `accept=".csv"` no campo de arquivo | Com 1.3.5; 24/11 |
| Q-08 | Reimportação repete entradas no histórico de pagamentos | Rodrigo | 19/10 | Aberta; sem reteste | Com 1.3.5; 24/11 |
| Q-09 | `teste.csv` com 9 lançamentos; limiares não medidos | Rodrigo | 16/10 | **Aberta.** `teste.csv` inalterado (9 linhas) | 18/11 |
| Q-10 | Sem tutorial dentro do aplicativo | Ronald e Thiago | 19/10 | **Aberta.** Nenhum tutorial no código | Com 1.3.6; 24/11 |
| Q-11 | Conta nova sem mensagem de lista vazia | Ronald | 19/10 | **Aberta.** Nenhuma mensagem de lista vazia no Painel nem no Relatório | 24/11 |
| Q-12 | F5 em tela interna volta ao painel | Ronald | 19/10 | **Aberta.** As telas continuam sob `/painel` em `App.tsx` | 24/11 |
| Q-13 | PSW não informou commit ou tag de congelamento | PSW (a nomear) | 16/10 | **Aberta.** O repositório não tem tags | 17/11 (tag do Marco 2, depois do merge da ação 2) |
| Q-14 | Responsáveis por pacote não confirmados | PSW (a nomear) | 16/10 | Aberta; os commits mostram Ronald, Thiago e Rodrigo ativos, mas sem confirmação formal | 16/11 (reunião) |
| Q-15 | Formalizar Marco 1 e Marco 2 | Gerência | 16/10 | Aberta; sem decisão do patrocinador | 16/11 (junto da confirmação por escrito) |
| Q-16 | Pessoas sem hora apontada | Gerência | 04/11 | **Parcial.** Rodrigo enviou relato (~10 h) e Thiago enviou 6 h de 03 a 09/11 (ata). Faltam os 4 da gerência, as semanas de 07 a 16/10 e as de Thiago depois de 09/11 | 18/11 |
| Q-17 | Relato de 1.4.1 depois do fim planejado | PSW (Rodrigo) | 04/11 | **Atualizada.** 1.4.1 começou em 19/10 (commits c2ce5af e ede571b); fim real NI; critério não verificado | 18/11 |
| Q-18 | 10 de 11 pacotes sem critério verificado; folga em uso | Gerência com a PSW | 09/11 | **Aberta.** A folga até 10/11 foi consumida sem verificação | 19/11 (junto da ação 4) |

### 10.2 Ações do SR2: o que foi feito

| Ação do SR2 | Prazo | Situação em 15/11 |
| --- | --- | --- |
| Registrar, por pessoa, a semana em que a medição começou | 03/11 | Sem evidência |
| Coletar as horas dos 4 da gerência | 03/11 | Sem evidência; horas NI |
| Confirmar com Ronald e Thiago o pacote das 14 h | 03/11 | Parcial: mapeamento deduzido dos commits (seção 5.1), aguardando confirmação (Q-25) |
| Coletar horas de Rodrigo e as semanas de 07 a 16/10 | 04/11 | Parcial: Rodrigo enviou relato sem divisão por semana; 07 a 16/10 segue NI |
| Coletar datas reais, duração e esforço restante, com commits como evidência | 04/11 | Parcial: datas reais de 1.4.1 e 1.5.1 conforme os commits; o restante NI |
| Nomear o responsável por 1.3.4 e 1.4.4 (D5) | 04/11 | Sem evidência |
| Recalcular VP, VA, CR e índices e reenviar o relatório | 05/11 | Parcial: esta versão recalcula VP, VA, CR e índices (seção 7), com CR parcial; falta o reteste |
| Decidir CHG-01 a CHG-06 e a definição do Marco 2 | 06/11 | **Sem decisão;** adiada para a entrega final |
| Verificar o critério dos pacotes relatados como concluídos | 09/11 | Sem evidência |
| Corrigir as questões abertas antes de 10/11 | 10/11 | Não: as questões Q-01 a Q-12 seguem abertas (seção 10.1) |

### 10.3 Novas questões

Data de registro: 15/11/2026. Prazos propostos pela gerência; o grupo confirma.

| ID | Questão | Pacote | Dono (proposta) | Prazo (proposto) | Impacto em escopo, prazo e custo |
| --- | --- | --- | --- | --- | --- |
| Q-19 | Horas de 19/10 relatadas por Thiago (3 h) coincidem com commits da conta de Ronald; confirmar autoria e evitar dupla contagem | 1.4.1 | Ronald e Thiago | 18/11 | Escopo: sem impacto. Prazo: sem impacto. Custo: o CR pode cair de 35,5 h para 32,5 h |
| Q-20 | Branch `feature/refresh-tokens-openapi-tests` fora da `develop` | 1.4.1 e 1.4.2 | Ronald | 17/11 | Escopo: testes e refresh token ficam fora da entrega. Prazo: risco para o Marco 2 (R10). Custo: ~5,5 h de 11/11 sem VA |
| Q-21 | Conflito entre `develop` e `main`; a `main` tem 4 commits de documentação que a `develop` não tem | Todos | Thiago | 17/11 | Escopo: todos os pacotes. Prazo: bloqueia a integração (R7 e R10). Custo: NI |
| Q-22 | README da `develop` desatualizado (json-server; back-end «não ligado») | Documentação | Rodrigo | 18/11 | Escopo: documentação. Prazo: sem impacto. Custo: NI |
| Q-23 | 1.3.5 e 1.4.5 (caminho crítico) sem commit, a 2 dias úteis do Marco 2 | 1.3.5 e 1.4.5 | Rodrigo | 16/11 | Escopo: critério dos dois pacotes não atendido. Prazo: Marco 2 e entrega de 11/12 em risco. Custo: 28 h planejadas (16 + 12) sem VA |
| Q-24 | Gerência sem horas apontadas e sem commits depois de 19/10 | 1.1.2 | João | 16/11 | Escopo: 1.1.2 sem evidência. Prazo: revisão semanal do cronograma não ocorreu. Custo: 36 h planejadas sem apontamento |
| Q-25 | Mapeamento dos relatos aos pacotes da EAP (seção 5.1) | Todos | Gerência | 16/11 | Escopo: sem impacto. Prazo: sem impacto. Custo: define onde as 35,5 h entram no CR e no VA |
| Q-26 | Erros pontuais do back-end citados no relatório de testes, sem descrição nem situação (corrigido ou não) | 1.4.1, 1.4.2 e 1.4.4 | Ronald e Thiago | 18/11 | Escopo: define se 1.4.2 pode ser aceito. Prazo: sem estimativa. Custo: horas de correção NI |
| Q-27 | Erros do front-end em correção, sem lista nem responsável; testes finais de integração pendentes | 1.3.2, 1.3.4 e 1.5.1 | Rodrigo [confirmar] | 18/11 | Escopo: define o reteste da ação 4. Prazo: sem estimativa. Custo: NI |
| Q-28 | Confirmar os comandos exatos para executar a aplicação (seção 13), pedidos pela ata | Documentação | Ronald (back-end) e Rodrigo (front-end e README) | 18/11 | Escopo: documentação. Prazo: sem impacto. Custo: NI |

## 11. Decisões pedidas ao patrocinador

D1 a D5 vêm do Plano (seções 10 e 12.3): D1 back-end real, D2 OFX, D3 casos de uso pendentes, D4 carga dos desenvolvedores e D5 responsável pelos Tetos. As opções de D2 são proposta da gerência.

| # | Decisão | Opções | Efeito em horas e prazo |
| --- | --- | --- | --- |
| 1 | Confirmar por escrito que CHG-01 a CHG-06 e D1 a D5 serão decididas na entrega final | (a) Confirmar; (b) decidir antes do Marco 2 | (a) as horas de back-end real ficam sem VA até a decisão e o risco R4 é aceito; (b) o esforço de 1.4.x e 1.5.1 é recalculado |
| 2 | D1 e CHG-06: back-end real | (a) Aprovar, com nova linha de base para 1.4.x e 1.5.1; (b) manter o json-server | (a) as ~35,5 h passam a gerar VA se o critério for verificado, e o esforço de 1.4.x e 1.5.1 muda, sem estimativa; (b) as ~35,5 h ficam como CR sem VA (o VC de −6,3 h piora) e o retrabalho de voltar ao json-server não foi estimado |
| 3 | D2: OFX | (a) Manter fora do escopo, só CSV (RQ08); (b) incluir | (a) sem horas; (b) esforço NI, em pacotes do caminho crítico (1.3.5 e 1.4.5) |
| 4 | D3, CHG-01 e CHG-02: casos de uso pendentes (UC05, UC07, UC08, UC15, UC16) | Aprovar a redução ou manter o critério original e pedir a conclusão | Teto de 12 h em 1.3.3 e de 16 h em 1.3.5; 1.4.3 (8 h) e 1.4.5 (12 h) podem ser afetados; a redução não foi estimada |
| 5 | CHG-03, CHG-04 e CHG-05 (UC12, Confirmar Pagamento, Criar Conta e Esqueceu a senha) | Aprovar cada uma ou manter o critério original | NI; esforço não estimado |
| 6 | D4 e R2: carga dos desenvolvedores. Base do Plano e do SR2: 192 h de esforço contra 108 h de capacidade, 84 h acima; não recalculada | (a) Aumentar as horas dos desenvolvedores; (b) realocar esforço à gerência; (c) cortar escopo; (d) rever a data; (e) usar a contingência | (a) +84 h no total, +28 h por desenvolvedor, de 4 para cerca de 7,1 h por semana em 9 semanas; (b) 84 h passam para a gerência, que iria de 36 h para 120 h de esforço, dentro de 144 h de capacidade; (c) cortar 84 h de pacotes dos desenvolvedores, a escolher; (d) sem mudar as horas, cerca de 7 semanas além de 11/12, e a data final é fixa no Plano; (e) até 23 h, só com risco nomeado que tenha ocorrido e ciência do patrocinador. O efeito sobre as horas restantes reais é NI. Com os números desta versão, o caminho crítico tem 62 h contra 45,6 h de capacidade (faltam 16,4 h); (a) pede cerca de 5,4 h por semana por desenvolvedor, e 7,2 h se 1.3.3 e 1.4.3 forem mantidos |
| 7 | D5: responsável pelos Tetos (1.3.4 e 1.4.4) | Nomear uma pessoa | Sem horas novas; define o dono de 18 h planejadas (12 + 6) |
| 8 | Ponto de decisão 2 e prioridade de 1.3.5 e 1.4.5 (R1) | (a) Consumir a contingência do R1; (b) reduzir ao que for possível com um único layout; (c) replanejar a data (seção 8.2) | (a) até 8 h; (b) tira escopo de pacotes de 16 h e 12 h; (c) altera o Marco 3. Define se o Marco 2 é cumprido |
| 9 | Consulta de encerramento antecipado ou com escopo reduzido (Plano, 14.2) | Avaliar os critérios em risco da seção 8.3 | Define se a entrega de 11/12 é mantida |
| 10 | Definição do Marco 2 (Q-15) | (a) Plano: 17/11, front-end e API; (b) SR1: Marco 2 = API própria | (a) 134 h planejadas em 1.3.x e 1.4.x; (b) 50 h em 1.4.x |

### 11.1 Alavancas com a data fixa (efeito em horas)

A data de 11/12 é fixa no Plano. Para fechar o déficit de 16,4 h (ou 36,4 h, se 1.3.3 e 1.4.3 forem mantidos), cada alavanca troca tempo por outra coisa e vai ao patrocinador antes de ser usada.

| Alavanca | Efeito em horas | Custo ou risco |
| --- | --- | --- |
| Escopo: CHG-01 (1.3.3 e 1.4.3) | Até −20 h, fora do caminho crítico | Remove UC05, UC07 e UC08. Só reduz o déficit de 36,4 h para 16,4 h |
| Escopo: CHG-02 e ponto de decisão 2(b) (1.3.5 e 1.4.5) | Teto de −28 h; a redução real é NI | Atinge o RQ02, de prioridade máxima, e o caminho crítico |
| Compressão: mais horas dos desenvolvedores (D4, opção a) | +16,4 h, ou cerca de +1,4 h por semana por desenvolvedor (de 4 para 5,4 h); +3,2 h por semana se 1.3.3 e 1.4.3 forem mantidos | Depende da disponibilidade real, que é NI (provas e outras disciplinas) |
| Realocação à gerência (D4, opção b) | Até 84 h pelo Plano; a gerência tem 60,8 h de capacidade nominal restante e nenhuma hora apontada | Só vale para trabalho que não é código |
| Reserva: contingência do R1 | Até 8 h | Paga horas extras, mas não cria capacidade. Exige risco ocorrido (o R1 ocorreu) e ciência do patrocinador |
| Data (ponto de decisão 2c) | Move o Marco 3 de 11/12 | Depende do patrocinador (Termo de Abertura) |

## 12. Próximas ações

Prazos propostos pela gerência; o grupo confirma. As ações 12 a 17 foram acrescentadas na versão anterior para consolidar o plano da seção 3.5 e os limites do Plano. As ações 18 a 21 vêm da ata e do relatório de testes (revisão de 16/11).

| # | Ação | Responsável | Prazo |
| --- | --- | --- | --- |
| 1 | Reunião de acompanhamento no Teams, com ata e rodada de participação; preencher os níveis atuais da matriz (seção 3.1) e o esforço restante por pacote (aba «Entregas Marco 2» da pauta) | João | 16/11 |
| 2 | Resolver o conflito `develop` × `main` e mesclar a branch de refresh token na `develop` | Thiago e Ronald | 17/11 |
| 3 | Rodrigo informa se consegue iniciar 1.3.5 e 1.4.5 (leitor de CSV com 3 layouts), com apoio de Ronald e Thiago. Sem início até 16/11, a gerência pede a decisão formal de corte ou replanejamento (ponto de decisão 2, seção 8.2) | Rodrigo, com apoio de Ronald e Thiago; Davi (pedido ao patrocinador) | 16/11 |
| 4 | Retestar 1.3.2 a 1.3.6 com o software integrado à API e registrar o resultado | Gerência | 19/11 |
| 5 | Coletar horas por pacote e por semana de todos, com link de commit, no canal do projeto | Vinicius | 18/11 |
| 6 | Confirmar o mapeamento de pacotes (seção 5.1) e resolver a possível dupla contagem de 19/10 | Gerência, Ronald e Thiago | 16/11 |
| 7 | Anexar ao relatório os prints das mensagens do Teams (a ata de 13 e 14/11 já está incorporada, seção 4.4) | João | 17/11 |
| 8 | Pedir ao patrocinador a confirmação por escrito de que as decisões ficam para a entrega final, enviando a tabela da seção 11 e o aviso dos limites da seção 8.1 | Davi | 16/11 |
| 9 | Nomear o responsável por 1.3.4 e 1.4.4 (D5) | PSW | 16/11 |
| 10 | Atualizar o README da `develop`, incluindo como executar a aplicação, principalmente o back-end (seção 13 e Q-28) | Rodrigo, com Ronald no back-end | 18/11 |
| 11 | Abrir no GitHub o registro de cada mudança (CHG-01 a CHG-06) com o impacto da seção 9, e o registro dos limites ultrapassados (seção 8.1) | Davi | 18/11 |
| 12 | Definir o roteiro e quem conduz a demonstração do Marco 2 (seção 6.3) | Ronald | 16/11 |
| 13 | Conversa individual com quem não comparecer ou não responder (Rodrigo e a gerência, em primeiro lugar) | Davi | 18/11 |
| 14 | Cobertura entre pares para 1.3.5 e 1.4.5 (R3), se Rodrigo não confirmar disponibilidade | João, com Ronald e Thiago | 16/11 |
| 15 | Alerta formal ao patrocinador por R8, se não houver retorno até o prazo | Davi | 19/11 |
| 16 | Registrar, por pessoa, a semana em que a medição começou (seção 4.2.1) e coletar as horas dos 4 da gerência | Vinicius | 18/11 |
| 17 | Recalcular VP, VA, CR e índices depois do reteste e reenviar este relatório, com esforço restante e datas reais | Gerência | 20/11 |
| 18 | Detalhar os erros pontuais do back-end e dizer se já foram corrigidos (Q-26) | Ronald e Thiago | 18/11 |
| 19 | Concluir as correções do front-end e listar os erros corrigidos (Q-27) | Rodrigo [confirmar] | 18/11 |
| 20 | Realizar os testes finais das APIs de assinatura e os testes finais de integração entre front-end e back-end (ata) | Equipe de desenvolvimento | 19/11 |
| 21 | Fazer o merge das branches na `main` e apagar as demais, depois de resolver o conflito com a `develop` (ata e ação 2) | Thiago e Ronald | Ao final, antes do Marco 3 (11/12) |

## 13. Como executar a aplicação

A ata pede que o relatório explique como rodar a aplicação, principalmente o back-end. Os passos abaixo vêm do relatório de testes, da ata e dos relatos. Os comandos exatos não constam nos documentos recebidos e estão marcados [confirmar] até que Ronald (back-end) e Rodrigo (front-end) os validem (Q-28).

| # | Passo | O que fazer | Fonte |
| --- | --- | --- | --- |
| 1 | Branch | Usar `feature/refresh-tokens-openapi-tests`, a branch definida para teste | Ata |
| 2 | Banco de dados | Subir o PostgreSQL no Docker, na porta 5433, para evitar conflito com instalações locais [comando a confirmar] | Relatório de testes e ata |
| 3 | Migrações | Aplicar as migrações do Prisma [comando a confirmar] | Relatório de testes |
| 4 | Seed | Carregar o usuário de teste [comando e credenciais a confirmar] | Relatório de testes |
| 5 | API | Iniciar a API Express com TypeScript. O front-end usa a porta 3001 [comando e variáveis de ambiente a confirmar, como as da recuperação de senha por e-mail] | Relato de Rodrigo |
| 6 | Documentação da API | Abrir o Swagger em `/api-docs` | Relatório de testes |
| 7 | Testes | Executar `npm test` (login, renovação e rotação de sessão, logout, rotas protegidas e isolamento das assinaturas entre usuários) | Relatório de testes |
| 8 | Front-end | Iniciar o front-end em React com Vite, apontando para a API [comando a confirmar] | Plano, seção 2 |

---
