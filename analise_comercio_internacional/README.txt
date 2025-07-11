# Análise Preditiva e Estratégica do Comércio Internacional

## Sobre o Projeto

Este projeto utiliza técnicas de **Machine Learning** para analisar dados de comércio internacional.

O objetivo principal é **prever o valor financeiro** de transações comerciais com base em variáveis como país, setor do produto e tipo de fluxo (importação/exportação). Para isso, foi desenvolvido um modelo de Regressão (*Random Forest*) que alcançou uma alta precisão (**R² de 0,991**), mostrando-se uma ferramenta útil para planejamento estratégico.

## Tecnologias Utilizadas

* **Linguagem:** Python
* **Bibliotecas Principais:**
    * **Pandas:** Para manipulação e tratamento dos dados.
    * **Scikit-Learn:** Para a criação do modelo preditivo.
    * **SpaCy:** Para a análise de texto (NLP) dos setores de produtos.
    * **Matplotlib / Seaborn:** Para a criação de gráficos.

## Estrutura do Repositório

```
└── analise_comercio_internacional/
    ├── data/         # Contém o arquivo .csv com os dados
    ├── notebooks/    # Contém os notebooks Jupyter com as análises
    └── README.md     # Este arquivo
```