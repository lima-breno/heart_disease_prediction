# ❤️ **Análise de Risco de Doença Cardíaca Coronariana (DCC) em 10 Anos**
Este projeto investiga fatores de risco para doenças cardíacas coronarianas em um horizonte de 10 anos, utilizando dados do estudo Framingham. O objetivo principal é modelar a probabilidade de desenvolver DCC com base em variáveis demográficas, como gênero e idade, através de Regressão Logística, e analisar a relevância de outros fatores como o tabagismo.

## 📜 Workflow do Projeto

1. Preparação, Tratamento e Limpeza de Dados
2. Análise Exploratória Inicial
3. Modelagem de Regressão Logística
   
     3.1 Modelo 1: Avaliação do impacto do gênero no risco de DCC.
  
     3.2 Modelo 2: Avaliação do impacto do gênero e tabagismo no risco de DCC.
  
     3.3 Modelo 3: Avaliação do impacto da idade no risco de DCC.
  
4. Avaliação e Interpretação dos Modelos
     4.1 Testes de adequação do modelo (Teste de Deviance e Pearson Chi-Square).
   
5. Interpretação dos coeficientes (razão de chance - Odds Ratio).
      5.1 Análise de resíduos (Deviance Residuals vs. Fitted Values e vs. Index).
   
6. Avaliação do poder preditivo: Geração e análise de Curvas ROC (Receiver Operating Characteristic) e AUC (Area Under the Curve)
7. Comparação dos modelos via Critério de Informação de Akaike (AIC).


## **Insights Chave**
**Risco por Gênero:** Homens apresentaram chances significativamente menores de desenvolver DCC em comparação com mulheres no Modelo 1.

**Impacto do Tabagismo:** A variável currentSmoker não se mostrou estatisticamente significativa no Modelo 2.

**Impacto da Idade:** A idade é um fator com relação inversa ao risco de DCC neste modelo simplificado, onde um aumento na idade corresponde a uma diminuição das odds de DCC. O Modelo 3 teve o menor AIC, indicando um melhor ajuste.

**Desempenho dos Modelos:** O modelo com a idade (Modelo 3) apresentou o menor AIC, sugerindo ser o mais bem ajustado entre os testados, apesar de um baixo poder preditivo individual (AUC de 0.31).


## **Resultados do Projeto:**

**Modelo 1 (Gênero):** Odds Ratio para homens de 0.60, indicando 40% menos chance de DCC que mulheres. Testes de Deviance e Pearson Chi-Square apresentaram p-valores elevados, sugerindo um bom ajuste. AUC de aproximadamente 0.53, indicando baixo poder preditivo.
**Modelo 2 (Gênero + Tabagismo):** A variável Tabagismo não foi estatisticamente significativa (p-valor > 0.05), sugerindo que ser fumante não demonstrou influência direta no risco de DCC neste modelo.
**Modelo 3 (Idade):** Odds Ratio para idade de 0.925, indicando que para cada ano adicional, as chances de DCC diminuem em cerca de 7.47%. Este modelo obteve o menor AIC (2924.29) entre os três, mas sua Curva ROC com AUC de 0.31 indica que a idade, por si só, é um preditor muito fraco para DCC.

## **Conclusão:**
Os modelos iniciais de regressão logística apontam que o gênero e a idade são fatores relacionados ao risco de DCC. Homens apresentam menores chances de desenvolver a doença em comparação com mulheres, enquanto um aumento na idade está associado a uma leve diminuição nas odds de DCC neste contexto. No entanto, é crucial notar que a variável tabagismo não se mostrou relevante e que os modelos univariados apresentam baixo poder preditivo, conforme indicado pelos valores de AUC. A amostra desbalanceada de gênero pode influenciar os resultados, e a inclusão de mais variáveis preditoras seria necessária para construir um modelo mais robusto e preditivo.

## **🛠️ Tech Stack**
🐍 Python

🐼 Pandas

📊 Seaborn / Matplotlib

🔢 NumPy

📉 Statsmodels (Regressão Logística)

🧪 SciPy

🤖 Scikit-learn (Sklearn)
