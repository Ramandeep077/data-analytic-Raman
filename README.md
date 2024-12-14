

<img width="604" alt="image" src="https://github.com/user-attachments/assets/82bf721a-4935-44f6-934a-ce7959ebd23f" />

# Hi, I'm Ramandeep Kaur 👋


### 👨‍💻 About Me:
- 📚 I’m an MBA student with a background in engineering, specializing in Computer Science.
- ☁️ Currently working on cloud computing projects using AWS and Python, exploring innovative solutions to real-world problems.
- 🌟 Passionate about combining technology and creativity to drive impactful results.

### 📧 Connect With Me:
📩 **Email:** [khindakhinda54@gmail.com](mailto:khindakhinda54@gmail.com)

# Data-Analytic-Raman

## Descriptive Analysis

### Project Title:
**Designing and Implementing a Data Analytic Platform (DAP) for Vancouver City Business Licence Dataset**

### Project Description:
This project focuses on developing a Data Analytic Platform (DAP) to analyze business license datasets from the City of Vancouver. The dataset begins from 2024 and provides insights into the licensing process governed by Licence By-Law No. 4450. The primary goal is to investigate financial compliance in the "Business Support Services" category within Vancouver.
<img width="943" alt="image" src="https://github.com/user-attachments/assets/eaea29c6-7c5d-453f-9e6b-d17c53638095" />

### Objective:
To systematically analyze and understand the compliance of businesses with the required license fees and identify trends in payment behaviors across local areas in Vancouver. The analysis provides actionable insights to enhance operational transparency and decision-making.

### Dataset:
- **Raw Data:** Sourced from the city-raw-raman S3 bucket.
- **Transformed Data:** Cleaned and prepared for analysis, stored in the city-trf-raman S3 bucket.
- **Key Features:** FeePaid, LocalArea, BusinessCategory, among others.

## Methodology

### Step 1: Data Ingestion
- **Buckets:**
  - **city-raw-raman:** Stored raw, untouched data.
  - **city-trf-raman:** Stored cleaned and transformed data for analysis.
- Ensured a structured workflow to maintain data integrity.

