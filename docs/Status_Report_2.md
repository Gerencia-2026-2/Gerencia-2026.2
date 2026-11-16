# Status Report 2 — SubTracker

Marco 2 contra a linha de base da AV1 · Grupo de gerência (GPTI): Davi Luiz Rodrigues da Conceição, João Henrique Lima Gualberto, Michael Patrick Ferreira da Silva Borba e Vinicius da Silva Mendes

**Como ler este relatório.** NI significa «não informado»: o dado não foi fornecido ao grupo até a data de status. Nenhum valor foi estimado. Onde falta dado, o índice não foi calculado e a fórmula aparece com os números que já existem. A linha de base vem do Plano do Projeto v3.0, da EAP e do Dicionário (AV1). O escopo anterior vem do Status Report 1 (SR1). A ferramenta de IA ajudou a montar as tabelas e revisar as fórmulas; a regra de crédito, a leitura dos índices e as decisões pedidas são do grupo.

## 1. Data de status e período coberto

| Item | Conteúdo |
| --- | --- |
| Data de status | 02/11/2026 |
| Período coberto | 07/10/2026 (dia seguinte ao corte do SR1) a 02/11/2026 |
| Início da medição de horas | NI. O SR1 previa o início do apontamento até 16/10/2026; os relatos recebidos (Ronald e Thiago) começam na semana de 19 a 23/10; de 07 a 16/10 não há relato (NI) |
| Semanas reconstituídas | Os relatos de Ronald e de Thiago trazem horas aproximadas e chegaram depois das semanas relatadas (o de Thiago em 02/11); por isso são tratados como reconstituídos. O grupo confirma |
| Horas recebidas | 2 relatos: Ronald, cerca de 6 h (19 a 23/10), e Thiago, cerca de 8 h (19/10: 3 h; 23/10: 2 h; 26 a 30/10: 0 h, sem atividade registrada; 02/11: 3 h). Rodrigo e a gerência ainda não enviaram |
| Linha de base | Plano v3.0 (AV1). Mudança aprovada pelo patrocinador desde a AV1: NI. Enquanto não houver aprovação, vale o plano original |
| Marco 2 | 17/11/2026, conforme o Plano (pacotes 1.2.2, 1.3.1 a 1.3.6 e 1.4.1 a 1.4.6). A separação Marco 1 (front-end) e Marco 2 (API própria) proposta no SR1 (Q-15) não foi formalizada; este relatório usa o Plano. Entre 03/11 e 17/11 restam 11 dias úteis (descontados os feriados de 02/11 e 20/11) |
| Taxa de valoração | R$ 10,00 por hora, igual para todos (Plano, seção 7.1); por isso índices em horas e em R$ coincidem |

## 2. Situação geral de escopo, prazo e custo

| Dimensão | Cor | Número | Justificativa |
| --- | --- | --- | --- |
| Escopo | **VERMELHO** | 1 de 6 pacotes de front-end com critério verificado (SR1) | Cinco pacotes falharam no SR1 e o software não mudou desde o SR1 (informado pelo grupo), então o resultado se mantém. Seguem pendentes UC05, UC07, UC08, UC12, UC15, UC16 e o tutorial |
| Prazo | Não determinada | VA comprovado: 16 h de VP 158,2 h | IDP não calculado: o VA conhecido é só o mínimo comprovado e as datas reais são NI. Pela linha de base, 11 pacotes (136 h) já deveriam estar concluídos e só 1 (1.3.1, 16 h) tem critério verificado |
| Custo | Não determinada | CR parcial: 14 h de 2 pessoas entre 7 | IDC não calculado: com 2 de 7 integrantes apontados, o índice refletiria falta de apontamento e não o custo do projeto |

## 3. As três perguntas do relatório

