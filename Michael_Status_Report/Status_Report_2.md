# Status Report 2 — SubTracker

Marco 3 contra a linha de base aprovada · Grupo de gerência: Davi Luiz Rodrigues da Conceição, João Henrique Lima Gualberto, Michael Patrick Ferreira da Silva Borba e Vinicius da Silva Mendes

**Como ler este relatório.** NI significa "não informado": o dado não foi fornecido ao grupo até a data de status. Nenhum valor foi estimado. Onde falta dado, o índice não foi calculado e a fórmula aparece com os números que já existem. A linha de base vem do Plano do Projeto v4.0, da EAP e do Dicionário (v2.1). O escopo anterior vem do Status Report 1 (SR1). A ferramenta de IA ajudou a montar as tabelas e revisar as fórmulas; a regra de crédito, a leitura dos índices e as decisões pedidas são do grupo.

## 1. Data de status e período coberto

| Item | Conteúdo |
| --- | --- |
| Data de status | 02/11/2026 |
| Período coberto | 07/10/2026 (dia seguinte ao corte do SR1) a 02/11/2026 |
| Início da medição de horas | NI. O SR1 previa o início do apontamento até 16/10/2026; os relatos recebidos (Ronald e Thiago) começam na semana de 19 a 23/10; de 07 a 16/10 não há relato (NI) |
| Semanas reconstituídas | Os relatos de Ronald e de Thiago trazem horas aproximadas e chegaram depois das semanas relatadas (o de Thiago em 02/11); por isso são tratados como reconstituídos. O grupo confirma |
| Horas recebidas | 2 relatos: Ronald, cerca de 6 h (19 a 23/10), e Thiago, cerca de 8 h (19/10: 3 h; 23/10: 2 h; 26 a 30/10: 0 h, sem atividade registrada; 02/11: 3 h). Rodrigo e a gerência ainda não enviaram |
| Linha de base | Plano v4.0. Mudança aprovada pelo patrocinador desde a linha de base: NI. Enquanto não houver aprovação, vale o plano original |
| Marco 2 (já concluído) | 06/10/2026, conforme o Plano. Este relatório mede o progresso em direção ao Marco 3 (07 a 11/12/2026) |
| Marco 3 | 07 a 11/12/2026, conforme o Plano (pacotes 1.5.1 a 1.5.3 e 1.6.1). Entre 03/11 e 11/12 restam cerca de 27 dias úteis (descontados os feriados de 02/11 e 20/11) |
| Taxa de valoração | R$ 10,00 por hora, igual para todos (Plano, seção 7.1); por isso índices em horas e em R$ coincidem |

## 2. Situação geral de escopo, prazo e custo

| Dimensão | Cor | Número | Justificativa |
| --- | --- | --- | --- |
| Escopo | **VERMELHO** | 1 de 6 pacotes de front-end com critério verificado (SR1) | Cinco pacotes falharam no SR1 e o software não mudou desde o SR1 (informado pelo grupo), então o resultado se mantém. Seguem pendentes o tutorial e a validação de importação de CSV |
| Prazo | Não determinada | VA comprovado: 16 h de VP 165,5 h | IDP não calculado: o VA conhecido é só o mínimo comprovado e as datas reais são NI. Pela linha de base, 13 pacotes (150 h) já deveriam estar concluídos até 02/11 e só 1 (1.3.1, 16 h) tem critério verificado |
| Custo | Não determinada | CR parcial: 14 h de 2 pessoas entre 7 | IDC não calculado: com 2 de 7 integrantes apontados, o índice refletiria falta de apontamento e não o custo do projeto |

## 3. As três perguntas do relatório

1. **O caminho crítico ainda entrega o Marco 3 em 11/12?** Não é possível responder. As datas reais e a duração restante de 1.4.5, que está no caminho crítico, são NI. Data planejada: 11/12/2026.
2. **O valor agregado mostra trabalho feito no ritmo e no custo planejados?** Não é possível responder com índice. O VP é 165,5 h; o VA comprovado é 16 h (só 1.3.1) e o CR conhecido é 14 h. Os dois últimos são incompletos, então IDP e IDC não foram calculados.
3. **As horas que faltam cabem na capacidade que resta até o Marco 3?** Não é possível responder: o esforço restante por atividade é NI. Referências: a capacidade nominal restante é de cerca de 21,6 h por pessoa (27 dias úteis × 4 h/semana ÷ 5) para a equipe de desenvolvimento; na linha de base, os pacotes do Marco 3 (1.5.1 a 1.5.3 e 1.6.1) somam 38 h.

