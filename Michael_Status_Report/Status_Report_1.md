# Status Report 1 — SubTracker

Verificação da entrega de front-end (Marco 1) · Grupo de gerência: Davi Luiz Rodrigues da Conceição, João Henrique Lima Gualberto, Michael Patrick Ferreira da Silva Borba e Vinicius da Silva Mendes

## 1. Data de status e período coberto

- **Data de status (corte):** 06/10/2026, data da entrega do front-end pela equipe de desenvolvimento.
- **Período coberto:** 04/08/2026 a 06/10/2026.
- **Entrega verificada:** front-end com backend simulado por `json-server` e `db.json`. A API própria (backend real) pertence à entrega seguinte e não é tratada como falta neste relatório.
- **Linha de base:** declaração do escopo (Plano do Projeto, seção 2.3), EAP, Dicionário da EAP (versão 2.1, 03/10/2026), pacotes 1.3.1 a 1.3.6, e matriz de rastreabilidade (Plano, seção 2.2).
- **Como foi verificado:** instalação seguindo o manual (`npm install`), `npm run build`, `npm run server` e `npm run dev`, e testes no navegador com contas de teste. A verificação foi feita até 12/10/2026 sobre a versão disponível no repositório. A equipe de desenvolvimento não forneceu commit ou tag do congelamento, então não é possível afirmar que a versão testada é idêntica à de 06/10 (Q-13).
- **Origem da evidência:** parte dos testes foi executada pelo grupo de gerência e parte pela ferramenta GitHub Copilot, que leu o repositório e executou a bateria de testes. O `db.json` foi copiado antes da bateria da ferramenta e restaurado ao final (SHA-256 `AE9F32537D06F05BA172146B1F486143C626A4A32D8C65C82785474031AC56B6`). Os resultados da ferramenta entram como evidência; a conclusão de cada pacote é do grupo. A base de teste continha um valor inserido pelo próprio grupo (Spotify trimestral de R$ 200.000.001,90); ele não é defeito da equipe de desenvolvimento e não entra nas questões.
- **Fora deste relatório:** cronograma, custo e valor agregado (serão tratados no Status Report 2). Os resultados abaixo comparam a entrega com o critério do Dicionário e não avaliam prazo.

## 2. Situação geral

**VERMELHO — a entrega não está pronta para recomendação de aceite.**

Justificativa, ligada a fatos do escopo:

- Dos seis pacotes verificados, **um passou** (1.3.1) e **cinco falharam** (1.3.2 a 1.3.6) no critério do Dicionário.
- A importação aceita arquivos incompatíveis (CSV com colunas diferentes e PDF) como "Analisado", com zero resultados, em vez de rejeitá-los.
- Não há tutorial de uso dentro da aplicação (pacote 1.3.6).
- O painel mostra uma cobrança vencida como "Em -7 dias".
- Não há exclusão de teto (UC12); definir zero mantém a categoria com teto de R$ 0,00.

**Recomendação ao patrocinador:** aceitar o pacote 1.3.1 e não aceitar os pacotes 1.3.2 a 1.3.6 neste corte. Pede-se decisão sobre as mudanças de escopo da seção 5 e nova verificação independente depois das correções. Este relatório registra a entrega verificada e uma recomendação; **não declara aceite formal de nenhum pacote**.

## 3. Escopo: verificado, pendente e não demonstrado

| Pacote | Resultado | Recomendação |
| --- | --- | --- |
| 1.3.1 — Estrutura de front-end e rotas | **Passou** | Aceitar |
| 1.3.2 — Assinaturas e dashboard | **Falhou** | Não aceitar |
| 1.3.3 — Serviços e cancelamento | **Falhou** | Não aceitar |
| 1.3.4 — Tetos e consumo orçamentário | **Falhou** | Não aceitar |
| 1.3.5 — Extratos e conciliação | **Falhou** | Não aceitar |
| 1.3.6 — Relatório e tutorial | **Falhou** | Não aceitar |

### 1.3.1 — Estrutura de front-end e rotas

- **Critério (Dicionário):** "Rotas e estrutura organizadas e navegáveis, com layout base estável para os módulos do sistema."
- **Resultado:** Passou.
- **Evidência:** `npm run build` concluiu sem erro (4); login levou ao painel (7); Início, Adicionar, Relatório, importação, perfil e detalhes abriram sem tela em branco (8); menu e cabeçalho mantiveram o layout (9); a 390 px não houve rolagem horizontal e a navegação móvel apareceu (10).
- **Ressalva:** F5 em tela interna mantém a sessão, mas volta ao painel, porque as telas internas ficam sob `/painel` (11). O resultado desse item divergiu entre testadores e está registrado como Q-12.
- **Não demonstrado:** uso do fluxo principal só com teclado (59), fora do critério deste pacote (Q-02).

### 1.3.2 — Assinaturas e dashboard

