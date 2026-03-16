# House Sale Data ETL Pipeline

## Overview

In this assignment you will build an ETL (Extract, Transform, Load) pipeline using **PySpark** that processes a house sales dataset and loads it into PostgreSQL, with each neighborhood stored in its own table.

---

## Repository Structure

```
house-sale-etl/
├── dataset/
│   └── historical_purchases.csv     # input data (do not modify)
├── src/
│   └── etl_pipeline.py              # your implementation goes here
├── tests/
│   ├── compare_csvs.py              # automated CSV comparison (do not modify)
│   └── expected/                    # reference output (do not modify)
├── .env.example                     # environment variable template
└── .gitignore
```

---

## Dataset

`dataset/historical_purchases.csv` contains house sale records across multiple neighborhoods. It includes all features describing each property and its sale.

---

## Setup

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Configure environment variables

Copy `.env.example` to `.env` and fill in your PostgreSQL credentials:

```bash
cp .env.example .env
```

---

## Your Task

Open `src/etl_pipeline.py` and implement the three functions:

- **`extract`** – load the CSV into a PySpark DataFrame
- **`transform`** – split the data by neighborhood and save each as a separate CSV file
- **`load`** – insert each neighborhood's data into its own PostgreSQL table

---

## Grading

| Component | Description |
|---|---|
| **Commit history** | Changes must be committed and pushed to GitHub Classroom on time. If you used an AI assistant, it must be listed as a co-author in your commit message. |
| **Implementation** | All three functions are correctly implemented. |
| **CI tests** | Both the lint check and CSV output check must pass on GitHub Actions. |
| **Live demo** | Demo the pipeline running on your local machine. The PostgreSQL tables must be populated and visible during the demo. |

### AI Policy

You are allowed to use AI tools. If you do, the AI must be listed as a co-author in every commit it contributed to:

```
git commit -m "Your message

Co-Authored-By: AI Tool Name <email>"
```
