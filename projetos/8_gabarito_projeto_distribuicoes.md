# 📝 Gabarito — Projeto 8: Explorando Distribuições de Dados

## 1. Distribuição Uniforme

```python
import numpy as np
import matplotlib.pyplot as plt

uniforme = np.random.uniform(20, 80, 2000)
plt.hist(uniforme, 20, color='royalblue', alpha=0.7)
plt.title('Histograma — Distribuição Uniforme (20 a 80)')
plt.xlabel('Valores')
plt.ylabel('Frequência')
plt.show()
```

**Interpretação:**
- O histograma mostra barras de alturas semelhantes, indicando que todos os valores entre 20 e 80 têm a mesma chance de ocorrer.
- Isso caracteriza uma **distribuição uniforme**.

---

## 2. Distribuição Normal

```python
normal = np.random.normal(50, 10, 2000)
plt.hist(normal, 20, color='orange', alpha=0.7)
plt.title('Histograma — Distribuição Normal (média=50, desvio=10)')
plt.xlabel('Valores')
plt.ylabel('Frequência')
plt.show()
```

**Interpretação:**
- O histograma tem formato de sino, com a maioria dos valores próximos de 50.
- Valores extremos (muito distantes da média) são raros.
- Comparando com a distribuição uniforme, a normal é "concentrada" no centro.

---

## 3. Comparação entre distribuições

```python
plt.hist(uniforme, 20, alpha=0.7, label='Uniforme')
plt.hist(normal, 20, alpha=0.7, label='Normal')
plt.title('Comparação: Uniforme vs Normal')
plt.xlabel('Valores')
plt.ylabel('Frequência')
plt.legend()
plt.show()
```

**Interpretação:**
- A distribuição uniforme cobre todo o intervalo de forma equilibrada.
- A normal é "alta" no centro e baixa nas extremidades.
- Visualmente, a diferença entre "espalhamento" e "concentração" fica clara.

---

## 4. Explorando o desvio padrão

```python
normal_5 = np.random.normal(50, 5, 2000)
normal_10 = np.random.normal(50, 10, 2000)
normal_20 = np.random.normal(50, 20, 2000)

plt.hist(normal_5, 20, alpha=0.6, label='Desvio = 5')
plt.hist(normal_10, 20, alpha=0.6, label='Desvio = 10')
plt.hist(normal_20, 20, alpha=0.6, label='Desvio = 20')
plt.title('Distribuições Normais com Diferentes Desvios')
plt.xlabel('Valores')
plt.ylabel('Frequência')
plt.legend()
plt.show()
```

**Interpretação:**
- Quanto maior o desvio padrão, mais "espalhada" fica a curva.
- Desvio pequeno: curva estreita e alta.
- Desvio grande: curva larga e baixa.

---

## 5. Análise final (exemplo de texto)

A escolha da distribuição afeta diretamente a visualização e a interpretação dos dados. Distribuições uniformes indicam que todos os valores têm a mesma chance de ocorrer, enquanto distribuições normais mostram concentração em torno de um valor central (a média), com poucos valores extremos.

Entender a distribuição dos dados é fundamental antes de aplicar modelos de Machine Learning, pois muitos algoritmos assumem ou se beneficiam de dados normalmente distribuídos. Além disso, a identificação de outliers e padrões depende da análise da distribuição.

**Exemplos reais:**
- **Distribuição normal:** altura de pessoas, notas de provas, erros de medição.
- **Distribuição uniforme:** sorteios, números aleatórios, seleção de amostras.
- **Distribuição normal com diferentes desvios:** tempo de atendimento em serviços pode variar pouco (desvio baixo) ou muito (desvio alto), dependendo do contexto. 