1. **O caminho crítico ainda entrega o Marco 2 em 17/11?** Não é possível responder. As datas reais e a duração restante de 1.3.5 e 1.4.5, que estão no caminho crítico, são NI. Data planejada: 17/11/2026.
2. **O valor agregado mostra trabalho feito no ritmo e no custo planejados?** Não é possível responder com índice. O VP é 158,2 h; o VA comprovado é 16 h (só 1.3.1) e o CR conhecido é 14 h. Os dois últimos são incompletos, então IDP e IDC não foram calculados.
3. **As horas que faltam cabem na capacidade que resta até o Marco 2?** Não é possível responder: o esforço restante por atividade é NI. Referências: a capacidade nominal restante é de cerca de 26,4 h para a PSW (seção 10); na linha de base, os pacotes do Marco 2 em 1.3.x e 1.4.x somam 134 h.

## 4. Escopo desde o Status Report 1

| Pacote | Resultado no SR1 (corte 06/10) | Desde então |
| --- | --- | --- |
| 1.3.1 Estrutura de front-end e rotas | Passou | Sem mudança. Aceite formal do patrocinador: NI |
| 1.3.2 Assinaturas e dashboard | Falhou | Software inalterado desde o SR1; continua Falhou |
| 1.3.3 Serviços e cancelamento | Falhou | Software inalterado desde o SR1; continua Falhou |
| 1.3.4 Tetos e consumo orçamentário | Falhou | Software inalterado desde o SR1; continua Falhou |
| 1.3.5 Extratos, histórico e conciliação | Falhou | Software inalterado desde o SR1; continua Falhou |
| 1.3.6 Relatório e tutorial | Falhou | Software inalterado desde o SR1; continua Falhou |
| 1.4.1 Estrutura da API e modelagem do banco | Não verificado no SR1 | Relato de Ronald, com o código no repositório da PSW (informado pelo grupo): base da API com Express, Prisma e PostgreSQL, autenticação JWT, validação com Zod e isolamento de dados por usuário, cerca de 6 h em 19 a 23/10. Relato de Thiago, também sobre a base do back-end: 19/10, cerca de 3 h (configuração inicial, dependências, migration inicial do banco e seed do Prisma); 23/10, cerca de 2 h (integração da versão final da base na branch `develop`, com Docker, schema do Prisma e documentação). Critério do Dicionário não verificado |
| 1.4.2 a 1.4.6 | Não verificados no SR1 | NI |
| 1.1.1, 1.1.2, 1.2.1, 1.2.2 | Fora do SR1 | NI |

**Verificados:** 1.3.1 (SR1). **Pendentes:** UC05, UC07, UC08, UC12, UC15, UC16 e tutorial (SR1); sem correção, porque o software não mudou desde o SR1. **Não demonstrados:** abertura da página externa do link de cancelamento e uso do fluxo principal só com teclado (SR1, Q-02); software inalterado, sem novo teste.

## 5. Cronograma

★ = caminho crítico. NI = não informado. Datas planejadas da linha de base (Plano, seção 5.2).

