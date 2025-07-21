# 📝 Gabarito — Projeto 9: Análise Completa de Dados

## 1. Preparação do ambiente

```bash
python3 -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate
pip install numpy scipy matplotlib
```

---

## 2. Estatística básica

```python
import numpy as np
from scipy import stats

notas = [55, 70, 68, 90, 88, 76, 95, 60, 80, 85, 78, 92, 73, 65, 87, 81, 77, 69, 84, 79, 91, 74, 82, 67, 89, 72, 83, 66, 93, 71]
tempos = [45, 50, 48, 60, 55, 52, 65, 49, 54, 58, 53, 62, 51, 47, 59, 56, 57, 46, 61, 55, 63, 50, 60, 48, 64, 49, 58, 47, 66, 52]

# Notas
media_notas = np.mean(notas)
mediana_notas = np.median(notas)
moda_notas = stats.mode(notas, keepdims=True)

# Tempos
media_tempos = np.mean(tempos)
mediana_tempos = np.median(tempos)
moda_tempos = stats.mode(tempos, keepdims=True)

print(f"Notas - Média: {media_notas:.2f}, Mediana: {mediana_notas}, Moda: {moda_notas.mode[0]}")
print(f"Tempos - Média: {media_tempos:.2f}, Mediana: {mediana_tempos}, Moda: {moda_tempos.mode[0]}")
```

**Interpretação:**
- Média e mediana próximas indicam distribuição simétrica.
- Moda pouco relevante se não houver repetições marcantes.

---

## 3. Medidas de dispersão

```python
var_notas = np.var(notas)
desvio_notas = np.std(notas)
var_tempos = np.var(tempos)
desvio_tempos = np.std(tempos)

print(f"Notas - Variância: {var_notas:.2f}, Desvio padrão: {desvio_notas:.2f}")
print(f"Tempos - Variância: {var_tempos:.2f}, Desvio padrão: {desvio_tempos:.2f}")
```

**Interpretação:**
- Desvios altos indicam turma heterogênea; baixos, turma homogênea.

---

## 4. Percentis

```python
p25_notas = np.percentile(notas, 25)
p50_notas = np.percentile(notas, 50)
p75_notas = np.percentile(notas, 75)

p25_tempos = np.percentile(tempos, 25)
p50_tempos = np.percentile(tempos, 50)
p75_tempos = np.percentile(tempos, 75)

print(f"Notas - 25º: {p25_notas}, 50º: {p50_notas}, 75º: {p75_notas}")
print(f"Tempos - 25º: {p25_tempos}, 50º: {p50_tempos}, 75º: {p75_tempos}")
```

**Interpretação:**
- Percentis mostram a distribuição dos alunos: quem está entre os melhores, medianos e piores desempenhos/tempos.

---

## 5. Visualização e análise de distribuição

```python
import matplotlib.pyplot as plt

plt.hist(notas, 20, alpha=0.7, color='royalblue')
plt.title('Histograma das Notas')
plt.xlabel('Notas')
plt.ylabel('Frequência')
plt.show()

plt.hist(tempos, 20, alpha=0.7, color='orange')
plt.title('Histograma dos Tempos de Prova')
plt.xlabel('Tempo (min)')
plt.ylabel('Frequência')
plt.show()
```

**Interpretação:**
- As notas tendem a se concentrar no centro, mas podem não ser perfeitamente normais.
- Os tempos podem mostrar mais dispersão ou assimetria.

---

## 6. Simulação de distribuição normal

```python
notas_normais = np.random.normal(media_notas, desvio_notas, 1000)
plt.hist(notas_normais, 20, alpha=0.7, label='Normal simulada')
plt.hist(notas, 20, alpha=0.7, label='Notas reais')
plt.title('Comparação: Notas reais vs Normal simulada')
plt.xlabel('Notas')
plt.ylabel('Frequência')
plt.legend()
plt.show()
```

**Interpretação:**
- Se as notas reais se parecem com a curva normal simulada, a turma segue uma distribuição próxima da normal.
- Diferenças podem indicar outliers, assimetria ou agrupamentos.

---

## 7. Análise final (exemplo de texto)

A análise mostra que a turma tem desempenho médio de X e tempo médio de Y minutos. A maioria dos alunos está próxima da média, mas há casos de notas e tempos muito altos ou baixos. Os percentis ajudam a identificar quem está entre os melhores e piores desempenhos.

A distribuição das notas se aproxima de uma normal, mas há pequenas diferenças, indicando possíveis outliers ou grupos distintos. Entender a distribuição dos dados é essencial para tomar decisões pedagógicas, como oferecer reforço para alunos abaixo do 25º percentil ou propor desafios para os acima do 75º.

**Sugestões:**
- Monitorar alunos com notas ou tempos muito fora do padrão.
- Usar a análise para ajustar métodos de ensino e avaliação.
- Repetir a análise em outras turmas para comparar perfis. 