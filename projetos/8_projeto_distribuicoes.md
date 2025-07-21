# Projeto 8 — Explorando Distribuições de Dados em Machine Learning

## Contexto

Você está trabalhando como analista de dados em uma empresa de saúde. Seu objetivo é analisar e comparar diferentes distribuições de dados para entender padrões, identificar possíveis anomalias e preparar os dados para futuros modelos de Machine Learning.

Distribuições de dados são fundamentais para:
- Visualizar padrões e tendências
- Detectar outliers e anomalias
- Escolher o modelo estatístico ou de ML mais adequado
- Comunicar resultados de forma clara para outros profissionais

Neste projeto, você irá gerar, visualizar e comparar distribuições uniformes e normais, além de analisar o impacto do desvio padrão na forma dos dados.

---

## Tarefas

### 1. Distribuição Uniforme
- Gere um array com 2.000 valores aleatórios entre 20 e 80 usando a distribuição uniforme (`np.random.uniform`).
- Plote um histograma desses valores com 20 barras.
- **Objetivo:** Entender como uma distribuição uniforme se comporta visualmente.
- **Pergunta:** O histograma ficou equilibrado? O que isso indica sobre a distribuição?

### 2. Distribuição Normal
- Gere um array com 2.000 valores normalmente distribuídos, com média 50 e desvio padrão 10 (`np.random.normal`).
- Plote um histograma desses valores com 20 barras.
- **Objetivo:** Visualizar a "curva de sino" da distribuição normal.
- **Pergunta:** Compare visualmente com o histograma da distribuição uniforme. O que muda?

### 3. Comparação entre distribuições
- Plote os dois histogramas (uniforme e normal) no mesmo gráfico, usando cores diferentes e transparência (`alpha`).
- **Objetivo:** Facilitar a comparação visual entre as duas distribuições.
- **Pergunta:** Descreva as principais diferenças entre as distribuições.

### 4. Explorando o desvio padrão
- Gere mais dois arrays de 2.000 valores normalmente distribuídos:
  - Um com média 50 e desvio padrão 5.
  - Outro com média 50 e desvio padrão 20.
- Plote os três histogramas normais (desvio 5, 10 e 20) no mesmo gráfico, cada um com uma cor diferente.
- **Objetivo:** Entender como o desvio padrão afeta a "largura" da curva normal.
- **Pergunta:** O que acontece com a forma da curva conforme o desvio padrão aumenta?

### 5. Análise final
- Escreva um breve relatório explicando:
  - Como a escolha da distribuição afeta a visualização dos dados.
  - Por que é importante entender a distribuição dos dados antes de aplicar modelos de Machine Learning.
  - Exemplos de situações reais onde cada tipo de distribuição pode aparecer (ex: altura de pessoas, tempo de atendimento, sorteios, etc).

---

> Utilize as funções e conceitos apresentados nos capítulos 7 e 8 para resolver cada etapa. Dica: use `matplotlib.pyplot` para visualização. 