| ID | Atividade | Responsável | Início plan. | Fim plan. | Início real | Fim real | Duração restante | Situação |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1.1.1 | Documentação e acompanhamento | Gerência | 03/10 | 05/10 | NI | NI | NI | NI (fim planejado já passou) |
| 1.1.2 | Monitoramento, riscos e comunicação | Gerência | 05/10 | 11/12 | NI | NI | NI | Em andamento pelo plano; real NI |
| 1.2.1 | Levantamento e rastreabilidade | Ronald, Rodrigo, Thiago | 03/10 | 05/10 | NI | NI | NI | NI (fim planejado já passou) |
| 1.2.2 | Prototipagem e matrizes | Ronald, Rodrigo, Thiago | 03/10 | 10/10 | NI | NI | NI | NI (fim planejado já passou) |
| 1.3.1 | Estrutura de front-end e rotas | Ronald | 06/10 | 12/10 | NI | NI | 0 | Concluída; critério verificado no SR1 |
| 1.3.2 | Assinaturas e dashboard | Ronald | 06/10 | 31/10 | NI | NI | NI | Critério falhou no SR1; software inalterado |
| 1.3.3 | Serviços e cancelamento | Thiago | 12/10 | 31/10 | NI | NI | NI | Critério falhou no SR1; software inalterado |
| 1.3.4 | Tetos e consumo orçamentário | Equipe de desenvolvimento\* | 12/10 | 31/10 | NI | NI | NI | Critério falhou no SR1; software inalterado |
| 1.3.5 ★ | Extratos, histórico e conciliação | Rodrigo | 06/10 | 17/11 | NI | NI | NI | Em andamento pelo plano; falhou no SR1; software inalterado |
| 1.3.6 ★ | Relatório e tutorial | Ronald e Thiago | 10/11 | 17/11 | NI | NI | NI | Início planejado 10/11 (futuro); falhou no SR1 |
| 1.4.1 | Estrutura da API e modelagem do banco | Rodrigo | 06/10 | 12/10 | NI | NI | NI | NI; fim planejado já passou; ver Q-17 |
| 1.4.2 | API de Assinaturas | Ronald | 12/10 | 31/10 | NI | NI | NI | NI (fim planejado já passou) |
| 1.4.3 | API de Serviços | Thiago | 12/10 | 31/10 | NI | NI | NI | NI (fim planejado já passou) |
| 1.4.4 | API de Tetos | Equipe de desenvolvimento\* | 12/10 | 31/10 | NI | NI | NI | NI (fim planejado já passou) |
| 1.4.5 ★ | Importação de extratos e conciliação | Rodrigo | 06/10 | 17/11 | NI | NI | NI | Em andamento pelo plano; real NI |
| 1.4.6 ★ | Relatório, projeção e acesso | Ronald e Thiago | 10/11 | 17/11 | NI | NI | NI | Início planejado 10/11 (futuro) |
| 1.5.1 ★ | Integração front-end/back-end | Ronald, Rodrigo, Thiago | 18/11 | 24/11 | NI | NI | NI | Início planejado 18/11 (futuro) |
| 1.5.2 ★ | Testes de validação funcional | Ronald, Rodrigo, Thiago | 25/11 | 03/12 | NI | NI | NI | Início planejado 25/11 (futuro) |
| 1.5.3 ★ | Ajustes e validação final | Ronald, Rodrigo, Thiago | 04/12 | 11/12 | NI | NI | NI | Início planejado 04/12 (futuro) |
| 1.6.1 ★ | Documentação final e entrega | Gerência | 07/12 | 11/12 | NI | NI | NI | Início planejado 07/12 (futuro) |

\*O Dicionário não nomeia a pessoa; a decisão D5 do Plano (responsável pelos Tetos) segue sem resposta.

**Leitura.** Pela linha de base, 11 pacotes (136 h) tinham término planejado até 02/11. Só 1 (1.3.1, 16 h) tem critério verificado; os outros 10 (120 h) estão sem verificação (Q-18).

## 6. Caminho crítico e data prevista do Marco 2

- **Caminho crítico da linha de base (Plano, seção 5.3):** 1.3.5 e 1.4.5 (06/10 a 17/11), depois 1.3.6 e 1.4.6 (término em 17/11), depois 1.5.1, 1.5.2, 1.5.3 e 1.6.1 (entrega final em 11/12).
- **Caminho crítico atualizado:** NI. Depende das datas reais e da duração restante de 1.3.5 e 1.4.5.
- **Data prevista do Marco 2:** NI. A data vem do caminho crítico, não do IDP. Data planejada: 17/11/2026, com 11 dias úteis restantes a partir de 03/11.
- **Folga:** 1.3.2 a 1.3.4 e 1.4.2 a 1.4.4 tinham 5 dias úteis de folga (terminam em 31/10 e só são necessárias em 10/11). Uso atual dessa folga: NI. Como 1.3.2 a 1.3.4 falharam no SR1 e o software não mudou desde então, a folga pode estar sendo consumida.
- **Sem reserva de prazo** entre 1.5.3 e a entrega (Plano, seção 5.3): atraso no caminho crítico atinge diretamente 11/12.

