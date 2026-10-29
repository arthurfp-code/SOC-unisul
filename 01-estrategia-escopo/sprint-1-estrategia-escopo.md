# Sprint 1 — Estratégia & Escopo

**Projeto:** SOC-unisul — dashboard web para monitoramento de segurança  
**Unidade curricular:** IHC & UX / A3 2026.2  
**Etapa:** Sprint 1 — Estratégia & Escopo  
**Status:** primeira versão documental; personas e necessidades são hipóteses de design a validar.

> Madgascar

## 1. Visão do projeto

O SOC-unisul propõe um dashboard web para apoiar a visualização e a triagem inicial de eventos de segurança. A interface deverá ajudar a pessoa responsável pelo monitoramento a identificar alertas prioritários, compreender seu contexto e consultar informações importantes sem depender de uma tela desorganizada.

O foco desta A3 é IHC/UX, documentação, prototipação e validação da experiência. O projeto não pretende construir um centro de operações de segurança real nem conectar a interface a sistemas de produção. O protótipo utilizará dados fictícios e deixará claras as ações que forem apenas simuladas.

## 2. Contexto e problema

### Contexto de uso

Em um ambiente de operações de segurança, eventos podem chegar de diferentes fontes e variar em severidade, horário, ativo afetado e estado de tratamento. A pessoa que monitora precisa reconhecer o que merece atenção primeiro, localizar detalhes e compreender o próximo passo.

### Problema central

Quando muitos eventos são apresentados sem hierarquia, filtros claros ou informação contextual, pode ser difícil encontrar alertas importantes, comparar prioridades e entender o que exige atenção. Isso aumenta o esforço para interpretar a tela e pode tornar a triagem menos eficiente.

**Declaração do problema:** profissionais que monitoram eventos de segurança precisam de uma interface que organize os alertas por prioridade e contexto, permita localizar eventos relevantes e apresente detalhes legíveis para apoiar a triagem inicial.

Esta declaração é a hipótese inicial do projeto, baseada no tema existente no README do repositório. Não representa resultados de entrevistas. A equipe deverá validá-la com pessoas representativas do público sempre que possível.

## 3. Público-alvo

**Público primário:** analistas de segurança da informação que acompanham alertas e fazem triagem inicial.

**Público secundário:** estudantes e profissionais em formação na área de cibersegurança, além de pessoas que precisam acompanhar o panorama geral dos alertas.

### Necessidades previstas

- Entender o estado geral do monitoramento de relance.
- Perceber quais alertas merecem atenção prioritária.
- Filtrar e localizar eventos por severidade, estado e período.
- Consultar os detalhes de um alerta sem perder a referência da lista.
- Distinguir claramente severidade, estado e horário.
- Consultar as informações essenciais em diferentes larguras de tela.

## 4. Objetivos

### Objetivo geral

Projetar e avaliar um protótipo de dashboard de SOC que torne a triagem visual de alertas mais organizada, compreensível e consistente.

### Objetivos específicos

1. Apresentar um resumo do cenário de segurança com métricas e alertas recentes.
2. Facilitar a priorização por severidade e estado.
3. Permitir pesquisar e filtrar a lista de alertas.
4. Apresentar detalhes relevantes, como origem, horário, ativo afetado e descrição.
5. Definir estados claros de carregamento, erro, ausência de resultados e confirmação.
6. Aplicar princípios básicos de acessibilidade, legibilidade e responsividade.
7. Validar um fluxo prioritário com pelo menos duas pessoas externas à equipe e registrar melhorias.

### Indicadores que serão usados na avaliação

Estes são indicadores propostos para o teste futuro, não resultados já obtidos.

- A pessoa localiza um alerta de severidade alta sem receber instruções sobre onde clicar.
- A pessoa aplica e remove um filtro e consegue reconhecer quais critérios estão ativos.
- A pessoa identifica a severidade e o estado sem depender exclusivamente da cor.
- O moderador registra conclusão, hesitações, erros e termos que não foram compreendidos.
- As observações do teste originam pelo menos uma decisão documentada sobre a interface.

