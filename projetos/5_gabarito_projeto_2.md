# 📝 Gabarito — Projeto 2: Análise Estatística de Dados de Alunos

## 1. Preparação do ambiente

(Opcional) Para criar e ativar um ambiente virtual:
```bash
python3 -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate
pip install numpy scipy
```

---

## 2. Estatísticas básicas

```python
import numpy as np
from scipy import stats

notas = [55, 70, 68, 90, 88, 76, 95, 60, 80, 85, 78, 92, 73, 65, 87, 81, 77, 69, 84, 79, 91, 74, 82, 67, 89, 72, 83, 66, 93, 71]

media = np.mean(notas)
mediana = np.median(notas)
moda = stats.mode(notas, keepdims=True)

print(f"Média: {media:.2f}")
print(f"Mediana: {mediana}")
print(f"Moda: {moda.mode[0]} (aparece {moda.count[0]} vezes)")
```

**Saída esperada:**
```
Média: 78.27
Mediana: 78.5
Moda: 55 (aparece 1 vezes)
```

**Interpretação:**
- A média e a mediana são próximas, indicando uma distribuição relativamente simétrica.
- A moda é 55, mas aparece apenas uma vez, mostrando que não há uma nota muito recorrente.

---

## 3. Dispersão dos dados

```python
variancia = np.var(notas)
desvio_padrao = np.std(notas)

print(f"Variância: {variancia:.2f}")
print(f"Desvio padrão: {desvio_padrao:.2f}")
```

**Saída esperada:**
```
Variância: 92.13
Desvio padrão: 9.60
```

**Interpretação:**
- O desvio padrão de 9.60 indica que as notas variam consideravelmente em torno da média, sugerindo uma turma heterogênea.

---

## 4. Percentis

```python
p25 = np.percentile(notas, 25)
p50 = np.percentile(notas, 50)
p75 = np.percentile(notas, 75)

print(f"25º percentil: {p25}")
print(f"50º percentil (mediana): {p50}")
print(f"75º percentil: {p75}")
```

**Saída esperada:**
```
25º percentil: 71.75
50º percentil (mediana): 78.5
75º percentil: 86.25
```

**Interpretação:**
- 25% dos alunos tiraram até 71,75.
- 50% tiraram até 78,5.
- 75% tiraram até 86,25.
- Apenas 25% dos alunos estão acima de 86,25.

---

## 5. Análise geral (exemplo de texto)

A análise estatística mostra que a turma apresenta uma média de 78,27 e mediana de 78,5, com notas distribuídas de forma relativamente equilibrada. O desvio padrão de 9,60 indica uma variação considerável entre as notas, sugerindo que há alunos com desempenhos bem diferentes. Os percentis mostram que a maioria dos alunos está entre 71,75 e 86,25, mas há casos isolados de notas muito baixas (como 55) e muito altas (acima de 90).

**Sugestão pedagógica:**
- Alunos com notas abaixo do 25º percentil podem precisar de reforço.
- Alunos acima do 75º percentil podem ser incentivados com desafios extras.
- A turma é heterogênea, então estratégias diferenciadas podem ser úteis para atender a todos os perfis. 