## 7. Valor agregado por atividade

**Regra de crédito (escolha do grupo): 20/80.** A atividade em andamento recebe 20% do esforço planejado ao começar e os 80% restantes ao ser concluída com o critério do Dicionário verificado. O crédito de 20% só vale com início real comprovado. Justificativa: nos pacotes de desenvolvimento, começar é mais fácil do que cumprir o critério completo, como mostrou o SR1 (5 de 6 pacotes falharam).

**Distribuição do VP no tempo (escolha do grupo): linear pelos dias úteis do Plano**, para as atividades em andamento pelo cronograma. Fórmula: VP = esforço × dias úteis decorridos até 02/11 ÷ duração planejada em dias úteis. Atividade com fim planejado até 02/11 entra com o esforço inteiro; atividade com início planejado depois de 02/11 entra com 0.

| ID | Esforço planejado (h) | VP em 02/11 (h) | Horas gastas | Esforço restante | Regra de crédito | VA (h) |
| --- | --- | --- | --- | --- | --- | --- |
| 1.1.1 | 20 | 20 | NI | NI | 20/80; critério NI | NI |
| 1.1.2 | 12 | 4,85 (12 × 19 ÷ 47) | NI | NI | 20/80; início NI | NI |
| 1.2.1 | 10 | 10 | NI | NI | 20/80; critério NI | NI |
| 1.2.2 | 14 | 14 | NI | NI | 20/80; critério NI | NI |
| 1.3.1 | 16 | 16 | NI | 0 | Concluída; critério verificado no SR1 (100%) | 16 |
| 1.3.2 | 20 | 20 | NI | NI | 20/80; início NI; critério falhou no SR1 | NI |
| 1.3.3 | 12 | 12 | NI | NI | 20/80; início NI; critério falhou no SR1 | NI |
| 1.3.4 | 12 | 12 | NI | NI | 20/80; início NI; critério falhou no SR1 | NI |
| 1.3.5 | 16 | 9,93 (16 × 18 ÷ 29) | NI | NI | 20/80; início NI; critério falhou no SR1 | NI |
| 1.3.6 | 8 | 0 | NI | NI | 20/80; início NI | NI |
| 1.4.1 | 10 | 10 | NI | NI | 20/80; critério não verificado | NI |
| 1.4.2 | 8 | 8 | NI | NI | 20/80; início NI | NI |
| 1.4.3 | 8 | 8 | NI | NI | 20/80; início NI | NI |
| 1.4.4 | 6 | 6 | NI | NI | 20/80; início NI | NI |
| 1.4.5 | 12 | 7,45 (12 × 18 ÷ 29) | NI | NI | 20/80; início NI | NI |
| 1.4.6 | 6 | 0 | NI | NI | 20/80; início NI | NI |
| 1.5.1 | 10 | 0 | NI | NI | 20/80; início NI | NI |
| 1.5.2 | 12 | 0 | NI | NI | 20/80; início NI | NI |
| 1.5.3 | 8 | 0 | NI | NI | 20/80; início NI | NI |
| 1.6.1 | 8 | 0 | NI | NI | 20/80; início NI | NI |
| **Total dos pacotes** | **228** | **158,23** | **14 (parcial)** | NI |  | **16 (parcial)** |

