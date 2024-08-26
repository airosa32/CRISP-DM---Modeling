# CRISP - DM: Modeling

# Análise e Modelagem de Regressão para Estimativa de Preços de Casas em Boston
## 1. Introdução
O objetivo deste projeto foi construir e avaliar modelos de machine learning para prever o preço de imóveis em Boston, utilizando um conjunto de dados com diversas características das casas. A abordagem incluiu a aplicação de técnicas de regressão, como Regressão Linear, Support Vector Regression (SVR) e Regressão com Árvore de Decisão utilizando XGBoost. Além disso, foi realizada uma otimização dos hiperparâmetros do modelo XGBoost para melhorar a precisão das previsões.

## 2. Preparação dos Dados
Os dados foram obtidos do conjunto de dados de Boston Housing. Inicialmente, os dados foram lidos e processados para formar um DataFrame com as seguintes colunas: CRIM, ZN, INDUS, CHAS, NOX, RM, AGE, DIS, RAD, TAX, PTRATIO, B, LSTAT e MEDV. Após a leitura e transformação dos dados, o DataFrame foi preparado para a modelagem, com separação das características das casas (X) e dos preços (Y).

## 3. Técnicas de Modelagem
### 3.1 Regressão Linear
A Regressão Linear foi aplicada para prever os preços das casas. A métrica de avaliação usada foi o Erro Quadrático Médio (MSE) e a Raiz do Erro Quadrático Médio (RMSE). Os resultados obtidos foram:
- MSE Linear: 24.29
- RMSE Linear: 4.93
 
### 3.2 Support Vector Regression (SVR)
A SVR foi utilizada para capturar relações não lineares entre as variáveis. Os resultados das métricas foram:
- MSE SVR: 52.84
- RMSE SVR: 7.27
  
### 3.3 Regressão com Árvore de Decisão (XGBoost)
A técnica de Regressão com XGBoost, conhecida por sua capacidade de lidar com grandes quantidades de dados e melhorar a performance dos modelos, foi aplicada. As métricas obtidas foram:
- MSE XGB: 6.91
- RMSE XGB: 2.63
  
## 4. Otimização de Hiperparâmetros
Para aprimorar o desempenho do modelo XGBoost, foi realizada uma otimização dos hiperparâmetros utilizando o método GridSearchCV. A busca envolveu a variação de parâmetros como max_depth, learning_rate, gamma, min_child_weight, entre outros. Os melhores parâmetros encontrados foram:
- booster: gbtree
- gamma: 0
- learning_rate: 0.2
- max_delta_step: 0
- max_depth: 5
- min_child_weight: 1
- n_jobs: 5
- objective: reg
- subsample: 1

Após a otimização, os resultados das métricas foram:
- MSE XGB com GRID: 6.06
- RMSE XGB com GRID: 2.46
  
## 5. Conclusão
Através da modelagem e otimização, o modelo XGBoost com hiperparâmetros ajustados apresentou o melhor desempenho na previsão de preços de imóveis em Boston. O erro médio de previsão foi reduzido para 2.46 dólares, indicando uma melhoria significativa em relação aos modelos iniciais. Essa otimização demonstra a importância de ajustar os parâmetros dos modelos para obter resultados mais precisos e confiáveis.


