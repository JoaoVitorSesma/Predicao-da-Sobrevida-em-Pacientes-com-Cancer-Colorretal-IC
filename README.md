# **Predição de Sobrevida em Pacientes com Câncer Colorretal com Dados da FOSP**

## Descrição do Projeto:
  
Este projeto explora a análise de sobrevivência com foco em dados de saúde. Utilizando técnicas de regressão de Cox e curvas de Kaplan-Meier, o objetivo é prever tempos de sobrevida em pacientes, proporcionando insights sobre fatores de risco e probabilidade de sobrevivência ao longo do tempo.

## Estrutura do Projeto
O projeto é composto por dois notebooks principais e um outro notebook de curvas de sobrevivência:

### [1. Predição da Sobrevida em Pacientes com Câncer Colorretal - COX](https://colab.research.google.com/github/JoaoVitorSesma/Predicao-da-Sobrevida-em-Pacientes-com-Cancer-Colorretal-IC/blob/main/Predi%C3%A7%C3%A3o_da_Sobrevida_em_Pacientes_com_C%C3%A2ncer_Colorretal_COX.ipynb)
Este notebook realiza a aplicação do modelo de COX diretamente no Banco de Dados da FOSP, para poder fazer a predição sobrevivência. Sendo assim, o código foi estruturado da seguinte maneira:

#### Importação e Pré-Processamento dos Dados: Preparação dos dados, incluindo limpeza e codificação de variáveis categóricas.

#### Ajuste do Modelo: Configuração e ajuste do modelo de Cox, seguido pela seleção de variáveis significativas com base nos p-values.

#### Métricas de Avaliação: Cálculo de métricas de desempenho, como C-Index, MSE, RMSE, MAE, MAPE e R² para avaliar a precisão do modelo.

#### Predição de Sobrevida: Estimativa dos tempos de sobrevida esperados, com comparações entre o modelo original e o modelo ajustado com variáveis significativas.

#### Visualização com Gráficos:
- Comparação entre valores reais e previsões.
- Distribuição dos resíduos (diferença entre tempos reais e previstos).
- Curva de Sobrevivência Kaplan-Meier, representando a probabilidade de sobrevivência ao longo do tempo.
- Histograma da distribuição dos tempos de sobrevivência ao longo dos 60 meses.
Esses gráficos fornecem uma visão intuitiva e ajudam a validar os resultados do modelo, permitindo identificar possíveis melhorias ou ajustes.

### [2. Banco de Dados (Lifelines)](https://colab.research.google.com/github/JoaoVitorSesma/Predicao-da-Sobrevida-em-Pacientes-com-Cancer-Colorretal-IC/blob/main/Banco_de_Dados_(Lifelines).ipynb)
Nesse outro notebook foi feita a implementação do modelo de COX que serviu como um modelo experimental, antes de ser feita a análise definitiva para o Banco de Dados da FOSP. Sendo um notebook instrutivo de como o modelo foi aplicado, além de outros diversos ensinamentos. Esse notebook está dividido nas seguintes partes:

#### Importação e Processamento de Dados:

- Uso do conjunto de dados load_breast_cancer, contendo 198 amostras e 82 variáveis.
- Pré-processamento com OneHotEncoder para codificação de variáveis categóricas.

#### Criação de colunas auxiliares:
- days: Representa o tempo de sobrevivência em dias.
- event: Indica se o evento de interesse (morte) ocorreu.

#### Ajuste do Modelo de Cox:
- Ajuste do modelo utilizando o CoxPHFitter da biblioteca Lifelines.
- Análise do sumário estatístico com métricas como coeficientes, hazard ratios e valores-p.

#### Análise de Métricas:

- Cálculo do Índice de Concordância (C-Index) para avaliar a precisão das predições.
- Comparação de modelos com variáveis significativas e completas.
- Avaliação de métricas como MSE, RMSE, MAE, MAPE, e R2.

#### Visualizações:
Geração de curvas de sobrevivência utilizando:
- Estimador Kaplan-Meier.
- Funções de sobrevivência ajustadas com o modelo de Cox.
- Comparação gráfica entre os tempos de sobrevivência reais e previstos.
- Gráficos de dispersão, histogramas e boxplots para análise de hazard ratios.

#### Predições e Comparações:
- Previsão da função de sobrevivência com predict_survival_function.
- Estimativa do tempo médio de sobrevivência com predict_expectation.
- Análise do impacto das variáveis significativas no tempo de sobrevivência.

#### Interpretação dos Hazard Ratios:
- Identificação de grupos de risco com base nos hazard ratios.
- Visualização da função de risco cumulativo usando o estimador Nelson-Aalen.

### [3. FOSP_curvas_Kaplan-Meier](https://colab.research.google.com/github/JoaoVitorSesma/Predicao-da-Sobrevida-em-Pacientes-com-Cancer-Colorretal-IC/blob/main/FOSP_curvas_Kaplan_Meier.ipynb)
Neste notebook, foram implementados processos para gerar curvas de sobrevivência Kaplan-Meier utilizando a base de dados da FOSP (Fundação Oncocentro de São Paulo). O objetivo foi analisar diferentes tipos de câncer com base nos códigos topográficos padronizados e realizar uma visualização da probabilidade de sobrevivência ao longo do tempo.

**Principais etapas do código:**

#### Importação e Preparação dos Dados:
- Utilização do banco de dados atualizado em dezembro de 2023, contendo informações detalhadas sobre diferentes tipos de câncer.
- Criação de uma tabela auxiliar que mapeia os tipos de câncer e seus respectivos códigos.
  
#### Funções de Seleção e Ajuste:
- **Seleção de dados:** Filtragem dos casos de acordo com critérios específicos, como topografia, estado de residência (SP), confirmação microscópica, morfologia específica, e diagnósticos realizados até 2019.
- **Ajustes para Kaplan-Meier:** Conversão das colunas de tempo de diagnóstico em meses, eliminação de casos inválidos e criação de variáveis binárias para eventos de óbito.

#### Geração e Visualização das Curvas Kaplan-Meier:
- Visualização por tipo de câncer, com indicadores como mediana de sobrevivência, número de amostras e período analisado.
- Salvamento das curvas em arquivos PNG e exibição conjunta em um painel de imagens para facilitar a análise comparativa.

## Bibliografias:

As principais bibliografias estão a baixo, além de outros diversos artigos que também foram referência para o estudo
1. [XU, L. et al. Comparison of the cox regression to machine learning in predicting the survival of anaplastic thyroid carcinoma. BMC Endocrine Disorders, v. 23, n. 1, 5 jun. 2023.](https://pmc.ncbi.nlm.nih.gov/articles/PMC10249166/)

2. [SHAYESTE ALINIA et al. Survival prediction and prognostic factors in colorectal cancer after curative surgery: insights from cox regression and neural networks. Scientific Reports, v. 13, n. 1, 21 set. 2023.](https://www.nature.com/articles/s41598-023-42926-0)

3. [Pesquisas_IC](https://github.com/JoaoVitorSesma/Predicao-da-Sobrevida-em-Pacientes-com-Cancer-Colorretal-IC/blob/main/PESQUISAS%20IC.pdf)

‌

‌