## 4. Escopo desde o Status Report 1

| Pacote | Resultado no SR1 (corte 06/10) | Desde então |
| --- | --- | --- |
| 1.3.1 Estrutura de front-end e rotas | Passou | Sem mudança. Aceite formal do patrocinador: NI |
| 1.3.2 Assinaturas e dashboard | Falhou | Software inalterado desde o SR1; continua Falhou |
| 1.3.3 Serviços e cancelamento | Falhou | Software inalterado desde o SR1; continua Falhou |
| 1.3.4 Tetos e consumo orçamentário | Falhou | Software inalterado desde o SR1; continua Falhou |
| 1.3.5 Extratos e conciliação | Falhou | Software inalterado desde o SR1; continua Falhou |
| 1.3.6 Relatório e tutorial | Falhou | Software inalterado desde o SR1; continua Falhou |
| 1.4.1 Estrutura da API e modelagem do banco | Não verificado no SR1 | Relato de Ronald, com o código no repositório: base da API com Express, Prisma e PostgreSQL, autenticação JWT, validação com Zod e isolamento de dados por usuário, cerca de 6 h em 19 a 23/10. Relato de Thiago, também sobre a base do back-end: 19/10, cerca de 3 h (configuração inicial, dependências, migration inicial do banco e seed do Prisma); 23/10, cerca de 2 h (integração da versão final da base na branch `develop`, com Docker, schema do Prisma e documentação). Critério do Dicionário não verificado |
| 1.4.2 a 1.4.6 | Não verificados no SR1 | NI |
| 1.1.1, 1.1.2, 1.2.1, 1.2.2 | Fora do SR1 | NI |

**Verificados:** 1.3.1 (SR1). **Pendentes:** tutorial e validação de importação (SR1); sem correção, porque o software não mudou desde o SR1. **Não demonstrados:** abertura da página externa do link de cancelamento e uso do fluxo principal só com teclado (SR1, Q-02); software inalterado, sem novo teste.

## 5. Cronograma

★ = caminho crítico. NI = não informado. Datas planejadas da linha de base (Plano, seção 5.2).

| ID | Atividade | Responsável | Início plan. | Fim plan. | Início real | Fim real | Duração restante | Situação |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1.1.1 | Documentação e acompanhamento | Gerência | 03/08 | 05/10 | NI | NI | NI | NI (fim planejado já passou) |
| 1.1.2 | Monitoramento, riscos e comunicação | Gerência | 05/10 | 11/12 | NI | NI | NI | Em andamento pelo plano; real NI |
| 1.2.1 | Levantamento e rastreabilidade | Ronald, Rodrigo, Thiago | 03/08 | 05/10 | NI | NI | NI | NI (fim planejado já passou) |
| 1.2.2 | Prototipagem e matrizes | Ronald, Rodrigo, Thiago | 03/08 | 05/10 | NI | NI | NI | NI (fim planejado já passou) |
| 1.3.1 | Estrutura de front-end e rotas | Ronald | 05/10 | 06/10 | NI | NI | 0 | Concluída; critério verificado no SR1 |
| 1.3.2 | Assinaturas e dashboard | Ronald | 05/10 | 06/10 | NI | NI | NI | Critério falhou no SR1; software inalterado |
| 1.3.3 | Serviços e cancelamento | Thiago | 05/10 | 06/10 | NI | NI | NI | Critério falhou no SR1; software inalterado |
| 1.3.4 | Tetos e consumo orçamentário | Thiago | 05/10 | 06/10 | NI | NI | NI | Critério falhou no SR1; software inalterado |
| 1.3.5 | Extratos e conciliação | Rodrigo | 05/10 | 06/10 | NI | NI | NI | Critério falhou no SR1; software inalterado |
| 1.3.6 | Relatório e tutorial | Ronald e Thiago | 05/10 | 06/10 | NI | NI | NI | Critério falhou no SR1; software inalterado |
| 1.4.1 | Estrutura da API e modelagem do banco | Rodrigo | 06/10 | 12/10 | 19/10 | NI | NI | Trabalho relatado por Ronald e Thiago; critério não verificado |
| 1.4.2 | API de Assinaturas | Ronald | 12/10 | 31/10 | NI | NI | NI | NI (fim planejado já passou) |
| 1.4.3 | API de Serviços | Thiago | 12/10 | 31/10 | NI | NI | NI | NI (fim planejado já passou) |
| 1.4.4 | API de Tetos | Thiago | 12/10 | 31/10 | NI | NI | NI | NI (fim planejado já passou) |
| 1.4.5 ★ | Importação de extratos e conciliação | Rodrigo | 06/10 | 17/11 | NI | NI | NI | Em andamento pelo plano; real NI |
| 1.4.6 ★ | Relatório, projeção e acesso | Ronald e Thiago | 10/11 | 17/11 | NI | NI | NI | Início planejado 10/11 (futuro) |
| 1.5.1 ★ | Integração front-end/back-end | Ronald, Rodrigo, Thiago | 18/11 | 24/11 | NI | NI | NI | Início planejado 18/11 (futuro) |
| 1.5.2 ★ | Testes de validação funcional | Ronald, Rodrigo, Thiago | 25/11 | 03/12 | NI | NI | NI | Início planejado 25/11 (futuro) |
| 1.5.3 ★ | Ajustes e validação final | Ronald, Rodrigo, Thiago | 04/12 | 11/12 | NI | NI | NI | Início planejado 04/12 (futuro) |
| 1.6.1 ★ | Documentação final e entrega | Gerência | 07/12 | 11/12 | NI | NI | NI | Início planejado 07/12 (futuro) |

