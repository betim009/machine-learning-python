# 📊 Scatter Plot (Gráfico de Dispersão) em Machine Learning

O scatter plot (gráfico de dispersão) é uma das ferramentas mais importantes
para a **análise exploratória de dados (EDA - Exploratory Data Analysis)** em
Machine Learning. Ele permite visualizar **a distribuição de pontos** e detectar
**relações ou padrões** entre variáveis antes de aplicar qualquer modelo.

## O que é um Scatter Plot?

Um **scatter plot** é um gráfico de dispersão que mostra a **relação entre duas variáveis numéricas**. Ele é amplamente usado em Machine Learning e análise de dados para **visualizar padrões, correlações ou outliers**.

Cada ponto no gráfico representa **uma observação** do conjunto de dados.

---

## Para que serve?

- Entender **como duas variáveis estão relacionadas**.
- Identificar **tendências ou padrões** nos dados.
- Verificar se existe **correlação positiva ou negativa**.
- Explorar dados antes de aplicar um modelo de Machine Learning.
- Avaliar a **distribuição dos dados**.
- Identificar **outliers** (valores muito fora do padrão).
- Verificar **grupos naturais ou clusters** nos dados.

---

## Exemplo com Python

Usando a biblioteca `matplotlib`, podemos criar um scatter plot com facilidade:

```python
import matplotlib.pyplot as plt

# Dados de exemplo
x = [5, 7, 8, 7, 2, 17, 2, 9]
y = [99, 86, 87, 88, 100, 86, 103, 87]

# Criando o gráfico
plt.scatter(x, y)
plt.xlabel("Idade")
plt.ylabel("Velocidade")
plt.title("Exemplo de Scatter Plot")
plt.show()
```

## Outro exemplo: relação entre tempo de estudo e nota

Vamos ver outro exemplo, simulando a relação entre horas de estudo e nota final:

```python
import matplotlib.pyplot as plt

horas_estudo = [1, 2, 3, 4, 5, 6, 7, 8]
nota_final =   [50, 55, 65, 70, 75, 80, 85, 90]

plt.scatter(horas_estudo, nota_final)
plt.xlabel("Horas de Estudo")
plt.ylabel("Nota Final")
plt.title("Horas de Estudo vs Nota Final")
plt.grid(True)
plt.show()
```

Esse gráfico mostra uma **correlação positiva** clara: quanto mais a pessoa estuda, maior tende a ser sua nota.

---

## Comparando múltiplas variáveis

Você também pode usar mais de uma variável no scatter plot utilizando **cores**,
**tamanhos** ou **formas** diferentes. Isso permite ver como **mais de dois fatores**
se relacionam em um mesmo gráfico.

```python
import matplotlib.pyplot as plt

x = [5, 7, 8, 7, 2, 17, 2, 9]
y = [99, 86, 87, 88, 100, 86, 103, 87]
cores = [0, 1, 2, 3, 4, 5, 6, 7]  # Categoria para cada ponto

plt.scatter(x, y, c=cores, cmap='viridis')
plt.xlabel("Idade")
plt.ylabel("Velocidade")
plt.title("Scatter Plot com Categorias por Cor")
plt.colorbar()
plt.show()
```

Esse gráfico usa a cor para representar uma **terceira variável categórica**.

## Exemplo com tamanhos diferentes (quarta variável)

Você também pode usar o parâmetro `s` para indicar o **tamanho dos pontos** com base em uma quarta variável:

```python
import matplotlib.pyplot as plt

x = [5, 7, 8, 7, 2, 17, 2, 9]
y = [99, 86, 87, 88, 100, 86, 103, 87]
cores = [0, 1, 2, 3, 4, 5, 6, 7]
tamanhos = [20, 40, 60, 80, 100, 120, 140, 160]

plt.scatter(x, y, c=cores, s=tamanhos, cmap='plasma', alpha=0.7)
plt.xlabel("Idade")
plt.ylabel("Velocidade")
plt.title("Scatter Plot com Tamanhos Variáveis")
plt.colorbar(label='Categoria')
plt.show()
```

Neste exemplo, os **tamanhos dos pontos** representam uma variável quantitativa adicional, o que enriquece a análise visual.

---

## Interpretação

- Se os pontos estiverem próximos formando uma linha reta de baixo para cima: **correlação positiva**.
- Se os pontos estiverem alinhados de cima para baixo: **correlação negativa**.
- Se os pontos estiverem espalhados aleatoriamente: **sem correlação**.

---

## Dica

Você pode usar diferentes **cores** ou **marcadores** para representar **categorias diferentes**, o que é muito útil em problemas de classificação.

---

## Conclusão

O scatter plot é uma ferramenta visual essencial para analisar e compreender seus dados antes de aplicar algoritmos de Machine Learning. Ele ajuda a **identificar relações escondidas** e **evitar erros na modelagem**.

Essa visualização é especialmente útil quando você quer **comprovar
visualmente a hipótese** de que uma variável influencia outra — por exemplo,
em problemas de **regressão**, onde esperamos que a variável alvo (y)
cresça ou diminua em função da variável explicativa (x).

---