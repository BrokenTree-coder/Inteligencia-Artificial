# 📊 Análise de Dados e Modelagem Preditiva: Regressão (NBA) e Classificação (Performance)

Este repositório contém um projeto prático de Inteligência Artificial dividido em duas frentes de análise principais: previsão de sucesso de times da NBA (Regressão) e avaliação de performance física humana (Classificação). O pipeline abrange desde o tratamento dos dados brutos até a aplicação de técnicas de redução de dimensionalidade (PCA) e múltiplos algoritmos de aprendizado supervisionado e não supervisionado.

---

## 🏗️ Estrutura do Projeto

O projeto resolve dois problemas distintos de Machine Learning, documentados em profundidade:

### 1. 🏀 Regressão: Previsão de Sucesso na NBA

**Objetivo:** Prever o número de vitórias de um time nos Playoffs utilizando exclusivamente suas estatísticas da temporada regular.

* **Dataset:** Dados estatísticos extraídos via `nba_api` abrangendo as temporadas regulares de 1996 a 2024, totalizando cerca de 800 amostras.
* **Engenharia de Atributos:** O dataset bruto de 47 colunas foi refinado para 13 variáveis relevantes (como `OFF_RATING`, `DEF_RATING`, `TS_PCT`, `PACE`), tendo `PLAYOFF_WINS` como variável alvo.
* **Modelagem e Resultados:** Foram testados Regressão Linear, Decision Tree, Random Forest, XGBoost, SVR e Rede Neural (MLP). 
* A **Rede Neural (MLP)** obteve a melhor performance, alcançando um $R^{2}$ de 0.49 e provando ser a mais eficaz para identificar a equipe campeã (previu 14.6 vitórias para o Boston Celtics na base de teste).
* O **SVR** obteve o menor Erro Absoluto (MAE de 1.92), mas penalizou-se por ser conservador demais nas extremidades.
* **Agrupamento:** O uso de K-Means e DBSCAN revelou que forçar os times em "prateleiras" isoladas não é o ideal, pois o nível técnico da NBA atua como um espectro contínuo.

### 2. 🏃‍♂️ Classificação: Body Performance

**Objetivo:** Classificar o desempenho físico de indivíduos em quatro categorias (A, B, C e D) baseando-se em métricas corporais e testes atléticos.

* **Dataset:** Dados da Korea Sports Promotion Foundation via Kaggle, incluindo idade, percentual de gordura, pressão arterial, força de pegada, flexibilidade e saltos.
* **Modelagem e Resultados:** Avaliamos Regressão Logística, SVM (SVC), Rede Neural (MLP), Árvore de Decisão, Random Forest e XGBoost.
* Nos dados padronizados normais, o **XGBoost** liderou os resultados com uma acurácia de 76,30% e um ROC-AUC de 92,81%.
* **Análise de PCA:** A aplicação do PCA para reduzir o problema a 2D explicou 63,58% da variância total, no entanto, impactou negativamente a performance preditiva, fazendo as acurácias dos modelos caírem para a faixa de 38% a 41%.

---

## 🛠️ Tecnologias e Bibliotecas

As seguintes ferramentas compuseram o ambiente de desenvolvimento:

* **Python 3**
* **Pandas & NumPy:** Manipulação de dados, tratamento de nulos e normalização com `StandardScaler`.
* **Scikit-learn:** Redução com PCA, algoritmos de clustering (K-Means, DBSCAN) e criação de pipelines de modelos de ML.
* **XGBoost:** Otimização via gradient boosting para classificação e regressão.
* **Matplotlib & Seaborn:** Criação de matrizes de confusão, correlação, Silhouette Plots e projeções 2D.
* **Jupyter Notebook:** Ambiente de desenvolvimento para exploração interativa.

---

## 🚀 Como Executar o Projeto

* Clone o repositório:

```bash
   git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
   ```

* Crie e ative um ambiente virtual (recomendado):

```bash
   python -m venv .venv
   source .venv/bin/activate  # No Linux/WSL
   ```

* Instale as dependências essenciais no .venv:

```bash
   pip install pandas numpy scikit-learn xgboost matplotlib seaborn jupyer ipykernel kagglehub
   ```

* Agora voce pode refazer todas as etapas.
