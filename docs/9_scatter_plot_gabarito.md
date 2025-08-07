

# 📝 Atividade: Scatter Plot em Python

## Enunciado

Você recebeu um conjunto de dados com a quantidade de horas de sono e a produtividade (em % de tarefas concluídas) de 10 pessoas durante uma semana.

Com base nesses dados:

```python
sono = [4, 5, 6, 5, 7, 8, 6, 9, 7, 8]
produtividade = [50, 55, 60, 58, 68, 75, 64, 80, 70, 78]
```

### Sua tarefa:

1. Crie um gráfico de dispersão (scatter plot) com os dados acima.
2. Coloque o título do gráfico como: **"Sono vs Produtividade"**.
3. Adicione os rótulos nos eixos: "Horas de Sono" (eixo x) e "Produtividade (%)" (eixo y).
4. Use `plt.grid(True)` para melhorar a visualização.

---

## 🧩 Exercício 2

Você está analisando o impacto do tempo gasto em redes sociais no desempenho escolar de um grupo de alunos. Os dados abaixo representam o número médio de horas por dia nas redes sociais e a nota final dos alunos:

```python
tempo_redes = [1, 2, 3, 4, 5, 6, 7, 8]
notas = [85, 83, 78, 75, 70, 68, 65, 60]
```

### Sua tarefa:

1. Crie um gráfico de dispersão com os dados.
2. Adicione título: **"Redes Sociais vs Nota Final"**.
3. Coloque os rótulos apropriados nos eixos.
4. Interprete a tendência visível no gráfico.

---

## 🧩 Exercício 3

Você está ajudando uma empresa a entender a relação entre o número de cafés tomados por dia e o nível de energia relatado pelos funcionários no final do expediente.

```python
cafes = [0, 1, 2, 3, 4, 5, 6]
energia = [40, 50, 60, 65, 70, 68, 65]
```

### Sua tarefa:

1. Crie um scatter plot com os dados acima.
2. Use título: **"Café vs Energia"**.
3. Rótulos dos eixos: "Cafés por Dia" e "Nível de Energia".
4. Use `plt.grid(True)`.

---

## 💡 Dica

Use a biblioteca `matplotlib.pyplot` e o método `plt.scatter(x, y)`.

---

## ✅ Gabarito

```python
import matplotlib.pyplot as plt

sono = [4, 5, 6, 5, 7, 8, 6, 9, 7, 8]
produtividade = [50, 55, 60, 58, 68, 75, 64, 80, 70, 78]

plt.scatter(sono, produtividade)
plt.title("Sono vs Produtividade")
plt.xlabel("Horas de Sono")
plt.ylabel("Produtividade (%)")
plt.grid(True)
plt.show()
```

Esse gráfico permite observar a **tendência positiva** entre sono e produtividade:
quanto mais horas de sono, maior tende a ser a produtividade.

---

## ✅ Gabarito Exercício 2

```python
import matplotlib.pyplot as plt

tempo_redes = [1, 2, 3, 4, 5, 6, 7, 8]
notas = [85, 83, 78, 75, 70, 68, 65, 60]

plt.scatter(tempo_redes, notas)
plt.title("Redes Sociais vs Nota Final")
plt.xlabel("Horas em Redes Sociais")
plt.ylabel("Nota Final")
plt.grid(True)
plt.show()
```

Esse gráfico mostra uma **correlação negativa**: quanto mais tempo nas redes sociais, menor tende a ser a nota.

---

## ✅ Gabarito Exercício 3

```python
import matplotlib.pyplot as plt

cafes = [0, 1, 2, 3, 4, 5, 6]
energia = [40, 50, 60, 65, 70, 68, 65]

plt.scatter(cafes, energia)
plt.title("Café vs Energia")
plt.xlabel("Cafés por Dia")
plt.ylabel("Nível de Energia")
plt.grid(True)
plt.show()
```

Aqui observamos um aumento de energia com o consumo de café, até certo ponto. Após 4 cafés, o nível de energia começa a cair levemente, o que pode indicar excesso de consumo.

---