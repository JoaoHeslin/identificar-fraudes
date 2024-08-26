# Projeto de Detecção de Fraudes em Cartões de Crédito

## Descrição
Este projeto visa identificar fraudes em transações de cartões de crédito utilizando técnicas de aprendizado de máquina. A base de dados utilizada contém informações de transações, e o objetivo é classificar essas transações como fraudulentas ou não fraudulentas.

## Estrutura do Projeto
- *Dados*: A base de dados contém informações sobre transações, incluindo tempo, valor e variáveis derivadas com PCA.
- *Modelos*: Diversos modelos de aprendizado de máquina foram testados para encontrar o melhor desempenho na detecção de fraudes.

## Objetivo
O objetivo principal é desenvolver um modelo que possa identificar fraudes de forma eficaz, priorizando a métrica de recall para garantir que a maior quantidade possível de fraudes seja detectada.

## Metodologia

### 1. Importação e Pré-processamento dos Dados
- *Importação dos Dados*: A base de dados é carregada e inspecionada para verificar a presença de valores nulos, duplicatas e dados desbalanceados.
- *Análise Exploratória*: Exploração dos dados para entender a distribuição das transações e verificar a necessidade de balanceamento.

### 2. Balanceamento dos Dados
- *Random Under-Sampling*: A classe majoritária foi reduzida para balancear os dados e melhorar a capacidade do modelo de detectar fraudes.

### 3. Modelagem
- *Modelos Testados*: Regressão Logística, Árvore de Decisão, SVC, KNN e Random Forest.
- *Avaliação de Modelos*: Métricas como acurácia, precisão, recall e AUC foram usadas para avaliar o desempenho dos modelos.

### 4. Ajuste de Hiperparâmetros
- *GridSearchCV*: Ajuste dos parâmetros do modelo de Regressão Logística para otimizar o desempenho com base na métrica de recall.

### 5. Resultados
- *Modelo Selecionado*: Regressão Logística foi escolhida devido ao seu bom equilíbrio entre precisão e recall, com uma alta taxa de recall (90.12%).
- *Resultados do GridSearchCV*:
  - *Acurácia*: 96.07%
  - *Precisão*: 3.82%
  - *Recall*: 90.12%