**Horas sem atividade confirmada:** 14 h: 6 h de Ronald (19 a 23/10) e 8 h de Thiago (19/10: 3 h; 23/10: 2 h; 02/11: 3 h). Ronald relata a base da API (Express, Prisma e PostgreSQL, autenticação JWT, validação com Zod e isolamento de dados por usuário). Thiago relata, em 19/10, a configuração inicial do back-end (dependências, migration inicial e seed do Prisma); em 23/10, a integração da versão final da base na branch `develop` (Docker, schema do Prisma e documentação); e, em 02/11, a autenticação do back-end com Passport e JWT (cadastro, login, proteção das rotas, redefinição de senha demonstrativa) e testes de funcionamento. Os relatos não nomeiam o pacote da EAP; a atribuição depende da confirmação deles. Pelo conteúdo, o trabalho de Thiago não está nos pacotes de que ele é responsável (1.3.3 e 1.4.3) e se aproxima de 1.4.1 (responsável: Rodrigo). Se forem de pacotes 1.4.x, não geram VA enquanto o critério não for verificado e enquanto CHG-06 não for aprovada.

| Total | Valor | De onde saiu |
| --- | --- | --- |
| VP | **158,2 h** (R$ 1.582,30) | 136 h dos 11 pacotes com fim planejado até 02/11 (1.1.1 20 + 1.2.1 10 + 1.2.2 14 + 1.3.1 16 + 1.3.2 20 + 1.3.3 12 + 1.3.4 12 + 1.4.1 10 + 1.4.2 8 + 1.4.3 8 + 1.4.4 6) + 22,23 h pela distribuição linear de 1.1.2 (4,85), 1.3.5 (9,93) e 1.4.5 (7,45). Dias úteis decorridos até 02/11, sem contar o feriado: 19 em 1.1.2 (duração de 47) e 18 em 1.3.5 e 1.4.5 (duração de 29). Os pacotes sem início planejado até 02/11 (1.3.6, 1.4.6, 1.5.1, 1.5.2, 1.5.3 e 1.6.1; 52 h) contribuem com 0 |
| VA | **16 h** (parcial; mínimo comprovado) | Só 1.3.1, com critério verificado no SR1. Os demais pacotes não entram porque o início real e a verificação do critério são NI |
| CR | **14 h** (parcial) | Relatos de Ronald (6 h, 19 a 23/10) e de Thiago (8 h: 3 h em 19/10, 2 h em 23/10 e 3 h em 02/11). Horas dos outros 5 integrantes: NI |

## 8. Variações e índices

| Medida | Fórmula | Conta com os dados atuais | Valor |
| --- | --- | --- | --- |
| VPr | VA − VP | VA − 158,2 | Não calculado |
| VC | VA − CR | VA − CR (CR parcial de 14 h) | Não calculado |
| IDP | VA ÷ VP | VA ÷ 158,2 | Não calculado |
| IDC | VA ÷ CR | VA ÷ CR | Não calculado |

**Motivo.** O VA só inclui um pacote e o CR só inclui 2 de 7 integrantes. Dividir 16 h de VA por 14 h de CR daria um IDC que só reflete apontamento parcial (5 integrantes ainda sem apontar), não custo baixo. Com esses dados, qualquer índice mede a falta de informação e não o desempenho do projeto. Os índices serão calculados quando houver VA, CR e a semana de início da medição declarada.

## 9. Previsão

| Item | Conteúdo |
| --- | --- |
| ONT (orçamento no término) | 228 h (soma dos pacotes, Plano seção 7.2) |
| Limite de comparação | 251 h = 228 h + 23 h de contingência (R$ 2.510 a R$ 10,00 por hora) |
| ENT | Fórmula: ENT = ONT ÷ IDC = 228 ÷ IDC. Premissa: o desvio de custo observado até a data de corte continua até o término. Valor: não calculado (IDC não calculado) |
| EPT | Fórmula: EPT = ENT − CR. Valor: não calculado |
| VNT (opcional) | ONT − ENT = 228 − ENT. Não calculado |
| IDPT (opcional) | (ONT − VA) ÷ (ONT − CR) = (228 − VA) ÷ (228 − CR). Não calculado |

Entradas que faltam: VA, CR completo e horas restantes por atividade. Depois de calculada, a ENT será comparada com o limite de 251 h. A previsão de prazo vem do caminho crítico (seção 6); o índice só indica a tendência.