- **Critério:** "UC01–UC04 operacionais no front-end e consistentes com os dados de teste e a lógica da aplicação."
- **Resultado:** Falhou.
- **Operacional (passou):** criar assinatura e vê-la na listagem (13); persistência após F5 (14); edição refletida no painel (15); pausar e reativar com reflexo no total (16, 17); excluir com confirmação e persistência (18); bloqueio de valor vazio e negativo (19); histórico e "Confirmar Pagamento" persistindo (20); próximas cobranças em ordem cronológica (22).
- **Consistência (falhou):** a cobrança de Netflix de 05/10/2026 aparece no painel como "Em -7 dias" (23). O total mensal do painel confere com a soma das assinaturas ativas (24), inclusive com o valor atípico inserido pelo grupo no teste.
- **Nota:** o "-7" foi observado em 12/10; no corte de 06/10 seria "-1". O defeito é o mesmo: cobrança vencida exibida como contagem negativa.

### 1.3.3 — Serviços e cancelamento

- **Critério:** "UC06 e UC18 disponíveis na interface e com fluxo de cancelamento informado ao usuário."
- **Resultado:** Falhou.
- **Evidência:** o usuário consulta os serviços disponíveis (28) e o link "Cancelar no Provedor" aparece nos detalhes (29), mas não há passo a passo de cancelamento (30).
- **Não demonstrado:** a página externa de destino do link não foi aberta (54; Q-02).

### 1.3.4 — Tetos e consumo orçamentário

- **Critério:** "UC09–UC12 operacionais, com indicadores de consumo e atualização de valores orçamentários."
- **Resultado:** Falhou.
- **Evidência:** definir teto por categoria (33), alteração persistente (34), consumo versus teto no painel (35), consumo atualizado ao criar ou pausar assinatura (36) e indicação "Limite" quando excede (39). Não existe ação de excluir teto (37) e definir zero mantém a categoria com teto de R$ 0,00 (38), logo UC12 não é atendida.

### 1.3.5 — Extratos e conciliação

- **Critério:** "UC13 e UC14 funcionais; importação aceita CSV e rejeita layouts incompatíveis."
- **Resultado:** Falhou.
- **Evidência:** `teste.csv` válido (9 lançamentos) levou à revisão com seis serviços reconhecidos (40, 41); a confirmação criou as assinaturas e elas persistiram (42); desmarcar um lançamento impediu sua criação (44); reimportar não duplicou assinaturas (43), mas repetiu entradas no histórico de pagamentos.
- **Falhas:** CSV com colunas diferentes e PDF foram mostrados como "Analisado" com zero resultados, sem rejeição clara (47, 48); arquivo vazio fica sem mensagem (49).
- **Não demonstrado:** os limiares de importação do Plano (mínimo de 10 lançamentos e 80% de reconhecimento) não podem ser medidos com `teste.csv`, que tem 9 lançamentos (Q-09).

### 1.3.6 — Relatório e tutorial

- **Critério:** "UC17 e UC18 acessíveis na aplicação e com informações que apoiam a tomada de decisão do usuário."
- **Resultado:** Falhou.
- **Evidência:** relatório com distribuição por categoria, ranking e projeção; a projeção do mês seguinte e o custo anual conferem com o cálculo manual (R$ 272,70 × 12 = R$ 3.272,40) (50, 51, 52). Não foi encontrado tutorial de uso dentro da aplicação (53). Conta nova mostra zeros, sem mensagem explícita de lista vazia (55).
- **Não demonstrado:** abertura da página externa do link de cancelamento (54).

### As três perguntas do controle do escopo

1. **O que está na EAP deste marco foi entregue? Não integralmente.** Há estrutura navegável, painel, gestão de assinaturas, tetos, relatório e importação de CSV. Faltam o tutorial e a validação do formato de importação.
2. **O que foi entregue está na EAP? Em grande parte, sim.** As exceções são "Confirmar Pagamento" (56) e as telas "Criar Conta" e "Esqueceu a senha?" (57), registradas como CHG-04 e CHG-05.
3. **O que foi entregue atende ao aceite do Dicionário? Não integralmente:** um pacote passou e cinco falharam. Nenhum resultado equivale a aceite formal.

## 4. Requisitos do Marco 1 atendidos e pendentes

Rastreabilidade conforme Plano do Projeto, seção 2.2. "Sem pacote verificado" significa que nenhum pacote de front-end com critério passado cobre integralmente o requisito neste corte; não significa que o requisito foi excluído. As APIs (pacotes 1.4.x) ficam para a entrega seguinte.

