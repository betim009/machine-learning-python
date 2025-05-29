
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

## ✅ Conclusão

Essas três medidas são fundamentais em Machine Learning para:

- Entender a **distribuição** dos dados.
- Detectar valores atípicos.
- Escolher modelos mais apropriados.

Saber calcular média, mediana e moda é o primeiro passo antes de aplicar algoritmos de aprendizado de máquina.