## 10. Recursos

Planejado: Plano, seção 7.6 (pacotes compartilhados divididos igualmente). Capacidade da linha de base: 4 h por semana por pessoa. Capacidade nominal restante de 03/11 a 17/11: 11 dias úteis = 2,2 semanas, ou seja, 2,2 × 4 = 8,8 h por pessoa. É capacidade nominal; a disponibilidade real de cada pessoa (provas, outras disciplinas) é NI.

| Pessoa | Disciplina | Planejado (h) | Apontado (h) | Capacidade restante até 17/11 (nominal) |
| --- | --- | --- | --- | --- |
| Ronald | PSW | 70,3 | 6 (19 a 23/10; pacote NI) | 8,8 h |
| Rodrigo | PSW | 57,3 | NI | 8,8 h |
| Thiago | PSW | 64,3 | 8 (19/10: 3; 23/10: 2; 26 a 30/10: 0; 02/11: 3; pacote NI) | 8,8 h |
| Davi | GPTI | 9 | NI | 8,8 h |
| João | GPTI | 9 | NI | 8,8 h |
| Michael | GPTI | 9 | NI | 8,8 h |
| Vinicius | GPTI | 9 | NI | 8,8 h |
| **Total PSW** |  | 192 | 14 (parcial) | 26,4 h |
| **Total GPTI** |  | 36 | NI | 35,2 h |

**Referências da linha de base.** Os desenvolvedores têm 192 h de esforço para 108 h de capacidade nominal (9 semanas × 4 h × 3), ou seja, 84 h acima. A gerência tem 36 h de esforço para 144 h de capacidade, ou seja, 108 h de folga. Os pacotes 1.3.x e 1.4.x do Marco 2 somam 134 h planejadas. Só como cenário de referência, e não como previsão: se nada além de 1.3.1 estivesse pronto, restariam 118 h desses pacotes contra 26,4 h de capacidade nominal da PSW até 17/11. O esforço restante real é NI.

## 11. Questões e mudanças

### 11.1 Itens herdados do SR1

Donos e prazos conforme o SR1. O software não mudou desde o SR1 (informado pelo grupo); por isso as questões ligadas a esses pacotes seguem abertas e não há o que retestar.

| ID | Resumo | Dono | Prazo (SR1) | Situação em 02/11 |
| --- | --- | --- | --- | --- |
| Q-01 | Cobrança vencida exibida como «Em -7 dias» (1.3.2) | Ronald | 19/10 | Aberta; prazo vencido; software inalterado |
| Q-02 | Link externo de cancelamento e uso só com teclado não demonstrados | Gerência | 16/10 | Aberta; software inalterado; prazo vencido |
| Q-03 | Sem cadastro, edição e exclusão de serviço (UC05, UC07, UC08) | Thiago | 19/10 | Aberta; prazo vencido; software inalterado |
| Q-04 | Sem perfil Administrador distinto | Ronald | 19/10 | Aberta; prazo vencido; software inalterado |
| Q-05 | Sem exclusão de teto (UC12) | Equipe de desenvolvimento (a nomear) | 19/10 | Aberta; prazo vencido; software inalterado |
| Q-06 | Sem histórico de importações nem descarte persistente (UC15, UC16) | Rodrigo | 19/10 | Aberta; prazo vencido; software inalterado |
| Q-07 | Importação aceita CSV incompatível e PDF; arquivo vazio sem mensagem | Rodrigo | 19/10 | Aberta; prazo vencido; software inalterado |
| Q-08 | Reimportação repete entradas no histórico de pagamentos | Rodrigo | 19/10 | Aberta; prazo vencido; software inalterado |
| Q-09 | teste.csv com 9 lançamentos; limiares de importação não medidos | Rodrigo | 16/10 | NI |
| Q-10 | Sem tutorial dentro do aplicativo | Ronald e Thiago | 19/10 | Aberta; prazo vencido; software inalterado |
| Q-11 | Conta nova sem mensagem de lista vazia | Ronald | 19/10 | Aberta; prazo vencido; software inalterado |
| Q-12 | F5 em tela interna volta ao painel | Ronald | 19/10 | Aberta; prazo vencido; software inalterado |
| Q-13 | PSW não informou commit ou tag de congelamento | PSW (a nomear) | 16/10 | NI |
| Q-14 | Responsáveis por pacote não confirmados | PSW (a nomear) | 16/10 | NI |
| Q-15 | Formalizar Marco 1 (front-end) e Marco 2 (API própria) | Gerência | 16/10 | Não formalizado; este relatório usa a data do Plano (17/11) |
| CHG-01 | Reduzir 1.3.3 (remover UC05, UC07, UC08) | Patrocinador | 16/10 | Decisão NI |
| CHG-02 | Reduzir 1.3.5 (remover UC15, UC16) | Patrocinador | 16/10 | Decisão NI |
| CHG-03 | UC12: exclusão real do teto ou definir zero | Patrocinador | 16/10 | Decisão NI |
| CHG-04 | Ação Confirmar Pagamento, fora da EAP | Patrocinador | 16/10 | Decisão NI |
| CHG-05 | Telas Criar Conta e Esqueceu a senha | Patrocinador | 16/10 | Decisão NI |