**Leitura.** Pela linha de base, 13 pacotes (150 h) tinham término planejado até 02/11. Só 1 (1.3.1, 16 h) tem critério verificado; os outros 12 (134 h) estão sem verificação (Q-18).

## 6. Caminho crítico e data prevista do Marco 3

- **Caminho crítico da linha de base (Plano, seção 5.3):** 1.4.5 (06/10 a 17/11), depois 1.4.6 (término em 17/11), depois 1.5.1, 1.5.2, 1.5.3 e 1.6.1 (entrega final em 11/12).
- **Caminho crítico atualizado:** NI. Depende das datas reais e da duração restante de 1.4.5.
- **Data prevista do Marco 3:** NI. A data vem do caminho crítico, não do IDP. Data planejada: 11/12/2026.
- **Folga:** 1.4.2 a 1.4.4 tinham 5 dias úteis de folga (terminam em 31/10 e só são necessárias em 10/11). Uso atual dessa folga: NI. Como 1.3.2 a 1.3.6 falharam no SR1 e o software não mudou desde então, a folga pode estar sendo consumida.
- **Sem reserva de prazo** entre 1.5.3 e a entrega (Plano, seção 5.3): atraso no caminho crítico atinge diretamente 11/12.

## 7. Valor agregado por atividade

**Regra de crédito (escolha do grupo): 20/80.** A atividade em andamento recebe 20% do esforço planejado ao começar e os 80% restantes ao ser concluída com o critério do Dicionário verificado. O crédito de 20% só vale com início real comprovado. Justificativa: nos pacotes de desenvolvimento, começar é mais fácil do que cumprir o critério completo, como mostrou o SR1 (5 de 6 pacotes falharam).

**Distribuição do VP no tempo (escolha do grupo): linear pelos dias úteis do Plano**, para as atividades em andamento pelo cronograma. Fórmula: VP = esforço × dias úteis decorridos até 02/11 ÷ duração planejada em dias úteis. Atividade com fim planejado até 02/11 entra com o esforço inteiro; atividade com início planejado depois de 02/11 entra com 0.

