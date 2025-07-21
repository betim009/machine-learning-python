# 📝 Gabarito — Exercício de Desvio Padrão e Variância

## Enunciado

Você recebeu os seguintes dados de alturas (em cm):

```python
alturas = [170, 172, 168, 171, 169, 173, 170]
```

1. Calcule a média, a variância e o desvio padrão dessas alturas usando NumPy.
2. Explique, com suas palavras, se o grupo é homogêneo ou heterogêneo em relação à altura.

---

## Resolução

```python
import numpy as np

alturas = [170, 172, 168, 171, 169, 173, 170]

media = np.mean(alturas)
variancia = np.var(alturas)
desvio_padrao = np.std(alturas)

print(f"Média: {media:.2f} cm")
print(f"Variância: {variancia:.2f}")
print(f"Desvio padrão: {desvio_padrao:.2f} cm")
```

**Saída esperada:**
```
Média: 170.43 cm
Variância: 2.53
Desvio padrão: 1.59 cm
```

---

## Interpretação

O desvio padrão de aproximadamente 1,59 cm indica que as alturas estão bem próximas da média (170,43 cm). Isso mostra que o grupo é **homogêneo** em relação à altura, ou seja, não há grandes diferenças entre os participantes.

- **Homogêneo:** quando o desvio padrão é baixo, os valores são próximos entre si.
- **Heterogêneo:** se o desvio padrão fosse alto, indicaria maior variação entre as alturas. 