# Fase 1 – Processo de Avaliação

## **Contexto de Trabalho**

Este trabalho foi desenvolvido no âmbito da disciplina de **Qualidade de Software**, com o objetivo de proporcionar aos alunos a compreensão, do início ao fim, da execução de um processo de avaliação de um produto de software, aplicando conceitos, metodologias e normas padronizadas e reconhecidas internacionalmente. Para isso, foi selecionado o **ChamaControl**, um software criado por estudantes da disciplina de Métodos de Desenvolvimento de Software.

O projeto envolve diferentes atores em sua concepção e uso. O desenvolvimento do ChamaControl foi conduzido por um grupo de estudantes, que atuaram como responsáveis pela implementação técnica do sistema e também pelo seu papel de operadores durante a execução acadêmica, cuidando da infraestrutura e manutenção básica. A disponibilização do software ocorreu de forma aberta, em repositório público, o que permite classificá-los também como fornecedores da solução. A avaliação é conduzida por estudantes da disciplina de Qualidade de Software, sendo essa avaliação requisitada pela professora da turma. Os usuários finais abrangem cidadãos em geral, pesquisadores, órgãos públicos e organizações ambientais, todos interessados em acessar informações atualizadas sobre queimadas de forma simples e confiável.

## **Software Escolhido**

**Nome do produto:** ChamaControl

**Versão do produto:** Versão inicial acadêmica

#### **Domínio de Aplicação**

O sistema se insere no domínio de **monitoramento ambiental**, oferecendo uma interface web intuitiva para a consulta de dados públicos do **INPE** relacionados a focos de incêndio no Brasil. O ChamaControl organiza informações de forma estruturada e acessível, permitindo acompanhar tanto os registros anuais de queimadas quanto os focos diários mais recentes, atualizados todos os dias às 10h com base em arquivos disponibilizados pelo INPE.

#### **Classificação Técnica**

Assim, o ChamaControl foi classificado como **Software de Tempo Real** conforme Pressman (2002), devido à sua função de monitoramento contínuo de incêndios e necessidade de resposta em tempo útil.

Já sob a ótica da norma **IEEE 1062**, enquadra-se como **COTS (Commercial Off-The-Shelf Software)**, pois foi desenvolvido para atender a um público amplo, sem customização específica para um cliente. Além disso, o produto está de acordo com as características de escopo, manutenção, custo de aquisição, entre outras, padrões de softwares da categoria COTS.

#### **Funcionalidades do Sistema**

Além dos **dashboards interativos**, o sistema incorpora uma tela dedicada a notícias sobre queimadas, alimentada por meio da **API do GNews**, fornecendo informações complementares e contextualizadas sobre os eventos monitorados.

Para manter a base de dados atualizada, o ChamaControl conta com **três scrapers principais**:

- **processaDadosAnual**, que popula o banco de dados com registros históricos entre 2003 e 2024;
- **processaDadosDiarios30Dias**, que insere os focos registrados diariamente nos últimos 30 dias;
- **processaDadoDiario**, responsável por atualizar a aplicação diariamente com os dados mais recentes.

#### **Objetivo da avaliação**

A análise de qualidade do ChamaControl busca verificar se o sistema atende aos padrões definidos pelo modelo ISO/IEC 25010, considerando atributos como Eficiência de Desempenho e Manutenibilidade.

Entre os objetivos específicos destacam-se:
Avaliar se o sistema utiliza os recursos computacionais de forma adequada e se responde dentro de prazos aceitáveis, considerando seu propósito de monitoramento ambiental;

Identificar melhorias que possam otimizar o tempo de resposta, a utilização de recursos e a capacidade do sistema;

Examinar o grau de modularidade, testabilidade e modificabilidade do software, verificando se sua estrutura favorece manutenção e evolução;

Produzir um diagnóstico técnico direcionado a essas duas características, servindo como base para ajustes futuros e comparações com sistemas de propósito semelhante.

## Classificação e Ênfase das Características de Qualidade

Nesta etapa inicial do processo de avaliação, foram definidas as características de qualidade a serem analisadas com base nos objetivos do trabalho e no perfil do público-alvo do ChamaControl. A escolha levou em conta tanto a necessidade de garantir o bom desempenho do sistema quanto a importância de facilitar sua manutenção e evolução futura.

Foram priorizadas as características de Eficiência de Desempenho e Manutenibilidade, pois estão diretamente ligadas à capacidade do sistema de processar e apresentar dados atualizados do INPE em tempo adequado, além de permitir que sua estrutura seja mantida e modificada de forma confiável pelos desenvolvedores.

A seguir, apresenta-se a classificação das características de qualidade, conforme a abordagem SQuaRE (ISO/IEC 25010), em uma escala de 1 a 5:

| Característica           | Ênfase (1-5)         |
| ------------------------ | -------------------- |
| Eficiência de Desempenho | 5 – grande interesse |
| Manutenibilidade         | 5 – grande interesse |
| Usabilidade              | 4 – baixo interesse  |
| Confiabilidade           | 3 – baixo interesse  |
| Segurança                | 3 – nenhum interesse |
| Compatibilidade          | 3 – nenhum interesse |
| Portabilidade            | 3 – nenhum interesse |
| Funcionalidade           | 3 – nenhum interesse |

Essa priorização servirá como base para a definição das métricas e critérios de avaliação, garantindo foco nos aspectos mais relevantes para a análise do sistema.


