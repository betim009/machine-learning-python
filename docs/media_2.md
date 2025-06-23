
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

### 🎯 Conclusão

Com esses novos exemplos, reforçamos o uso prático de **NumPy** e **SciPy** para calcular medidas estatísticas. Esses cálculos são simples, mas poderosos para análise de dados iniciais em qualquer projeto de Machine Learning.