### 11.2 Registros novos

Data de registro: 02/11/2026. Os prazos de resolução são propostos e o grupo confirma.

| ID | Registro | Escopo | Prazo | Custo | Dono | Data |
| --- | --- | --- | --- | --- | --- | --- |
| Q-16 | Pessoas sem hora apontada: Rodrigo e os 4 da gerência (relatos pendentes). Ronald e Thiago só têm relato a partir de 19/10; de 07 a 16/10 não há relato de nenhum dos dois | Sem impacto direto | Impede medir o CR e calcular IDC; efeito no prazo NI | CR incompleto (14 h de 2 de 7 pessoas); IDC e ENT não calculáveis | Gerência | Registro 02/11; resolução proposta 04/11 |
| Q-17 | 1.4.1: o relato da base da API refere-se a 19 a 23/10, depois do fim planejado (12/10). O código está no repositório da PSW (informado pelo grupo). Conclusão e verificação do critério: NI | Critério de 1.4.1 não verificado | Fim planejado 12/10; fim real NI | NI | PSW (Rodrigo, responsável por 1.4.1 no Dicionário; confirmar) | Registro 02/11; resolução proposta 04/11 |
| Q-18 | 10 dos 11 pacotes com fim planejado até 02/11 (120 h de VP) estão sem critério verificado; 1.3.2 a 1.3.4 consomem a folga de 5 dias úteis até 10/11 | 1.3.2 a 1.3.4 falharam no SR1; os demais NI | Folga em uso; efeito no caminho crítico NI | VA não creditado de 120 h de VP | Gerência (verificação) com a PSW | Registro 02/11; resolução proposta 09/11 |
| CHG-06 | Back-end real, relatado por Ronald (base da API com Express, Prisma e PostgreSQL, autenticação JWT) e por Thiago (migration e seed do Prisma, Docker, integração na branch `develop` e autenticação com Passport e JWT), presente no repositório da PSW (informado pelo grupo). A linha de base prevê json-server, db.json e autenticação simulada (Dicionário 1.4.1; Plano P6 e D1) | Trabalho fora da linha de base se não aprovada; o relato de Thiago de 02/11 inclui cadastro, login, proteção das rotas e redefinição de senha demonstrativa (não é fluxo completo), possivelmente ligados a CHG-05 | NI | As 14 h (Ronald 6 h, Thiago 8 h) entram no CR; sem aprovação não geram VA | PSW (Ronald e Thiago relataram; Rodrigo é responsável por 1.4.1); decisão do patrocinador | Registro 02/11; decisão pedida até 06/11 (proposta) |

