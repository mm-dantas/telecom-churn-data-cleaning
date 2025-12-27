# telecom-churn-data-cleaning

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)

Este repositório contém um projeto focado na etapa de **Data Wrangling** (limpeza e preparação) de dados de uma empresa de telecomunicações. O objetivo principal é transformar dados brutos no formato JSON em um DataFrame estruturado e limpo, pronto para processos de análise exploratória e modelagem preditiva de *Churn*.

## 🚀 Visão Geral

O projeto aborda o desafio comum de manipular dados hierárquicos (JSON aninhado). Através do uso de bibliotecas de análise de dados, realizei a extração, tratamento de inconsistências e a engenharia de atributos necessária para que os dados possam ser interpretados por algoritmos de Machine Learning.

## 🛠️ Etapas do Desenvolvimento

O notebook segue o seguinte fluxo de trabalho:

1.  **Carregamento e Normalização**:
    * Importação dos dados brutos.
    * Utilização da função `json_normalize` para achatar as estruturas de dicionários (como `cliente`, `telefone`, `internet` e `conta`) em colunas separadas.

2.  **Limpeza Inicial**:
    * Identificação e remoção de registros com a variável alvo (`Churn`) vazia.
    * Tratamento de duplicatas no conjunto de dados.

3.  **Tratamento de Dados Faltantes e Tipagem**:
    * Identificação de valores nulos (`NaN`) em colunas como `cliente.tempo_servico`.
    * Conversão de tipos de dados (ex: transformar strings numéricas em `float64`).
    * Tratamento de espaços vazios que não foram capturados como nulos inicialmente.

4.  **Codificação de Variáveis (Encoding)**:
    * Mapeamento de variáveis binárias (sim/nao) para valores numéricos `0` e `1`.
    * Aplicação de técnicas de criação de variáveis *dummy* para atributos categóricos multiclasse (ex: tipo de contrato e método de pagamento).

5.  **Análise e Remoção de Outliers**:
    * Uso de técnicas estatísticas e visualização com `boxplot` para identificar valores atípicos em colunas como `tempo_servico`.
    * Filtragem de outliers para garantir a qualidade estatística dos dados.

## 📁 Estrutura do Arquivo Original

Os dados originais possuem informações sobre:
- **ID e Churn**: Identificação do cliente e se ele cancelou o serviço.
- **Cliente**: Gênero, se é idoso, se possui parceiro ou dependentes e tempo de serviço.
- **Serviços**: Detalhes sobre serviço de telefone, internet, segurança online, streaming, etc.
- **Faturamento**: Tipo de contrato, método de pagamento e valores das faturas.

## ⚙️ Como utilizar

1. Certifique-se de ter o Python e o Pandas instalados.
2. Coloque o arquivo `dataset-telecon.json` na mesma pasta do notebook.
3. Execute as células do notebook `Limpeza_tratamento_churn_.ipynb` sequencialmente.

---
Desenvolvido como parte de um estudo sobre preparação de dados para Ciência de Dados.
