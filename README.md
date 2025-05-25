# logistica-ml-pipeline
Pipeline de ML para prever status logístico com foco em arquitetura de dados. Simula ingestão, validação e treino de modelo Random Forest usando dados transformados. Inclui observabilidade técnica e geração de dashboards interativos para análise e rastreabilidade.

# 🚚 Dataflow Sentinel – Status Logístico por Machine Learning

Pipeline completo de Machine Learning focado em **arquitetura de dados**, simulando um fluxo produtivo de **previsão do status logístico** de entregas. Utiliza Random Forest como modelo preditivo, com observabilidade técnica e dashboards interativos.

---

## 📊 Objetivo

Prever o status final de entregas logísticas (`delivered`, `failed`, `in_transit`) com base em dados históricos enriquecidos e transformados. O projeto simula um ambiente real com foco em:

- Arquitetura de dados
- Engenharia de features
- Modelagem supervisionada
- Observabilidade técnica
- Visualização de qualidade dos dados

---

## 🔁 Pipeline de Execução

### 1. `04_modelo_consumo.ipynb`
> Pipeline de ingestão, seleção de variáveis, treino com Random Forest e avaliação de desempenho.

### 2. `05_observabilidade_pipeline.ipynb`
> Validações técnicas do dataset: rastreamento, colunas obrigatórias, integridade, proporção de nulos, tempo de execução.

### 3. `05B_qualidade_visual_dados.ipynb`
> Relatório visual com **heatmaps de nulos**, **distribuições** e **boxplots** por categoria de status.

### 4. `06_dashboard_streamlit_app.ipynb`
> Início da construção de um dashboard interativo com **Streamlit** (em ambiente local).

---

## 📁 Estrutura dos Arquivos

📦 dataflow-sentinel/
├── 04_modelo_consumo.ipynb
├── 05_observabilidade_pipeline.ipynb
├── 05B_qualidade_visual_dados.ipynb
├── 06_dashboard_streamlit_app.ipynb
├── dataflow_transformado.parquet
├── dataflow_modelo_status.pkl

---

## 🧠 Técnicas Utilizadas

- `Pandas`, `NumPy` – manipulação de dados
- `Scikit-learn` – Random Forest, avaliação, split
- `Joblib` – serialização de modelo
- `Seaborn`, `Matplotlib`, `Missingno` – visualizações
- `Logging` – rastreamento técnico por bloco
- `Streamlit` – protótipo de dashboard interativo

---

## 📈 Métricas do Modelo

Accuracy: 0.69
Precision: 0.58
Recall: 0.69
F1-score: 0.59

> O modelo obteve bons resultados para classe `delivered`, porém possui baixa performance para `in_transit`, evidenciando oportunidade de reengenharia de features.

---

## 🚀 Futuras Extensões (sugeridas)

- Servir modelo via API REST (FastAPI)
- Deploy contínuo com GitHub Actions
- Monitoramento de deriva com Evidently AI
- Agendamento em lote com Apache Airflow
- Data lineage com OpenLineage ou Marquez

---

## 📜 Licença

Distribuído sob a licença **MIT**.

---

## 👨‍💻 Autor

**Rodrigo de Souza**  


