# M3 - Cobertura de Documentação (CD)

## 1. Objetivo da Métrica
Avaliar a qualidade e a disponibilidade da documentação do projeto ChamaControl, considerando tanto a **documentação externa** (README, GitHub Pages, artefatos de projeto) quanto a **documentação interna** (comentários no código), verificando se há material suficiente para apoiar compreensão, manutenção e evolução do sistema.

A métrica é avaliada em uma escala qualitativa de 1 a 5:

- 1 - Documentação muito baixa  
- 2 - Documentação insuficiente  
- 3 - Documentação mediana  
- 4 - Documentação boa  
- 5 - Documentação completa  

---

## 2. Método de Coleta

A avaliação foi feita de forma **manual**, com inspeção dos seguintes elementos:

- **Documentação externa (D_ext):**
    - `README.md` do repositório principal:
        - Explica claramente o objetivo do sistema.
        - Descreve as principais funcionalidades.
        - Traz passo a passo de execução com Docker/Docker Compose.
        - Mostra configuração de variáveis de ambiente (ex.: `VITE_NEWS_API_KEY`).
        - Lista equipe, licença e links relevantes.
    - [GitHub Pages](https://unb-mds.github.io/2024-2-ChamaControl/) com navegação configurada:
        - `Home (index.md)`
        - `Como Contribuir? (CONTRIBUTING.md)`
        - `Arquitetura (arquitetura.md)`
        - `Story Map (StoryMap.md)`
        - `Protótipo (prototipo.md)`
        - `Sprints 0 a 7 (sprints/Sprint-x.md)`
    - Isso indica documentação externa bem cuidada, cobrindo visão geral, arquitetura, processo e protótipo.

- **Documentação interna (D_int):**
    - Comentários no **backend**:
        - Existem poucos comentários explicativos, quase inexistente.
        - Parte da lógica é compreendida apenas pelos nomes de funções/variáveis, contudo não há comentários.
    - Comentários no **frontend (web)**:
        - Também há poucos comentários.
        - Destaque negativo para o arquivo:
            - `web/src/pages/Dashboard/Dashboard.jsx`
            - Arquivo central, de **alta complexidade**, responsável por múltiplos gráficos, tabelas e filtros.
            - Realiza várias chamadas à API, monta datasets para Chart.js, manipula estado e renderiza diferentes visualizações.
            - **Não possui comentários explicando o fluxo de dados, as decisões de filtragem ou a organização dos gráficos**, o que torna a manutenção e entendimento mais difíceis.

---

## 3. Fórmula e Pesos Utilizados

Para tornar a avaliação mais objetiva, a Cobertura de Documentação (CD) foi calculada a partir de dois componentes:

- **D_ext** → Qualidade da documentação externa (README + GitHub Pages)  
- **D_int** → Qualidade da documentação interna (comentários de código)

Foi definida a seguinte fórmula ponderada:

CD = (0,4 * D_ext) + (0,6 * D_int)
> Arredondamento para ter um resultado inteiro


### **Notas utilizadas:**
- **D_ext = 4/5**  
  (Documentação externa boa e bem estruturada)
- **D_int = 2/5**  
  (Documentação do código insuficiente, tendendo à inexistente em partes complexas)

### **Cálculo:**
CD_bruto = (0.4 * 4) + (0.6 * 2)

CD_bruto = (1.6) + (1.2) = 2.8

Arredondando temos a nota 3


### **Resultado Final:**
**CD = 3/5 > Documentação Mediana**

---

## 4. Resultado Obtido

- **Cobertura de Documentação (CD): 3/5 - nível mediano**

### Pontos fortes:
- README muito bem feito e completo.
- Documentação externa robusta via GitHub Pages (arquitetura, sprints, protótipo, guia de contribuição).
- Boa rastreabilidade do desenvolvimento.

### Pontos fracos:
- Comentários escassos no backend e frontend.
- Ausência de comentários em arquivos críticos como `Dashboard.jsx`.
- Falta de padronização de documentação interna.
- Partes mais complexas do sistema não possuem explicações, aumentando o custo de manutenção.

---

## 5. Interpretação dos Resultados

O valor **3/5** indica que:

- A **documentação externa** está **acima da média**, muito bem construída e completa.
- A **documentação interna** está **abaixo da média**, com escassez de comentários em partes complexas, afetando negativamente analisabilidade e modificabilidade.
- O saldo final resulta em documentação **mediana**:
    - Forte para entendimento macro do sistema.
    - Fraca para entendimento micro (código).

Em termos de qualidade de software, isso significa:

- Boa documentação para onboarding inicial.
- Dificuldade moderada a alta para manutenção detalhada.
- A documentação externa puxa a nota para cima.
- A documentação interna puxa a nota para baixo.

---

## 6. Ligação entre a Questão e a Hipótese

### Questão Q3  
"**O código contém documentação suficiente?**"

### Hipótese 3  
"**A maioria das funções possui comentários e instruções de manutenção.**"

### Avaliação da hipótese
- **Não confirmada.**
- Embora exista documentação externa robusta e bem produzida, **o código não possui documentação suficiente**.
- Arquivo `Dashboard.jsx`, altamente complexo, não possui nenhum comentário, contrariando diretamente a hipótese.

---

## 7. Evidência da Coleta (Vídeo)
<iframe width="1425" height="570" src="https://www.youtube.com/embed/fghB8n0siKI" title="Cobertura de Documentação" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Histórico de versão
| Versão | Data       | Descrição                                                                                                         | Autor(es)                                        | Revisor(es)                                |
| ------ | ---------- | ----------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ | ------------------------------------------ |
| 1.0    | 17/11/2025 | Criação do documento                                                                                        | [Leonardo Sauma](https://github.com/leohssjr), [Gabriel Soares](https://github.com/SAnjos3) |                                            |
| 1.1    | 28/11/2025 | Adição do vídeo                                                                                        | [Leonardo Sauma](https://github.com/leohssjr) |                                            |