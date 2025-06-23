# Projeto 1: Análise de Idades em um Evento de Corrida

## Contexto

Você faz parte da equipe organizadora de uma corrida de rua na sua cidade. Após o evento, a equipe coletou as idades dos 20 primeiros colocados para entender melhor o perfil dos participantes e planejar futuras edições.

A organização quer responder às seguintes perguntas:
- Qual é a idade média dos corredores mais rápidos?
- Qual é a idade central (mediana) desse grupo?
- Existe uma idade que aparece mais vezes entre os primeiros colocados (moda)? O que isso pode indicar sobre o perfil dos participantes?

**Dados coletados:**

```python
idades = [22, 25, 27, 22, 30, 28, 25, 24, 29, 22, 31, 28, 27, 26, 25, 24, 23, 22, 29, 28]
```

## Tarefas

1. Calcule a **média** das idades dos 20 primeiros colocados.
2. Calcule a **mediana** das idades.
3. Calcule a **moda** das idades.
4. Escreva um breve parágrafo explicando o que cada uma dessas medidas revela sobre o perfil dos corredores mais rápidos e como essas informações podem ajudar a organização do evento.

> Utilize as bibliotecas `numpy` e `scipy` para os cálculos.

---

## Gabarito (Resolução)

```python
import numpy as np
from scipy import stats

idades = [22, 25, 27, 22, 30, 28, 25, 24, 29, 22, 31, 28, 27, 26, 25, 24, 23, 22, 29, 28]

# 1. Média
media = np.mean(idades)
print(f"Média: {media:.2f}")  # Média: 25.85

# 2. Mediana
mediana = np.median(idades)
print(f"Mediana: {mediana}")  # Mediana: 26.0

# 3. Moda
moda = stats.mode(idades)
print(f"Moda: {moda.mode[0]} (aparece {moda.count[0]} vezes)")  # Moda: 22 (aparece 4 vezes)

# 4. Interpretação
print("""
A média indica que, em geral, os corredores mais rápidos têm cerca de 26 anos. 
A mediana mostra que metade dos primeiros colocados tem até 26 anos, e metade tem mais. 
A moda revela que a idade mais comum entre os primeiros colocados é 22 anos, sugerindo que muitos jovens se destacaram na prova.
Essas informações ajudam a organização a entender o perfil predominante dos participantes de elite, podendo direcionar ações de divulgação, premiação ou categorias específicas para faixas etárias mais representativas.
""")
``` 