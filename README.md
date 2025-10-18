# 🚗 Projeto 2 — Car Insurance Premium Prediction

Este repositório apresenta o desenvolvimento completo de um **pipeline de tratamento e preparação de dados** para predição de prêmios de seguros automotivos, utilizando o **Databricks Free Edition** como ambiente principal.  

O projeto segue uma arquitetura de camadas — **Bronze → Silver → Gold** — com foco em aplicar boas práticas de **engenharia e ciência de dados** para preparar os dados de forma robusta e escalável.

---

## 🧩 Estrutura do Repositório

```
projeto_car_insurance/
├── data/
│   ├── raw/                     # Dados originais (car_insurance_premium_dataset.csv, TEST.csv)
│   ├── bronze/                  # Dados padronizados e limpos
│   ├── silver/                  # Dados tratados e prontos para modelagem
│   └── gold/                    # (Futuro) Dados modelados e métricas
├── notebooks/
│   ├── script_bronze.ipynb      # Ingestão e padronização (camada Bronze)
│   ├── script_silver.ipynb      # Tratamento e EDA (camada Silver)
│   └── script_gold.ipynb        # (Planejado) Modelagem GLM
├── img/                         # Imagens e prints do Databricks
│   ├── databricks_workspace.png
│   └── pipeline.png
├── requirements.txt
├── LICENSE
└── README.md
```

---

## 🎯 Objetivo do Projeto

O objetivo principal é desenvolver um **pipeline de dados no Databricks** capaz de:
- Realizar **tratamentos de dados estruturados** em camadas (Bronze, Silver e Gold);
- Efetuar o **tratamento de outliers e missing values**;
- **Codificar variáveis categóricas** e padronizar os dados para modelagem;
- Gerar uma base final limpa e pronta para uso em **modelos GLM (Generalized Linear Models)**.

---

## ☁️ Ambiente de Desenvolvimento: Databricks

O pipeline foi implementado integralmente no **Databricks Free Community Edition**, explorando notebooks interativos com **PySpark e Pandas**, além de visualizações integradas para análise exploratória.

### 💻 Print do Ambiente
![Databricks Workspace](img/databricks_workspace.png)

### 🔄 Print do Pipeline
![Pipeline Camadas](img/pipeline.png)

---

## ⚙️ Tecnologias e Ferramentas Utilizadas

- **Databricks Free Edition** — execução dos notebooks e controle de versão  
- **PySpark / Spark SQL** — leitura e transformação de dados em escala  
- **Pandas / NumPy** — manipulação e análise estatística  
- **Matplotlib / Seaborn** — visualização e EDA  
- **Scikit-learn** — imputação e codificação  
- **Statsmodels** — modelagem GLM (planejada)  
- **GitHub** — versionamento e documentação  

---

## 🧱 Estrutura de Camadas

| Camada | Descrição | Arquivo |
|:-------|:-----------|:--------|
| **Bronze** | Ingestão e padronização dos dados brutos | `script_bronze.ipynb` |
| **Silver** | Tratamento, codificação e EDA | `script_silver.ipynb` |
| **Gold (planejada)** | Modelagem GLM e métricas de avaliação | `script_gold.ipynb` |

---

## 🧹 Etapas Principais do Pipeline

### 🔸 Bronze
- Leitura dos arquivos `.csv` no Databricks;  
- Aplicação de `lowercase` nos nomes das colunas;  
- Remoção de caracteres especiais e substituição de espaços por `_`;  
- Conversão e validação dos tipos de dados;  
- Salvamento da tabela no formato Delta (`/bronze`).

### 🔸 Silver
- **Tratamento de outliers** com IQR e Z-Score, substituindo por mediana;  
- **Imputação de missing values** com mediana;  
- **Codificação de variáveis categóricas** (Label e One-Hot Encoding);  
- **EDA com visualizações** e estatísticas descritivas;  
- Exportação da base tratada (`/silver`).

### 🔸 Gold (futuro)
- Construção do modelo GLM com `statsmodels`;  
- Avaliação de desempenho (R², RMSE, MAE);  
- Interpretação dos coeficientes e importância das variáveis.

---

## 📊 Principais Análises (EDA)
 
- Visualização de outliers com boxplots e histogramas.

---

## 🧠 Insights Iniciais


---

## 📂 Fonte dos Dados

Os dados utilizados são **sintéticos**, inspirados em políticas reais de precificação de seguros.  
Disponíveis publicamente em:  
🔗 [https://github.com/MathMachado/DSWP/tree/master/Projetos/Projeto2](https://github.com/MathMachado/DSWP/tree/master/Projetos/Projeto2)

---

## 👩‍💻 Autora

**Ana Beatriz Almeida**  
Engenheira de Dados Júnior | Estudante de Ciência e Tecnologia (UFABC)  
📍 Databricks | PySpark | SQL | Machine Learning  
🔗 [linkedin.com/in/anaupdating](https://linkedin.com/in/anaupdating)

---

## 🪪 Licença

Este projeto está licenciado sob os termos da **MIT License**.  
Consulte o arquivo `LICENSE` para mais informações.