| ID | Esforço planejado (h) | VP em 02/11 (h) | Horas gastas | Esforço restante | Regra de crédito | VA (h) |
| --- | --- | --- | --- | --- | --- | --- |
| 1.1.1 | 20 | 20 | NI | NI | 20/80; critério NI | NI |
| 1.1.2 | 26 | 10,51 (26 × 19 ÷ 47) | NI | NI | 20/80; início NI | NI |
| 1.2.1 | 10 | 10 | NI | NI | 20/80; critério NI | NI |
| 1.2.2 | 14 | 14 | NI | NI | 20/80; critério NI | NI |
| 1.3.1 | 16 | 16 | NI | 0 | Concluída; critério verificado no SR1 (100%) | 16 |
| 1.3.2 | 20 | 20 | NI | NI | 20/80; início NI; critério falhou no SR1 | NI |
| 1.3.3 | 8 | 8 | NI | NI | 20/80; início NI; critério falhou no SR1 | NI |
| 1.3.4 | 12 | 12 | NI | NI | 20/80; início NI; critério falhou no SR1 | NI |
| 1.3.5 | 12 | 12 | NI | NI | 20/80; início NI; critério falhou no SR1 | NI |
| 1.3.6 | 8 | 8 | NI | NI | 20/80; início NI; critério falhou no SR1 | NI |
| 1.4.1 | 10 | 10 | 14 (Ronald 6 + Thiago 8) | NI | 20/80; critério não verificado | NI |
| 1.4.2 | 8 | 8 | NI | NI | 20/80; início NI | NI |
| 1.4.3 | 6 | 6 | NI | NI | 20/80; início NI | NI |
| 1.4.4 | 6 | 6 | NI | NI | 20/80; início NI | NI |
| 1.4.5 | 8 | 4,97 (8 × 18 ÷ 29) | NI | NI | 20/80; início NI | NI |
| 1.4.6 | 6 | 0 | NI | NI | 20/80; início NI | NI |
| 1.5.1 | 10 | 0 | NI | NI | 20/80; início NI | NI |
| 1.5.2 | 12 | 0 | NI | NI | 20/80; início NI | NI |
| 1.5.3 | 8 | 0 | NI | NI | 20/80; início NI | NI |
| 1.6.1 | 8 | 0 | NI | NI | 20/80; início NI | NI |
| **Total dos pacotes** | **228** | **165,48** | **14 (parcial)** | NI |  | **16 (parcial)** |

**Horas sem atividade confirmada:** 14 h: 6 h de Ronald (19 a 23/10) e 8 h de Thiago (19/10: 3 h; 23/10: 2 h; 02/11: 3 h). Ronald relata a base da API (Express, Prisma e PostgreSQL, autenticação JWT, validação com Zod e isolamento de dados por usuário). Thiago relata, em 19/10, a configuração inicial do back-end (dependências, migration inicial e seed do Prisma); em 23/10, a integração da versão final da base na branch `develop` (Docker, schema do Prisma e documentação); e, em 02/11, a autenticação do back-end com Passport e JWT (cadastro, login, proteção das rotas, redefinição de senha demonstrativa) e testes de funcionamento. Os relatos não nomeiam o pacote da EAP; a atribuição depende da confirmação deles. Pelo conteúdo, o trabalho de Thiago não está nos pacotes de que ele é responsável (1.3.3 e 1.4.3) e se aproxima de 1.4.1 (responsável: Rodrigo). Se forem de 1.4.1, o esforço de 14 h já supera o planejado de 10 h; o critério não foi verificado.

| Total | Valor | De onde saiu |
| --- | --- | --- |
| VP | **165,5 h** (R$ 1.655,00) | 150 h dos 13 pacotes com fim planejado até 02/11 (1.1.1 20 + 1.2.1 10 + 1.2.2 14 + 1.3.1 16 + 1.3.2 20 + 1.3.3 8 + 1.3.4 12 + 1.3.5 12 + 1.3.6 8 + 1.4.1 10 + 1.4.2 8 + 1.4.3 6 + 1.4.4 6) + 15,48 h pela distribuição linear de 1.1.2 (10,51) e 1.4.5 (4,97). Dias úteis decorridos até 02/11, sem contar o feriado: 19 em 1.1.2 (duração de 47) e 18 em 1.4.5 (duração de 29). Os pacotes sem início planejado até 02/11 (1.4.6, 1.5.1, 1.5.2, 1.5.3 e 1.6.1; 44 h) contribuem com 0 |
| VA | **16 h** (parcial; mínimo comprovado) | Só 1.3.1, com critério verificado no SR1. Os demais pacotes não entram porque o início real e a verificação do critério são NI |
| CR | **14 h** (parcial) | Relatos de Ronald (6 h, 19 a 23/10) e de Thiago (8 h: 3 h em 19/10, 2 h em 23/10 e 3 h em 02/11). Horas dos outros 5 integrantes: NI |

