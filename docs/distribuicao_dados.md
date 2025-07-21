# 📊 Capítulo 5 — Distribuição de Dados em Machine Learning

## 📌 Introdução

Em Machine Learning, entender como os dados estão distribuídos é fundamental para escolher o melhor modelo, identificar padrões e detectar possíveis problemas, como outliers ou dados desbalanceados.

No mundo real, os conjuntos de dados costumam ser grandes e complexos. Por isso, é comum usar ferramentas para gerar, visualizar e analisar distribuições de dados.

---

## 🧪 Gerando dados aleatórios com NumPy

Para testar conceitos e algoritmos, muitas vezes criamos conjuntos de dados artificiais. O NumPy facilita isso:

```python
import numpy as np

# Cria um array com 250 números aleatórios entre 0 e 5
x = np.random.uniform(0.0, 5.0, 250)
print(x)
```

---

## 📊 Visualizando a distribuição: Histograma

Um histograma mostra como os valores estão distribuídos em intervalos (faixas). É uma das formas mais simples e poderosas de visualizar a distribuição dos dados.

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.random.uniform(0.0, 5.0, 250)

plt.hist(x, 5)  # 5 barras (bins)
plt.title('Histograma da distribuição dos dados')
plt.xlabel('Intervalos')
plt.ylabel('Frequência')
plt.show()
```

**O que significa cada barra?**
- Cada barra representa quantos valores estão dentro de um determinado intervalo.
- Exemplo: a primeira barra mostra quantos valores estão entre 0 e 1, a segunda entre 1 e 2, e assim por diante.

---

## 🏋️‍♂️ Trabalhando com grandes volumes de dados

Você pode criar conjuntos de dados ainda maiores para simular cenários reais:

```python
x = np.random.uniform(0.0, 5.0, 100000)
plt.hist(x, 100)
plt.title('Histograma de 100.000 valores aleatórios')
plt.show()
```

- Com mais dados e mais barras, o histograma mostra uma distribuição mais suave e detalhada.

---

## 📝 Exercício Proposto

1. Gere um array com 500 valores aleatórios entre 10 e 50.
2. Plote um histograma desses valores com 10 barras.
3. Responda: O histograma ficou equilibrado? O que isso indica sobre a distribuição dos dados?

> Dica: use `np.random.uniform()` e `plt.hist()`.

---

**Referência:**  
[W3Schools - Python Machine Learning Data Distribution](https://www.w3schools.com/python/python_ml_data_distribution.asp) 