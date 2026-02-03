# 🚀 Amazon Sales Data Pipeline & Automation

This project demonstrates an end-to-end data engineering pipeline using **AWS** and **Databricks**. It covers cloud data ingestion, processing via Medallion Architecture, and event-driven monitoring using serverless components.

## 🛠 Tech Stack

* **Cloud:** AWS (S3, SNS, Lambda, IAM)
* **Data Processing:** Databricks (Spark SQL, Unity Catalog)
* **Infrastructure & Scripting:** AWS CLI & PowerShell
* **Documentation:** Markdown

---

## 📁 Project Structure

| File | Description |
| --- | --- |
| `Report.md` | Detailed step-by-step documentation of Part 1 & Part 2 with screenshots. |
| `cli-csv-upload.md` | AWS CLI commands and PowerShell logs for S3 bucket management and data upload. |
| `Databricks-SQL.ipynb` | Spark SQL queries performed on Databricks for data transformation and analysis. |

---

## 🏗 Pipeline Architecture

1. **Data Ingestion:** Raw datasets were ingested into the S3 "Landing" zone using the **AWS CLI**.
2. **Data Processing (Medallion Architecture):** * S3 was integrated with Databricks as an **External Location**.
* Data was transformed from **Bronze** (Raw) to **Gold** (Insights) layers using Spark SQL.


3. **Analytics:** Performed deep-dive analysis to identify top-performing states, best-selling categories, and Average Order Value (AOV).
4. **Event-Driven Monitoring:**
* Configured **S3 Event Notifications** to trigger on new object uploads.
* Developed an **AWS Lambda** function to parse S3 events and format custom alerts.
* Automated email notifications via **AWS SNS**.



---

## 📈 Key Insights

* **Top Revenue State:** Analysis identified Maharashtra as the state with the highest sales volume.
* **Automated Reporting:** Insight visualizations (PNGs) are automatically synced to the `gold/insights/` S3 prefix via CLI.

---

## ⚙️ Setup and Deployment

1. Configure AWS credentials: `aws configure`.
2. Follow `cli-csv-upload.md` to initialize the S3 bucket hierarchy.
3. Import the `Databricks-SQL.ipynb` into your Databricks Workspace and attach it to a cluster.
4. Set up the Lambda trigger and SNS subscription as detailed in `report.md`.

---

### 💡 Disclaimer

*This project was conducted within the AWS Free Tier and free Databricks Community Edition. For security purposes, all IAM Access Keys were kept confidential and all cloud resources were terminated upon project completion.*

---