## 12. Decisões pedidas ao patrocinador

| Decisão | Opções | Efeito em horas |
| --- | --- | --- |
| CHG-06 (back-end real, D1 do Plano) | (a) Aprovar, com nova linha de base para 1.4.x e 1.5.1; (b) manter json-server | (a) as 14 h (Ronald e Thiago) passam a gerar VA se o critério for verificado; o esforço de 1.4.x e 1.5.1 muda e não foi estimado. (b) as 14 h ficam como CR sem VA (VC piora em 14 h) |
| CHG-01 e CHG-02 (reduzir 1.3.3 e 1.3.5) | Aprovar a redução ou manter o critério original e pedir a conclusão | A redução não foi estimada; o teto é o esforço do pacote (1.3.3: 12 h; 1.3.5: 16 h), e 1.4.3 e 1.4.5 podem ser afetados |
| CHG-03 a CHG-05 (UC12, Confirmar Pagamento, Criar Conta e Esqueceu a senha) | Aprovar cada uma ou manter o critério original | NI; esforço não estimado |
| Definição do Marco 2 (Q-15) | (a) Plano: 17/11, front-end e API (1.2.2, 1.3.x e 1.4.x); (b) SR1: Marco 2 = API própria | (a) 134 h planejadas em 1.3.x e 1.4.x; (b) 50 h planejadas em 1.4.x (1.4.1 a 1.4.6) |
| Carga dos desenvolvedores (R2 do Plano). Base: 192 h de esforço contra 108 h de capacidade, 84 h acima | (a) Aumentar as horas dos desenvolvedores; (b) realocar esforço à gerência; (c) cortar escopo; (d) rever a data; (e) usar a contingência | (a) +84 h no total, +28 h por desenvolvedor, de 4 para cerca de 7,1 h por semana em 9 semanas; (b) 84 h passam para a gerência, que iria de 36 h para 120 h de esforço, dentro dos 144 h de capacidade; (c) cortar 84 h de pacotes dos desenvolvedores, a escolher; (d) sem mudar as horas, 84 h a 12 h por semana (3 × 4 h) pedem cerca de 7 semanas além de 11/12, e a data final é fixa no Plano; (e) até 23 h, só com risco nomeado que tenha ocorrido e ciência do patrocinador (Plano, seção 7.1). O efeito sobre as horas restantes reais é NI |

## 13. Próximas ações

Prazos propostos pelo grupo; o grupo confirma.

| Ação | Responsável | Prazo |
| --- | --- | --- |
| Registrar, por pessoa, a semana em que a medição começou e quais semanas foram reconstituídas | Gerência | 03/11 |
| Coletar as horas dos 4 integrantes da gerência | Gerência | 03/11 |
| Confirmar com Ronald e Thiago a que pacote da EAP pertencem as 14 h (6 h e 8 h); no caso de Thiago, o trabalho de 19/10, 23/10 e 02/11 não está em 1.3.3 nem 1.4.3 | Gerência | 03/11 |
| Coletar horas por semana e por atividade de Rodrigo, e as semanas de 07 a 16/10 de Ronald e Thiago | Gerência e PSW | 04/11 |
| Coletar datas reais, duração restante e esforço restante por atividade, com commits como evidência | Gerência e PSW | 04/11 |
| Nomear o responsável pelos pacotes 1.3.4 e 1.4.4 (D5 do Plano) | PSW | 04/11 |
| Recalcular VP, VA, CR, índices, ENT e EPT e reenviar este relatório | Gerência | 05/11 |
| Decidir CHG-01 a CHG-06 e a definição do Marco 2 | Patrocinador | 06/11 |
| Verificar o critério dos pacotes relatados como concluídos (retestar 1.3.2 a 1.3.6 só depois que o software mudar) | Gerência | 09/11 |
| Corrigir as questões abertas e apresentar evidências de teste | PSW, donos indicados | Antes do início de 1.3.6 e 1.4.6, em 10/11 |
