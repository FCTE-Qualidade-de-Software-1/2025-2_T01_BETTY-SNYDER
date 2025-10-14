# Fase 2 - Especificação

## Aplicação da Metodologia GQM

A metodologia **GQM (Goal-Question-Metric)** tem como propósito estabelecer uma relação direta entre os **objetivos da avaliação de qualidade** e as **métricas utilizadas para mensurá-los**. O método propõe uma estrutura em três níveis hierárquicos:

- **Goal (Objetivo):** Define o propósito da medição, o objeto a ser analisado, o ponto de vista e o contexto.

- **Question (Questões):** Traduzem o objetivo em perguntas específicas que ajudam a compreender se ele está sendo atingido.

- **Metric (Métricas):** São os indicadores quantitativos e qualitativos usados para responder às perguntas formuladas.

Essa abordagem garante que a medição da qualidade seja **focada, rastreável e alinhada aos objetivos do projeto**, evitando métricas arbitrárias e promovendo uma análise consistente e objetiva.

## Aplicação do GQM ao ChamaControl

Com base na [Fase 1 - Processo de Avaliação](../Fase%201/index.md), foram priorizadas as características de qualidade Manutenibilidade e Eficiência de Desempenho, conforme a ISO/IEC 25010.
A seguir, são detalhados os objetivos, perguntas e métricas definidos para cada uma delas.

### Objetivo da Medição 1: Manutenibilidade

<table border="1">
  <tr>
    <td>Analisar</td>
    <td>o ChamaControl</td>
  </tr>
  <tr>
    <td>Para o propósito de</td>
    <td>avaliar a facilidade de manutenção e evolução do código</td>
  </tr>
  <tr>
    <td>Com respeito a</td>
    <td>manutenabilidade</td>
  </tr>
  <tr>
    <td>Do ponto de vista da</td>
    <td>equipe de desenvolvimento</td>
  </tr>
  <tr>
    <td>No contexto da</td>
    <td>disciplina de Qualidade de Software</td>
  </tr>
</table>

#### Questões de Manutenabilidade

**Q1:** O código do ChamaControl é modular, com funções e classes bem organizadas?  
**Hipótese 1:** Mais de 80% das funções estão agrupadas de forma coerente e com responsabilidade clara, facilitando modificações.  

**Q2:** É possível modificar um módulo sem impactar outros componentes do sistema?  
**Hipótese 2:** Alterações em módulos independentes afetam menos de 10% de outros módulos, indicando baixo acoplamento. 

**Q3:** O código contém documentação suficiente (comentários, README, guias de execução)?  
**Hipótese 3:** Pelo menos 90% das funções e módulos críticos possuem comentários e instruções básicas de manutenção.

**Q4:** Existe duplicação de código ou funções repetidas que possam dificultar manutenção?  
**Hipótese 4:** Menos de 10% do código é duplicado, permitindo maior facilidade de manutenção e evolução.  

**Q5:** É possível compreender rapidamente a lógica do sistema para realizar diagnósticos ou correções?  
**Hipótese 5:** Desenvolvedores conseguem identificar e modificar funções críticas em menos de 30 minutos, na média.  

#### Métricas de Manutenabilidade
Em desenvolvimento...

### Objetivo da Medição 2: Eficiência de Desempenho

<table border="1">
  <tr>
    <td>Analisar</td>
    <td>o ChamaControl</td>
  </tr>
  <tr>
    <td>Para o propósito de</td>
    <td>avaliar o desempenho e tempo de resposta</td>
  </tr>
  <tr>
    <td>Com respeito a</td>
    <td>eficiência de desempenho</td>
  </tr>
  <tr>
    <td>Do ponto de vista da</td>
    <td>equipe de desenvolvimento</td>
  </tr>
  <tr>
    <td>No contexto da</td>
    <td>disciplina de Qualidade de Software</td>
  </tr>
</table>

#### Questões de Eficiência de Desempenho

**Q1:** O sistema responde rapidamente às requisições da interface e da API?  
**Hipótese 1:** O tempo médio de resposta das APIs e das páginas é inferior a 2 segundos em mais de 90% das consultas.  

**Q2:** O carregamento dos dashboards e gráficos é ágil e sem travamentos?  
**Hipótese 2:** Mais de 95% dos gráficos e dashboards carregam completamente em menos de 3 segundos.  

**Q3:** O consumo de CPU e memória durante a execução do sistema está dentro de limites aceitáveis?  
**Hipótese 3:** O uso de CPU não ultrapassa 70% e a memória utilizada não ultrapassa 80% da capacidade disponível durante operações críticas.  

**Q4:** O sistema mantém desempenho estável com múltiplos usuários simultâneos?  
**Hipótese 4:** Até 50 usuários simultâneos não causam degradação significativa no tempo de resposta ou erros de execução.  

**Q5:** O processo de atualização diária de dados é concluído dentro do prazo esperado?  
**Hipótese 5:** Os scrapers e pipelines processam os dados diários em menos de 30 minutos em 95% das execuções.

#### Métricas de Eficiência de Desempenho
Em desenvolvimento...

## Referências Bibliográficas
> LC00-GQM-Introducao. Disponível em: <https://aprender3.unb.br/pluginfile.php/3230283/mod_folder/content/0/LC00-GQM-Introducao.pdf?forcedownload=1>. Acesso em: 14 de outubro de 2025.

> LC01-GQM-Planejamento. Disponível em: <https://aprender3.unb.br/pluginfile.php/3230283/mod_folder/content/0/LC01-GQM-Planejamento.pdf?forcedownload=1>. Acesso em: 14 de outubro de 2025.

> LC02-GQM-Definicao. Disponível em: <https://aprender3.unb.br/pluginfile.php/3230283/mod_folder/content/0/LC02-GQM-Definicao.pdf?forcedownload=1>. Acesso em: 14 de outubro de 2025.

> LC03-GQM-Coleta. Disponível em: <https://aprender3.unb.br/pluginfile.php/3230283/mod_folder/content/0/LC03-GQM-Coleta.pdf?forcedownload=1>. Acesso em: 14 de outubro de 2025.

> LC04-GQM-Interpretacao. Disponível em: <https://aprender3.unb.br/pluginfile.php/3230283/mod_folder/content/0/LC04-GQM-Interpretacao.pdf?forcedownload=1>. Acesso em: 14 de outubro de 2025.

> LC05-GQM-Exemplo. Disponível em: <https://aprender3.unb.br/pluginfile.php/3230283/mod_folder/content/0/LC05-GQM-Exemplo.pdf?forcedownload=1>. Acesso em: 14 de outubro de 2025.


## Histórico de versão

|Versão|Data|Descrição|Autor(es)|Revisor(es)|
|-|-|-|-|-|
|1.0 | 14/10/2025 | Criação do documento base|[Leonardo Sauma](https://github.com/leohssjr)||
|1.1 | 14/10/2025 | Adição de objetivos e questões sobre as caracterísitcas Manutenabilidade e Eficiência de Desempenho|[Leonardo Sauma](https://github.com/leohssjr)||