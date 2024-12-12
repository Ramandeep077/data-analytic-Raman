

<img width="604" alt="image" src="https://github.com/user-attachments/assets/82bf721a-4935-44f6-934a-ce7959ebd23f" />

# Hi, I'm Ramandeep Kaur 👋


### 👨‍💻 About Me:
- 📚 I’m an MBA student with a background in engineering, specializing in Computer Science.
- ☁️ Currently working on cloud computing projects using AWS and Python, exploring innovative solutions to real-world problems.
- 🌟 Passionate about combining technology and creativity to drive impactful results.

### 📧 Connect With Me:
📩 **Email:** [khindakhinda54@gmail.com](mailto:khindakhinda54@gmail.com)

# Start With First project
# Data-analytic-Raman
This project is focused on designing and implementing a Data Analytic Platform (DAP) to analyze business licence datasets from the City of Vancouver.The dataset, is begins from 2024, provides insights into the licensing process governed by Licence By-Law No. 4450. 
<img width="959" alt="image" src="https://github.com/user-attachments/assets/1c617e9a-106d-4dd3-811d-e9150ebc31ce" />
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

## Step 1: Data Ingestion
- 1.1.	city-raw-raman
For the data ingestion in my project, I used two S3 buckets: city-raw-raman and city-trf-raman. The purpose of this setup is to keep the workflow structured and organized.
![image](https://github.com/user-attachments/assets/d6a656cc-3899-44c7-8059-bb5a74ccd961)
Actual structure of Raw bucket is showing below:
![image](https://github.com/user-attachments/assets/9002055e-74ce-4000-8c1d-5eba9966efee)
Created by Ramandeep using Excel
1.2.	city-trf-raman
The city-trf-raman bucket stores all the transformed data, ready for analysis. This separation helps keep raw data untouched while ensuring cleaned data is optimized for querying, reporting, and analysis tasks.
 ![image](https://github.com/user-attachments/assets/b0a677cf-b319-4e43-b7bb-18a9e7e6dbb7)
## Step:2-Data Profiling :
During the data profiling phase for the Vancouver City business license project, AWS Glue DataBrew was utilized to analyze the raw data stored in the city-raw-raman bucket.
Creating the Database
![image](https://github.com/user-attachments/assets/a08cbb0c-95d8-4136-8f60-faf22e94c0d4)
Profiling the Raw Data
![image](https://github.com/user-attachments/assets/f4200453-c2d8-41e0-ad99-e7e269f360a5)
Storing Profiling Results
After completing the profiling, the results were exported to the raw-trf-raman bucket under the profiling folder. 
![image](https://github.com/user-attachments/assets/d944cace-2937-4bb2-af2d-6cfc75f059f7)
## Step:3-Data Cleaning 
After completing the data profiling process, the next step was to clean the data for analysis and ensure it met the quality standards required for descriptive and exploratory analytics.

![image](https://github.com/user-attachments/assets/6454984f-042c-4a05-9959-9d3fee0658fb)
Running the Cleaning Job

![image](https://github.com/user-attachments/assets/bff30be9-7f8d-4d8d-8e90-74b0bba23225)
Data linkage for cleaning process:

![image](https://github.com/user-attachments/assets/6aa901be-4126-4e94-bd53-13e21adeeaf4)
## Step:4: Data Pipeline
The pipeline starts by ingesting the cleaned dataset stored in the city-trf-raman. AWS Glue Job was created to process the ingested data and prepare it for analysis:
1.	Filtered businesses with valid Fee Paid data (Fee Paid >0).
2.	Grouped businesses by Local Area.
3.	Aggregated the number of businesses with:
•	Fee Paid > 0 (Paid).
•	Fee Paid = 0 (Unpaid).
   -- Pipeline design

  	![image](https://github.com/user-attachments/assets/c87777e7-b356-4327-8ded-5fd8675d16b0)
  	## Results

  	![image](https://github.com/user-attachments/assets/05d06178-1e63-4d9b-b6ea-5850966bfc0b)
  	Job executed successfully

  	![image](https://github.com/user-attachments/assets/6ddb97cd-b514-4a03-b8a3-786d9c340a90)

   ## [Diagnostic Analysis](Assignment2_predictive.ipynb)
   
   ### 📊 Diagnostic Analysis: Heart Disease Dataset

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

   
   











