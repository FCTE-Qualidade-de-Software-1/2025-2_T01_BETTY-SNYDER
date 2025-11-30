# Tempo Médio de Resposta (TR)

## Objetivo da Métrica
Avaliar a velocidade média com que o sistema ChamaControl responde às requisições realizadas durante o uso normal. Essa métrica está vinculada à subcaracterística **Comportamento em Relação ao Tempo**, pertencente à característica de qualidade **Eficiência de Desempenho** (ISO/IEC 25010).

O tempo de resposta influencia diretamente a experiência do usuário e a fluidez da navegação, além de evidenciar possíveis gargalos no back-end, banco de dados ou frontend.

O TR é fundamental para avaliar:
- fluidez da experiência do usuário,  
- eficiência das rotas da API,  
- eventuais gargalos no backend ou banco de dados.

---

## Condições de Coleta

Para garantir reprodutibilidade e confiabilidade da medição, o experimento foi conduzido sob condições controladas, conforme descrito abaixo:

- **Dispositivo utilizado:** Computador pessoal (desktop)  
- **Sistema operacional:** Windows 10 Pro (64 bits)  
- **Tipo de conexão:** Ethernet (cabo)  
- **Velocidade da internet:** 70 Mb/s (download) / 70 Mb/s (upload)  
- **Roteador / Provedor:** Conexão residencial estável (sem perda de pacote no momento do teste)  
- **Navegador utilizado:** Google Chrome **131.0.6778.86** (versão estável mais recente disponível no momento)  
- **Ferramentas utilizadas:** Chrome DevTools → Aba **Network**  
- **Caches:** Cache do navegador limpo antes da primeira medição  
- **Situação do sistema:**  
    - Nenhuma aba adicional aberta  
    - Sistema com baixo uso de CPU e memória  
    - Sem downloads ou aplicações pesadas em execução  

Essas condições asseguram que o tempo de resposta medido reflete principalmente o desempenho da aplicação, e não limitações do ambiente de teste.

## Método de Coleta
A coleta seguiu passo a passo o método descrito na Fase 3:

1. Acessar o sistema `https://chamacontrol.online/`.  
2. Abrir **Chrome DevTools → Network**.  
3. Limpar o cache do navegador.  
4. Atualizar a página repetidas vezes (20 execuções).  
5. Registrar o valor da coluna **Finish** para cada requisição principal.  
6. Registrar os tempos em planilha.  
7. Calcular a média.  
8. Exportar e anexar evidências.

Todo o procedimento foi reproduzível e seguiu integralmente o plano.

As medições foram realizadas em sequência, atualizando a página e observando o tempo total consumido para carregar o conteúdo principal do dashboard.

---

## Amostragem Realizada

As 20 amostras coletadas foram:

| Coleta | Tempo (ms) |
|--------|------------|
| Coleta 1 | 595 |
| Coleta 2 | 576 |
| Coleta 3 | 552 |
| Coleta 4 | 550 |
| Coleta 5 | 577 |
| Coleta 6 | 883 |
| Coleta 7 | 564 |
| Coleta 8 | 543 |
| Coleta 9 | 549 |
| Coleta 10 | 540 |
| Coleta 11 | 285 |
| Coleta 12 | 556 |
| Coleta 13 | 556 |
| Coleta 14 | 555 |
| Coleta 15 | 556 |
| Coleta 16 | 557 |
| Coleta 17 | 541 |
| Coleta 18 | 563 |
| Coleta 19 | 551 |
| Coleta 20 | 566 |


### Cálculo da Média

```
(595 + 576 + 552 + 550 + 577 + 883 + 564 + 543 + 549 + 540 +
 285 + 556 + 556 + 555 + 556 + 557 + 541 + 563 + 551 + 566) / 20
= 560.75 ms
```

### Resultado Obtido
- **Tempo Médio de Resposta (TR): 560,75 ms (~0,56 s)**

---

## Ligação entre a Questão e a Hipótese
### Questão Q4  
**“O sistema responde rapidamente às requisições realizadas durante o uso normal?”**

### Hipótese H4  
“**O tempo médio de resposta permanece ≤ 2 segundos.**”

### Resultado
- TR obtido: **0.56 s**
- Limite máximo permitido: **2 s**

### Conclusão da Hipótese
✅ **HIPÓTESE CONFIRMADA.**

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
| 1.1    | 17/11/2025 | Adição condições de coleta                                                                                     | [Leonardo Sauma](https://github.com/leohssjr)    |                                            |
| 1.3 | 27/11/2025 | Ajustes finais da documentação | [Leonardo Sauma](https://github.com/leohssjr) |  |
