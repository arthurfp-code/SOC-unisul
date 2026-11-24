# Sprint 2 — Mapa de navegação e rótulos

**Projeto:** SOC-unisul
**Etapa:** Sprint 2 — Estrutura (issue #3)
**Data:** 11/2026

## 1. Objetivo deste documento

Transformar os requisitos da Sprint 1 em um mapa de navegação com hierarquia de informações, priorizando a consulta de alertas por Camila e a leitura de indicadores por Diego. O documento define as seções do protótipo, os caminhos de entrada e retorno, a relação com os requisitos RF01 a RF10 e a nomenclatura de filtros, indicadores e eventos.

## 2. Hierarquia das seções

O protótipo terá três telas principais e um grupo de estados que aparece dentro delas. Não haverá menu de múltiplos níveis: o fluxo é curto e a volta é sempre explícita.

```
SOC-unisul
├── Visão geral (dashboard)                     RF01, RF09
│   ├── Indicadores resumidos
│   ├── Distribuição dos alertas
│   └── Acesso para a lista de alertas
├── Lista de alertas                            RF02, RF04, RF05, RF06
│   ├── Filtros de severidade
│   ├── Filtros de estado
│   ├── Pesquisa por identificador ou texto
│   └── Resultados (registros fictícios)
│       └── Detalhes do alerta                  RF03, RF08
│           └── Retorno à lista com filtros     RF10
└── Estados da interface                        RF07
    ├── Carregamento
    ├── Erro de consulta (com nova tentativa)
    ├── Lista sem resultados (com limpar filtros)
    └── Confirmação de ação simulada
```

## 3. Telas, entrada e retorno

| Tela | Como entra | Como retorna | O que precisa permanecer |
| --- | --- | --- | --- |
| Visão geral | Ponto inicial do protótipo | Botão na barra superior | Período de referência dos indicadores |
| Lista de alertas | Botão "Ver alertas" na visão geral, ou indicador clicável | Botão "Voltar para a visão geral" | — |
| Detalhes do alerta | Clique em um registro da lista | Botão "Voltar para a lista" | Filtros e pesquisa aplicados antes da abertura |
| Estados (carregamento, erro, vazio) | Aparecem na própria lista, sem tela separada | Ação dentro da mensagem | Filtros permanecem visíveis em todos os estados |

O retorno da tela de detalhes para a lista preserva os filtros (RF10). Essa decisão atende diretamente à necessidade da persona Camila de consultar detalhes sem perder a referência do alerta selecionado.

## 4. Relação das áreas com requisitos e personas

| Área do mapa | Requisitos | Persona atendida | Prioridade no MVP |
| --- | --- | --- | --- |
| Visão geral com indicadores | RF01, RF09 | Diego | Essencial |
| Lista de alertas | RF02 | Camila e Diego | Essencial |
| Filtro de severidade | RF04 | Camila | Essencial |
| Filtro de estado | RF05 | Camila | Essencial |
| Pesquisa por texto ou identificador | RF06 | Camila | Importante |
| Detalhes do alerta | RF03 | Camila | Essencial |
| Estados de interface | RF07 | Ambas | Essencial |
| Confirmação de ação simulada | RF08 | Camila | Importante |
| Retorno com filtros preservados | RF10 | Camila | Importante |

### Prioridades do MVP

1. Visão geral, lista, filtros de severidade e estado, detalhes e retorno: sem esses itens não há tarefa principal demonstrável.
2. Estados de carregamento, erro e lista vazia: exigidos pela issue como parte do fluxo e pelo RF07.
3. Pesquisa por texto e confirmação de ação simulada: entram depois do essencial, pois melhoram a experiência sem quebrar o fluxo principal.
4. Gráfico de distribuição (RF09): fica na visão geral, com título, valores e período; pode ser substituído por barras com rótulos textuais.

## 5. Rótulos e nomenclatura

### 5.1 Severidade

| Rótulo exibido | Como aparece | Uso |
| --- | --- | --- |
| Alta | Texto "Alta" + marcador sólido + ícone de exclamação | Nunca apenas cor |
| Média | Texto "Média" + marcador com contorno | Nunca apenas cor |
| Baixa | Texto "Baixa" + marcador claro | Nunca apenas cor |

O filtro usa os mesmos três termos. Não há sinônimos como "crítico" ou "alto" nas telas: RC02 exige termos consistentes.

### 5.2 Estado do alerta

| Rótulo exibido | Significado |
| --- | --- |
| Aberto | Alerta ainda não foi tratado |
| Em análise | Alguém está avaliando o evento |
| Resolvido | Tratamento concluído |

O filtro de estado usa exatamente esses três termos (RC03). O padrão de exibição na lista é o estado em texto ao lado do identificador do evento.

### 5.3 Filtros e pesquisa

- Filtro de severidade: rótulo "Severidade", opções Todas / Alta / Média / Baixa.
- Filtro de estado: rótulo "Estado", opções Todos / Aberto / Em análise / Resolvido.
- Pesquisa: rótulo "Pesquisar", placeholder "ID do alerta ou texto", botão "Buscar".
- Filtros ativos aparecem como chips removíveis acima dos resultados, com o texto "Filtros aplicados: Alta, Aberto".
- Contagem sempre visível: "12 alertas encontrados" ou "Nenhum alerta encontrado".

### 5.4 Indicadores da visão geral

| Rótulo | O que significa | Período exibido |
| --- | --- | --- |
| Alertas no período | Total de registros fictícios no intervalo | Últimas 24 horas |
| Alta severidade | Registros com severidade Alta | Últimas 24 horas |
| Abertos | Registros com estado Aberto | Últimas 24 horas |
| Em análise | Registros com estado Em análise | Últimas 24 horas |

Todo indicador mostra título, valor e período de referência no mesmo bloco (RC04, RC05). A distribuição por severidade usa barras com rótulo e valor em texto, para não depender só de cores (RUA02, RUA08).

### 5.5 Eventos e identificadores

- Identificador no formato ALT-0001, sempre visível na lista e no detalhe.
- Horário no formato 12/11/2026 14:35, com fuso informado uma vez no rodapé da lista: "Horário de Brasília (UTC-3). Dados fictícios para demonstração."
- Ativo afetado sempre com o nome completo do equipamento, sem abreviação no detalhe.

## 6. Decisões registradas

| Pergunta | Decisão |
| --- | --- |
| Por que sem menu lateral? | O protótipo tem três telas; menu lateral criaria caminhos que a tarefa principal não usa e aumentaria o esforço de memória. |
| Por que os filtros ficam na lista e não em tela separada? | Camila aplica os filtros e lê os resultados no mesmo contexto, evitando idas e vindas. |
| Por que o retorno da lista para o detalhe preserva filtros? | Sem isso, a pessoa teria que refazer a filtragem a cada consulta (RF10, RUA05). |
| Por que rótulo textual na severidade? | Cor sozinha falha para quem tem deficiência visual e em telas com pouco contraste (RUA02, WCAG 2.2). |
| Por que estados dentro da lista? | Mensagens de carregamento e erro precisam aparecer onde a lista deveria estar, mantendo filtros e cabeçalho visíveis. |

## 7. Cobertura dos critérios da issue

- [x] Visão geral, lista, detalhes e demais seções mapeados, com entrada e retorno.
- [x] Áreas relacionadas aos requisitos RF01 a RF10 e às personas Camila e Diego.
- [x] Prioridades do MVP explícitas.
- [x] Rótulos de severidade e estado distintos; nomes consistentes para filtros, indicadores e eventos.
- [x] Documento salvo em `02-estrutura`, com link no README.

## Referências

1. Sprint 1 — Estratégia & Escopo. `01-estrategia-escopo/sprint-1-estrategia-escopo.md`
2. W3C WAI. Understanding Success Criterion 1.4.3: Contrast (Minimum), WCAG 2.2.
   https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html
3. Requisitos de conteúdo e usabilidade da Sprint 1 (RC01–RC06, RUA01–RUA08).
