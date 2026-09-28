GRUPO: Lucas Furquim (RM: 568690) ; Diogo Chiaradia (RM: 570246) ; Gustavo Torres de Oliveira (RM: 572952)

# Análise Preditiva de Energias Renováveis e Meteorologia (ANEEL & Open-Meteo)

Repositório desenvolvido para fins acadêmicos e aplicados com foco em Ciência de Dados e Machine Learning. O projeto realiza a extração, tratamento e modelagem preditiva utilizando dados abertos do setor elétrico brasileiro (ANEEL) combinados com dados meteorológicos horários da API Open-Meteo.

---

##  Sobre o Projeto

O projeto divide-se em duas grandes frentes de Machine Learning aplicadas ao setor de energias renováveis:

1. **Tarefa de Classificação (ANEEL)**: 
   * Coleta de dados abertos de empreendimentos de geração de energia (SIGA/ANEEL) via API.
   * Tratamento de coordenadas geográficas, limpeza de valores numéricos e padronização.
   * Categorização das usinas em três classes principais de fontes renováveis: **Solar**, **Eólica** e **Hidráulica**.
   * Treinamento e avaliação de modelos de classificação para prever o tipo de fonte de energia com base em atributos estruturais e geográficos.

2. **Tarefa de Regressão (Open-Meteo)**:
   * Coleta de dados meteorológicos históricos e horários para o município de **Petrolina (PE)**.
   * Engenharia de variáveis para estruturação do dataset.
   * Treinamento e avaliação de modelos de regressão com o objetivo de estimar/prever a **radiação solar** com base em variáveis climáticas.

---

##  Tecnologias e Bibliotecas Utilizadas

O pipeline foi inteiramente programado em **Python**, utilizando o ambiente do Google Colab e as seguintes bibliotecas:
* **Manipulação e Análise de Dados**: `pandas`, `numpy`
* **Requisições de APIs**: `requests` (com tratamento de repetição/`retry`)
* **Visualização de Dados**: `matplotlib`, `seaborn`
* **Machine Learning**: `scikit-learn` (pré-processamento, métricas de avaliação, modelos de classificação e regressão)

---

##  Estrutura do Repositório

```text
├── aneel_classificacao_orange.csv  # Dataset tratado gerado na etapa de classificação
├── notebook_projeto.ipynb          # Notebook principal contendo todo o código executável
└── README.md                       # Documentação do projeto
