# 🚀 Projeto de Machine Learning: Previsão de Custos de Seguro de Saúde

## 📋 Sobre o Projeto

Este projeto teve como objetivo construir e avaliar modelos de machine learning para prever os custos individuais de seguro saúde. O fluxo de trabalho abrange desde a análise e tratamento dos dados até o treinamento, avaliação e simulação da implantação de um modelo preditivo, utilizando um dataset público sobre segurados.

---

## 📊 Dataset

O dataset utilizado contém informações demográficas e de saúde de segurados. O objetivo é prever a coluna `charges` (custos) com base nas seguintes características:

* **`age`**: Idade do beneficiário.
* **`sex`**: Gênero do contratante (`male`, `female`).
* **`bmi`**: Índice de Massa Corporal (IMC).
* **`children`**: Número de dependentes cobertos pelo plano.
* **`smoker`**: Se a pessoa é fumante (`yes`, `no`).
* **`region`**: Área residencial do beneficiário nos EUA.
* **`charges`**: Custos médicos individuais faturados pelo seguro (variável alvo).

---

## 🛠️ Metodologia e Passos Realizados

O projeto seguiu um pipeline clássico de Ciência de Dados, executando as seguintes etapas:

1.  **Importação de Bibliotecas e Carga dos Dados**: O dataset foi carregado a partir de uma URL pública utilizando a biblioteca `pandas`.

2.  **Tratamento e Preparação dos Dados**:
    * Verificação da integridade do DataFrame, confirmando a ausência de valores nulos.
    * Transformação de colunas categóricas (`sex`, `smoker`, `region`) em formato numérico, utilizando técnicas de Mapeamento e *One-Hot Encoding* para torná-las compatíveis com os algoritmos de machine learning.

3.  **Análise Exploratória dos Dados (EDA)**:
    * Foram gerados gráficos para explorar a distribuição dos custos, a relação entre o hábito de fumar e os custos, e uma matriz de correlação entre as variáveis.
    * **Insights principais**: A análise gráfica destacou a forte influência do hábito de fumar (`smoker`) como principal fator no aumento dos custos do seguro.

4.  **Divisão dos Dados**: O dataset foi dividido em três conjuntos para garantir uma avaliação robusta e imparcial dos modelos:
    * **Treino (70%)**: Usado para treinar os algoritmos.
    * **Validação (15%)**: Usado para comparar e selecionar o melhor modelo.
    * **Teste (15%)**: Usado para a avaliação final do modelo escolhido, com dados nunca antes vistos por ele.

5.  **Treinamento dos Modelos**: Três algoritmos de regressão foram treinados com o conjunto de treino:
    * Regressão Linear
    * Random Forest Regressor
    * Gradient Boosting Regressor

6.  **Seleção e Avaliação de Modelos**: Os modelos foram avaliados no conjunto de validação utilizando as métricas **RMSE** (Erro Quadrático Médio) e **R²** (Coeficiente de Determinação). O modelo `Gradient Boosting` obteve o melhor desempenho e foi selecionado.

7.  **Implantação (Simulação)**:
    * O melhor modelo (`Gradient Boosting`) foi salvo em um arquivo (`.pkl`) usando a biblioteca `joblib`.
    * O modelo foi carregado e uma função foi criada para simular seu uso em um ambiente de produção, permitindo prever custos com base em novos dados de entrada.

---

## 🏆 Resultados e Análise de Métricas

O modelo **Gradient Boosting** foi o campeão e, após a seleção, foi avaliado no conjunto de teste para verificar sua performance final.

### Métricas de Avaliação no Conjunto de Teste:

* **RMSE (Root Mean Squared Error): $4,579.74**
    * **O que significa?** Este valor indica que, em média, a previsão do modelo difere em aproximadamente **$4,579.74** do custo real do seguro. Considerando a faixa de valores dos custos, este é um erro razoável.

* **R² (Coeficiente de Determinação): 0.8617**
    * **O que significa?** O nosso modelo consegue explicar aproximadamente **86.17%** da variância nos custos do seguro no conjunto de teste. Este é um resultado excelente e demonstra um alto poder preditivo.

---

## 🏁 Conclusão

O projeto demonstrou com sucesso um fluxo completo de desenvolvimento de um modelo de machine learning, desde a análise inicial até a simulação de implantação. O modelo **Gradient Boosting** provou ser altamente eficaz para esta tarefa, apresentando métricas de desempenho sólidas no conjunto de teste e confirmando sua capacidade de gerar previsões de custo de seguro com boa precisão.

---

## 💻 Como Executar o Projeto

1.  Clone este repositório para a sua máquina local.
2.  Abra o arquivo `.ipynb` no **Google Colab** ou em um ambiente Jupyter.
3.  Execute as células do notebook em ordem sequencial para reproduzir todas as etapas, desde a carga dos dados até a simulação de previsão.