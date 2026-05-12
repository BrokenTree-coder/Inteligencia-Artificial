\# 📊 Análise de Dados e Modelagem Preditiva: Do PCA a Regressões



Este repositório contém um pipeline de Ciência de Dados dividido em três etapas principais, implementadas em Jupyter Notebooks. O projeto abrange desde a exploração inicial dos dados até a aplicação de técnicas de redução de dimensionalidade e algoritmos de aprendizado supervisionado para regressão.



\---



\## 🏗️ Estrutura do Projeto



O projeto está organizado de forma sequencial, onde cada notebook representa uma fase do pipeline de Machine Learning:







\### 1. 🔍 Exploração e Preparação (`dataset\\\_ini.ipynb`)

Nesta etapa inicial, o foco é entender a natureza dos dados.

\- Carregamento do dataset.

\- Análise exploratória de dados (EDA).

\- Tratamento de valores ausentes e limpeza de dados.

\- Visualização de distribuições e correlações iniciais.



\### 2. 📉 Redução de Dimensionalidade (`pca\\\_pre\\\_supervision.ipynb`)

Antes da modelagem, aplicamos técnicas para lidar com a alta dimensionalidade e ruídos.

\- Normalização/Padronização de dados.

\- Implementação do \*\*Principal Component Analysis (PCA)\*\*.

\- Análise da variância explicada para determinar o número ideal de componentes.

\- Preparação do dataset "reduzido" para o aprendizado supervisionado.



\### 3. 📈 Modelagem Preditiva (`regressions.ipynb`)

A fase final onde os modelos são treinados para realizar predições.

\- Divisão entre conjuntos de treino e teste.

\- Implementação de diferentes algoritmos de \*\*Regressão\*\* (ex: Linear, Ridge, Lasso ou outros).

\- Avaliação de métricas de performance (MSE, RMSE, R²).

\- Comparação de resultados entre os dados originais e os dados processados via PCA.



\---



\## 🛠️ Tecnologias e Bibliotecas



As seguintes ferramentas foram utilizadas no desenvolvimento deste projeto:



\- Python 3

\- Pandas \& NumPy: Manipulação e processamento de dados.

\- Scikit-learn: Implementação de PCA e modelos de Machine Learning.

\- Matplotlib \& Seaborn: Visualização de dados e gráficos estatísticos.

\- Jupyter Notebook: Ambiente de desenvolvimento e documentação das análises.



\---



\## 🚀 Como Executar o Projeto



1\. Clone o repositório:



&#x09;```bash



&#x09;git clone \[https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)



2\. Crie um ambiente virtual (recomendado):



&#x09;```bash



&#x09;python -m venv .venv

&#x09;source .venv/bin/activate  # No Linux/WSL



3\. Instale as dependências:



&#x09;```bash



&#x09;pip install pandas numpy scikit-learn matplotlib seaborn notebook



4\. Inicie o Jupyter:



&#x09;```bash



&#x09;jupyter notebook

