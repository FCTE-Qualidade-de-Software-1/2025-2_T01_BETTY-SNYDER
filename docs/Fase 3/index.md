# Plano de Avaliação — Fase 3

## Introdução

Este documento reúne o Plano de Avaliação (Fase 3) para o projeto ChamaControl com base nas decisões tomadas na Fase 2 (GQM: objetivos, questões e métricas). O objetivo é descrever como a avaliação será aplicada na prática, quais recursos serão necessários, o cronograma das atividades e os critérios de sucesso para interpretar os resultados.

O plano segue a estrutura e o tom do exemplo utilizado como referência, adaptando os métodos e métricas à realidade e às prioridades definidas em Fase 2 (Manutenibilidade e Eficiência de Desempenho).

## Método de Avaliação

A avaliação será conduzida usando uma combinação de medições quantitativas (métricas automáticas e monitoramento) e avaliações qualitativas (testes de usabilidade, análise heurística e observação). As métricas concretas foram definidas na Fase 2 e incluem indicadores de manutenibilidade (GM, CBO, CD, DUP, CTA, CCM) e de eficiência (TR, FCP, Ucpu, Umem, TD).

### Abordagem selecionada

- Coleta automatizada: relatórios do SonarQube (manutenibilidade, acoplamento, duplicação, complexidade) e relatórios de cobertura de testes (CTA);
- Medições de desempenho: Lighthouse / DevTools para TR e FCP; monitoramento de CPU e memória em ambiente de teste para Ucpu e Umem; logs e uptime monitor para TD;
- Testes de usabilidade: sessões observadas com membros da equipe e/ou usuários-alvo para avaliar eficiência, eficácia, satisfação e acessibilidade;
- Análise heurística: aplicação das heurísticas de Nielsen para identificar problemas de usabilidade que não aparecem nas métricas automáticas.

### Critério de sucesso

A avaliação será considerada satisfatória se pelo menos 70% das métricas-chave (definidas na Fase 2) atingirem níveis aceitáveis ou melhores, conforme as interpretações estabelecidas em cada métrica (por exemplo, CTA ≥ 80%, TR ≤ 2s em 90% das requisições, DUP < 10%, CCM média ≤ 10, etc.).

## Instruções de execução

1. Preparação do ambiente de teste: provisionar instância(s) de teste que reproduzam, na medida do possível, o ambiente de produção (mesma versão do software, carga de dados representativa);
2. Coleta automática: executar análise SonarQube e testes de cobertura; exportar os relatórios para a pasta de evidências;
3. Medições de desempenho: executar rotinas de carga/fluxos típicos usando DevTools/Lighthouse e registrar TR e FCP; monitorar Ucpu/Umem durante os cenários;
4. Sessões de usabilidade: planejar 5–8 tarefas representativas, conduzir sessões com observador, coletar tempos, erros, taxa de sucesso e feedback qualitativo;
5. Análise heurística: aplicar as heurísticas de Nielsen em walkthroughs guiados por avaliadores;
6. Consolidação: reunir todos os dados, aplicar mapas de pontuação (Níveis da Fase 2) e gerar o relatório final com recomendações priorizadas.

Durante as sessões observadas, registrar: tempo por tarefa, sucesso/falha, erros encontrados, comentários relevantes e sugestões. Sempre que possível, gravar telas para análise posterior.

## Recursos necessários

### Materiais e documentação

- Documento de definição de métricas e critérios (Fase 2);
- Guias de execução de testes (roteiros de tarefas para usabilidade);
- Modelos de coleta (planilhas ou formulários para registrar tempos e observações).

### Ferramentas técnicas

- SonarQube (análise estática e métricas de manutenibilidade);
- Ferramenta de cobertura de testes (por exemplo Jest ou equivalente usado no projeto);
- Lighthouse / Chrome DevTools para métricas de front-end (FCP, TR);
- Ferramentas de monitoramento (htop, ferramentas de APM ou logs do servidor) para Ucpu e Umem;
- Ferramentas de gravação de tela (opcional) e cronômetro digital.

## Cronograma (sugestão)

| Tarefa                                  | Data de Início | Data de Conclusão | Responsável     |
|-----------------------------------------|----------------|-------------------|-----------------|
| Preparação do ambiente e scripts        | (semana 1)     | (semana 1)        | Equipe Técnica  |
| Coleta automática (SonarQube, cobertura) | (semana 2)     | (semana 2)        | Equipe Técnica  |
| Testes de desempenho e monitoramento    | (semana 3)     | (semana 3)        | Equipe Técnica  |
| Sessões de usabilidade e análise heurística | (semana 4)  | (semana 4)        | Avaliadores     |
| Consolidação e relatório final          | (semana 5)     | (semana 5)        | Equipe Técnica  |


Adapte as semanas para datas concretas conforme o calendário do grupo.

## Consolidação e critérios de relatório

O relatório final deve conter, para cada métrica, a descrição da coleta, os resultados brutos, a interpretação segundo os limiares da Fase 2 e recomendações práticas (priorizadas por impacto e esforço). Incluir também evidências (relatórios SonarQube, logs, planilhas de observação e gravações se houver).

## Tabela de Contribuição

| Integrante                                | Matrícula | Percentual |
|-------------------------------------------|-----------|------------|
| Breno Soares Fernandes                     | 202017540 | 16,6%      |
| Bruno Ricardo de Menezes                   | 221007680 | 16,6%      |
| Enrico Martins Mantoan Zoratto             | 222006688 | 16,6%      |
| Filipe Bressanelli Azevedo Filho           | 222024579 | 16,6%      |
| Gabriel Soares dos Anjos                   | 231026625 | 16,6%      |
| Leonardo Henrique Sobral Sauma Junior      | 231035428 | 16,6%      |

## Conclusão

Este Plano de Avaliação operacionaliza as decisões definidas na Fase 2, fornecendo passos claros para execução, medição e interpretação dos resultados. A aplicação rigorosa deste plano permitirá à equipe quantificar a manutenibilidade e a eficiência do sistema e priorizar ações de melhoria com base em dados.


## Histórico de Versões

| Versão | Data       | Descrição                             | Autor(es)                                   |
|--------|------------|---------------------------------------|----------------------------------------------|
| 1.0    | 10/11/2025 | Inicio do Plano de Avaliação (Fase 3) |[Gabriel Soares](github.com/SAnjos3)|

