<p><img width=100% src= "https://i.ibb.co/71LfsKD/capa-projeto-deteccao-doenca-cardiaca.png"  alt="logo"></p>
<p align="center">
    <!-- Python -->
    <img alt="python" src="https://img.shields.io/badge/python-FFFFFF?style=flat&labelColor=E30B21&color=FFFFFF&logo=python&logoColor=FFFFFF">
    <!-- Pandas -->
    <img alt="pandas" src="https://img.shields.io/badge/pandas-FFFFFF?style=flat&labelColor=E30B21&color=FFFFFF&logo=pandas&logoColor=FFFFFF">
    <!-- Seaborn -->
    <img alt="seaborn" src="https://img.shields.io/badge/seaborn-FFFFFF?style=flat&labelColor=E30B21&color=FFFFFF&logo=seaborn&logoColor=FFFFFF">
    <!-- Scikit-learn -->
    <img alt="scikit-learn" src="https://img.shields.io/badge/sklearn-FFFFFF?style=flat&labelColor=E30B21&color=FFFFFF&logo=scikitlearn&logoColor=FFFFFF">
    <!-- XGBoost -->
    <img alt="xgboost" src="https://img.shields.io/badge/xgboost-FFFFFF?style=flat&labelColor=E30B21&color=FFFFFF&logo=xgboost&logoColor=FFFFFF">
    <!-- Status -->
    <img alt="status" src="https://img.shields.io/badge/Status-Em_desenvolvimento-FFFFFF?style=flat&logoColor=1ED760&labelColor=000000">
</p>

# Projeto: Detecção de Doenças cardíacas

# Índice 

* [Descrição do Projeto](#descrição-do-projeto)
* [Funcionalidade e Demonstração](#funcionalidade-e-demonstração)
* [Tecnologias utilizadas](#tecnologias-utilizadas)
* [Licença](#licença)

# Descrição do projeto
Um grupo de pesquisa na área médica deseja criar um modelo de Machine Learning que consiga classificar se pacientes têm ou não doença cardíaca, com base em alguns dados demográficos e também resultados de exames médicos que essas pessoas fizeram.

O objetivo deste projeto é desenvolver um modelo de classificação, aprimorando o desempenho com XGBoost.

Os dados foram obtidos no [Kaggle](https://www.kaggle.com/datasets/rishidamarla/heart-disease-prediction/data), tendo como sua fonte primária [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/45/heart+disease). Esses dados foram doados em 1988 e provêm dos resultados clínicos e de testes não invasivos realizados em pacientes submetidos a exames na Cleveland Clinic em Cleveland (Ohio), no Instituto Húngaro de Cardiologia em Budapeste, em um Centro Médico em Long Beach (Califórnia), e também em pacientes de Hospitais universitários em Zurique e Basel (Suíça).

# Funcionalidade e Demonstração

Para acessar e executar o projeto, seguir os seguintes passos:

1. Faça download do arquivo [modelo_pipeline.pkl](modelo_pipeline.pkl)

2. Importe biblioteca joblib para carregar o modelo salvo da seguinte forma junto com arquivo onde contém os dados dos pacientes para realizar a previsão:
```python
# Carregando o modelo
modelo = joblib.load('modelo_pipeline.pkl')

# Carregando os novos pacientes
novos_pacientes = pd.read_csv('Dados/pacientes_novos.csv')

# Fazendo previsões
pred = modelo.predict(novos_pacientes)
pred
```

As previsões realizadas podem ser agrupadas em um DataFrame para facilitar a visualização e análise dos resultados.

# Tecnologias utilizadas
- **Linguagem:** Python 3.11.5
- **Bibliotecas:** 
    - Pandas: 2.1.1
    - Seaborn: 0.12.2
    - Scikit-learn: 1.3.0
    - Xgboost: 2.0.3

# Licença
[MIT License](https://opensource.org/license/mit/)