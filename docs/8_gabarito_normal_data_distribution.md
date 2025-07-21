# 📝 Gabarito — Distribuição Normal de Dados

## Exercício 1 — Gabarito

1. Gere um array com 10.000 valores normalmente distribuídos, com média 50 e desvio padrão 8.
2. Plote um histograma desses valores com 50 barras.
3. O que você observa sobre a concentração dos dados? E sobre os valores extremos?

```python
import numpy as np
import matplotlib.pyplot as plt

dados = np.random.normal(50, 8, 10000)
plt.hist(dados, 50)
plt.title('Histograma de distribuição normal (média=50, desvio=8)')
plt.xlabel('Valores')
plt.ylabel('Frequência')
plt.show()
```

**Interpretação:**
- A maioria dos valores está concentrada entre 42 e 58 (média ± 1 desvio padrão).
- Poucos valores estão muito distantes da média (valores extremos).
- O histograma tem formato de sino, típico da distribuição normal.

---

## Exercício 2 — Proposto

1. Gere dois arrays de 5.000 valores normalmente distribuídos:
   - O primeiro com média 0 e desvio padrão 1.
   - O segundo com média 0 e desvio padrão 5.
2. Plote os dois histogramas no mesmo gráfico, usando cores diferentes e transparência (`alpha`).
3. O que muda quando o desvio padrão aumenta?

### Gabarito Exercício 2

```python
import numpy as np
import matplotlib.pyplot as plt

dados1 = np.random.normal(0, 1, 5000)
dados2 = np.random.normal(0, 5, 5000)

plt.hist(dados1, 50, alpha=0.7, label='Desvio padrão = 1')
plt.hist(dados2, 50, alpha=0.7, label='Desvio padrão = 5')
plt.title('Comparação de distribuições normais com diferentes desvios')
plt.xlabel('Valores')
plt.ylabel('Frequência')
plt.legend()
plt.show()
```

**Interpretação:**
- O histograma azul (desvio padrão 1) é mais "estreito", com a maioria dos valores próximos de 0.
- O histograma laranja (desvio padrão 5) é mais "espalhado", com valores mais distantes da média.
- Quanto maior o desvio padrão, mais dispersos ficam os dados em torno da média. 