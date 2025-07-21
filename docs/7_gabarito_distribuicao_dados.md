# 📝 Gabarito — Distribuição de Dados

## Exercício Proposto

1. Gere um array com 500 valores aleatórios entre 10 e 50.
2. Plote um histograma desses valores com 10 barras.
3. Responda: O histograma ficou equilibrado? O que isso indica sobre a distribuição dos dados?

---

## Resolução

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.random.uniform(10.0, 50.0, 500)
plt.hist(x, 10)
plt.title('Histograma de 500 valores aleatórios entre 10 e 50')
plt.xlabel('Intervalos')
plt.ylabel('Frequência')
plt.show()
```

**Interpretação:**
- O histograma deve mostrar barras de alturas semelhantes, pois os valores são distribuídos uniformemente entre 10 e 50.
- Isso indica uma **distribuição uniforme**: todos os intervalos têm aproximadamente a mesma quantidade de valores.

---

# Exemplos Didáticos Adicionais

## 1. Distribuição Normal (Gaussiana)

```python
x = np.random.normal(50, 10, 1000)  # média 50, desvio padrão 10
plt.hist(x, 30)
plt.title('Histograma de distribuição normal')
plt.xlabel('Valores')
plt.ylabel('Frequência')
plt.show()
```

**Interpretação:**
- O histograma tem formato de sino (bell curve), típico da distribuição normal.
- A maioria dos valores está próxima da média (50), com poucos valores nas extremidades.

---

## 2. Distribuição Uniforme (faixa diferente)

```python
x = np.random.uniform(0, 100, 1000)
plt.hist(x, 20)
plt.title('Histograma de distribuição uniforme (0 a 100)')
plt.xlabel('Valores')
plt.ylabel('Frequência')
plt.show()
```

**Interpretação:**
- As barras têm alturas semelhantes, mostrando que todos os valores têm a mesma chance de ocorrer.

---

## 3. Distribuição com Outliers

```python
x = np.concatenate([np.random.normal(50, 5, 950), np.random.normal(100, 1, 50)])
plt.hist(x, 30)
plt.title('Histograma com outliers')
plt.xlabel('Valores')
plt.ylabel('Frequência')
plt.show()
```

**Interpretação:**
- A maior parte dos dados está em torno de 50, mas há um grupo pequeno de valores próximos de 100 (outliers).
- O histograma mostra uma barra isolada à direita, indicando a presença desses valores extremos.

---

## 4. Distribuição assimétrica (skewed)

```python
x = np.random.exponential(2, 1000)
plt.hist(x, 30)
plt.title('Histograma de distribuição assimétrica (Exponencial)')
plt.xlabel('Valores')
plt.ylabel('Frequência')
plt.show()
```

**Interpretação:**
- A maioria dos valores está concentrada à esquerda, com uma cauda longa à direita.
- Esse tipo de distribuição é comum em dados de tempo de espera, renda, etc.

---

Esses exemplos mostram como diferentes distribuições aparecem em histogramas e ajudam a entender o comportamento dos dados antes de aplicar modelos de Machine Learning. 