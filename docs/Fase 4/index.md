# Fase 4 

## Introdução

A Fase 4 corresponde à execução prática da avaliação de qualidade do **ChamaControl**, aplicando todas as métricas, critérios e procedimentos definidos nas fases anteriores (**Fase 1, Fase 2 e Fase 3**). Nesta etapa, serão testadas, na prática, as métricas propostas, bem como validadas as hipóteses formuladas a partir do modelo **GQM**.

O objetivo principal desta fase é verificar se os resultados obtidos por meio das medições confirmam ou refutam as hipóteses levantadas anteriormente, além de identificar pontos fortes, limitações técnicas e oportunidades concretas de melhoria no sistema.

---

## Objetivo da Fase 4

- Executar as medições definidas na [**Fase 2**](../Fase%202/index.md), conforme o plano estabelecido na [**Fase 3**](../Fase%203/index.md);
- Testar as métricas de **Manutenibilidade** e **Eficiência de Desempenho** em ambiente controlado;
- Validar as hipóteses associadas a cada questão do **GQM**;
- Registrar resultados reais, evidências e anomalias encontradas;
- Comparar os valores obtidos com os limiares de aceitação definidos anteriormente;
- Produzir insumos para as recomendações finais de melhoria.

---

## Execução das Métricas

Nesta fase, serão aplicadas, de forma efetiva, as seguintes métricas:

### Manutenibilidade

- Grau de Modularidade (GM)
- Cobertura de Documentação (CD)
- Percentual de Código Duplicado (DUP)
- Cobertura de Testes Automatizados (CTA)
- Complexidade Ciclomática Média (CCM)

### Eficiência de Desempenho

- Tempo Médio de Resposta (TR)
- Tempo até o Primeiro Conteúdo (FCP)
- Uso de CPU (Ucpu)
- Uso de Memória (Umem)
- Taxa de Disponibilidade (TD)

Cada métrica será coletada conforme o procedimento descrito na **Fase 3**, utilizando as ferramentas previamente definidas (**SonarQube, Jest, Lighthouse, DevTools, monitoramento de sistema**, entre outras).

---

## Teste das Propostas Definidas Anteriormente

Além da simples coleta de dados, esta fase tem como foco testar empiricamente tudo o que foi proposto nas fases anteriores, incluindo:

- A eficácia das métricas selecionadas;
- A adequação dos limites e faixas de interpretação definidos;
- A coerência das hipóteses do **GQM**;
- A viabilidade prática do plano de avaliação.

Os resultados obtidos serão confrontados diretamente com:

- As hipóteses da **Fase 2**;
- Os critérios de sucesso da **Fase 3**.

Dessa forma, será possível verificar se as proposições teóricas realmente se sustentam quando aplicadas ao sistema real.

---

## Consistência com o GQM

Para cada métrica, foi explicitamente indicado:

- Qual **Questão** do GQM ela responde  
- Qual **Hipótese** ela valida ou refuta  
- Como o resultado impacta os **Objetivos de Medição**

A rastreabilidade garante coerência da [Fase 1](../Fase%201/index.md) > [Fase 4](../Fase%204/index.md).


## Resultados e Evidências

Para cada métrica executada, serão apresentados:

- Valor obtido;
- Ferramenta utilizada;
- Evidências (prints, relatórios, logs);
- Classificação segundo o critério de julgamento;
- Observações técnicas relevantes.

## 10. Histórico de Versão

| Versão | Data | Descrição | Autor(es) | Revisor(es) |
|--------|------------|------------------------------|-------------------------------|----------------|
| 1.0 | 28/11/2025 | Criação do documento | [Enrico Zoratto](https://github.com/sidts) |  [Leonardo Sauma](https://github.com/leohssjr) |
| 1.1 | 29/11/2025 | Ajuste e revisão na documentação | [Leonardo Sauma](https://github.com/leohssjr) |  |