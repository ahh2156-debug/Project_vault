# Uber NYC Taxi Data Engineering & Analytics Project

![Python](https://img.shields.io/badge/Python-3.11-blue)
![BigQuery](https://img.shields.io/badge/Google%20BigQuery-Data%20Warehouse-orange)
![Spark SQL](https://img.shields.io/badge/Spark%20SQL-Analytics-red)
![Looker Studio](https://img.shields.io/badge/Looker%20Studio-Dashboards-green)

---

## 📌 Overview  
This project builds an **end-to-end data engineering pipeline** to process, clean, and analyze over **10 million NYC taxi trip records**. Using **Mage AI** as the orchestration tool, data is transformed and loaded into **Google BigQuery** for large-scale analytics. The processed data powers **Looker Studio dashboards** that visualize trip patterns, ride durations, peak hours, and revenue trends.

**Data Source:** [NYC Taxi & Limousine Commission Trip Records](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)  

---

## ⚙️ Tech Stack  
- **Languages:** Python (Pandas), SQL  
- **Tools:** Mage AI, Google BigQuery, Looker Studio  
- **Frameworks:** Spark SQL  
- **Other:** ETL best practices, chunked uploads for large datasets  

---

## 🗂 Data Model  
![Uber Data Model](docs/uber_data_model.png)  

---

## 📂 Project Structure  
```plaintext
etl/
 ├── extract.py            # Data extraction script
 ├── transform.py          # Data cleaning & transformation logic
 └── load.py               # BigQuery upload logic

sql/
 ├── fact_table.sql        # Fact table schema
 ├── date_dim.sql          # Date dimension table schema
 └── analytics_queries.sql

docs/
 ├── pipeline_diagram.png
 └── dashboard_screenshots/

README.md
```
🔄 Pipeline Workflow
Extract: Load raw NYC taxi trip data from CSV.

Transform: Clean and format datetime fields, calculate ride durations, and handle missing values.

Load: Upload cleaned datasets to Google BigQuery using chunked uploads to prevent memory issues.

Analytics: Create fact and dimension tables for scalable querying.

Visualization: Build Looker Studio dashboards to display KPIs and trends.


📈 Results & Insights
Peak demand identified on Fridays 6–8 PM, with ~20% higher trip volumes.

Average trip fare: $13.50, with longer trips concentrated in outer boroughs.

Seasonal trends show a ~15% drop in ridership during January.

📊 Dashboard Preview
View Dashboard

🚀 How to Run
Clone the repo:

bash
Copy
Edit
git clone https://github.com/your-username/uber-nyc-data-engineering.git
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Set up Google Cloud credentials for BigQuery.

Run ETL:

bash
Copy
Edit
python etl/extract.py
python etl/transform.py
python etl/load.py
🛠 Skills Demonstrated
Data Engineering

ETL Development

BigQuery Optimization

Spark SQL Processing

Data Visualization

yaml
Copy
Edit

