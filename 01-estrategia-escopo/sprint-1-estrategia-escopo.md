# Sprint 1 — Estratégia & Escopo

**Projeto:** SOC-unisul  
**Unidade curricular:** IHC & UX — A3 2026.2  
**Etapa:** Sprint 1 — Estratégia & Escopo

## 1. Apresentação do projeto

O SOC-unisul é um projeto de interface web voltado ao monitoramento de segurança da informação. A proposta é desenvolver um dashboard que ajude profissionais a acompanhar alertas, visualizar indicadores, consultar eventos e compreender o estado geral do ambiente monitorado.

SOC significa Security Operations Center, ou Centro de Operações de Segurança. Esse tipo de ambiente acompanha eventos de segurança, possíveis ameaças e incidentes que possam afetar os sistemas de uma organização.

O projeto acadêmico terá como foco a experiência do usuário, a organização das informações, a clareza visual e a facilidade de navegação. Os dados utilizados no protótipo serão fictícios, sem conexão com sistemas reais de monitoramento.

## 2. Contexto e definição do problema

### Contexto

Profissionais que acompanham eventos de segurança precisam lidar com alertas de diferentes níveis de severidade, horários, origens e estados de tratamento. Para interpretar essas informações, é importante que a interface apresente uma hierarquia clara e permita localizar rapidamente os eventos relevantes.

### Problema central

Quando muitos alertas são apresentados sem organização adequada, pode ser difícil identificar quais precisam de atenção primeiro, compreender o contexto de um evento e consultar as informações necessárias para uma análise inicial.

Essa dificuldade pode aumentar o esforço necessário para interpretar os dados e tornar a navegação menos eficiente.

### Declaração do problema

O projeto pretende atender às necessidades de pessoas que monitoram eventos de segurança por meio de uma interface que organize os alertas por prioridade, facilite a pesquisa e apresente informações claras sobre cada evento.

Essa definição é uma hipótese inicial de projeto e deverá ser revisada conforme a equipe obtenha evidências e realize avaliações de usabilidade.

## 3. Público-alvo

O público-alvo principal é formado por profissionais de segurança da informação que precisam acompanhar alertas e realizar uma triagem inicial de eventos.

O público secundário inclui estudantes de cibersegurança e profissionais que precisam acompanhar indicadores gerais de segurança.

### Necessidades identificadas inicialmente

- Consultar rapidamente o estado geral do monitoramento.
- Identificar alertas de maior severidade.
- Filtrar eventos por severidade e estado.
- Pesquisar alertas específicos.
- Consultar informações detalhadas de um evento.
- Entender os indicadores sem depender exclusivamente de cores.
- Utilizar a interface em diferentes tamanhos de tela.

Essas necessidades são hipóteses iniciais baseadas na proposta do projeto e deverão ser validadas pela equipe.

## 4. Objetivos do projeto

### Objetivo geral

Projetar um dashboard web de monitoramento de segurança que apresente alertas e indicadores de maneira organizada, compreensível e fácil de navegar.

### Objetivos específicos

1. Criar uma visão geral com métricas relacionadas aos alertas.
2. Destacar alertas por severidade e estado.
3. Permitir pesquisa e filtragem de eventos.
4. Apresentar detalhes relevantes de cada alerta.
5. Fornecer mensagens claras de carregamento, erro, ausência de resultados e confirmação.
6. Aplicar princípios de usabilidade e acessibilidade.
7. Demonstrar um fluxo completo de utilização por meio de um protótipo navegável.
8. Avaliar a experiência com participantes externos à equipe e documentar possíveis melhorias.

## 5. Personas

As personas a seguir são perfis fictícios iniciais, criados para orientar as decisões de design. Elas não representam pessoas entrevistadas nem resultados de uma pesquisa de campo.

### Persona 1 — Analista de segurança

**Nome fictício:** Camila Martins

**Perfil:** profissional júnior de segurança da informação que acompanha alertas e precisa identificar os eventos que exigem maior atenção.

**Objetivo principal:** encontrar alertas prioritários e consultar rapidamente as informações necessárias para realizar a triagem inicial.

**Necessidades:**
- Visualizar alertas de maior severidade.
- Filtrar eventos por prioridade e estado.
- Identificar o horário, a origem e o ativo afetado.
- Consultar detalhes sem perder a referência do alerta selecionado.
- Receber confirmação após realizar uma ação.

