#  ETL Pipeline Using AWS RDS

---

##  Overview  
A scalable **ETL pipeline** that extracts data from sources, transforms it as needed, and loads it into an **AWS RDS** database for storage and downstream analytics.

---

##  Features  
-  Data extraction from sources like CSV, JSON, or API  
-  Data cleaning and transformation logic in Python (e.g., filtering, casting)  
-  Loading transformed data into AWS RDS (MySQL / PostgreSQL)  
-  Logging and error handling for robust and traceable execution  

---

##  Tools & Technologies  
- **Python 3.x**  
- **Libraries**: `pandas`, `sqlalchemy`, database connector (e.g., `psycopg2` or `PyMySQL`)  
- **AWS RDS** (MySQL or PostgreSQL) — managed relational database  
- (Optional) **AWS S3**, **Airflow or cron** for orchestration  

---

##  Project Structure  
```
ETL-using-AWS-RDS/
├── data/                     # Sample datasets (CSV, JSON)
├── scripts/
│   ├── extract.py            # Data ingestion logic
│   ├── transform.py          # Cleaning and transformation code
│   └── load.py               # Database insertion logic via SQLAlchemy
├── main_etl.py               # Orchestrator running full ETL workflow
├── README.md                 # Documentation (this file)
└── requirements.txt          # Project dependencies
```

---

##  How to Run  
1. **Clone the repo**  
   ```bash
   git clone https://github.com/ranavikas1998/ETL-using-AWS-RDS.git
   cd ETL-using-AWS-RDS
   ```  

2. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```  

3. **Configure your RDS credentials**  
   Add your connection details in `load.py` or set environment variables:
   ```env
   DB_HOST=
   DB_PORT=
   DB_NAME=
   DB_USER=
   DB_PASSWORD=
   ```

4. **Run the ETL pipeline**  
   ```bash
   python main_etl.py
   ```  
   Check logs for successful data ingestion into your RDS instance.

---

##  Customization Tips  
- Add support for **S3 source data** or API ingest logic.  
- Use **AWS IAM** for secure credential handling.  
- Integrate **AWS Lambda** or **EventBridge** for automated runs.  
- Add **unit tests**, CI/CD workflows, or error alerting (e.g., via SNS).

---

##  Author  
**Vikas Rana**  
- GitHub: [ranavikas1998](https://github.com/ranavikas1998)  
- Expertise: Python | AWS | RDS | Data Engineering | BI

---

##  Contribution  
Improvements are welcome!  
- Fork this repo  
- Add enhancements (e.g., orchestration, parallel loading)  
- Submit a Pull Request  – let’s collaborate!


