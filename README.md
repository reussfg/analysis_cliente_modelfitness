# Análise de Clientes da Academia Model Fitness com Modelo de Machine Learning

## Introdução ao Projeto

No ambiente de crescente concorrência das academias, a Model Fitness busca se destacar ao utilizar abordagens analíticas avançadas para entender a rotatividade de seus membros. Utilizando o ambiente Jupyter, este projeto tem como objetivo compreender e prever o churn (rotatividade) dos clientes, alavancando dados históricos e técnicas preditivas para guiar decisões proativas de retenção.

## Problema da Rotatividade

A retenção de clientes é um pilar fundamental para o sucesso de qualquer negócio, especialmente em academias. O churn, ou rotatividade de clientes, é o fenômeno de clientes deixando a academia, o que pode ocorrer por inúmeros motivos. Identificar os sinais de um cliente potencialmente desistente permite ações estratégicas para mantê-lo.

## Objetivos do Projeto

O escopo deste projeto abrange:

### 1. Preparação e Análise Exploratória dos Dados
Analisaremos os dados fornecidos pela Model Fitness, abrangendo informações sobre comportamento, frequência e características dos clientes.

### 2. Construção de Modelos Preditivos

**3. Modelo de Rotatividade de Cliente**

Com o intuito de prever a rotatividade de clientes, construiremos um modelo de classificação binária. O objetivo será identificar a saída de usuários no mês subsequente.

Iremos realizar o seguinte procedimento:

- Dividir os dados em conjuntos de treinamento e validação usando a função `train_test_split()`.
  
- Treinar modelos de classificação utilizando:
  * Regressão logística
  * Floresta aleatória
  
- Avaliar métricas como acurácia, precisão e sensibilidade nos modelos treinados para compará-los.

```python
# Carregando bibliotecas de modelagem e métricas
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, precision_score, recall_score
```

### 4. Agrupamento de Clientes - Clusterização

Na etapa de clusterização, nosso objetivo é agrupar os clientes em segmentos baseados em características similares. Para isso, seguiremos os passos:

- Definição e tratamento de colunas pertinentes à rotatividade.
  
- Padronização dos dados para melhor eficiência nos modelos de clusterização.
  
- Uso da função `linkage()` para construir a matriz de distância e subsequente visualização via dendrograma.
  
- Aplicação do algoritmo K-means para segmentar os clientes em grupos (n=5 para fins deste projeto).
  
- Análise dos valores médios e distribuição das características nos clusters.
  
- Avaliação da taxa de rotatividade para cada cluster usando o método `groupby()`.

Ao final dessa etapa, buscaremos responder:

- Os clusters diferem em termos de taxa de rotatividade?
- Quais clusters tendem a apresentar maior churn e quais são mais leais?

---

A combinação de análise exploratória, modelagem preditiva e clusterização proporcionará uma compreensão abrangente do comportamento dos clientes da Model Fitness. A partir dos insights gerados, poderemos guiar estratégias proativas para otimizar a retenção de clientes e fortalecer o relacionamento com eles.
