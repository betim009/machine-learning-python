# 📊 Capítulo 4 — Percentis em Machine Learning

## 📌 Introdução

**Percentis** são usados em estatística para indicar o valor abaixo do qual uma certa porcentagem dos dados se encontra.

Por exemplo, o 75º percentil é o valor abaixo do qual 75% dos dados estão.

Percentis são úteis para entender a distribuição dos dados, identificar extremos e comparar grupos.

---

## 🧮 Exemplo Prático

Considere as idades dos moradores de uma rua:

```python
import numpy as np

idades = [5, 31, 43, 48, 50, 41, 7, 11, 15, 39, 80, 82, 32, 2, 8, 6, 25, 36, 27, 61, 31]

p75 = np.percentile(idades, 75)
print(f"75º percentil: {p75}")  # 43.0
```

**Interpretação:**
- 75% das pessoas têm **43 anos ou menos**.

Outro exemplo:

```python
p90 = np.percentile(idades, 90)
print(f"90º percentil: {p90}")  # 61.0
```

- 90% das pessoas têm **61 anos ou menos**.

---

## 📈 Como calcular outros percentis

Você pode calcular qualquer percentil usando a função `np.percentile(lista, valor_percentil)`.

Exemplo:
```python
p25 = np.percentile(idades, 25)
print(f"25º percentil: {p25}")
```

- O 25º percentil é o valor abaixo do qual 25% dos dados estão.

---

## 🎯 Aplicação Prática

Percentis são muito usados para:
- Analisar notas de provas (quem está entre os melhores ou piores)
- Avaliar salários em empresas
- Entender distribuição de idades, alturas, rendas, etc.

---

## 📝 Exercício Proposto

Você recebeu as seguintes notas de uma turma:

```python
notas = [55, 70, 68, 90, 88, 76, 95, 60, 80, 85, 78, 92, 73, 65, 87]
```

1. Calcule o 25º, 50º e 75º percentis dessas notas.
2. Explique, com suas palavras, o que cada um desses percentis representa nesse contexto.

> Dica: use a função `np.percentile()`.

---

**Referência:**  
[W3Schools - Python Machine Learning Percentile](https://www.w3schools.com/python/python_ml_percentile.asp) 