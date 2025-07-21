# Projeto 9 — Análise Completa de Dados: Do Básico à Distribuição

## Contexto

Você foi contratado como cientista de dados para analisar o desempenho de uma turma de alunos em uma escola. Além das notas finais, você também recebeu dados sobre o tempo (em minutos) que cada aluno levou para completar uma prova. Seu objetivo é realizar uma análise estatística completa, identificar padrões, possíveis problemas e apresentar recomendações para a equipe pedagógica.

---

## Dados

```python
notas = [55, 70, 68, 90, 88, 76, 95, 60, 80, 85, 78, 92, 73, 65, 87, 81, 77, 69, 84, 79, 91, 74, 82, 67, 89, 72, 83, 66, 93, 71]
tempos = [45, 50, 48, 60, 55, 52, 65, 49, 54, 58, 53, 62, 51, 47, 59, 56, 57, 46, 61, 55, 63, 50, 60, 48, 64, 49, 58, 47, 66, 52]
```

---

## Tarefas

### 1. Preparação do ambiente
- (Opcional) Crie e ative um ambiente virtual e instale as bibliotecas necessárias (`numpy`, `scipy`, `matplotlib`).

### 2. Estatística básica
- Calcule a média, mediana e moda das notas e dos tempos.
- Explique o que cada medida revela sobre o desempenho e o comportamento dos alunos.

### 3. Medidas de dispersão
- Calcule a variância e o desvio padrão das notas e dos tempos.
- O grupo é homogêneo ou heterogêneo em relação a cada variável?

### 4. Percentis
- Calcule o 25º, 50º e 75º percentis das notas e dos tempos.
- O que esses percentis indicam sobre a turma?

### 5. Visualização e análise de distribuição
- Plote histogramas das notas e dos tempos (20 barras cada).
- As distribuições se parecem mais com uma distribuição normal ou uniforme? Justifique.

### 6. Simulação de distribuição normal
- Gere um array de 1.000 valores normalmente distribuídos com média igual à média das notas e desvio padrão igual ao das notas.
- Plote o histograma desses valores e compare com o histograma real das notas.
- O que você observa?

### 7. Análise final
- Escreva um relatório respondendo:
  - Como é o perfil da turma em relação a desempenho e tempo de prova?
  - Existem alunos com desempenho ou tempo muito fora do padrão? O que pode ser feito?
  - Por que é importante entender a distribuição dos dados antes de tomar decisões pedagógicas?

---

> Utilize todos os conceitos e funções apresentados ao longo da trilha de estudos para resolver cada etapa. Seja detalhado nas análises e justificativas. 