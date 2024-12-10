# Data-analytic-Raman
This project is focused on designing and implementing a Data Analytic Platform (DAP) to analyze business licence datasets from the City of Vancouver.The dataset, is begins from 2024, provides insights into the licensing process governed by Licence By-Law No. 4450. 
# Descriptive Analysis 
This analysis investigates the financial compliance of businesses in the "Business Support Services" category within Vancouver.
![image](https://github.com/user-attachments/assets/653b93c8-aa34-4d58-a27f-b29be515124a)
Using the above visualization, we focus on the following descriptive analysis question:
"Which local area in Vancouver has the highest number of businesses that have paid the required fee (FeePaid > 0) compared to those that have not (FeePaid = 0)?"
### Using the structured draw.io diagram, the analysis follows a systematic approach:
![image](https://github.com/user-attachments/assets/fba50c7e-d825-445d-941a-a3aebc32c800)
Created by Ramandeep using Draw.io
# Methodology
1.	Data Ingestion (City-Raw-Raman Bucket)
2.	Data Profiling (AWS Glue DataBrew)
3.	Data Cleaning (City-Trf-Raman Bucket)
4.	Data Pipeline Design (AWS Glue)
Step 1: Data Ingestion 
For the data ingestion in my project, I used two S3 buckets: city-raw-raman and city-trf-raman. The purpose of this setup is to keep the workflow structured and organized.
![image](https://github.com/user-attachments/assets/d6a656cc-3899-44c7-8059-bb5a74ccd961)


