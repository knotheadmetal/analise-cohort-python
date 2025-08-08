# Projeto de Análise de Cohort em Python

Este repositório contém um projeto de análise de cohort desenvolvido em Python, utilizando as bibliotecas Pandas, Matplotlib e Seaborn. O objetivo principal é analisar o comportamento de grupos de usuários (cohortes) ao longo do tempo, com foco em retenção e engajamento.

## Objetivo do Projeto

Analisar o comportamento de grupos de usuários (cohortes) ao longo do tempo, baseado na primeira data de compra, para entender retenção, engajamento ou churn. Este projeto serve como um item de portfólio para análise de dados, sendo simples, bem estruturado e guiado passo a passo.

## Ferramentas Utilizadas

*   **Python**: Linguagem de programação.
*   **Pandas**: Para manipulação e análise de dados.
*   **Matplotlib e Seaborn**: Para visualização de dados, especialmente a criação do heatmap de retenção.
*   **Google Colab**: Ambiente de execução (o notebook Jupyter pode ser facilmente executado no Google Colab).

## Dataset

O dataset utilizado é o **Online Retail Dataset** do UCI Machine Learning Repository. Este conjunto de dados transacionais contém todas as compras realizadas por um varejista online baseado no Reino Unido entre 01/12/2010 e 09/12/2011.

## Estrutura do Projeto

O projeto é composto pelos seguintes arquivos:

*   `cohort_analysis_project.ipynb`: O notebook Jupyter completo com todas as etapas da análise, incluindo código, explicações e visualizações.
*   `cohort_retention_heatmap.png`: A imagem do heatmap gerado, que visualiza a matriz de retenção.
*   `cohort_analysis_report.md`: Um relatório textual detalhado com a interpretação dos resultados da análise de cohort e sugestões de negócio.
*   `Online Retail.xlsx`: O dataset original utilizado no projeto.
*   `README.md`: Este arquivo, com uma visão geral do projeto.

## Etapas da Análise

O projeto seguiu as seguintes etapas:

1.  **Importação e Visualização Inicial dos Dados**: Carregamento do dataset e uma primeira inspeção para entender sua estrutura e tipos de dados.
2.  **Limpeza e Preparação dos Dados**: Tratamento de valores ausentes, conversão de tipos de dados, remoção de duplicatas e filtragem de transações inválidas (quantidades e preços negativos/zero).
3.  **Criação das Cohortes**: Identificação da primeira data de compra para cada cliente e atribuição a uma cohorte. Cálculo do mês de atividade para cada compra e do índice de cohorte.
4.  **Cálculo da Retenção Mensal**: Determinação da porcentagem de usuários de cada cohorte que permaneceram ativos mês após mês.
5.  **Visualização da Análise de Cohort**: Criação de um heatmap para visualizar a matriz de retenção, facilitando a identificação de padrões.
6.  **Interpretação dos Resultados**: Análise dos padrões de retenção no heatmap, identificação de tendências e anomalias, e elaboração de uma análise textual detalhada.
7.  **Sugestões de Negócio**: Propostas de estratégias para melhorar a retenção de clientes com base nos insights obtidos da análise.

## Como Executar o Projeto

1.  **Clone o Repositório**: `git clone https://github.com/knotheadmetal/analise-cohort-python.git`
2.  **Abra no Google Colab**: Faça o upload do arquivo `cohort_analysis_project.ipynb` para o Google Colab.
3.  **Certifique-se do Dataset**: O arquivo `Online Retail.xlsx` deve estar no mesmo ambiente de execução do notebook.
4.  **Execute as Células**: Siga as células do notebook sequencialmente para reproduzir a análise.

## Contribuições

Sinta-se à vontade para explorar, usar e adaptar este projeto para seus próprios estudos ou portfólio. Sugestões e melhorias são bem-vindas!


