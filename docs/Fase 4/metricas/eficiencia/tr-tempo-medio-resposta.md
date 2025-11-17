# Tempo Médio de Resposta (TR)

## Objetivo da Métrica
Avaliar a velocidade média com que o sistema ChamaControl responde às requisições realizadas durante o uso normal. Essa métrica está vinculada à subcaracterística **Comportamento em Relação ao Tempo**, pertencente à característica de qualidade **Eficiência de Desempenho** (ISO/IEC 25010).

O tempo de resposta influencia diretamente a experiência do usuário e a fluidez da navegação, além de evidenciar possíveis gargalos no back-end, banco de dados ou frontend.

---

## Método de Coleta
A coleta foi realizada utilizando o **Chrome DevTools**, na aba **Network**, registrando o tempo total de finalização de cada requisição (campo **Finish**).  
Foram capturadas **20 amostras reais**, executando o sistema em condições normais de uso.

As medições foram realizadas em sequência, atualizando a página e observando o tempo total consumido para carregar o conteúdo principal do dashboard.

---

## Amostragem Realizada

As 20 amostras coletadas foram:

```
595, 576, 552, 550, 577, 883, 564, 543, 549, 540,
285, 556, 556, 555, 556, 557, 541, 563, 551, 566
```

### Cálculo da Média

```
(595 + 576 + 552 + 550 + 577 + 883 + 564 + 543 + 549 + 540 +
 285 + 556 + 556 + 555 + 556 + 557 + 541 + 563 + 551 + 566) / 20
= 560.75 ms
```

### Resultado Obtido
- **Tempo Médio de Resposta (TR): 560,75 ms (~0,56 s)**

---

## Interpretação dos Resultados

De acordo com os critérios definidos na Fase 2:

> *“Valores até 2 segundos indicam desempenho ideal. Respostas mais lentas sugerem gargalos nas rotas da API, consultas SQL complexas ou ausência de cache.”*

O valor obtido (**~0,56 segundos**) está **significativamente abaixo do limite recomendado de 2 segundos**, indicando:

- Excelente velocidade de resposta do servidor  
- Carregamento rápido dos dados principais  
- Baixa latência percebida pelo usuário  
- Ausência de gargalos críticos nas rotas analisadas  

Portanto, **a hipótese de que o sistema possui bom tempo de resposta foi confirmada**.

---

## Evidência da Coleta (Vídeo)

<iframe width="1351" height="480" src="https://www.youtube.com/embed/ZE89BVyEicw" title="Tempo Médio de Resposta" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


---

## Conclusão

A métrica **Tempo Médio de Resposta (TR)** apresenta desempenho adequado e dentro dos parâmetros recomendados.  
Com um tempo médio de **~0,56 s**, o sistema atende plenamente às expectativas de eficiência e oferece uma experiência fluida ao usuário.

## Histórico de versão

| Versão | Data       | Descrição                                                                                                         | Autor(es)                                        | Revisor(es)                                |
| ------ | ---------- | ----------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ | ------------------------------------------ |
| 1.0    | 17/11/2025 | Criação do documento                                                                                        | [Leonardo Sauma](https://github.com/leohssjr)    |                                            |
