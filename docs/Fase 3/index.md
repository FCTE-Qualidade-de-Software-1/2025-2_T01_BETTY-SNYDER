# Plano de Avaliação — Fase 3

## Introdução

Este documento reúne o Plano de Avaliação (Fase 3) para o projeto ChamaControl com base nas decisões tomadas na Fase 2 (GQM: objetivos, questões e métricas). O objetivo é descrever como a avaliação será aplicada na prática, quais recursos serão necessários, o cronograma das atividades e os critérios de sucesso para interpretar os resultados.

O plano segue a estrutura e o tom do exemplo utilizado como referência, adaptando os métodos e métricas à realidade e às prioridades definidas em Fase 2 (Manutenibilidade e Eficiência de Desempenho).

## Método de Avaliação

A avaliação será conduzida usando uma combinação de medições quantitativas (métricas automáticas e monitoramento) e avaliações qualitativas (observação da documentação). As métricas utilizadas foram definidas na Fase 2 e abrangem indicadores de manutenibilidade (GM, CD, DUP, CTA, CCM) e eficiência de desempenho (TR, FCP, Ucpu, Umem, TD).

### Abordagem selecionada

- Coleta automatizada: utilização do SonarQube para análise de manutenibilidade, duplicação de código, complexidade e demais métricas estruturais; além de ferramentas de cobertura de testes para cálculo do CTA.
- Medições de desempenho: uso do Lighthouse e do Chrome DevTools para mensurar TR e FCP; monitoramento de CPU e memória em ambiente de teste para avaliação de Ucpu e Umem; análise de logs e sistemas de uptime para a métrica TD.
- Análise estruturada: interpretação dos resultados com base nos limites definidos na Fase 2, priorizando identificação de pontos críticos e oportunidades de melhoria no código e no desempenho do sistema.

### Critério de sucesso

A avaliação será considerada satisfatória se pelo menos 70% das métricas-chave (definidas na Fase 2) atingirem níveis aceitáveis ou melhores, conforme as interpretações estabelecidas em cada métrica (por exemplo, CTA ≥ 80%, TR ≤ 2s em 90% das requisições, DUP < 10%, CCM média ≤ 10, etc.).

## Instruções de execução

1. Preparação do ambiente de teste: provisionar instância(s) de teste que reproduzam, na medida do possível, o ambiente de produção (mesma versão do software, carga de dados representativa);
2. Coleta automática: executar análise SonarQube e testes de cobertura; exportar os relatórios para a pasta de evidências;
3. Medições de desempenho: executar rotinas de carga/fluxos típicos usando DevTools/Lighthouse e registrar TR e FCP; monitorar Ucpu/Umem durante os cenários;
4. Consolidação: reunir todos os dados, aplicar mapas de pontuação (Níveis da Fase 2) e gerar o relatório final com recomendações priorizadas.

Durante as sessões observadas, registrar: tempo por tarefa, sucesso/falha, erros encontrados, comentários relevantes e sugestões. Sempre que possível, gravar telas para análise posterior.

## Recursos necessários

### Materiais e documentação

- Documento de definição de métricas e critérios (Fase 2);
- Relatórios SonarQube e arquivos de cobertura de testes;
- Modelos de coleta para registro de resultados das métricas.

### Ferramentas técnicas

- SonarQube (análise estática e métricas de manutenibilidade);
- Ferramenta de cobertura de testes (por exemplo Jest ou equivalente usado no projeto);
- Lighthouse / Chrome DevTools para métricas de front-end (FCP, TR);
- Ferramentas de monitoramento (htop, ferramentas de APM ou logs do servidor) para Ucpu e Umem;
- Ferramentas de gravação de tela (opcional) e cronômetro digital.

## Cronograma

