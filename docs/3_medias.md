# 📊 Capítulo 2 — Média, Mediana e Moda com Python

## 📌 Introdução

Em Machine Learning (e também em estatística), existem **três valores importantes** que nos ajudam a entender a distribuição dos dados:

- **Média (Mean)**: valor médio
- **Mediana (Median)**: valor do meio
- **Moda (Mode)**: valor que mais se repete

Vamos usar o exemplo da velocidade registrada em 13 carros:

```python
speed = [99, 86, 87, 88, 111, 86, 103, 87, 94, 78, 77, 85, 86]
```

---

## 1️⃣ Média (Mean)

A **média** é a soma de todos os valores dividida pela quantidade de elementos:

```text
(99+86+87+88+111+86+103+87+94+78+77+85+86) / 13 = 89.77
```

📌 **Com NumPy:**

```python
import numpy

speed = [99,86,87,88,111,86,103,87,94,78,77,85,86]
x = numpy.mean(speed)
print(x)  # 89.77
```

---

## 2️⃣ Mediana (Median)

A **mediana** é o valor do meio quando os dados estão ordenados.

Conjunto ordenado:

```
[77, 78, 85, 86, 86, 86, 87, 87, 88, 94, 99, 103, 111]
```

🧮 Como temos 13 números, a mediana é o valor na posição 7 → **87**

📌 **Com NumPy:**

```python
import numpy

speed = [99,86,87,88,111,86,103,87,94,78,77,85,86]
x = numpy.median(speed)
print(x)  # 87.0
```

📌 Se houver número **par** de elementos:

```text
[77, 78, 85, 86, 86, 86, 87, 94, 98, 99, 103, 111]

(86 + 87) / 2 = 86.5
```

---

## 3️⃣ Moda (Mode)

A **moda** é o número que aparece com maior frequência.

Na lista:

```
[99, 86, 87, 88, 111, 86, 103, 87, 94, 78, 77, 85, 86]
```

🔁 O número **86** aparece 3 vezes → Moda = **86**

📌 **Com SciPy:**

```python
from scipy import stats

speed = [99,86,87,88,111,86,103,87,94,78,77,85,86]
x = stats.mode(speed)
print(x.mode[0])  # 86
```

---

## ✅ Conclusão Parcial

Essas três medidas são fundamentais em Machine Learning para:

- Entender a **distribuição** dos dados.
- Detectar valores atípicos.
- Escolher modelos mais apropriados.

Saber calcular média, mediana e moda é o primeiro passo antes de aplicar algoritmos de aprendizado de máquina.

---

# 📊 Capítulo 2 – Parte 2: Praticando Média, Mediana e Moda

> Continuação do estudo de medidas estatísticas com novos exemplos.

---

## 📌 Relembrando

Antes de treinar um modelo de Machine Learning, é essencial entender como os dados estão distribuídos. Nesta parte, vamos **praticar** com novos conjuntos de dados e aplicar os métodos `mean()`, `median()` e `mode()`.

---

## 🔢 Novo exemplo de dados

Vamos analisar a idade de 12 pacientes:

```python
idades = [23, 45, 22, 34, 45, 27, 34, 29, 31, 30, 34, 40]
```

---

## 1️⃣ Média com NumPy

```python
import numpy

idades = [23, 45, 22, 34, 45, 27, 34, 29, 31, 30, 34, 40]
media = numpy.mean(idades)
print(media)  # saída esperada: 33.5
```

---

## 2️⃣ Mediana com NumPy

```python
import numpy

idades = [23, 45, 22, 34, 45, 27, 34, 29, 31, 30, 34, 40]
mediana = numpy.median(idades)
print(mediana)  # saída esperada: 32.5
```

⚠️ Neste caso temos 12 valores (número par), então a mediana será a média dos dois valores centrais após a ordenação.

---

## 3️⃣ Moda com SciPy

```python
from scipy import stats

idades = [23, 45, 22, 34, 45, 27, 34, 29, 31, 30, 34, 40]
moda = stats.mode(idades)
print(moda.mode[0])  # saída esperada: 34
```

🧠 O número 34 aparece 3 vezes → é o mais comum.

---

## 📌 Resumo

| Medida   | Valor     | Observação                    |
|----------|-----------|-------------------------------|
| Média    | 33.5      | Soma das idades ÷ 12          |
| Mediana  | 32.5      | Média entre os 6º e 7º valores ordenados |
| Moda     | 34        | Valor mais frequente          |

---

### 🎯 Conclusão Final

Com esses exemplos, reforçamos o uso prático de **NumPy** e **SciPy** para calcular medidas estatísticas. Esses cálculos são simples, mas poderosos para análise de dados iniciais em qualquer projeto de Machine Learning.

