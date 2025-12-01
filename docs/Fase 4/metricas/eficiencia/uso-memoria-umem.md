# Uso de Memória (Umem)

## Objetivo da Métrica
Avaliar se o sistema ChamaControl apresenta um consumo de memória adequado durante o uso normal, identificando possíveis gargalos, picos anormais ou comportamentos que indiquem risco de instabilidade.

Esta métrica está associada à subcaracterística **Utilização de Recursos**, pertencente à característica de qualidade **Eficiência de Desempenho** no modelo ISO/IEC 25010.

---

## Condições de Coleta

Para garantir a confiabilidade da medição, o teste foi realizado sob as seguintes condições controladas:

- **Navegador:** Google Chrome **131.x**
- **Ambiente:** Desktop
- **Conexão:** Internet estável
- **Estado do Sistema:**
    - Sem *throttling* de CPU ou rede ativado.
    - Sem outras abas pesadas abertas concorrendo por recursos.

---

## Método de Coleta
A coleta foi realizada utilizando o **Chrome DevTools**, na aba **Performance**, com a captura habilitada para monitoramento da memória JavaScript (**JS Heap**).

**Procedimento executado:**

1. Acessar o sistema hospedado em `https://chamacontrol.online/`.
2. Abrir o DevTools e navegar para a aba **Performance**.
3. Ativar a gravação (**Record**).
4. Interagir com a aplicação por aproximadamente **1 minuto**, realizando:
    - Navegação entre páginas.
    - Interações com elementos visuais.
    - Movimentação da interface.
5. Encerrar a gravação (**Stop**).
6. Analisar a faixa **JS Heap** no gráfico de memória resultante.

---

## Resultado Obtido

Durante o período monitorado, os valores coletados para o **JS Heap** foram:

| Indicador | Valor (MB) |
|-----------|------------|
| Mínimo | ~ 4.3 MB |
| Máximo | ~ 9.7 MB |
| **Média Aprox.** | **~ 7.0 MB** |

### Observações
- Os valores apresentados são extremamente baixos para uma aplicação web moderna.
- Não foram observados picos abruptos, vazamentos ou crescimento contínuo da memória.

---

## Interpretação dos Resultados

De acordo com os critérios definidos na Fase 2:

> *Para aplicações web, valores entre 0 e 30 MB indicam consumo excelente; entre 30 e 70 MB, consumo moderado; acima de 100 MB, risco de instabilidade e possível vazamento de memória.*

Como o consumo real registrado ficou entre **4.3 MB e 9.7 MB**, a aplicação apresenta:

- **Uso mínimo de memória** em relação à capacidade atual de hardware.
- **Excelente estabilidade** durante o uso.
- **Baixa pressão no Garbage Collector**.
- Capacidade de rodar em dispositivos modestos.
- Ausência de vazamento perceptível (*memory leak*).

---

## Ligação entre a Questão e a Hipótese

### Questão GQM Q6 (Eficiência)
"**O sistema consome muita memória durante o uso normal?**"

### Hipótese 6
"**O consumo de memória permanece dentro dos limites considerados normais para aplicações web (≤ 70 MB), sem ultrapassar faixas de risco (> 100 MB)."**"

### Avaliação da Hipótese
- **Consumo real:** ~7 MB (média).
- **Limiar crítico:** Acima de 100 MB → muito distante do observado.

### Conclusão da Hipótese
A hipótese foi **CONFIRMADA**.
O ChamaControl utiliza memória de forma eficiente e segura, sem risco de saturação.

---

## Evidência da Coleta (Print)

![Gráfico JS Heap](../../../assets/Memória(Umem)JSheap.png)
*(JS Heap variando entre 4.3 MB e 9.7 MB, conforme registrado no Chrome DevTools)*

---

## Evidência da Coleta (Vídeo)

<iframe width="1351" height="480" src="https://youtu.be/3DsymX7u5dM" title="Uso de Memória" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

---

## Conclusão

A métrica **Uso de Memória (Umem)** demonstra que o ChamaControl apresenta um consumo de memória extremamente baixo.
O comportamento observado é consistente com uma aplicação otimizada, sem indícios de vazamentos, má gestão de objetos ou sobrecarga nos componentes do frontend, garantindo eficiência e estabilidade.

## Histórico de versão

| Versão | Data       | Descrição                                         | Autor(es)                                      | Revisor(es) |
| ------ | ---------- | ------------------------------------------------- | ---------------------------------------------- | ----------- |
| 1.0    | 25/11/2025 | Criação do documento da métrica M10 (Uso de Memória) | [Breno Fernandes](https://github.com/BrenoFrds) |             |
| 1.1    | 30/11/2025 | Adicionando Vídeo M9 | [Bruno Ricardo](https://github.com/EhOBruno) |             |