| Tarefa                                       | Data de Início | Data de Conclusão | Responsável     |
|----------------------------------------------|----------------|-------------------|-----------------|
| Preparação do ambiente e scripts             | 18/11/2025     | 19/11/2025        | Equipe Técnica  |
| Coleta automática (SonarQube, cobertura)     | 20/11/2025     | 21/11/2025        | Equipe Técnica  |
| Testes de desempenho e monitoramento         | 22/11/2025     | 23/11/2025        | Equipe Técnica  |
| Consolidação e relatório final (Fase 3)      | 26/11/2025     | 27/11/2025        | Equipe Técnica  |



Adapte as semanas para datas concretas conforme o calendário do grupo.

## Consolidação e critérios de relatório

O relatório final deve conter, para cada métrica, a descrição da coleta, os resultados brutos, a interpretação segundo os limiares da Fase 2 e recomendações práticas (priorizadas por impacto e esforço). Incluir também evidências (relatórios SonarQube, logs, planilhas de observação e gravações se houver).

## Plano por Métrica — Manutenibilidade

---

### M1 — Grau de Modularidade (GM)

**Objetivo:**  
Avaliar se o sistema possui módulos bem organizados e com responsabilidades bem definidas.

#### Passos de Execução (preliminares)
- Abrir o projeto no SonarQube.
- Acessar o painel de *Maintainability Rating*.
- Listar todos os módulos classificados como A ou B.
- Registrar módulos com baixa coesão ou dívidas técnicas relacionadas.
- Anotar evidências básicas (prints do SonarQube).

**Entrada:** Relatório SonarQube (Maintainability)  
**Saída:** Percentual de módulos com rating A/B  
**Evidências:** Screenshots do dashboard + tabela de módulos

#### Cálculo
GM = (módulos A/B ÷ total de módulos) × 100

#### Critério de Julgamento
- ≥ 80% → Excelente modularidade  
- 60–79% → Aceitável  
- < 60% → Modularidade insuficiente  

---

### M2 — Cobertura de Documentação (CD)

**Objetivo:**  
Avaliar se o código está adequadamente documentado.

#### Passos de Execução (preliminares)
- Percorrer o repositório e analisar comentários em funções.
- Avaliar README e guias de execução.
- Atribuir nota qualitativa de 1 a 5.
- Registrar exemplos positivos e negativos de documentação.

**Entrada:** Código-fonte e documentação existente  
**Saída:** Nota CD (1 a 5)  
**Evidências:** Prints de trechos comentados, README etc.

#### Cálculo
Escala qualitativa previamente definida.

#### Critério de Julgamento
- 5 → Excelente  
- 4 → Boa  
- 3 → Mediana  
- 2 → Insuficiente  
- 1 → Muito baixa  

---

### M3 — Percentual de Código Duplicado (DUP)

**Objetivo:**  
Identificar duplicações de código que prejudicam reutilização e manutenção.

#### Passos de Execução (preliminares)
- Acessar no SonarQube a métrica *Duplicated Lines (%)*.
- Registrar arquivos com maior duplicação.
- Separar duplicações aceitáveis das problemáticas.

**Entrada:** Relatório SonarQube — Duplicated Lines  
**Saída:** Percentual de código duplicado  
**Evidências:** Prints dos arquivos com duplicação

#### Cálculo
Valor direto do SonarQube.

#### Critério de Julgamento
- < 10% → Excelente  
- 10–20% → Aceitável  
- > 20% → Ruim / requer refatoração  

---

### M4 — Cobertura de Testes Automatizados (CTA)

**Objetivo:**  
Avaliar a cobertura de testes das funcionalidades principais.

#### Passos de Execução (preliminares)
- Executar Jest com cobertura ativada.
- Registrar percentuais de *lines covered*.
- Identificar módulos não cobertos.
- Capturar relatório HTML ou terminal.

**Entrada:** Arquivo de cobertura do Jest  
**Saída:** Percentual total de cobertura  
**Evidências:** Print do relatório de cobertura

#### Cálculo
Valor reportado pelo Jest.

#### Critério de Julgamento
- ≥ 80% → Excelente  
- 60–79% → Aceitável  
- < 60% → Baixa testabilidade  

---

### M5 — Complexidade Ciclomática Média (CCM)

**Objetivo:**  
Avaliar a complexidade lógica das funções.

