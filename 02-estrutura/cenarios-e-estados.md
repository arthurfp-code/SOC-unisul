# Sprint 2 — Cenários de uso, estados e feedbacks

**Projeto:** SOC-unisul
**Etapa:** Sprint 2 — Estrutura (issue #5)
**Data:** 11/2026

## 1. Cenário 1 — Camila localiza um alerta prioritário

**Contexto:** Camila inicia o turno às 8h e precisa fazer a triagem inicial dos alertas da madrugada antes da reunião das 9h. Os dados da tela são fictícios.

**Objetivo:** encontrar um alerta de severidade Alta que ainda esteja Aberto e descobrir qual ativo foi afetado e a que horas o evento aconteceu.

**Caminho esperado:**

1. Abre a visão geral e lê os indicadores do período "Últimas 24 horas".
2. Clica em "Ver alertas" e aguarda a lista carregar.
3. Aplica os filtros: Severidade "Alta" e Estado "Aberto". Os chips "Alta" e "Aberto" aparecem acima dos resultados.
4. Confere a contagem "6 alertas encontrados" e escolhe o registro mais recente, ALT-0001.
5. Na tela de detalhes, lê as linhas "Ativo afetado" (srv-app-03) e "Horário do evento" (12/11/2026 14:35).
6. Clica em "Voltar para a lista" e encontra os mesmos filtros ainda aplicados.

**Condição de sucesso:** Camila conclui as etapas 1 a 6 sem instruções do moderador, identificando corretamente o ativo e o horário, e volta para a lista com os filtros preservados.

**Dificuldades previstas e tratamentos:**

| Dificuldade | Tratamento na interface |
| --- | --- |
| Não saber onde aplicar os filtros | Filtros no topo da lista, com rótulos "Severidade" e "Estado" |
| Perder os filtros ao voltar do detalhe | Retorno preserva filtros e chips (RF10) |
| Não saber se o filtro está ativo | Chips visíveis com "x" para remover e contagem atualizada |
| Confundir severidade apenas por cor | Rótulo textual "Alta" em todos os registros |

## 2. Cenário 2 — Diego interpreta um indicador e consulta os eventos

**Contexto:** Diego prepara o relatório semanal de segurança e precisa explicar ao time a quantidade de alertas do período.

**Objetivo:** entender a distribuição dos alertas por severidade e encontrar os eventos que compõem um dos indicadores.

**Caminho esperado:**

1. Abre a visão geral e lê o bloco "Alta severidade: 14 — Últimas 24 horas".
2. Confere a barra de distribuição, que repete o valor em texto ao lado do rótulo.
3. Clica no bloco "Alta severidade", que leva à lista já filtrada por Severidade "Alta".
4. Ajusta o estado para "Aberto" e confere a contagem correspondente.
5. Abre um registro para conferir ativo e horário, confirmando a relação entre o indicador e a lista.
6. Volta para a visão geral pelo botão "Voltar para a visão geral".

**Condição de sucesso:** Diego explica corretamente o período e a quantidade de alertas de alta severidade e localiza a lista correspondente, sem interpretar os números fora do período indicado.

**Dificuldades previstas e tratamentos:**

| Dificuldade | Tratamento na interface |
| --- | --- |
| Número sem período de referência | Todo indicador mostra "Últimas 24 horas" no mesmo bloco |
| Indicador diferente da lista | Clique no indicador abre a lista já com o filtro aplicado, evitando contagem manual |
| Gráfico sem valores | Barras com rótulo e número em texto (RUA08) |

## 3. Tabela de estados e feedbacks da tarefa principal

| Estado | Gatilho | Informação apresentada | Ação seguinte |
| --- | --- | --- | --- |
| Carregamento | Abrir a lista ou alterar filtro | Blocos em esqueleto na área da lista e texto "Carregando alertas…" | Aguarda; nenhum clique necessário |
| Carregamento com navegação liberada | Troca de filtro com lista já aberta | Chips de filtro atualizados antes da tabela | A pessoa pode remover um chip enquanto carrega |
| Erro de consulta | Falha simulada na rede | "Não foi possível carregar os alertas. Verifique a conexão e tente novamente." | Botão "Tentar novamente" |
| Erro na pesquisa | Falha simulada ao buscar | "Não foi possível concluir a pesquisa. Tente de novo." | Botão "Tentar novamente" mantém o termo digitado |
| Sucesso com resultados | Consulta com registros | "12 alertas encontrados" e tabela com severidade, estado, ativo e horário | Selecionar um registro |
| Sem resultados | Filtros ou pesquisa sem correspondência | "Nenhum alerta encontrado com os filtros aplicados: Alta, Aberto." | Botão "Limpar filtros" |
| Sucesso sem correspondência na pesquisa | Pesquisa por ID inexistente | "Nenhum alerta corresponde a ALT-9999." | Botão "Limpar pesquisa" |
| Confirmação de ação | Marcar alerta como "Em análise" | Aviso "Alerta ALT-0001 marcado como Em análise." | "Desfazer" por 5 segundos |
| Confirmação de limpeza | Limpar filtros com lista vazia | "Filtros removidos. Mostrando 48 alertas." | Continua na lista completa |
| Retorno ao contexto | Voltar dos detalhes | Lista restaurada com chips e contagem anteriores | Repetir ou encerrar a tarefa |

### Regras de escrita das mensagens

1. A mensagem diz o que aconteceu e o que fazer em seguida; nenhuma mensagem é só o erro.
2. Os termos "Alta", "Aberto" e "Em análise" são os mesmos do filtro, do registro e do detalhe (RC02, RC03).
3. A contagem sempre aparece por extenso, com a palavra "alertas" no singular e no plural.
4. Aviso de dados fictícios presente na lista e no detalhe: "Dados de demonstração." (RC01, RC06).

## 4. Preparação da avaliação e do teste

### 4.1 Tarefa crítica selecionada

**Tarefa:** "Encontre um alerta de alta severidade que ainda esteja aberto e consulte qual ativo foi afetado e quando o evento ocorreu."

**Público:** profissionais ou estudantes familiarizados com uso de computador, sem conhecimento prévio da ferramenta. Participantes externos à equipe, com dados fictícios e sem coleta de dados pessoais.

### 4.2 Registro padronizado (a preencher em cada participação)

| Campo | Como registrar |
| --- | --- |
| Identificação do participante | Código fictício (P1, P2) e contexto breve, sem nome nem dados pessoais |
| Conclusão | Sim / Não / Parcialmente, sem ensinar o caminho |
| Tempo aproximado | Do início até a leitura do ativo e do horário |
| Obstáculos | Hesitações, erros, termos incompreendidos, pontos de abandono |
| Fala do participante | Trecho relevante sobre dúvida de rótulo ou estado |
| Ajuste proposto | O que mudaria na interface e por quê |

### 4.3 Marcos

- **19/11 — avaliação exploratória:** percurso da tarefa nos wireframes pela equipe, registrando dificuldades e melhorias em `03-esqueleto/avaliacao-exploratoria.md`.
- **26/11 — teste com participantes externos:** aplicação da tarefa com no mínimo dois participantes, registro em `evidencias/teste-usabilidade-2026-11-26.md` e melhoria incorporada justificada.

## 5. Cobertura dos critérios da issue

- [x] Contexto, objetivo, caminho esperado e condição de sucesso registrados para os dois cenários.
- [x] Gatilho, informação apresentada e ação seguinte definidos para carregamento, erro, sucesso, filtros sem resultados e confirmação.
- [x] Severidade e estado com termos consistentes e sinais textuais; períodos dos indicadores claros.
- [x] Tarefa de teste preparada, com registro de conclusão sem ajuda, hesitações e erros.
- [x] Documento salvo em `02-estrutura`, com links para o mapa e o fluxo.

## Referências

1. Mapa de navegação. `02-estrutura/mapa-navegacao.md`
2. Fluxo da tarefa prioritária. `02-estrutura/fluxo-tarefa-prioritaria.md`
3. Sprint 1 — Estratégia & Escopo (personas e requisitos). `01-estrategia-escopo/sprint-1-estrategia-escopo.md`
4. Orientações da A3 — seção 3 (teste mínimo de usabilidade).
