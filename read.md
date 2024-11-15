Nome do Projeto
Descrição do Projeto
Este projeto explora a análise de sobrevivência com foco em dados de saúde. Utilizando técnicas de regressão de Cox e curvas de Kaplan-Meier, o objetivo é prever e interpretar tempos de sobrevida em pacientes, proporcionando insights sobre fatores de risco e probabilidade de sobrevivência ao longo do tempo.

Estrutura do Projeto
O projeto é composto por dois notebooks principais:

1. Notebook de Análise e Ajuste do Modelo de Sobrevivência
Este notebook aborda o ajuste de um modelo de sobrevivência de Cox Proportional Hazards, com os seguintes tópicos:

Importação e Pré-Processamento dos Dados: Preparação dos dados, incluindo limpeza e codificação de variáveis categóricas.
Ajuste do Modelo: Configuração e ajuste do modelo de Cox, seguido pela seleção de variáveis significativas com base nos p-values.
Métricas de Avaliação: Cálculo de métricas de desempenho, como C-Index, MSE, RMSE, MAE, MAPE e R² para avaliar a precisão do modelo.
Predição de Sobrevida: Estimativa dos tempos de sobrevida esperados, com comparações entre o modelo original e o modelo ajustado com variáveis significativas.
Visualização com Gráficos:
Comparação entre valores reais e previsões.
Distribuição dos resíduos (diferença entre tempos reais e previstos).
Curva de Sobrevivência Kaplan-Meier, representando a probabilidade de sobrevivência ao longo do tempo.
Histograma da distribuição dos tempos de sobrevivência ao longo dos 60 meses.
Esses gráficos fornecem uma visão intuitiva e ajudam a validar os resultados do modelo, permitindo identificar possíveis melhorias ou ajustes.

2. Notebook de Implementação de Previsão para Novos Pacientes
Este notebook se concentra na aplicação prática do modelo para prever a sobrevida de novos pacientes com dados inéditos:

Carregamento e Processamento dos Dados de Novos Pacientes: Preparação de um conjunto de dados de pacientes para previsão, aplicando o mesmo pré-processamento utilizado no ajuste do modelo.
Predição de Sobrevida: Utilização do modelo ajustado para estimar a sobrevida esperada dos novos pacientes e calcular a probabilidade de sobrevivência em intervalos específicos.
Comparação de Pacientes Específicos: Análise detalhada de pacientes específicos para identificar características associadas a tempos de sobrevivência mais longos ou mais curtos.
Avaliação do Desempenho: Verificação da acurácia das previsões do modelo usando métricas de desempenho e comparação com os dados de treinamento para verificar consistência.
Dependências
Este projeto depende de várias bibliotecas de Python, incluindo:

scikit-survival: Para modelagem de sobrevivência com CoxPHSurvivalAnalysis.
lifelines: Para análise de sobrevivência, incluindo CoxPHFitter e curvas de Kaplan-Meier.
sklearn: Para pré-processamento de dados e cálculo de métricas.
seaborn e matplotlib: Para visualizações de dados.
Instale todas as dependências com:

bash
Copiar código
pip install -r requirements.txt
Como Usar
Clone este repositório:
bash
Copiar código
git clone https://github.com/seu_usuario/seu_repositorio.git
Navegue até a pasta do projeto:
bash
Copiar código
cd seu_repositorio
Abra os notebooks e execute as células para reproduzir as análises e previsões.
Estrutura dos Arquivos
README.md: Descrição geral do projeto.
requirements.txt: Lista de dependências.
notebook_analise_sobrevivencia.ipynb: Notebook com análise e ajuste do modelo de sobrevivência.
notebook_previsao_novos_pacientes.ipynb: Notebook com previsões para novos pacientes.
data/: Diretório contendo os conjuntos de dados.
Resultados e Discussão
Os resultados deste projeto demonstram a aplicabilidade do modelo de Cox para prever o tempo de sobrevivência, com uma avaliação clara de variáveis significativas. As previsões de sobrevida e a análise de variáveis podem ser aplicadas para estudos de risco e decisões clínicas.

