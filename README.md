# 🌍 Digital Wellbeing Analytics using Databricks Lakehouse

![Databricks](https://img.shields.io/badge/Platform-Databricks-red?logo=databricks)
![PySpark](https://img.shields.io/badge/PySpark-3.x-orange?logo=apachespark)
![Delta Lake](https://img.shields.io/badge/Delta-Lake-blue)
![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![GitHub](https://img.shields.io/badge/Git-Version_Control-black?logo=github)

## 📖 Project Overview

This project demonstrates an **end-to-end Data Engineering pipeline** built entirely within the **Databricks Lakehouse Platform** using the **Medallion Architecture (Bronze → Silver → Gold)**.

The pipeline ingests a global **Digital Wellbeing & Mental Health** dataset, performs data cleansing and feature engineering using **PySpark**, creates business-ready analytical tables, orchestrates the workflow using **Databricks Workflows**, and visualizes insights through **Databricks Dashboards**.

---

## 🏗️ Architecture

<p align="center">
<img src="screenshots/Architecture.png" width="850">
</p>

### Pipeline Flow

```
Dataset (CSV)
        │
        ▼
Bronze Layer
(Raw Data Ingestion)
        │
        ▼
Silver Layer
(Data Cleaning & Feature Engineering)
        │
        ▼
Gold Layer
(Business Aggregations)
        │
        ▼
Databricks Dashboard
        │
        ▼
Databricks Workflow
```

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Databricks | Data Engineering Platform |
| PySpark | Data Processing |
| Delta Lake | Storage Format |
| Databricks Workflows | Pipeline Orchestration |
| Databricks SQL Dashboard | Visualization |
| GitHub | Version Control |

---

## Dashboard Preview

<p align="center">
<img src="screenshots/Dashboard1.png" width="900">
</p>

<p align="center">
<img src="screenshots/Dashboard2.png" width="900">
</p>

---

## ⚙️ Databricks Workflow

The ETL pipeline is orchestrated using **Databricks Workflows**.

Pipeline

```
Bronze Load
      │
      ▼
Silver Transformations
      │
      ▼
Gold Aggregations
```
WorkFlow Preview

<p align="center">
<img src="screenshots/Worflow.png" width="900">
</p>

---

### SuccessFull WorkFlow Preview

<p align="center">
<img src="screenshots/SuccessfullWorkflow.png" width="850">
</p>

<p align="center">
<img src="screenshots/SuccessfullWorkflow1.png" width="850">
</p>


---

### Workflow Failure Scenario

A validation failure was intentionally created to demonstrate production-style workflow monitoring.

#### Example

```text
NoteBook doesn't exists 
          │
          ▼
Validation Failure
          │
          ▼
Workflow Stops
          │
          ▼
Downstream Tasks Skipped
```
<p align="center">
<img src="screenshots/FailureWorkflow1.png" width="850">
</p>

<p align="center">
<img src="screenshots/FailureWorkflow2.png" width="850">
</p>


---

## How to Run

1. Upload the dataset into Databricks.
2. Create the Bronze table.
3. Execute the notebooks in order:

```
01_Bronze_Load

↓

02_Silver_Load

↓

03_Gold_Load
```

4. Run the Databricks Workflow.

---

### ⭐ If you found this project useful, consider giving it a star!
