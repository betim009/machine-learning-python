# 📊 Capítulo 3 — Desvio Padrão e Variância em Machine Learning

## 📌 Introdução

O **desvio padrão** é uma medida que descreve o quanto os valores de um conjunto de dados estão espalhados em relação à média.  
- Um desvio padrão **baixo** indica que a maioria dos valores está próxima da média.
- Um desvio padrão **alto** indica que os valores estão distribuídos em uma faixa mais ampla.

A **variância** é outra medida de dispersão, sendo o quadrado do desvio padrão.

Essas medidas são essenciais em Machine Learning para entender a distribuição dos dados, identificar outliers e avaliar a consistência dos dados.

---

## 🧮 Exemplos Práticos

### Exemplo 1: Valores próximos da média

```python
import numpy as np

speed = [86, 87, 88, 86, 87, 85, 86]
media = np.mean(speed)
desvio_padrao = np.std(speed)
variancia = np.var(speed)

print(f"Média: {media:.2f}")
print(f"Desvio padrão: {desvio_padrao:.2f}")
print(f"Variância: {variancia:.2f}")
```

**Saída esperada:**
```
Média: 86.43
Desvio padrão: 0.90
Variância: 0.86
```
A maioria dos valores está a menos de 1 unidade da média.

---

### Exemplo 2: Valores mais dispersos

```python
speed = [32, 111, 138, 28, 59, 77, 97]
media = np.mean(speed)
desvio_padrao = np.std(speed)
variancia = np.var(speed)

print(f"Média: {media:.2f}")
print(f"Desvio padrão: {desvio_padrao:.2f}")
print(f"Variância: {variancia:.2f}")
```

**Saída esperada:**
```
Média: 77.43
Desvio padrão: 37.85
Variância: 1432.20
```
Os valores estão muito mais espalhados em relação à média.

---

## 🧠 Como calcular manualmente a variância

1. Calcule a média dos valores.
2. Subtraia a média de cada valor e eleve ao quadrado.
3. Calcule a média desses quadrados (isso é a variância).
4. O desvio padrão é a raiz quadrada da variância.

Exemplo com os valores `[32, 111, 138, 28, 59, 77, 97]`:
- Média: 77.4
- Diferenças ao quadrado: 2061.16, 1128.96, 3672.36, 2440.36, 338.56, 0.16, 384.16
- Variância: 1432.2
- Desvio padrão: 37.85

---

## 📈 Interpretação

- **Desvio padrão baixo:** os dados são mais consistentes, próximos da média.
- **Desvio padrão alto:** os dados são mais variados, indicando maior dispersão ou presença de outliers.

---

## 🎯 Aplicação Prática

Imagine que você está analisando as notas de uma turma:

```python
notas = [7, 8, 7.5, 8, 7, 8, 7.5]
print(np.std(notas))  # Desvio padrão baixo

notas = [5, 10, 6, 9, 4, 10, 3]
print(np.std(notas))  # Desvio padrão alto
```

- Na primeira turma, as notas são próximas (baixa dispersão).
- Na segunda, há alunos com notas muito altas e muito baixas (alta dispersão).

---

## 📝 Exercício Proposto

Você recebeu os seguintes dados de alturas (em cm):

```python
alturas = [170, 172, 168, 171, 169, 173, 170]
```

1. Calcule a média, a variância e o desvio padrão dessas alturas usando NumPy.
2. Explique, com suas palavras, se o grupo é homogêneo ou heterogêneo em relação à altura.

> Dica: use as funções `np.mean()`, `np.var()` e `np.std()`.

---

**Referência:**  
[W3Schools - Python Machine Learning Standard Deviation](https://www.w3schools.com/python/python_ml_standard_deviation.asp) 