## 5. Personas iniciais (proto-personas)

As duas personas a seguir são **proto-personas hipotéticas** criadas para orientar o primeiro desenho da interface a partir do público definido no projeto. Não são entrevistas reais nem dados demográficos pesquisados. A equipe deverá validar, corrigir ou substituir os perfis durante a pesquisa.

### Persona 1 — Analista de segurança em triagem

**Nome fictício:** Camila Martins  
**Perfil:** analista júnior de segurança que acompanha alertas e encaminha casos para uma análise mais profunda.  
**Objetivo principal:** identificar quais alertas precisam de atenção e reunir contexto para a triagem inicial.

**Necessidades**
- Ver primeiro alertas críticos ou altos ainda abertos.
- Entender por que um alerta apareceu e qual ativo está envolvido.
- Filtrar por severidade e estado.
- Consultar horário, origem e descrição sem abrir muitas telas.
- Receber feedback quando uma ação é executada.

**Frustrações e barreiras hipotéticas**
- Listas extensas sem prioridade visual.
- Uso de cores sem texto explicativo.
- Termos técnicos que não estão definidos.
- Filtros ativos que não ficam visíveis.
- Ações sem confirmação ou indicação de sucesso/erro.

**Cenário de uso:** no início do turno, Camila abre o dashboard, verifica o volume de alertas, filtra os itens de severidade alta ainda abertos, seleciona um resultado e consulta a origem, o ativo afetado, o horário e a descrição.

**Critério de sucesso:** consegue encontrar um alerta correspondente aos critérios da tarefa e explicar sua prioridade com base nas informações da interface, sem ajuda do moderador.

### Persona 2 — Responsável pelo panorama operacional

**Nome fictício:** Diego Almeida  
**Perfil:** profissional que acompanha indicadores operacionais e comunica à equipe se há acúmulo de alertas ou mudanças relevantes. Não necessariamente investiga tecnicamente cada evento.  
**Objetivo principal:** compreender o panorama geral e acompanhar os alertas por estado e prioridade.

**Necessidades**
- Ver indicadores resumidos com seus significados.
- Distinguir volume total, alertas abertos e alertas críticos.
- Consultar o histórico dentro de um intervalo definido.
- Interpretar gráficos e tabelas com rótulos claros.
- Encontrar a lista de eventos relacionada a um indicador.

**Frustrações e barreiras hipotéticas**
- Métricas sem período de referência ou definição.
- Gráficos sem rótulos claros.
- Indicadores que dependem apenas de vermelho ou verde.
- Números diferentes entre o resumo e a lista.
- Excesso de detalhes técnicos na primeira tela.

**Cenário de uso:** em um acompanhamento da equipe, Diego abre o resumo, verifica a distribuição dos alertas por severidade e estado, consulta o histórico do período e abre a lista para conferir um aumento de alertas relevantes.

**Critério de sucesso:** consegue explicar o panorama apresentado e localizar os eventos que dão contexto a um indicador, sem interpretar incorretamente os rótulos.

## 6. Análise de soluções similares

A análise abaixo foi feita a partir de documentação oficial pública. Ela identifica funcionalidades e padrões documentados; não equivale a um teste prático de usabilidade nem comprova que uma solução seja mais fácil de usar do que outra.

### 6.1 Wazuh Dashboard

