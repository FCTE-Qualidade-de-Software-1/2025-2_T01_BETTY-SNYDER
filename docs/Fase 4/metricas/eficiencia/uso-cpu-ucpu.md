# M9 — Uso de CPU (Ucpu)

## Objetivo da Métrica

Avaliar a **carga média de processamento utilizada durante a execução do sistema ChamaControl**, identificando possíveis **gargalos no uso da CPU**.
Essa métrica está vinculada à subcaracterística **Utilização de Recursos**, pertencente à característica de qualidade **Eficiência de Desempenho** (ISO/IEC 25010).

O uso excessivo de CPU pode comprometer a estabilidade do sistema, aumentar o tempo de resposta e prejudicar a experiência do usuário.

---

## Condições de Coleta

Para garantir reprodutibilidade e confiabilidade da medição, o experimento foi conduzido sob condições controladas, conforme descrito abaixo:

* **Dispositivo utilizado:** Computador pessoal (desktop)
* **Sistema operacional:** Windows 11 Pro (64 bits)
* **Tipo de conexão:** Wi-Fi
* **Velocidade da internet:** 70 Mb/s (download) / 70 Mb/s (upload)
* **Roteador / Provedor:** Conexão residencial estável
* **Navegador utilizado:** Google Chrome (versão estável mais recente no momento do teste)
* **Ferramentas utilizadas:**

  * Chrome DevTools → Aba **Performance**
  * Lighthouse (executado localmente via GitHub do projeto)
* **Caches:** Cache do navegador limpo antes da execução
* **Situação do sistema:**

  * Nenhuma aba adicional aberta
  * Baixa utilização de memória
  * Sem processos pesados em segundo plano

Essas condições asseguram que o consumo de CPU registrado reflita prioritariamente o comportamento do sistema avaliado, e não limitações externas do ambiente.

---

## Método de Coleta

A coleta foi realizada utilizando o **Chrome DevTools**, na aba **Performance**, monitorando diretamente a utilização da CPU durante a navegação normal no sistema.

Foram executadas as **operações críticas do ChamaControl**, com registro contínuo do consumo de CPU ao longo da execução.
Os valores **médios e máximos de utilização** foram extraídos a partir do gráfico de desempenho apresentado pela ferramenta.

A métrica foi expressa em **porcentagem (%) de utilização da CPU**.

---

## Cálculo da Métrica

```
Ucpu = (Tempo de CPU usado / Tempo total de execução) × 100
```

---

## Resultado Obtido

* **Uso médio de CPU:** **8,73 %**
* **Uso máximo de CPU:** **aproximadamente 22 %**

---

## Evidência da Coleta (Imagem)

![Eficiencia M9](../../../assets/m9-eficiencia.png)


## Evidência da Coleta (Vídeo)

[Assistir no YouTube](https://www.youtube.com/watch?v=SEU_LINK_AQUI)

---

## Interpretação dos Resultados

De acordo com os critérios definidos na Fase 2:

> *“Valores até 70% indicam utilização adequada dos recursos. Valores superiores a esse limite indicam sobrecarga de processamento.”*

Os valores obtidos (**8,73% de uso médio** e **~22% de pico máximo**) encontram-se **muito abaixo do limite de 70%**, indicando:

* Baixa carga sobre o processador
* Ausência de gargalos de processamento
* Execução estável das operações do sistema
* Boa eficiência no uso dos recursos computacionais

Portanto, **a hipótese de que o sistema apresenta utilização adequada de CPU foi confirmada**.

---

## Conclusão

A métrica **Uso de CPU (Ucpu)** apresentou desempenho plenamente satisfatório.
Com consumo médio de **8,73%** e pico máximo de aproximadamente **22%**, o sistema **ChamaControl opera dentro dos padrões recomendados de eficiência de desempenho**, não apresentando sobrecarga nem necessidade imediata de otimizações relacionadas ao processamento.

---

## Histórico de versão

| Versão | Data       | Descrição                                   | Autor(es)                                     | Revisor(es) |
| ------ | ---------- | ------------------------------------------- | --------------------------------------------- | ----------- |
| 1.0    | 26/11/2025 | Criação do documento da métrica Ucpu        | [Enrico Zoratto](https://github.com/sidts) |             |
| 1.1    | 26/11/2025 |  |  |             |