**Dificuldades hipotéticas:**
- Listas extensas sem hierarquia visual.
- Informações importantes escondidas em várias telas.
- Cores sem rótulos claros.
- Filtros cujo estado não está evidente.
- Mensagens de erro que não explicam como prosseguir.

**Cenário de uso:**

Camila acessa o dashboard no início do expediente, verifica os indicadores gerais, filtra os alertas de alta severidade ainda abertos e seleciona um deles para consultar o horário, a origem, o ativo afetado e a descrição do evento.

**Critério de sucesso:**

Camila consegue localizar um alerta compatível com os critérios da tarefa e compreender as informações apresentadas sem receber instruções do moderador.

### Persona 2 — Responsável pelo acompanhamento operacional

**Nome fictício:** Diego Almeida

**Perfil:** profissional que acompanha indicadores operacionais e precisa compreender o panorama geral dos eventos de segurança para compartilhar informações com a equipe.

**Objetivo principal:** entender a quantidade e a distribuição dos alertas por severidade e estado.

**Necessidades:**
- Visualizar métricas resumidas.
- Compreender o significado dos indicadores.
- Consultar o histórico de eventos.
- Identificar variações na quantidade de alertas.
- Encontrar os eventos relacionados aos indicadores apresentados.

**Dificuldades hipotéticas:**
- Indicadores sem definição ou período de referência.
- Gráficos sem títulos e rótulos claros.
- Excesso de detalhes técnicos na primeira tela.
- Diferenças entre os números do resumo e a lista de eventos.
- Dependência exclusiva de cores para interpretar os dados.

**Cenário de uso:**

Diego acessa o dashboard antes de uma reunião, consulta a quantidade de alertas por severidade, verifica o histórico do período e abre a lista de eventos para entender quais registros estão relacionados aos indicadores.

**Critério de sucesso:**

Diego consegue explicar os principais indicadores e localizar a lista de eventos correspondente sem interpretar incorretamente os dados.

## 6. Análise de soluções similares

Foram selecionadas duas soluções relacionadas ao monitoramento e à investigação de eventos de segurança: Wazuh Dashboard e Microsoft Sentinel.

A análise utiliza documentação oficial pública para identificar conceitos e funcionalidades relevantes. Ela não substitui testes práticos de usabilidade.

### 6.1 Wazuh Dashboard

**Fonte oficial:**  
https://documentation.wazuh.com/current/getting-started/components/wazuh-dashboard.html

O Wazuh oferece um dashboard para visualização e análise de dados relacionados à segurança, incluindo alertas e informações sobre agentes monitorados.

**Características relevantes:**
- Apresentação de dados de segurança em dashboards.
- Visualização de alertas e informações relacionadas.
- Organização de informações por áreas de monitoramento.
- Recursos para explorar e filtrar eventos.

**Aspectos que podem orientar o SOC-unisul:**
- Separar os indicadores gerais da lista detalhada de eventos.
- Destacar informações de severidade.
- Organizar as informações para facilitar a investigação.
- Permitir que a pessoa passe da visão geral para os detalhes.

**Decisão para o projeto:**

O SOC-unisul terá um escopo menor e priorizará um fluxo simples: consultar o resumo, localizar um alerta e abrir seus detalhes. A intenção é demonstrar a experiência de uso de forma clara, sem tentar reproduzir toda a complexidade de uma plataforma profissional.

### 6.2 Microsoft Sentinel

**Fonte oficial:**  
https://learn.microsoft.com/pt-br/azure/sentinel/investigate-incidents

O Microsoft Sentinel oferece recursos para investigar incidentes, consultar alertas relacionados e analisar informações que ajudam a compreender um evento.

**Características relevantes:**
- Visualização das informações de um incidente.
- Consulta de alertas e entidades relacionados.
- Acesso a informações de contexto.
- Recursos para acompanhar eventos associados à investigação.

**Aspectos que podem orientar o SOC-unisul:**
- Agrupar informações relacionadas a um alerta.
- Apresentar o contexto do evento de forma organizada.
- Diferenciar os dados informativos das ações disponíveis.
- Evitar que a pessoa perca a referência do evento durante a consulta.

**Decisão para o projeto:**

O protótipo apresentará apenas os detalhes necessários para a tarefa principal. Não serão incluídas automações avançadas ou ações defensivas reais, pois o objetivo acadêmico é demonstrar a organização da interface e a experiência do usuário.

