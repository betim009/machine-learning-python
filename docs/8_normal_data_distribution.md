# 📈 Capítulo 8 — Distribuição Normal de Dados (Normal Data Distribution)

## 📌 Introdução

A **distribuição normal** (ou distribuição Gaussiana) é uma das distribuições de probabilidade mais importantes da estatística e do Machine Learning. Ela descreve dados que se concentram em torno de um valor central (a média), formando o famoso "formato de sino" (bell curve).

Muitos fenômenos naturais e sociais seguem, ao menos aproximadamente, uma distribuição normal: altura de pessoas, erros de medição, notas de provas, etc.

---

## 🧪 Gerando uma distribuição normal com NumPy

Podemos gerar dados normalmente distribuídos usando a função `numpy.random.normal()`:

```python
import numpy as np
import matplotlib.pyplot as plt

# Gera 100.000 valores com média 5.0 e desvio padrão 1.0
dados = np.random.normal(5.0, 1.0, 100000)

plt.hist(dados, 100)
plt.title('Histograma de uma distribuição normal')
plt.xlabel('Valores')
plt.ylabel('Frequência')
plt.show()
```

- A maioria dos valores estará próxima de 5.0 (a média), com poucos valores distantes desse centro.
- O desvio padrão (1.0) indica o "espalhamento" dos dados em torno da média.

---

## 🔍 O que observar no histograma?

- O topo do sino está na média (5.0).
- Aproximadamente 68% dos valores estão a até 1 desvio padrão da média (entre 4.0 e 6.0).
- A curva é simétrica: cauda esquerda ≈ cauda direita.

---

## 📝 Exercício Proposto

1. Gere um array com 10.000 valores normalmente distribuídos, com média 50 e desvio padrão 8.
2. Plote um histograma desses valores com 50 barras.
3. O que você observa sobre a concentração dos dados? E sobre os valores extremos?

> Dica: use `np.random.normal()` e `plt.hist()`.

---

**Referência:**  
[W3Schools - Python Machine Learning Normal Data Distribution](https://www.w3schools.com/python/python_ml_normal_data_distribution.asp) 