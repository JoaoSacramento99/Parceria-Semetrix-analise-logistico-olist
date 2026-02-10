# 📊 EDA — Análise de Desempenho Logístico de Entregas (Parceria Semantix)

## 🚀 Sobre o Projeto

Este repositório contém a implementação de uma **Análise Exploratória de Dados (EDA)** aplicada ao desempenho logístico de entregas em um grande e-commerce brasileiro, com foco em atrasos, diferenças regionais e métricas de eficiência.

O projeto foi desenvolvido como parte da disciplina de análise de dados, com apoio e **parceria da Semantix**, e tem como objetivo demonstrar o uso prático de dados para entender e solucionar um problema real de negócio: **atrasos na entrega de pedidos e suas causas regionais**.

---

## 📌 Problemática

Atrasos na entrega de pedidos são um dos maiores desafios operacionais para empresas de e-commerce. Eles impactam diretamente a experiência dos clientes, aumentam custos logísticos e podem comprometer a competitividade da empresa.

Neste projeto, buscamos responder perguntas como:
- Onde estão concentrados os atrasos no Brasil?
- Quais regiões apresentam maior percentual de atraso?
- Qual é o impacto de atrasos quando considerado o volume de entregas?
- Como as variáveis se correlacionam entre si?

---

## 📁 Estrutura do Repositório

O repositório está organizado da seguinte forma:

projeto-olist-logistica/
│
├── data/
│ ├── raw/ # Dados brutos obtidos do Kaggle
│ │ ├── olist_orders_dataset.csv
│ │ └── olist_customers_dataset.csv
│ │
│ └── processed/ # Dados preparados com PySpark
│ ├── pedidos_clientes_tratado.csv
│ └── agg_regiao_entrega.csv
│
├── notebooks/
│ ├── 01_etl_spark.ipynb # Tratamento e preparação de dados
│ └── 02_eda_pandas.ipynb # Análise exploratória e correlações
│
├── dashboard/
│ └── looker_studio_link.txt
│
└── README.md


---

## 📊 Fonte dos Dados

Os dados utilizados foram obtidos a partir do dataset público:

**Brazilian E-Commerce Public Dataset by Olist** — disponível no Kaggle:  
https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

Esse dataset contém dados reais anonimizados de um e-commerce incluindo informações sobre clientes, pedidos, entregas e localização geográfica.

---

## 🛠️ Tecnologias Utilizadas

| Ferramenta            | Propósito                          |
|----------------------|------------------------------------|
| 🐍 Python            | Linguagem principal                |
| ⚡ PySpark           | Tratamento e preparação dos dados  |
| 📊 Pandas           | Análise exploratória e estatística |
| 📈 Seaborn/Matplotlib | Visualizações gráficos             |
| 📋 Looker Studio     | Dashboard interativo               |

---

## 📌 Detalhes das Etapas

### 1️⃣ Tratamento de Dados (PySpark)
Nesta etapa, os dados brutos do Kaggle foram lidos, integrados e transformados para gerar dois datasets finais:

- **pedidos_clientes_tratado.csv** — dados por pedido com métricas de atraso
- **agg_regiao_entrega.csv** — dados agregados por região

Foram realizadas:
- padronização de datas
- junção entre pedidos e clientes
- criação de métricas de tempo (total_days, days_delay)
- classificação de status de entrega
- agregação por região

### 2️⃣ Análise Exploratória (EDA com Pandas)
Utilizando os dados tratados:
- foram geradas análises descritivas
- exploradas distribuições e padrões
- calculadas correlações entre métricas
- produzidas visualizações de apoio

### 3️⃣ Dashboard (Looker Studio)
Com os dados resultantes, foi criado um dashboard no Looker Studio para:
- comparar regiões
- visualizar KPIs de desempenho
- evidenciar insights relevantes

---

## 😄 Agradecimentos

Este projeto foi desenvolvido com o apoio da **Semantix**, reforçando a importância da análise de dados aplicada a problemas reais de negócios.

---

## 📜 Licença

Este projeto está sob a licença **MIT License** — consulte o arquivo `LICENSE` para mais detalhes.

---

## 👤 Autor

**João Victor Sacramento**  
Analista em formação — foco em análise de dados, engenharia de dados e storytelling de dados.

