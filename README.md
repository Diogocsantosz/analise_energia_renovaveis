# GRUPO: Lucas Furquim (RM: 568690) ; Diogo Chiaradia (RM: 570246) ; Gustavo Torres de Oliveira (RM: 572952)

# Análise Preditiva de Energias Renováveis e Meteorologia (ANEEL & Open-Meteo)

Repositório desenvolvido para fins acadêmicos e aplicados com foco em Ciência de Dados e Machine Learning. O projeto realiza a extração, tratamento e modelagem preditiva utilizando dados abertos do setor elétrico brasileiro (ANEEL) combinados com dados meteorológicos horários da API Open-Meteo.

---

## Sobre o Projeto

O projeto divide-se em duas grandes frentes de Machine Learning aplicadas ao setor de energias renováveis:

1. **Tarefa de Classificação (ANEEL):**

   * Coleta de dados abertos de empreendimentos de geração de energia (SIGA/ANEEL) via API.
   * Tratamento de coordenadas geográficas, limpeza de valores numéricos e padronização.
   * Categorização das usinas em três classes principais de fontes renováveis: **Solar**, **Eólica** e **Hidráulica**.
   * Treinamento e avaliação de modelos de classificação para prever o tipo de fonte de energia com base em atributos estruturais e geográficos.

2. **Tarefa de Regressão (Open-Meteo):**

   * Coleta de dados meteorológicos históricos e horários para o município de **Petrolina (PE)**.
   * Engenharia de variáveis para estruturação do dataset.
   * Treinamento e avaliação de modelos de regressão com o objetivo de estimar/prever a **radiação solar** com base em variáveis climáticas.

---

## Tecnologias e Bibliotecas Utilizadas

O pipeline foi inteiramente programado em **Python**, utilizando o ambiente do Google Colab e as seguintes bibliotecas:

* **Manipulação e Análise de Dados:** `pandas`, `numpy`
* **Requisições de APIs:** `requests` (com tratamento de repetição/`retry`)
* **Visualização de Dados:** `matplotlib`, `seaborn`
* **Machine Learning:** `scikit-learn` (pré-processamento, métricas de avaliação, modelos de classificação e regressão)

---

## Comparação entre os Gráficos

A análise dos gráficos permite observar diferentes aspectos relacionados às fontes de energia renovável presentes nos dados da ANEEL.

Enquanto um dos gráficos apresenta a **quantidade de empreendimentos** por fonte de energia, o outro apresenta a **potência outorgada**, permitindo comparar a quantidade de usinas com a capacidade de geração associada a cada fonte.

Essa comparação é importante porque uma fonte pode apresentar uma quantidade maior de empreendimentos, mas isso não significa necessariamente que ela possua a maior capacidade de geração. Da mesma forma, uma fonte com menos empreendimentos pode apresentar uma potência outorgada elevada devido à existência de usinas de maior porte.

Dessa forma, os dois gráficos devem ser analisados em conjunto. O primeiro permite visualizar a **distribuição dos empreendimentos entre as fontes Solar, Eólica e Hidráulica**, enquanto o segundo demonstra como a **potência de geração está distribuída entre essas fontes**.

A comparação entre quantidade de empreendimentos e potência outorgada proporciona uma visão mais completa dos dados, permitindo identificar diferenças entre a presença numérica das fontes renováveis e sua participação em termos de capacidade de geração.

---

## Estrutura do Repositório

```text
├── aneel_classificacao_orange.csv  # Dataset tratado gerado na etapa de classificação
├── notebook_projeto.ipynb          # Notebook principal contendo todo o código executável
└── README.md                       # Documentação do projeto
```