**Fontes oficiais:**
- [Wazuh Dashboard — Components](https://documentation.wazuh.com/current/getting-started/components/wazuh-dashboard.html)
- [Navigating the Wazuh dashboard](https://documentation.wazuh.com/current/user-manual/wazuh-dashboard/navigating-the-wazuh-dashboard.html)

**O que a documentação apresenta**
- Interface para visualizar, analisar e gerenciar dados de segurança.
- Dashboards voltados a temas como threat hunting, detecção de malware e monitoramento de integridade de arquivos.
- Monitoramento de agentes e recursos para análise dos eventos gerados.

**Padrões úteis para o SOC-unisul**
- Separar uma visão geral da investigação detalhada.
- Organizar dados por tarefa ou área de monitoramento.
- Tornar o estado do ambiente visível sem obrigar a pessoa a explorar todos os registros de imediato.

**Decisão para o projeto:** manter a primeira versão focada em um fluxo essencial de triagem, em vez de tentar reproduzir a amplitude de uma plataforma completa. Essa é uma decisão de escopo do SOC-unisul, não uma afirmação de que o Wazuh tenha uma interface inadequada.

### 6.2 Microsoft Sentinel — investigação de incidentes

**Fonte oficial:** [Investigar incidentes do Microsoft Sentinel em profundidade](https://learn.microsoft.com/pt-br/azure/sentinel/investigate-incidents).

**O que a documentação apresenta**
- Uma área de detalhes que reúne informações relevantes para investigar um incidente.
- Contexto relacionado a alertas, entidades, gravidade, estado e registros de atividade.
- Uma linha do tempo que ajuda a compreender a sequência dos eventos associados ao incidente.

**Padrões úteis para o SOC-unisul**
- Reunir informações relacionadas ao mesmo alerta/incidente.
- Disponibilizar contexto e horário para auxiliar a interpretação.
- Diferenciar os dados do incidente das ações que podem ser realizadas.
- Permitir aprofundar a análise sem perder a referência do item selecionado.

**Decisão para o projeto:** não incluir ações defensivas reais, automações ou exploração técnica avançada. O objetivo da A3 será demonstrar um fluxo de baixa complexidade, com dados fictícios e foco na compreensão do usuário. Essa redução é deliberada e não representa uma limitação atribuída ao Microsoft Sentinel.

### 6.3 Síntese comparativa

| Dimensão | Wazuh Dashboard | Microsoft Sentinel | Direção do SOC-unisul |
|---|---|---|---|
| Visão geral | Visualizações de dados e áreas de monitoramento | Gestão de incidentes e contexto associado | Resumo com métricas definidas e período explícito |
| Contexto | Dados de segurança e monitoramento de agentes | Alertas, entidades, detalhes e linha do tempo | Lista filtrável e detalhes do alerta selecionado |
| Exploração | Navegação e recursos de análise | Investigação aprofundada de incidentes | Fluxo curto de dashboard → filtro → detalhes |
| Escopo | Plataforma abrangente de segurança | Plataforma de gestão e investigação | Protótipo acadêmico, restrito a uma tarefa principal |

**Conclusão:** as referências demonstram padrões de organização de eventos e de transição entre visão geral e contexto detalhado. O SOC-unisul aplicará esses padrões com foco em clareza, hierarquia visual, rótulos explícitos e um fluxo pequeno o suficiente para ser validado durante a A3.

## 7. Requisitos do projeto

Prioridades: **M — Must:** essencial para demonstrar o fluxo; **S — Should:** importante se houver tempo; **C — Could:** desejável nesta versão.

### 7.1 Requisitos funcionais

| ID | Prioridade | Requisito | Critério de aceite inicial |
|---|---|---|---|
| RF-01 | M | Exibir dashboard com resumo de alertas | Métricas rotuladas e período de referência explícito |
| RF-02 | M | Exibir lista de alertas de exemplo | Cada item possui título/ID, severidade, estado, horário e origem/ativo quando aplicável |
| RF-03 | M | Abrir detalhes de um alerta | A pessoa consegue identificar claramente o alerta selecionado |
| RF-04 | M | Filtrar por severidade e estado | Os filtros ativos ficam visíveis e a lista acompanha a seleção |
| RF-05 | S | Pesquisar por texto ou identificador | A busca é rotulada e apresenta resultados ou estado vazio |
| RF-06 | S | Ordenar por horário ou severidade | A ordenação ativa fica perceptível |
| RF-07 | M | Apresentar estados de erro, carregamento, vazio e confirmação quando aplicáveis | Cada estado explica o que ocorreu e, quando pertinente, o próximo passo |
| RF-08 | S | Simular mudança do estado de um alerta no protótipo | A ação gera feedback e fica claro que não altera sistemas reais |
| RF-09 | C | Exibir gráfico simples de distribuição dos alertas | O gráfico tem título, período e rótulos legíveis |
| RF-10 | S | Retornar dos detalhes para a lista preservando o contexto | O retorno é claro e os filtros permanecem quando viável |

### 7.2 Requisitos de conteúdo

| ID | Requisito |
|---|---|
| RC-01 | Usar dados fictícios e sinalizá-los como demonstração; não incluir dados reais ou pessoais |
| RC-02 | Usar uma escala consistente de severidade, por exemplo: Crítica, Alta, Média e Baixa |
| RC-03 | Usar estados consistentes, por exemplo: Aberto, Em análise e Resolvido |
| RC-04 | Apresentar horário e intervalo temporal em formato claro e consistente |
| RC-05 | Explicar métricas e abreviações não autoexplicativas |
| RC-06 | Não apresentar números simulados como se fossem ameaças reais |

### 7.3 Requisitos de usabilidade e acessibilidade

| ID | Requisito | Como verificar |
|---|---|---|
| RUA-01 | A hierarquia visual deve destacar a tarefa e os alertas prioritários | Revisão da interface e teste de localização de alerta |
| RUA-02 | Cor não deve ser o único meio de informar severidade/estado | Conferir rótulo textual e, se houver, ícone complementar |
| RUA-03 | Buscar contraste mínimo WCAG 2.2 de 4,5:1 para texto normal e 3:1 para texto grande, observadas as exceções da norma | Verificar combinações com ferramenta de contraste |
| RUA-04 | Controles devem ter rótulos claros e foco visível | Inspeção por teclado e revisão dos rótulos |
| RUA-05 | Conteúdo essencial deve se adaptar a desktop e mobile | Verificar as telas em larguras distintas |
| RUA-06 | Filtros, busca e ações devem fornecer feedback | Percorrer o fluxo e verificar estados de sucesso, vazio e erro |
| RUA-07 | Termos, rótulos e estados devem ser consistentes | Revisão do conteúdo por alguém que não escreveu a tela |
| RUA-08 | Informações essenciais não devem depender apenas de gráficos | Conferir se existem rótulos e valores textuais equivalentes |

**Referência de acessibilidade:** [W3C WAI — WCAG 2.2: Contrast (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html). A norma define os critérios mínimos de contraste para texto e apresenta as exceções aplicáveis.

### 7.4 Requisitos não funcionais e restrições

- **RNF-01 — Responsividade:** adaptar conteúdos essenciais a diferentes larguras, sem esconder ações indispensáveis.
- **RNF-02 — Consistência:** usar os mesmos nomes, severidades, estados e formatos de data em todas as telas.
- **RNF-03 — Privacidade:** usar dados sintéticos; não publicar credenciais, logs reais ou informações pessoais.
- **RNF-04 — Integridade:** identificar o protótipo como demonstração e não apresentar ações simuladas como respostas reais a incidentes.
- **RNF-05 — Documentação:** manter decisões, fontes e referências do protótipo versionadas no GitHub.
- **RNF-06 — Acessibilidade básica:** revisar contraste, legibilidade, foco e significado textual dos estados.

## 8. Limites do escopo

### Incluído

- Dashboard visual com métricas de exemplo.
- Lista de alertas simulados, filtros e detalhe de um alerta.
- Estados essenciais da interface.
- Responsividade dos fluxos prioritários.
- Wireframes, protótipo de alta fidelidade e UI Kit nas próximas sprints.
- Teste de um fluxo crítico com pelo menos duas pessoas externas à equipe e registro das melhorias.

### Fora do escopo

- Conexão com SIEM/SOC real, endpoints ou fontes de logs.
- Detecção de ameaças ou análise automatizada em produção.
- Autenticação real, gestão de contas ou permissões.
- Isolamento de máquinas, bloqueio de IPs ou execução de ações defensivas.
- Garantia de monitoramento em tempo real.
- Substituição de ferramentas profissionais de segurança.

## 9. Riscos e decisões de UX

| Risco | Efeito possível | Prevenção proposta |
|---|---|---|
| Excesso de informação na primeira tela | Dificulta encontrar prioridades | Começar por métricas essenciais e lista de alertas |
| Uso de cores sem rótulos | Estado pode ser interpretado incorretamente | Usar texto e ícones complementares |
| Dados fictícios parecem reais | Interpretação equivocada do protótipo | Identificar os dados como demonstração |
| Escopo visual muito grande | Risco de não concluir e validar o fluxo | Priorizar dashboard → filtro → detalhes |
| Fluxo não testado | Problemas de compreensão permanecem ocultos | Testar com duas pessoas externas e registrar observações |

## 10. Fluxo crítico para as próximas sprints

**Tarefa de teste proposta:** “Encontre um alerta de severidade alta que ainda esteja aberto e consulte qual ativo foi afetado e quando o evento ocorreu.”

1. A pessoa abre o dashboard.
2. Identifica a área de alertas.
3. Filtra por severidade Alta e estado Aberto.
4. Seleciona um alerta compatível.
5. Consulta severidade, horário, origem/ativo e descrição.
6. Retorna à lista, mantendo os filtros quando possível.

Esse fluxo será detalhado na Sprint 2 com arquitetura da informação, rótulos, estados alternativos, cenários e diagrama de navegação.

## 11. O que falta validar com a equipe

- Confirmar se as duas proto-personas fazem sentido para o público que a equipe consegue alcançar.
- Conversar, se viável, com alguém com familiaridade em segurança da informação e anotar o que confirmou ou contrariou as hipóteses.
- Se houver inspeção prática de produtos similares, registrar observações e capturas permitidas com as fontes.
- Revisar o documento com o grupo antes de considerá-lo fechado.
- Registrar autoria individual em commits reais e vincular o trabalho à Issue da sprint.

Não marcar essas atividades como concluídas antes de serem realizadas.

## 12. Checklist da Sprint 1

- [x] Problema e contexto inicial descritos a partir do tema do repositório.
- [x] Objetivo geral, objetivos específicos e público-alvo definidos.
- [x] Duas proto-personas documentadas e identificadas como hipóteses.
- [x] Duas soluções similares analisadas com fontes oficiais.
- [x] Requisitos funcionais e de conteúdo definidos.
- [x] Requisitos básicos de usabilidade, acessibilidade e responsividade definidos.
- [x] Escopo incluído e excluído delimitado.
- [ ] Hipóteses e proto-personas validadas com usuários/pessoas representativas.
- [ ] Revisão da equipe realizada e decisões registradas.
- [ ] Arquivo inserido no repositório e contribuição ligada à Issue/commit individual.

**Critério de conclusão:** o documento é uma primeira versão preparada. Os itens pendentes exigem atividade real da equipe e não devem ser considerados realizados apenas porque a documentação está escrita.

## Referências

1. Wazuh. *Wazuh Dashboard — Components*. https://documentation.wazuh.com/current/getting-started/components/wazuh-dashboard.html
2. Wazuh. *Navigating the Wazuh dashboard*. https://documentation.wazuh.com/current/user-manual/wazuh-dashboard/navigating-the-wazuh-dashboard.html
3. Microsoft Learn. *Investigar incidentes do Microsoft Sentinel em profundidade*. https://learn.microsoft.com/pt-br/azure/sentinel/investigate-incidents
4. W3C WAI. *Understanding Success Criterion 1.4.3: Contrast (Minimum), WCAG 2.2*. https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html
5. Repositório do projeto SOC-unisul. *README.md*. https://github.com/arthurfp-code/SOC-unisul

---
Madgascar