## 8. Variações e índices

| Medida | Fórmula | Conta com os dados atuais | Valor |
| --- | --- | --- | --- |
| VPr | VA − VP | 16 − 165,5 | −149,5 h |
| VC | VA − CR | 16 − 14 | +2 h (parcial) |
| IDP | VA ÷ VP | 16 ÷ 165,5 | 0,097 |
| IDC | VA ÷ CR | 16 ÷ 14 | 1,14 (parcial) |

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

Planejado: Plano, seção 7.6 (pacotes compartilhados divididos igualmente). Capacidade da linha de base: 4 h por semana por pessoa. Capacidade nominal restante de 03/11 a 11/12: cerca de 27 dias úteis = 5,4 semanas, ou seja, 5,4 × 4 = 21,6 h por pessoa. É capacidade nominal; a disponibilidade real de cada pessoa (feriados, outras demandas) é NI.

| Pessoa | Disciplina | Planejado (h) | Apontado (h) | Capacidade restante até 11/12 (nominal) |
| --- | --- | --- | --- | --- |
| Ronald | Desenvolvimento | 67,9 | 6 (19 a 23/10; pacote NI) | 21,6 h |
| Rodrigo | Desenvolvimento | 41,3 | NI | 21,6 h |
| Thiago | Desenvolvimento | 54,3 | 8 (19/10: 3; 23/10: 2; 26 a 30/10: 0; 02/11: 3; pacote NI) | 21,6 h |
| Davi | Gerência | 13,5 | NI | 21,6 h |
| João | Gerência | 13,5 | NI | 21,6 h |
| Michael | Gerência | 13,5 | NI | 21,6 h |
| Vinicius | Gerência | 13,5 | NI | 21,6 h |
| **Total Desenvolvimento** |  | 163,5 | 14 (parcial) | 64,8 h |
| **Total Gerência** |  | 54 | NI | 86,4 h |

**Referências da linha de base.** Os desenvolvedores têm 163,5 h de esforço para 108 h de capacidade nominal (9 semanas × 4 h × 3), ou seja, 55,5 h acima. A gerência tem 54 h de esforço para 144 h de capacidade, ou seja, 90 h de folga. Os pacotes do Marco 3 (1.5.1 a 1.5.3 e 1.6.1) somam 38 h. Só como cenário de referência, e não como previsão: se nada além de 1.3.1 estivesse pronto, restariam 38 h contra 64,8 h de capacidade nominal da equipe de desenvolvimento até 11/12. O esforço restante real é NI.

## 11. Questões e mudanças

### 11.1 Itens herdados do SR1

Donos e prazos conforme o SR1. O software não mudou desde o SR1 (informado pelo grupo); por isso as questões ligadas a esses pacotes seguem abertas e não há o que retestar.

| ID     | Resumo                                                               | Dono            | Prazo (SR1) | Situação em 02/11                          |
| ------ | -------------------------------------------------------------------- | --------------- | ----------- | ------------------------------------------ |
| Q-01   | Cobrança vencida exibida como "Em -7 dias" (1.3.2)                   | Ronald          | 19/10       | Aberta; prazo vencido; software inalterado |
| Q-02   | Link externo de cancelamento e uso só com teclado não demonstrados   | Gerência        | 16/10       | Aberta; software inalterado; prazo vencido |
| Q-05   | Sem exclusão de teto (UC12)                                          | Thiago          | 19/10       | Aberta; prazo vencido; software inalterado |
| Q-07   | Importação aceita CSV incompatível e PDF; arquivo vazio sem mensagem | Rodrigo         | 19/10       | Aberta; prazo vencido; software inalterado |
| Q-08   | Reimportação repete entradas no histórico de pagamentos              | Rodrigo         | 19/10       | Aberta; prazo vencido; software inalterado |
| Q-09   | teste.csv com 9 lançamentos; limiares de importação não medidos      | Rodrigo         | 16/10       | NI                                         |
| Q-10   | Sem tutorial dentro do aplicativo                                    | Ronald e Thiago | 19/10       | Aberta; prazo vencido; software inalterado |
| Q-11   | Conta nova sem mensagem de lista vazia                               | Ronald          | 19/10       | Aberta; prazo vencido; software inalterado |
| Q-12   | F5 em tela interna volta ao painel                                   | Ronald          | 19/10       | Aberta; prazo vencido; software inalterado |


