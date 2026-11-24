# Sprint 3 — Avaliação exploratória dos wireframes

**Projeto:** SOC-unisul
**Etapa:** Sprint 3 — Esqueleto (issue #6)
**Data:** 11/2026

## 1. Objetivo

Avaliar a tarefa prioritária nos wireframes antes de investir na identidade visual, registrando as dificuldades encontradas e as melhorias incorporadas. A avaliação cobre a tarefa: "Encontre um alerta de alta severidade que ainda esteja aberto e consulte qual ativo foi afetado e quando o evento ocorreu."

## 2. Método

Inspeção heurística com percurso da tarefa nos arquivos de `wireframes/`, percorrendo as telas na ordem em que uma pessoa as usaria. Foram consideradas as heurísticas pertinentes ao escopo:

1. Visibilidade do estado do sistema.
2. Correspondência entre o sistema e o mundo real.
3. Controle e liberdade do usuário.
4. Consistência e padrões.
5. Prevenção de erros.
6. Reconhecimento em vez de memorização.
7. Flexibilidade e eficiência de uso.
8. Estética e design minimalista.
9. Ajudar a reconhecer, diagnosticar e corrigir erros.
10. Ajuda e documentação.

Participaram da inspeção Rafael, Arthur e Matheus, com revisão de Juan. A avaliação é interna e exploratória; ela não substitui o teste com participantes externos previsto para 26/11.

## 3. Percurso da tarefa

| Etapa | Tela | Resultado do percurso |
| --- | --- | --- |
| Abrir a visão geral | `01-visao-geral.html` | Indicadores com título, valor e período no mesmo bloco |
| Ir para a lista | `02-lista-alertas.html` | Botão único de saída; lista já chega com filtros de exemplo |
| Aplicar filtros Alta e Aberto | `02-lista-alertas.html` | Chips visíveis, contagem "6 alertas encontrados" |
| Escolher um alerta | `02-lista-alertas.html` | Registro ALT-0001 com severidade, estado, ativo e horário na mesma linha |
| Ler ativo e horário | `03-detalhe-alerta.html` | Linhas próprias com os rótulos usados na tarefa |
| Voltar à lista | `03-detalhe-alerta.html` → `02-lista-alertas.html` | Retorno explícito no topo, filtros mantidos |

## 4. Achados e melhorias incorporadas

| # | Achado | Heurística | Severidade | Melhoria incorporada | Onde aparece |
| --- | --- | --- | --- | --- | --- |
| 1 | O período dos indicadores ficava apenas no título da página | Visibilidade do estado | Alta | Período repetido em cada bloco de indicador e na distribuição | `01-visao-geral.html` |
| 2 | A distribuição por severidade dependia só das cores das barras | Correspondência / acessibilidade | Alta | Valor em texto ao lado de cada barra, com a palavra "alertas" | `01-visao-geral.html` |
| 3 | Não havia como saber quais filtros estavam ativos após abrir um registro | Reconhecimento | Alta | Chips "Alta" e "Aberto" acima da tabela, com "x" para remover | `02-lista-alertas.html` |
| 4 | O retorno do detalhe para a lista refazia a filtragem | Controle e liberdade | Alta | Retorno explícito "Voltar para a lista (filtros mantidos)" | `03-detalhe-alerta.html` |
| 5 | O rótulo "Alto" em um documento e "Alta" na tela geravam dúvida | Consistência | Média | Termo único "Alta" em filtro, lista, detalhe e documentos | mapa de navegação, wireframes |
| 6 | Mensagem de erro sem saída obrigaria a recarregar a página | Recuperar erros | Alta | Erro com "Tentar novamente" na própria área da lista | `04-estados.html` |
| 7 | Lista vazia não dizia por que não havia resultados | Reconhecimento | Média | Mensagem repete os filtros aplicados e oferece "Limpar filtros" | `04-estados.html` |
| 8 | Pesquisa sem resultado obrigaria a digitar de novo | Prevenção de erros | Média | Termo preservado no campo, com "Limpar pesquisa" | `04-estados.html` |
| 9 | "Marcar em análise" sem aviso podia ser clicado sem querer | Prevenção de erros | Média | Confirmação com "Desfazer" por 5 segundos | `03-detalhe-alerta.html`, `04-estados.html` |
| 10 | Ativo afetado aparecia abreviado na lista | Reconhecimento | Baixa | Nome completo no detalhe, abreviação só na tabela | `03-detalhe-alerta.html` |

## 5. Justificativas das decisões de interface

| Decisão | Por que ajuda |
| --- | --- |
| Rótulos textuais em severidade e estado | Reduz ambiguidade para quem não distingue cores e mantém a leitura em telas de baixo contraste (RUA02, WCAG 2.2) |
| Período no mesmo bloco do indicador | Evita interpretação de número fora de contexto, dificuldade apontada na persona Diego |
| Chips de filtro sempre visíveis | A pessoa reconhece o estado da busca sem memorizar o que digitou antes |
| Retorno que preserva filtros | Corta dois passos da tarefa e evita refazer a filtragem a cada consulta (RF10) |
| Mensagens com ação de recuperação | Nenhum erro exige recarregar a página ou voltar ao início (RF07) |
| Sem menu lateral | Menos caminhos para aprender; a tarefa usa três telas |
| Confirmação com desfazer | Permite errar o clique sem consequência permanente |

## 6. Esforço cognitivo

- **Memorização:** os rótulos da lista são idênticos aos dos filtros; não há sinônimos para decorar.
- **Ambiguidade:** todo indicador traz período; toda severidade traz palavra.
- **Probabilidade de erro:** ações destrutivas simuladas têm confirmação; filtros têm limpeza em um clique.
- **Esforço de leitura:** a tarefa principal cabe em três telas, sem submenu.

## 7. Registro da avaliação

| Campo | Registro |
| --- | --- |
| Data | 19/11/2026 |
| Tipo | Avaliação exploratória interna (inspeção heurística) |
| Participantes | Rafael, Arthur, Matheus (execução) e Juan (revisão) |
| Tarefa avaliada | Encontrar alerta de alta severidade aberto e consultar ativo e horário |
| Conclusão | Sim, sem necessidade de instrução adicional no percurso |
| Dificuldades | Achados 1 a 10 da seção 4 |
| Melhorias incorporadas | As dez da seção 4, aplicadas nos wireframes desta pasta |
| Pendência | Repetir a tarefa com participantes externos em 26/11 e registrar conclusão, obstáculos e ajustes |

## 8. Cobertura dos critérios da issue

- [x] Wireframes de visão geral, filtros Alta/Aberto, detalhe e retorno à lista.
- [x] Carregamento, erro e lista vazia, preservando filtros e rótulos de severidade.
- [x] Tarefa avaliada, com dificuldades e melhorias registradas.
- [x] Artefatos em `03-esqueleto`, com link no README e commit correspondente.

## Referências

1. Mapa de navegação. `02-estrutura/mapa-navegacao.md`
2. Fluxo da tarefa prioritária. `02-estrutura/fluxo-tarefa-prioritaria.md`
3. Cenários e estados. `02-estrutura/cenarios-e-estados.md`
4. NIELSEN, J. Heurísticas de usabilidade. https://www.nngroup.com/articles/ten-usability-heuristics/
5. W3C WAI. WCAG 2.2 — Understanding Success Criterion 1.4.3: Contrast (Minimum).
   https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html
