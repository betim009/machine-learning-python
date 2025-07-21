# 📝 Gabarito — Exercício de Percentis

## Enunciado

Você recebeu as seguintes notas de uma turma:

```python
notas = [55, 70, 68, 90, 88, 76, 95, 60, 80, 85, 78, 92, 73, 65, 87]
```

1. Calcule o 25º, 50º e 75º percentis dessas notas.
2. Explique, com suas palavras, o que cada um desses percentis representa nesse contexto.

---

## Resolução

```python
import numpy as np

notas = [55, 70, 68, 90, 88, 76, 95, 60, 80, 85, 78, 92, 73, 65, 87]

p25 = np.percentile(notas, 25)
p50 = np.percentile(notas, 50)
p75 = np.percentile(notas, 75)

print(f"25º percentil: {p25}")
print(f"50º percentil (mediana): {p50}")
print(f"75º percentil: {p75}")
```

**Saída esperada:**
```
25º percentil: 70.0
50º percentil (mediana): 78.0
75º percentil: 88.0
```

---

## Interpretação

- **25º percentil (70.0):** 25% dos alunos tiraram nota **70 ou menos**.
- **50º percentil (78.0):** 50% dos alunos tiraram nota **78 ou menos** (esse valor é a mediana).
- **75º percentil (88.0):** 75% dos alunos tiraram nota **88 ou menos**.

Esses percentis ajudam a entender a distribuição das notas:
- O 25º percentil mostra o limite inferior das notas mais baixas.
- O 50º percentil (mediana) divide a turma ao meio.
- O 75º percentil mostra o limite superior das notas da maioria dos alunos, destacando quem está entre os melhores desempenhos. 