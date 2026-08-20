<div align="center">

![Hassan Salam — Data Engineer, DataOps, Cloud Engineer](https://capsule-render.vercel.app/api?type=waving&height=250&color=0:020617,45:0F766E,100:2DD4BF&text=Hassan%20Salam&fontColor=F8FAFC&fontSize=56&fontAlignY=37&desc=DATA%20ENGINEER%20%E2%80%A2%20DATAOPS%20%E2%80%A2%20CLOUD%20ENGINEER&descAlignY=58&descSize=17&animation=fadeIn)

### I build data systems that are designed to survive production.

From ingestion and transformation to infrastructure, delivery, and observability.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/hassansalamb)
[![Projects](https://img.shields.io/badge/GitHub-View_projects-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/HassanSalamB?tab=repositories)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit_site-0F766E?style=for-the-badge&logo=googlechrome&logoColor=white)](https://hassansalamb.github.io)

</div>

---

## Engineering data from source to service

I'm **Hassan**, a Data Engineer, DataOps practitioner, and Cloud Engineer based in Germany.

I work across the full operational life of data: collecting it, moving it, transforming it, modeling it, serving it, and keeping the platform healthy after deployment. My focus is not simply making a pipeline run once—it is making the system repeatable, observable, maintainable, and ready to evolve.

## Platform toolbox

<div align="center">

### Build and transform

[![Build and transform](https://skillicons.dev/icons?i=python,azure,postgres,mongodb,mysql,kafka&theme=dark)](https://skillicons.dev)

`Databricks` · `Apache Spark` · `Apache Airflow` · `dbt` · `Pandas` · `Parquet` · `Delta Lake` · `Snowflake` · `Neo4j` · `H3`

### Ship and operate

[![Ship and operate](https://skillicons.dev/icons?i=docker,kubernetes,terraform,aws,githubactions,linux,git&theme=dark)](https://skillicons.dev)

`Microsoft Azure` · `CI/CD` · `Infrastructure as Code` · `Prometheus` · `Grafana` · `Alertmanager` · `Docker Compose`

### Serve and communicate

[![Serve and communicate](https://skillicons.dev/icons?i=fastapi,flask&theme=dark)](https://skillicons.dev)

`REST APIs` · `Streamlit` · `Dash` · `Plotly` · `Technical documentation` · `Architecture diagrams`

</div>

```text
SOURCES          DATA PLANE                PLATFORM PLANE            CONSUMERS

APIs       ─┐    Kafka  ─┐                CI/CD       ─┐             FastAPI
Files       ├──▶ Airflow ├──▶ Spark/dbt ─▶ Terraform  ├──▶ Observe ─▶ Dashboards
Events      ┘    Python  ┘                Containers   ┘             Data products

                      PostgreSQL • Neo4j • Snowflake • Azure • Databricks
                      Prometheus • Grafana • Testing
```

## What I bring to a data platform

<table>
<tr>
<td width="33%" valign="top">

### ⚙️ Data Engineering

Batch and streaming ingestion, ETL/ELT, medallion architecture, data modeling, orchestration, analytics engineering, and API delivery.

</td>
<td width="33%" valign="top">

### 🔁 DataOps

Automated workflows, testable transformations, CI/CD, environment consistency, monitoring, alerting, and operational documentation.

</td>
<td width="33%" valign="top">

### ☁️ Cloud Engineering

Containerized services, infrastructure as code, cloud-ready architecture, deployment design, secure configuration, and scalable foundations.

</td>
</tr>
</table>

## Systems I've built

### 01 / 🗺️ [Tourism Big Data Recommender](https://github.com/HassanSalamB/tourism-big-data-recommender)

> A country-scale tourism platform that turns raw DATAtourisme points of interest into useful destination analytics and itinerary recommendations.

<p align="center">
  <a href="https://github.com/HassanSalamB/tourism-big-data-recommender">
    <img width="48%" src="https://raw.githubusercontent.com/HassanSalamB/tourism-big-data-recommender/dev/artifacts/screenshots/01-streamlit-dashboard.png" alt="Tourism recommendation dashboard" />
  </a>
  <a href="https://github.com/HassanSalamB/tourism-big-data-recommender">
    <img width="48%" src="https://raw.githubusercontent.com/HassanSalamB/tourism-big-data-recommender/dev/artifacts/screenshots/03-airflow-dag-grid.png" alt="Airflow pipeline orchestration" />
  </a>
</p>

| Challenge | System design | Output |
|---|---|---|
| Process a large national POI feed without rebuilding everything on every run. | Content-hash change detection, bronze/silver/gold layers, Airflow orchestration, Spark features, dbt marts, and graph relationships. | Searchable destination data, itinerary recommendations, analytics dashboards, REST endpoints, and observable pipeline operations. |

```text
DATAtourisme → Airflow → Bronze JSONB → Silver/Parquet → Spark + dbt
             → PostgreSQL + Neo4j → FastAPI + Streamlit → Kafka + Observability
```

`Airflow` `Kafka` `Spark` `dbt` `PostgreSQL` `Neo4j` `FastAPI` `Streamlit` `Prometheus` `Grafana` `Terraform`

[![Explore the architecture](https://img.shields.io/badge/Explore_the_architecture-0F766E?style=for-the-badge&logo=github&logoColor=white)](https://github.com/HassanSalamB/tourism-big-data-recommender)

---

### 02 / ✈️ [Flight Delay Analytics Platform](https://github.com/HassanSalamB/dst-airlines)

> A multi-database analytics system built around 560,000+ US domestic flights, live weather enrichment, route intelligence, and delay prediction.

| Scale | Data architecture | Product surface | Operational model |
|---|---|---|---|
| **560K+ flights** across 2018–2024 | PostgreSQL medallion layers, MongoDB live workloads, Neo4j route graph | 11 FastAPI endpoints and a seven-page Dash application | Seven containerized services launched through Docker Compose |

```text
Flights + Weather
       ↓
Collect & validate ──▶ PostgreSQL / MongoDB / Neo4j
       ↓                         ↓
Feature engineering       Graph route analysis
       └──────────▶ FastAPI + Dash ◀──────────┘
                         ↓
              Delay insights & prediction
```

**What the platform delivers**

- Interactive airport and delay exploration across real historical flight data
- Live Open-Meteo context for weather-aware analysis
- Shortest-path queries over a 346-airport Neo4j graph
- Delay classification and regression workflows
- A single-command, reproducible local deployment

`Python` `PostgreSQL` `MongoDB` `Neo4j` `FastAPI` `Dash` `Docker` `scikit-learn` `Open-Meteo`

[![Explore the platform](https://img.shields.io/badge/Explore_the_platform-0F766E?style=for-the-badge&logo=github&logoColor=white)](https://github.com/HassanSalamB/dst-airlines)

## My engineering standard

| Principle | What it means in practice |
|---|---|
| **Automate repetition** | Pipelines, tests, builds, and deployments should be reproducible—not dependent on memory. |
| **Observe the system** | Metrics, logs, alerts, and clear failure boundaries are part of the architecture. |
| **Design for change** | Configuration belongs outside code; services and data layers should evolve independently. |
| **Protect data quality** | Validation and lineage matter from ingestion through every downstream consumer. |
| **Document decisions** | A platform is easier to operate when its tradeoffs and runbooks are visible. |

## Activity

<div align="center">

<img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=HassanSalamB&theme=github_dark" alt="Hassan Salam's GitHub activity" />

![Profile views](https://komarev.com/ghpvc/?username=HassanSalamB&label=Profile%20views&color=0F766E&style=flat-square)

</div>

---

<div align="center">

### Have a data-platform problem worth discussing?

[![Start a conversation](https://img.shields.io/badge/Start_a_conversation-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/hassansalamb)
[![Explore the work](https://img.shields.io/badge/Explore_the_work-GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/HassanSalamB?tab=repositories)

![Footer](https://capsule-render.vercel.app/api?type=waving&height=120&section=footer&color=0:020617,45:0F766E,100:2DD4BF)

</div>
