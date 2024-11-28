# Projecto_18
 
Previsão de Renda Anual 
Este projeto usa algoritmos de Machine Learning para prever se uma pessoa com certos atributos excede uma renda anual de $50.000. A análise compara três modelos de classificação — Naive Bayes, Árvore de Decisão e Random Forest — e identifica o modelo mais eficaz para este problema.

1. Objetivo do Projeto
O objetivo é prever se um indivíduo ganha mais de $50.000 anuais com base em atributos demográficos e socioeconômicos presentes na base de dados de censo de 1994. Este é um problema de classificação binária, onde as classes são:

<=50K: Renda anual até $50.000.
>50K: Renda anual acima de $50.000.
Como esse problema envolve balanceamento entre precisão e recall, são usadas métricas como acurácia, precisão, recall e f1-score para avaliar o desempenho dos modelos.

A base de dados foi extraída por Barry Becker e está disponível para consulta no link(https://archive.ics.uci.edu/ml/datasets/adult).

2. Estrutura do Projeto
O projeto é dividido em diversas etapas, descritas no notebook, para garantir uma abordagem estruturada de análise e modelagem dos dados:

Análise Exploratória dos Dados (EDA): Exploração inicial para entender as características das variáveis e distribuição dos dados.
Visualização dos Dados: Gráficos e visualizações para compreender a relação entre as variáveis.
Codificação de Variáveis Categóricas: Transformação de variáveis categóricas para formato numérico, facilitando o uso em algoritmos de Machine Learning.
Escalonamento e Padronização dos Dados: Ajuste das variáveis numéricas para otimizar o desempenho dos algoritmos.
Divisão dos Dados: Separação dos dados em conjuntos de treinamento e teste para validação justa dos modelos.

Treinamento e Avaliação dos Modelos:
Naive Bayes
Árvore de Decisão
Random Forest

Relatório e Interpretação dos Resultados: Análise das métricas e comparação do desempenho dos modelos.

3. Modelos Utilizados e Resultados
3.1 Naive Bayes
Acurácia Geral: 48%
Desempenho por Classe:
Classe <=50K: precisão de 0.97, recall de 0.32, f1-score de 0.48.
Classe >50K: precisão de 0.31, recall de 0.97, f1-score de 0.48.
Interpretação: O Naive Bayes apresenta dificuldades de balancear o desempenho entre as classes, com baixa acurácia e desempenho inconsistente. O modelo não é o mais adequado para este problema, pois apresenta recall baixo na classe <=50K, resultando em baixa detecção de quem ganha até $50K.

3.2 Árvore de Decisão
Acurácia Geral: 81%
Desempenho por Classe:
Classe <=50K: precisão de 0.88, recall de 0.87, f1-score de 0.87.
Classe >50K: precisão de 0.61, recall de 0.61, f1-score de 0.61.
Interpretação: A árvore de decisão fornece um desempenho balanceado, com alta acurácia e métricas relativamente equilibradas para ambas as classes, embora o desempenho na classe >50K possa ser melhorado. Este modelo é uma escolha razoável, mas tem margem para ajustes.

3.3 Random Forest
Acurácia Geral: 85%
Desempenho por Classe:
Classe <=50K: precisão de 0.88, recall de 0.93, f1-score de 0.90.
Classe >50K: precisão de 0.73, recall de 0.62, f1-score de 0.67.
Interpretação: O Random Forest alcança a melhor acurácia e métricas bem equilibradas entre as classes, especialmente para a classe <=50K. Para a classe >50K, o desempenho também é bom, embora ainda com margem para melhorias no recall. Esse modelo é a escolha mais robusta para esse problema.

4. Comparação e Considerações Finais
Naive Bayes: A baixa acurácia e o desempenho inconsistente entre as classes indicam que esse modelo é inadequado para o problema, possivelmente devido às suposições de independência entre as variáveis.
Árvore de Decisão: Este modelo apresenta um desempenho razoável, com métricas equilibradas entre as classes. Ainda assim, a acurácia e o f1-score para a classe >50K indicam que há espaço para otimização.
Random Forest: Com o melhor desempenho geral e a maior acurácia, o Random Forest demonstra ser o modelo mais adequado para este problema, equilibrando bem as métricas de ambas as classes.

6. Conclusão e Recomendação
O Random Forest é o modelo mais indicado para este projeto, com acurácia de 85% e um desempenho bem balanceado entre precisão e recall para ambas as classes. Para melhorar a performance na classe >50K, recomenda-se:
Ajuste de Hiperparâmetros: Testar diferentes profundidades, número de estimadores e critérios de divisão.
Técnicas de Balanceamento: Aplicar técnicas de oversampling para melhorar o recall da classe >50K.
Este modelo pode ser usado para prever de forma robusta a renda anual dos indivíduos, auxiliando em análises e decisões baseadas em atributos socioeconômicos.

6. Repositório
O notebook do projeto contém a implementação completa dos modelos, pré-processamento e análise dos resultados. As seções incluem desde a análise exploratória dos dados até o relatório detalhado das métricas de cada modelo.


Nota: Os dados deste projeto foram extraídos de uma base de dados pública e estão disponíveis para consulta através do link [Census Income Dataset](https://archive.ics.uci.edu/ml/datasets/adult).

Organização do Repositório
notebooks/: Contém o notebook principal com a análise de dados, implementação dos modelos e relatórios de desempenho.
data/: Arquivo de dados em formato CSV para fácil acesso e replicação do projeto.