### 6.3 Comparação das soluções

| Critério | Wazuh Dashboard | Microsoft Sentinel | Proposta do SOC-unisul |
|---|---|---|---|
| Visão geral | Dashboards de segurança | Informações sobre incidentes | Resumo de métricas essenciais |
| Consulta de eventos | Visualização e exploração de alertas | Investigação de incidentes e alertas relacionados | Lista filtrável de eventos |
| Contexto | Dados de monitoramento e segurança | Informações relacionadas ao incidente | Detalhes do alerta selecionado |
| Organização | Diferentes áreas de monitoramento | Informações organizadas para investigação | Fluxo reduzido e objetivo |
| Escopo | Plataforma de segurança | Plataforma de investigação | Protótipo acadêmico de interface |

### Conclusão da análise

As soluções estudadas demonstram a importância de organizar os dados de segurança, apresentar informações sobre os eventos e permitir a passagem da visão geral para os detalhes.

Com base nessa análise, o SOC-unisul priorizará a clareza das informações, a identificação da severidade, os filtros e um fluxo de navegação simples.

Essa escolha constitui uma decisão inicial de design e deverá ser revisada durante as próximas etapas do projeto.

## 7. Requisitos do projeto

Os requisitos estão divididos em funcionais e de conteúdo. As prioridades indicam o que deve ser desenvolvido primeiro no protótipo.

- **Essencial:** necessário para demonstrar o fluxo principal.
- **Importante:** desejável para melhorar a experiência.
- **Opcional:** poderá ser incluído conforme o tempo disponível.

### 7.1 Requisitos funcionais

| ID | Prioridade | Requisito | Critério de aceite |
|---|---|---|---|
| RF01 | Essencial | Exibir um dashboard com indicadores gerais | A tela apresenta métricas com títulos e significados claros |
| RF02 | Essencial | Exibir uma lista de alertas fictícios | Cada registro mostra informações relevantes do evento |
| RF03 | Essencial | Abrir os detalhes de um alerta | A pessoa consegue identificar qual evento está consultando |
| RF04 | Essencial | Filtrar alertas por severidade | A lista apresenta somente os registros compatíveis com o filtro |
| RF05 | Essencial | Filtrar alertas por estado | O estado selecionado é visível e aplicado à lista |
| RF06 | Importante | Pesquisar alertas por texto ou identificador | A busca permite localizar registros e apresenta um estado sem resultados |
| RF07 | Essencial | Mostrar estados de interface | Mensagens de erro, carregamento, sucesso e ausência de resultados são compreensíveis |
| RF08 | Importante | Simular a mudança de estado de um alerta | A interface apresenta feedback da ação simulada |
| RF09 | Opcional | Mostrar um gráfico de distribuição dos alertas | O gráfico possui título, rótulos e valores compreensíveis |
| RF10 | Importante | Permitir retornar aos resultados | A navegação de retorno é clara e preserva os filtros quando possível |

### 7.2 Requisitos de conteúdo

| ID | Requisito |
|---|---|
| RC01 | Utilizar dados fictícios identificados como demonstração |
| RC02 | Utilizar termos consistentes para as severidades |
| RC03 | Utilizar termos consistentes para os estados dos alertas |
| RC04 | Apresentar horários e períodos de maneira clara |
| RC05 | Explicar métricas e abreviações que possam gerar dúvidas |
| RC06 | Não apresentar dados simulados como se fossem incidentes reais |

### 7.3 Requisitos de usabilidade e acessibilidade

| ID | Requisito | Verificação proposta |
|---|---|---|
| RUA01 | Destacar visualmente os alertas prioritários | Revisar a hierarquia visual e testar a localização de um alerta |
| RUA02 | Não depender apenas de cores para transmitir severidade | Conferir se existem rótulos textuais claros |
| RUA03 | Manter contraste adequado entre texto e fundo | Verificar as cores usando uma ferramenta de contraste |
| RUA04 | Utilizar rótulos claros em botões e filtros | Revisar os controles e suas funções |
| RUA05 | Apresentar feedback após ações relevantes | Testar as mensagens de sucesso, erro e ausência de resultados |
| RUA06 | Adaptar o conteúdo a diferentes tamanhos de tela | Avaliar a interface em desktop e celular |
| RUA07 | Manter consistência entre as telas | Revisar nomes, estados e padrões visuais |
| RUA08 | Evitar gráficos que não possam ser compreendidos sem sua representação visual | Incluir títulos, valores e informações textuais quando necessário |