| Requisito                                                                            | Pacotes      | Situação no corte                                     | Lacuna                                                                                                     |
| ------------------------------------------------------------------------------------ | ------------ | ----------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| **RQ01** — Total mensal, próximas cobranças ordenadas e consumo frente às metas      | 1.3.2, 1.3.4 | Parcial; sem pacote verificado                        | Total, ordenação e consumo funcionam (22, 24, 35); "Em -7 dias"; 1.3.2 e 1.3.4 falharam                    |
| **RQ02** — Identificar assinaturas recorrentes por extrato e confirmar a conciliação | 1.3.5        | Parcial; sem pacote verificado                        | Detecção e confirmação persistem (40 a 42); falta rejeição de layout e verificação dos limiares            |
| **RQ03** — Cadastrar, consultar, editar, pausar e excluir assinatura com histórico   | 1.3.2        | Operações atendidas; sem pacote verificado            | Todas as operações persistem (13 a 20); o pacote falhou por consistência (Q-01)                            |
| **RQ04** — Definir teto por categoria e acompanhar consumo                           | 1.3.4        | Parcial; sem pacote verificado                        | Falta exclusão de teto (UC12)                                                                              |
| **RQ05** — Acessar cancelamento do provedor a partir da assinatura                   | 1.3.3, 1.3.6 | Parcial; sem pacote verificado                        | Link existe (29); falta o tutorial e o fluxo de cancelamento informado                                     |
| **RQ06** — Distribuição, ranking, projeção do mês seguinte e custo anual             | 1.3.6        | Funções de relatório atendidas; sem pacote verificado | Cálculos conferidos (50 a 52); falta o tutorial                                                            |
| **RQ07** — Usabilidade móvel e perfis distintos (Usuário e Administrador)            | 1.3.1        | Parcial                                               | Móvel atendido (10); perfis distintos não existem (31)                                                     |
| **RQ08** — CSV como formato; sem pagamentos nem conexão direta a bancos ou cartões   | 1.3.5        | Parcial                                               | Não há pagamento real nem conexão a banco ou cartão (58); a validação do formato CSV é deficiente (47, 48) |

Nenhum dos oito requisitos está integralmente atendido neste corte.

## 5. Questões e mudanças solicitadas

### Registro de questões

Prazos propostos pela gerência. Os donos seguem o Dicionário da EAP e precisam ser confirmados pela equipe de desenvolvimento (Q-14).

| ID   | Questão e evidência                                                                                                                                                   | Pacote / requisito  | Dono            | Prazo      |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- | --------------- | ---------- |
| Q-01 | Cobrança vencida exibida como "Em -7 dias" no painel (23). Corrigir estado e texto de cobrança vencida.                                                               | 1.3.2 / RQ01        | Ronald          | 19/10/2026 |
| Q-02 | Não demonstrados: abertura da página externa do link de cancelamento (54) e fluxo principal só com teclado (59). Reteste independente.                                | 1.3.1, 1.3.3, 1.3.6 | Gerência        | 16/10/2026 |
| Q-05 | Não há exclusão de teto; definir zero mantém a categoria com R$ 0,00 (37, 38; UC12).                                                                                  | 1.3.4 / RQ04        | Thiago          | 19/10/2026 |
| Q-07 | CSV com colunas diferentes e PDF chegam à revisão como "Analisado" com zero resultados; arquivo vazio não gera mensagem (47 a 49).                                    | 1.3.5 / RQ02, RQ08  | Rodrigo         | 19/10/2026 |
| Q-08 | Reimportar o mesmo arquivo repete entradas no histórico de pagamentos (43).                                                                                           | 1.3.5 / RQ02        | Rodrigo         | 19/10/2026 |
| Q-09 | `teste.csv` tem 9 lançamentos; os limiares do Plano (mínimo de 10 lançamentos, 80% de reconhecimento) não podem ser medidos (41). Fornecer arquivo de teste adequado. | 1.3.5 / RQ02        | Rodrigo         | 16/10/2026 |
| Q-10 | Não há tutorial de uso dentro da aplicação (53); a orientação de cancelamento se limita a um link e uma frase curta (30).                                             | 1.3.6 / RQ05, RQ06  | Ronald e Thiago | 19/10/2026 |
| Q-11 | Conta nova abre painel e relatório com zeros, sem mensagem explícita de lista vazia (55).                                                                             | 1.3.6               | Ronald          | 19/10/2026 |
| Q-12 | F5 em tela interna volta ao painel; as telas internas ficam sob `/painel` (11). Resultado divergente entre testadores; reteste.                                       | 1.3.1               | Ronald          | 19/10/2026 |


### Registro de mudanças e decisões de escopo

Não foi localizada solicitação de mudança aprovada para nenhum dos itens abaixo (62). Até a decisão do patrocinador, a linha de base original permanece vigente.

| ID     | Mudança ou esclarecimento                                                       | Situação observada                                                             | Decisão pedida ao patrocinador                                                                   | Prazo      |
| ------ | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ---------- |
| CHG-03 | UC12: exclusão real do teto ou "definir zero" como substituto. Ver Q-05.        | Definir zero mantém a categoria com R$ 0,00.                                   | Aprovar a interpretação e atualizar a linha de base, ou exigir a exclusão.                       | 16/10/2026 |
| CHG-04 | Ação "Confirmar Pagamento", fora da EAP, feita sem solicitação de mudança (56). | Registra "Pago" e avança a próxima cobrança; não processa pagamento real (58). | Incorporar formalmente ao escopo, ou registrar como detalhe interno do pacote com justificativa. | 16/10/2026 |
| CHG-05 | Telas "Criar Conta" e "Esqueceu a senha?" (57).                                 | Presentes na aplicação; falta confirmar se constam na linha de base.           | Confirmar se estão no escopo ou incorporá-las formalmente.                                       | 16/10/2026 |
