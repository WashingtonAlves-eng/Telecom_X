# Análise de Churn de Clientes da Telecom X

Este projeto realiza uma análise exploratória de dados (EDA) e constrói modelos de machine learning para prever o churn (cancelamento de serviço) de clientes da empresa fictícia Telecom X. O objetivo é identificar os principais fatores que influenciam a decisão dos clientes de cancelar seus serviços e, com base nesses insights, propor estratégias para melhorar a retenção.

## 🚀 Propósito da Análise

O principal objetivo deste projeto é entender as causas do churn de clientes na Telecom X. Ao identificar os padrões e características dos clientes que cancelam seus serviços, a empresa pode desenvolver estratégias mais eficazes para:

  * **Reduzir a taxa de churn**: Implementar ações direcionadas para reter clientes em risco.
  * **Melhorar a satisfação do cliente**: Entender os pontos de atrito e melhorar a experiência do cliente.
  * **Otimizar a alocação de recursos**: Focar os esforços de retenção nos segmentos de clientes mais propensos a cancelar.
  * **Aumentar a lucratividade**: Manter clientes existentes é mais econômico do que adquirir novos.

## 📂 Estrutura do Projeto

O repositório está organizado da seguinte forma:

  * `Telecom_X.ipynb`: Notebook Jupyter contendo todo o processo de análise, desde a importação das bibliotecas, carregamento dos dados, limpeza, transformação, até a análise exploratória e a construção dos modelos de machine learning.
  * `TelecomX_Data.json`: O conjunto de dados original em formato JSON, contendo informações demográficas dos clientes, serviços contratados e status de churn.
  * `README.md`: Este arquivo, que fornece uma visão geral do projeto, seus objetivos, e como executá-lo.

## 📊 Análise e Insights

A análise exploratória dos dados revelou vários padrões significativos que ajudam a entender por que os clientes estão cancelando seus serviços.

### 1\. Perfil Geral do Churn

A taxa de churn geral na base de dados é de aproximadamente **26,5%**, o que representa uma perda considerável de clientes e justifica uma investigação mais aprofundada.


### 2\. Relação entre o Churn e os Serviços Contratados

  - **Tipo de Contrato**: O tipo de contrato é um dos indicadores mais fortes de churn. Clientes com contrato **Mês a Mês** cancelam em uma proporção muito maior do que aqueles com contratos de um ou dois anos, que demonstram maior fidelidade.
  - **Serviço de Internet**: Clientes com **Fibra Óptica** têm uma taxa de churn significativamente maior do que aqueles com DSL. Isso pode estar relacionado ao custo mais elevado ou a problemas de qualidade percebida.
  - **Serviços de Proteção e Suporte**: Clientes sem serviços de **Segurança Online**, **Backup Online** e **Suporte Técnico** são muito mais propensos a cancelar. Esses serviços adicionais parecem aumentar a percepção de valor e a lealdade do cliente.


### 3\. Fatores Demográficos e Financeiros

  - **Idosos (SeniorCitizen)**: Clientes idosos apresentam uma taxa de churn consideravelmente maior em comparação com os mais jovens. Isso sugere que este grupo pode ter necessidades específicas que não estão sendo atendidas.
  - **Cobranças Mensais**: Clientes que cancelam tendem a ter cobranças mensais mais altas. A mediana do valor mensal para clientes que cancelaram é significativamente maior do que para os que permaneceram.
  - **Forma de Pagamento**: Clientes que pagam com **Cheque Eletrônico** são muito mais propensos a cancelar.


## 🤖 Modelagem Preditiva

Para prever o churn de clientes, foram treinados e avaliados quatro modelos de classificação:

1.  **Regressão Logística**
2.  **Árvore de Decisão**
3.  **Random Forest**
4.  **XGBoost**

O modelo **XGBoost** apresentou o melhor desempenho geral, com uma acurácia de **79.5%** no conjunto de teste. Este modelo pode ser utilizado para identificar proativamente clientes com alta probabilidade de churn, permitindo que a empresa tome medidas preventivas.

## 🚀 Como Executar o Notebook

Para reproduzir esta análise, siga os passos abaixo:

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
    ```
2.  **Navegue até o diretório do projeto:**
    ```bash
    cd nome-do-repositorio
    ```
3.  **Instale as dependências necessárias:**
    ```bash
    pip install pandas plotly scikit-learn
    ```
4.  **Execute o Jupyter Notebook:**
    Abra o arquivo `Telecom_X.ipynb` em um ambiente Jupyter (como Jupyter Notebook, JupyterLab ou Google Colab) e execute as células na ordem em que aparecem. O notebook irá carregar os dados, realizar a limpeza e gerar as visualizações e modelos apresentados neste README.

> **Nota:** O notebook busca o arquivo de dados (`TelecomX_Data.json`) diretamente de um link da web, portanto, não é necessário fazer o download manual dos dados, desde que você tenha uma conexão com a internet.
