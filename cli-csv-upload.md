# AWS CLI - S3 Operations Log

This document records the terminal operations performed using Windows PowerShell to configure AWS and manage S3 bucket activities.

### 1. AWS CLI Configuration
First, the environment was configured with the necessary credentials and region settings.

```powershell
PS C:\Users\HP> aws configure
AWS Access Key ID [************************]: **YOUR_ACCESS_KEY_ID**
AWS Secret Access Key [********************]: **YOUR_ACCESS_KEY**
Default region name [None]: eu-north-1
Default output format [json]: json

```

### 2. Creating the S3 Bucket

A new bucket named `amazon-sale-vit` was created in the specified region.

```powershell
PS C:\Users\HP> aws s3 mb s3://amazon-sale-vit
make_bucket: amazon-sale-vit

```

### 3. Data Ingestion (Local to S3)

Navigated to the project directory and uploaded the raw dataset to the `landing/` folder.

```powershell
PS C:\Users\HP\Desktop\VIT\Week9_CloudComputing> aws s3 ls
2026-01-27 20:35:52 amazon-sale-vit

PS C:\Users\HP\Desktop\VIT\Week9_CloudComputing> aws s3 cp "Amazon Sale Report.csv" s3://amazon-sale-vit/landing/
upload: .\Amazon Sale Report.csv to s3://amazon-sale-vit/landing/Amazon Sale Report.csv

```

### 4. Verifying the Upload

Checked the contents of the landing zone to ensure the file was successfully transferred.

```powershell
PS C:\Users\HP\Desktop\VIT\Week9_CloudComputing> aws s3 ls s3://amazon-sale-vit/landing/
2026-01-27 20:40:50   68923428 Amazon Sale Report.csv

```

