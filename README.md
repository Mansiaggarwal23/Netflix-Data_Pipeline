# 🎬 Netflix Data Pipeline

A complete end-to-end data pipeline project that simulates Netflix-style movie analytics using the [MovieLens 20M Dataset](https://grouplens.org/datasets/movielens/20m/). This project demonstrates the ingestion, transformation, and analysis of movie rating data with a modern data engineering stack.

---

## 📦 Dataset

We use the **MovieLens 20M** dataset, which contains 20 million ratings and tag applications applied to 27,000 movies by 138,000 users. This dataset is publicly available at:

🔗 [https://grouplens.org/datasets/movielens/20m/](https://grouplens.org/datasets/movielens/20m/)

---

## 🚀 Project Overview

This project mimics a simplified Netflix data pipeline to:
- Ingest raw CSV data
- Clean and transform data using **DBT**
- Load transformed data into a warehouse
- Perform basic movie analytics

---

## 🔧 Tech Stack

- **DBT (Data Build Tool)** – for data transformations and modeling  
- **Python + Virtualenv** – for scripting and environment isolation  
- **Git + GitHub** – version control and collaboration  
- **MovieLens Dataset** – source of movie ratings and metadata  
- **Snowflake Database** – for loading the data

## 🧪 Setup Instructions

1. **Clone the repository**

   ```bash
   git clone https://github.com/Mansiaggarwal23/Netflix-Data_Pipeline.git
   cd Netflix-Data_Pipeline
   ```

2. **Create and activate a virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Set up DBT profile**

   Configure your DBT profile in the `~/.dbt/profiles.yml` file with your database connection settings. Example for a PostgreSQL setup:

   ```yaml
   netflix_pipeline:
     target: dev
     outputs:
       dev:
         type: snowflake
         host: localhost
         user: your_username
         password: your_password
         port: 5432
         dbname: your_database
         schema: dbt_yourname
   ```

5. **Run the DBT pipeline**

   ```bash
   dbt run
   ```

---

## 📜 License

This project is intended for **educational and demonstration purposes only**.