![Data Ingestion Workflow](https://github.com/user-attachments/assets/d6a656cc-3899-44c7-8059-bb5a74ccd961)

### Step 2: Data Profiling
- **Tool Used:** AWS Glue DataBrew.
- **Process:**
  - Created a database and analyzed raw data from city-raw-raman.
  - Exported profiling results to city-trf-raman under the profiling folder.

![Profiling Results](https://github.com/user-attachments/assets/f4200453-c2d8-41e0-ad99-e7e269f360a5)

### Step 3: Data Cleaning
- **Objective:** Address missing values, duplicates, and inconsistencies.
- **Process:**
  - Ran cleaning jobs using AWS Glue DataBrew.
  - Linked cleaned data back to city-trf-raman for further processing.

![Cleaning Workflow](https://github.com/user-attachments/assets/6454984f-042c-4a05-9959-9d3fee0658fb)

### Step 4: Data Pipeline Design
- **Tool Used:** AWS Glue.
- **Process:**
  1. Filtered businesses with FeePaid > 0.
  2. Grouped businesses by Local Area.
  3. Aggregated FeePaid data (Paid vs. Unpaid).

![Pipeline Design](https://github.com/user-attachments/assets/c87777e7-b356-4327-8ded-5fd8675d16b0)

## Results:

### Descriptive Analysis Question:
**"Which local area in Vancouver has the highest number of businesses that have paid the required fee (FeePaid > 0) compared to those that have not (FeePaid = 0)?"**

### Key Findings:
- Local area trends identified through descriptive statistics and visualizations.
- Business compliance rates analyzed to support operational decision-making.

![Results Visualization](https://github.com/user-attachments/assets/05d06178-1e63-4d9b-b6ea-5850966bfc0b)

## Tools and Technologies
- **AWS Services:** S3, Glue, Glue DataBrew.
- **Visualization Tools:** Tableau, Draw.io.
- **Programming Languages:** Python.

---

## Deliverables:
1. A cleaned and transformed dataset stored in city-trf-raman.
2. Profiling results exported for deeper insights.
3. Visualizations highlighting compliance trends.
4. A structured data pipeline for scalable analytics.

This structured approach ensures that the analysis is comprehensive, actionable, and aligned with project goals.

   ---------------------------------------------------------------------------------------------------------------------------------------------------------------

   # 🌟 Project 2: DATA QUALITY CONTROL 🌟

**Project Description:** This project focuses on implementing a robust data quality control process to ensure accurate, complete, and reliable datasets for analyzing business licences in Vancouver. The 2024 dataset offers insights into the licensing process governed by Licence By-Law No. 4450. Our goal is to establish a scalable system for maintaining data integrity and usability for meaningful insights.

**Objective:** To establish a comprehensive data quality control framework that enhances data reliability, improves insights, and ensures compliance with data governance practices.

**Background:**
The City of Vancouver’s business licensing process involves complex data interactions. Inaccuracies or inconsistencies in datasets can lead to flawed insights. This project introduces measures like data enrichment, encryption, governance, and monitoring to mitigate such issues while optimizing data usability.

**Scope:**
The Data Quality Control Initiative emphasizes:
- **Data Enrichment:** Ensuring raw data is structured and organized for processing.
- **Data Protection:** Implementing encryption and redundancy to secure data.
- **Data Governance:** Setting and enforcing quality standards for datasets.
- **Data Observability:** Proactively monitoring data flow and quality metrics.

**Methodology:**
1. **Data Ingestion:**
   - Extracted raw data from DynamoDB and loaded it into Amazon S3 for structured storage.
   - Organized data into logical folders to ensure accessibility and clarity.
2. **Data Profiling:**
   - Analyzed data attributes to understand distributions, trends, and anomalies.
   - Verified key metrics like completeness and uniqueness for all data fields.
3. **Data Cleaning:**
   - Addressed missing values and inconsistencies in critical fields like `status` and `licencesrn`.
   - Standardized data formats to ensure compatibility with downstream processes.
4. **Data Enrichment:**
   - ### Enhanced datasets with additional attributes for improved analytical capabilities.
     ![image](https://github.com/user-attachments/assets/7d3ba2d0-c464-4520-8c5c-11b3633e5c8d)

   - # Validated enriched data using SQL queries in Amazon Athena.
     ![image](https://github.com/user-attachments/assets/c506e140-8b5b-4d41-875d-36a321493dba)

5. **Data Protection:**
   - ### Applied AWS KMS encryption to secure all S3 buckets.
     ![image](https://github.com/user-attachments/assets/eefcc72c-652c-486b-a01f-b21c1604a5db)
     ![image](https://github.com/user-attachments/assets/ff62f9d4-d531-4a77-b139-3587f7809965)


   - ### Enabled bucket versioning and established replication rules for data redundancy.
     ![image](https://github.com/user-attachments/assets/b7731463-3a01-4cfd-9b0b-9eb8cc1bccec)
     ![image](https://github.com/user-attachments/assets/51457292-d2e1-4d1b-8004-4952b5323a95)
     ![image](https://github.com/user-attachments/assets/2d089441-8301-47ac-96ae-28fcdcc0c922)



6. **Data Governance:**
   - ### Developed pipelines to evaluate data completeness (95%) and uniqueness (99%).
     ![image](https://github.com/user-attachments/assets/8a48c8b8-65d3-4140-9330-7c0cef0e9039)

   - ### Routed high-quality records to designated processing groups.
     ![image](https://github.com/user-attachments/assets/f4ba696e-4c1e-4b6d-b59b-2573c5113cc0)
     # Quality data 
     ![image](https://github.com/user-attachments/assets/ec276997-9233-4b24-8454-0723a55a6acd)


7. **Data Observability:**
   - ### Built dashboards to track data usage and flow.
     ![image](https://github.com/user-attachments/assets/cdb6b53d-afda-4b35-a3c8-38129abcf88c)
     ![image](https://github.com/user-attachments/assets/017946ec-0b46-4e2b-8fd3-ec221ae4b004)


   - ### Configured alerts to detect anomalies in object counts or quality metrics.
   ![image](https://github.com/user-attachments/assets/7cb5f551-ab21-4088-8e52-9b0fb705695e)


**Tools and Technologies:**
- **Data Processing:** AWS S3, DynamoDB, Glue, Athena
- **Security:** AWS KMS, S3 Replication, Versioning
- **Monitoring:** CloudWatch Dashboards, Conditional Routers
- **Programming:**  SQL

**Deliverables:**
- Enriched and validated datasets stored in S3.
- Automated pipelines for data quality assurance.
- Dashboards for monitoring data integrity and flow.
- Secure and redundant data storage with KMS encryption and replication.
- Comprehensive quality control report and insights.

---------------------------------------------------------------------------------------------------------------------------------------------------

   ## [Diagnostic Analysis](Assignment2_predictive.ipynb)
   
   # 🚀  Diagnostic Analysis: Heart Disease Dataset 🚀 

**Project Title:** Diagnostic Analysis of Heart Disease Dataset

**Project Description:** This project focuses on analyzing a dataset related to heart disease to understand its patterns and predict future outcomes. By leveraging advanced machine learning techniques, we aim to identify key risk factors and provide insights for early diagnosis and prevention.

**Objective:** To diagnose and predict the presence of heart disease by exploring data patterns and leveraging predictive models to enhance understanding and prevention efforts.

**Background:**
Heart disease remains one of the leading health concerns globally. Early diagnosis and understanding of contributing factors can significantly improve patient outcomes. This project investigates a dataset containing key clinical, demographic, and medical history attributes to analyze and predict heart disease occurrences.
<img width="464" alt="image" src="https://github.com/user-attachments/assets/f532b4f9-1bf4-4bda-b1cb-4cb23b8f4372" />
**Dataset:**
The dataset consists of 920 entries with 16 features, including:
- **Patient Demographics:** Age and gender.
- **Clinical Data:** Blood pressure (trestbps), cholesterol levels (chol), maximum heart rate achieved (thalach), and more.
- **Medical History:** Chest pain types (cp), fasting blood sugar (fbs), exercise-induced angina (exang), and existing conditions (num).
- **Data Details:** Some columns have missing values, such as slope, ca, and thal, which will be addressed during preprocessing.
- <img width="331" alt="image" src="https://github.com/user-attachments/assets/6bcfefa0-038c-480a-bad9-525841d65c98" />


**Methodology:**
1. **Data Cleaning:** Handle missing values, normalize features, and encode categorical variables.
2. **Exploratory Analysis:** Visualize data distributions and identify correlations between features and target outcomes.
3. **Modeling:** Use K-Nearest Neighbors (KNN) and Decision Trees (DT) to predict the presence of heart disease.
4. **Validation:** Evaluate models using accuracy, precision, recall, and F1 scores.

**Tools and Technologies:**
- **Programming Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Scikit-learn
- **Platform:** Colab notebook

**Deliverables:**
- A cleaned and preprocessed dataset ready for analysis.
- Visualization and insights derived from the data.
- Predictive models with evaluation metrics.
- A detailed report summarizing findings and recommendations.

   
   