Como referência de acessibilidade, a WCAG 2.2 estabelece critérios mínimos de contraste para texto, incluindo uma relação de 4,5:1 para texto comum e 3:1 para texto grande, conforme as condições e exceções previstas na norma.

Fonte oficial:  
https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html

## 8. Limites do escopo

### Incluído no projeto

- Dashboard com indicadores fictícios.
- Lista de alertas simulados.
- Filtros por severidade e estado.
- Pesquisa de eventos.
- Visualização dos detalhes de um alerta.
- Estados de carregamento, erro, sucesso e ausência de resultados.
- Interface responsiva para as tarefas essenciais.
- Wireframes e protótipo navegável nas próximas etapas.
- UI Kit básico.
- Teste de usabilidade e registro de melhorias.

### Fora do escopo desta versão

- Conexão com sistemas reais de monitoramento.
- Coleta de logs de empresas ou usuários.
- Detecção real e automatizada de ameaças.
- Bloqueio real de endereços IP ou isolamento de máquinas.
- Autenticação de produção e controle real de permissões.
- Garantia de monitoramento em tempo real.

Essas restrições mantêm o projeto concentrado na interface digital, na prototipação e na experiência do usuário.

## 9. Riscos e decisões iniciais

| Risco | Consequência possível | Medida preventiva |
|---|---|---|
| Excesso de informações | Dificuldade para localizar os alertas prioritários | Priorizar os indicadores mais relevantes |
| Dependência de cores | Dificuldade de interpretação dos estados | Utilizar texto e outros sinais visuais |
| Métricas sem contexto | Interpretação equivocada dos indicadores | Mostrar títulos, valores e períodos |
| Crescimento excessivo do escopo | Dificuldade de concluir o protótipo | Priorizar o fluxo principal |
| Falta de testes com usuários | Problemas de compreensão não identificados | Avaliar o fluxo com participantes externos |

## 10. Fluxo prioritário para as próximas sprints

A tarefa principal proposta é:

"Encontre um alerta de alta severidade que ainda esteja aberto e consulte qual ativo foi afetado e quando o evento ocorreu."

O fluxo inicial será:

1. A pessoa acessa o dashboard.
2. Consulta a área de alertas.
3. Seleciona os filtros de alta severidade e estado aberto.
4. Escolhe um alerta compatível.
5. Consulta os detalhes do evento.
6. Retorna à lista de alertas.

Na Sprint 2, esse fluxo será detalhado por meio da arquitetura da informação, do mapa de navegação e dos diagramas de interação.

## 11. Próximas atividades

- Revisar as personas com os integrantes da equipe.
- Validar as hipóteses com pessoas representativas do público, quando possível.
- Revisar a análise das soluções similares.
- Confirmar os requisitos prioritários.
- Registrar as contribuições individuais no GitHub.
- Utilizar esta documentação como base para a Sprint 2.

## 12. Checklist da Sprint 1

- [x] Problema e contexto definidos inicialmente.
- [x] Objetivos e público-alvo descritos.
- [x] Duas proto-personas documentadas.
- [x] Duas soluções similares analisadas.
- [x] Requisitos funcionais e de conteúdo definidos.
- [x] Requisitos de usabilidade e acessibilidade registrados.
- [x] Limites do escopo documentados.
- [ ] Hipóteses das personas validadas com usuários.
- [ ] Documento revisado pela equipe.
- [ ] Contribuições individuais registradas no GitHub.

As tarefas pendentes devem ser marcadas somente depois de serem realizadas.

## Referências

1. Wazuh. Wazuh Dashboard — Components.  
   https://documentation.wazuh.com/current/getting-started/components/wazuh-dashboard.html

2. Microsoft Learn. Investigar incidentes do Microsoft Sentinel em profundidade.  
   https://learn.microsoft.com/pt-br/azure/sentinel/investigate-incidents

3. W3C WAI. Understanding Success Criterion 1.4.3: Contrast (Minimum), WCAG 2.2.  
   https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html

4. Repositório do projeto SOC-unisul.  
   https://github.com/arthurfp-code/SOC-unisul
