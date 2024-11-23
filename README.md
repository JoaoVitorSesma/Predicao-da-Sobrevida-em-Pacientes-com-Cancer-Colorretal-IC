# **Predição de Sobrevida em Pacientes com Câncer Colorretal com Dados da FOSP**

## Descrição do Projeto:
  
Este projeto explora a análise de sobrevivência com foco em dados de saúde. Utilizando técnicas de regressão de Cox e curvas de Kaplan-Meier, o objetivo é prever tempos de sobrevida em pacientes, proporcionando insights sobre fatores de risco e probabilidade de sobrevivência ao longo do tempo.

## Estrutura do Projeto
O projeto é composto por dois notebooks principais e um outro notebook de curvas de sobrevivência:

### [1. Predição da Sobrevida em Pacientes com Câncer Colorretal - COX](https://colab.research.google.com/github/JoaoVitorSesma/Predicao-da-Sobrevida-em-Pacientes-com-Cancer-Colorretal-IC/blob/main/Predi%C3%A7%C3%A3o_da_Sobrevida_em_Pacientes_com_C%C3%A2ncer_Colorretal_COX.ipynb)
Este notebook realiza a aplicação do modelo de COX diretamente no Banco de Dados da FOSP, para poder fazer a predição sobrevivência. Sendo assim, o código foi estruturado da seguinte maneira:

#### Importação e Pré-Processamento dos Dados: Preparação dos dados, incluindo limpeza e codificação de variáveis categóricas.

### Ajuste do Modelo: Configuração e ajuste do modelo de Cox, seguido pela seleção de variáveis significativas com base nos p-values.

#### Métricas de Avaliação: Cálculo de métricas de desempenho, como C-Index, MSE, RMSE, MAE, MAPE e R² para avaliar a precisão do modelo.

#### Predição de Sobrevida: Estimativa dos tempos de sobrevida esperados, com comparações entre o modelo original e o modelo ajustado com variáveis significativas.

#### Visualização com Gráficos:
- Comparação entre valores reais e previsões.
- Distribuição dos resíduos (diferença entre tempos reais e previstos).
- Curva de Sobrevivência Kaplan-Meier, representando a probabilidade de sobrevivência ao longo do tempo.
- Histograma da distribuição dos tempos de sobrevivência ao longo dos 60 meses.
Esses gráficos fornecem uma visão intuitiva e ajudam a validar os resultados do modelo, permitindo identificar possíveis melhorias ou ajustes.

### [2. Banco de Dados (Lifelines)](https://colab.research.google.com/github/JoaoVitorSesma/Predicao-da-Sobrevida-em-Pacientes-com-Cancer-Colorretal-IC/blob/main/Banco_de_Dados_(Lifelines).ipynb)
Nesse outro notebook foi feita a implementação do modelo de COX que serviu como um modelo experimental, antes de ser feita a análise definitiva para o Banco de Dados da FOSP. Sendo um notebook instrutivo de como o modelo foi aplicado, além de outros diversos ensinamentos.

### [3. FOSP_curvas_Kaplan-Meier](https://colab.research.google.com/github/JoaoVitorSesma/Predicao-da-Sobrevida-em-Pacientes-com-Cancer-Colorretal-IC/blob/main/FOSP_curvas_Kaplan_Meier.ipynb)
Neste notebook, foram implementados processos para gerar curvas de sobrevivência Kaplan-Meier utilizando a base de dados da FOSP (Fundação Oncocentro de São Paulo). O objetivo foi analisar diferentes tipos de câncer com base nos códigos topográficos padronizados e realizar uma visualização da probabilidade de sobrevivência ao longo do tempo.

**Principais etapas do código:**

#### Importação e Preparação dos Dados:
- Utilização do banco de dados atualizado em dezembro de 2023, contendo informações detalhadas sobre diferentes tipos de câncer.
- Criação de uma tabela auxiliar que mapeia os tipos de câncer e seus respectivos códigos.
  
#### Funções de Seleção e Ajuste:
- **Seleção de dados:** Filtragem dos casos de acordo com critérios específicos, como topografia, estado de residência (SP), confirmação microscópica, morfologia específica, e diagnósticos realizados até 2019.
- **Ajustes para Kaplan-Meier:** Conversão das colunas de tempo de diagnóstico em meses, eliminação de casos inválidos e criação de variáveis binárias para eventos de óbito.

#### Geração das Curvas Kaplan-Meier:
Visualização por tipo de câncer, com indicadores como mediana de sobrevivência, número de amostras e período analisado.

#### Visualização das Curvas:
Salvamento das curvas em arquivos PNG e exibição conjunta em um painel de imagens para facilitar a análise comparativa.

## Artigos de Referência:
1. XU, L. et al. Comparison of the cox regression to machine learning in predicting the survival of anaplastic thyroid carcinoma. BMC Endocrine Disorders, v. 23, n. 1, 5 jun. 2023.

2. SHAYESTE ALINIA et al. Survival prediction and prognostic factors in colorectal cancer after curative surgery: insights from cox regression and neural networks. Scientific Reports, v. 13, n. 1, 21 set. 2023.

‌

‌