### 11.2 Registros novos

Data de registro: 02/11/2026. Os prazos de resolução são propostos e o grupo confirma.

| ID   | Registro                                                                                                                                                                                   | Escopo                                      | Prazo                                                | Custo                                                               | Dono                                                                      | Data                                     |
| ---- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------- | ---------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------------- | ---------------------------------------- |
| Q-16 | Pessoas sem hora apontada: Rodrigo e os 4 da gerência (relatos pendentes). Ronald e Thiago só têm relato a partir de 19/10; de 07 a 16/10 não há relato de nenhum dos dois                 | Sem impacto direto                          | Impede medir o CR e calcular IDC; efeito no prazo NI | CR incompleto (14 h de 2 de 7 pessoas); IDC e ENT não calculáveis   | Gerência                                                                  | Registro 02/11; resolução proposta 04/11 |
| Q-17 | 1.4.1: o relato da base da API refere-se a 19 a 23/10, depois do fim planejado (12/10). O código está no repositório (informado pelo grupo). Conclusão e verificação do critério: NI       | Critério de 1.4.1 não verificado            | Fim planejado 12/10; fim real NI                     | NI                                                                  | Desenvolvimento (Rodrigo, responsável por 1.4.1 no Dicionário; confirmar) | Registro 02/11; resolução proposta 04/11 |
| Q-18 | 12 dos 13 pacotes com fim planejado até 02/11 (134 h de VP) estão sem critério verificado; 1.3.2 a 1.3.6 consomem a folga de 5 dias úteis até 10/11                                        | 1.3.2 a 1.3.6 falharam no SR1; os demais NI | Folga em uso; efeito no caminho crítico NI           | VA não creditado de 134 h de VP                                     | Gerência (verificação) com o desenvolvimento                              | Registro 02/11; resolução proposta 09/11 |
| Q-19 | O backend real (Express, Prisma, PostgreSQL, JWT) está sendo desenvolvido por Ronald e Thiago, mas o responsável pelo pacote 1.4.1 é Rodrigo. A RAM não reflete a divisão real do trabalho | 1.4.1                                       | NI                                                   | As 14 h de Ronald e Thiago já superam as 10 h planejadas para 1.4.1 | Gerência e desenvolvimento                                                | Registro 02/11; resolução proposta 04/11 |


## 12. Próximas ações

Prazos propostos pelo grupo; o grupo confirma.

| Ação                                                                                                                                                               | Responsável                      | Prazo                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------- | ---------------------------------- |
| Registrar, por pessoa, a semana em que a medição começou e quais semanas foram reconstituídas                                                                      | Gerência                         | 03/11                              |
| Coletar as horas dos 4 integrantes da gerência                                                                                                                     | Gerência                         | 03/11                              |
| Confirmar com Ronald e Thiago a que pacote da EAP pertencem as 14 h (6 h e 8 h); no caso de Thiago, o trabalho de 19/10, 23/10 e 02/11 não está em 1.3.3 nem 1.4.3 | Gerência                         | 03/11                              |
| Coletar horas por semana e por atividade de Rodrigo, e as semanas de 07 a 16/10 de Ronald e Thiago                                                                 | Gerência e desenvolvimento       | 04/11                              |
| Coletar datas reais, duração restante e esforço restante por atividade, com commits como evidência                                                                 | Gerência e desenvolvimento       | 04/11                              |
| Atualizar a RAM para refletir que Ronald e Thiago estão trabalhando em 1.4.1 (Q-19)                                                                                | Gerência                         | 04/11                              |
| Recalcular VP, VA, CR, índices, ENT e EPT e reenviar este relatório                                                                                                | Gerência                         | 05/11                              |
| Decidir CHG-03 a CHG-05                                                                                                                                            | Patrocinador                     | 06/11                              |
| Verificar o critério dos pacotes relatados como concluídos (retestar 1.3.2 a 1.3.6 só depois que o software mudar)                                                 | Gerência                         | 09/11                              |
| Corrigir as questões abertas e apresentar evidências de teste                                                                                                      | Desenvolvimento, donos indicados | Antes do início de 1.4.6, em 10/11 |