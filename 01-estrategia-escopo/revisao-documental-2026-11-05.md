# Revisão documental da Sprint 1 — 05/11/2026

Projeto: SOC-unisul  
Disciplina: IHC & UX — A3 2026.2  
Referência: [Sprint 1 — Estratégia e escopo](sprint-1-estrategia-escopo.md)  
Tarefa relacionada: [issue #2](https://github.com/arthurfp-code/SOC-unisul/issues/2)

## Por que fizemos este registro

A Sprint 1 já havia reunido a definição do problema, duas proto-personas, uma comparação de soluções existentes e os requisitos para a interface. Este arquivo organiza a **revisão documental** realizada em 05/11/2026 e deixa as decisões de projeto mais fáceis de conferir. Trata-se de uma conferência técnica do conteúdo escrito, não de um teste com usuários nem de uma reunião de revisão coletiva da equipe.

## 1. Coerência entre o problema e as personas

O problema descrito no relatório é a dificuldade de identificar alertas importantes quando há muitas informações na mesma interface. Isso se conecta diretamente à necessidade principal de **Camila**, que precisa localizar os alertas mais urgentes e consultar os detalhes. **Diego** representa um uso complementar: entender os números gerais e chegar aos eventos que explicam esses indicadores.

Os dois perfis têm funções diferentes no projeto, o que evita criar telas sem uma tarefa clara. Ambos permanecem como **proto-personas fictícias**. Não há registro de pesquisa de campo que autorize tratá-los como perfis validados.

## 2. Coerência entre requisitos e fluxo principal

A tarefa escolhida no relatório é: localizar um alerta de alta severidade em estado aberto, identificar o ativo afetado e verificar quando o evento ocorreu.

| Passo | O que deve aparecer na interface | Requisitos associados |
| --- | --- | --- |
| Abrir a visão geral | Indicadores com rótulos e período | RF01, RC04, RC05 |
| Acessar alertas | Lista com dados fictícios reconhecíveis | RF02, RC01, RC06 |
| Aplicar filtros | Severidade **Alta** e estado **Aberto**, com seleção visível | RF04, RF05, RUA02, RUA04 |
| Escolher um evento | Identificador e dados essenciais do alerta | RF02, RF03 |
| Consultar os detalhes | Ativo afetado, horário e contexto do evento | RF03, RC04 |
| Voltar para a lista | Retorno claro, preservando filtros quando viável | RF10, RUA07 |

**Resultado da análise:** o fluxo tem suporte nos requisitos já definidos. A pesquisa textual (RF06), a simulação de mudança de estado (RF08) e o gráfico (RF09) são complementos; não precisam bloquear a demonstração da tarefa principal.

## 3. Decisões para evitar inconsistências na próxima sprint

1. **Filtros combinados:** a lista deve permitir buscar alertas pela combinação de severidade e estado, e não apenas por um critério de cada vez.
2. **Rótulos explícitos:** o texto “Alta” e o estado “Aberto” devem acompanhar as cores. A interface não deve depender só da cor para distinguir situações.
3. **Horário e ativo:** os detalhes precisam mostrar os dois dados pedidos pela tarefa, de maneira legível.
4. **Indicadores e lista:** toda métrica exibida deve ter período e regra de contagem claros para não contradizer os registros apresentados.
5. **Retorno:** ao voltar dos detalhes, os filtros aplicados devem ser preservados sempre que a solução adotada permitir.
6. **Estados de interface:** prever carregamento, erro e lista sem resultados. Esses estados devem explicar o que aconteceu e o que o usuário pode fazer.
7. **Limite de escopo:** nenhum botão do protótipo deve ser descrito como ação de resposta a um incidente real; eventuais alterações de estado são apenas simuladas.

Essas decisões detalham o documento de origem. Não representam funcionalidades já implementadas.

## 4. Conferência dos materiais da Sprint 1

| Material | Verificação documental em 05/11 |
| --- | --- |
| Problema e objetivo | Compatíveis com a proposta de reduzir o esforço para localizar e entender alertas |
| Público-alvo | Coerente com o uso por analistas de segurança e acompanhamento operacional |
| Camila e Diego | Atendem a tarefas distintas e permanecem identificados como hipóteses |
| Wazuh e Microsoft Sentinel | Referências de solução similares presentes com fontes oficiais; não são apresentados como testes práticos |
| RF01 a RF10 | Abrangem o fluxo central e funções adicionais, com prioridade definida |
| Requisitos de conteúdo | Preveem identificação de dados fictícios, padronização de termos e contextualização de horários |
| Usabilidade e acessibilidade | Contêm orientações de rótulos, contraste, mensagens e adaptação a telas |
| Escopo | Distingue protótipo de UX de um SOC operacional |
| Fluxo prioritário | Possui início, filtragem, consulta aos detalhes e retorno |

## 5. Pendências que ficam para etapas próprias

- Validar as hipóteses das personas com participantes representativos do público-alvo, quando a pesquisa for executada.
- Desenvolver o mapa de navegação, fluxos detalhados, wireframes e protótipo na Sprint 2.
- Realizar os testes de usabilidade depois de existir uma interface demonstrável.
- Obter e registrar a confirmação dos integrantes sobre a revisão coletiva e a atribuição específica de suas contribuições. O relato de colaboração do grupo está documentado, mas não substitui essa confirmação.

## 6. Evidências e rastreabilidade

- [Documento-base da Sprint 1](sprint-1-estrategia-escopo.md)
- [Registro da equipe](contribuicoes-equipe.md)
- [Issue #1](https://github.com/arthurfp-code/SOC-unisul/issues/1)
- [Issue #2](https://github.com/arthurfp-code/SOC-unisul/issues/2)
- [Histórico de commits](https://github.com/arthurfp-code/SOC-unisul/commits/main/)

Este registro foi preparado com base nos materiais existentes no repositório. A publicação e a identificação do commit desta atualização devem ser adicionadas à issue #2 após o envio das alterações para o GitHub.