#### Passos de Execução (preliminares)
- Abrir no SonarQube as métricas de *Cyclomatic Complexity*.
- Registrar valores por função/arquivo.
- Calcular média geral.
- Registrar funções com CC > 15.

**Entrada:** Relatório SonarQube (Complexity)  
**Saída:** CCM média  
**Evidências:** Prints das funções com maior CC

#### Cálculo
CCM = Σ CCᵢ / n

#### Critério de Julgamento
- ≤ 10 → Boa manutenibilidade  
- 11–20 → Moderada  
- > 20 → Alta complexidade  

---

## Plano por Métrica — Eficiência de Desempenho

---

### M6 — Tempo Médio de Resposta (TR)

**Objetivo:**  
Medir a velocidade de respostas das APIs e páginas.

#### Passos de Execução (preliminares)
- Abrir DevTools → aba *Network*.
- Simular uso real do sistema.
- Registrar tempos de resposta das requisições.
- Calcular média geral.

**Entrada:** Logs DevTools/Lighthouse  
**Saída:** TR médio  
**Evidências:** Capturas do *Network*

#### Cálculo
TR = Σ tempos ÷ total de requisições

#### Critério de Julgamento
- ≤ 2s → Excelente  
- > 2s → Necessita análise  

---

### M7 — Tempo até Primeiro Conteúdo (FCP)

**Objetivo:**  
Avaliar quão rápido o usuário vê o primeiro conteúdo útil.

#### Passos de Execução
- Executar Lighthouse.
- Registrar FCP em cenários típicos.
- Comparar com o limite definido.

**Entrada:** Relatório Lighthouse  
**Saída:** Tempo FCP  
**Evidências:** Screenshot da aba *Performance*

#### Critério de Julgamento
- ≤ 3s → Ótimo  
- > 3s → Carregamento lento  

---

### M8 — Uso de CPU (Ucpu)

**Objetivo:**  
Identificar gargalos no uso de processamento.

#### Passos de Execução
- Monitorar o sistema via *htop* ou DevTools Performance.
- Executar operações críticas.
- Registrar valores máximos e médios.

**Entrada:** Monitor do sistema / navegador  
**Saída:** Porcentagem de CPU  
**Evidências:** Capturas dos gráficos

#### Critério de Julgamento
- ≤ 70% → Adequado  
- > 70% → Sobrecarga  

---

### M9 — Uso de Memória (Umem)

**Objetivo:**  
Avaliar se o sistema consome memória de forma eficiente.

#### Passos de Execução
- Monitorar consumo durante operações críticas.
- Registrar valores médios.
- Comparar com limites estabelecidos.

**Entrada:** Monitor do sistema  
**Saída:** Consumo de memória em MB (JS Heap)  
**Evidências:** Prints dos gráficos

#### Critério de Julgamento
- 0 a 30 MB → Excelente
- 30 a 70 MB → Alto, porém aceitável
- mais 100 MB → Ruim / risco de instabilidade
- mais 150 MB → Provável vazamento de memória
- mais 200 MB → Praticamente comprovado memory leak

---

### M10 — Taxa de Disponibilidade (TD)

**Objetivo:**  
Verificar a estabilidade do sistema ao longo do tempo.

#### Passos de Execução
- Analisar logs de uptime do servidor.
- Registrar janelas de indisponibilidade.
- Calcular percentual.

**Entrada:** Logs da hospedagem  
**Saída:** % de disponibilidade  
**Evidências:** Prints ou relatórios de uptime

#### Critério de Julgamento
- ≥ 99% → Excelente  
- < 99% → Requer análise  


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
| 1.1    | 17/11/2025 | Atualização do cronograma com datas reais             | [Breno Fernandes](https://github.com/BrenoFrds) |
| 1.2    | 20/11/2025 | Adicionada a estrutura preliminar do Plano por Métrica, incluindo seções e templates de execução para todas as métricas definidas na Fase 2 | [Breno Fernandes](https://github.com/BrenoFrds) |