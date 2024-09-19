<h1 align="center">AWS Project 1</h1>


# Project Description: Implementation and Analysis of Safety-Issued Operating Permits Using AWS
* The City of Vancouver requires a robust and efficient data platform to manage and analyze safety-issued operating permits for water systems, including cooling towers, water features, and other public systems.

## Project Title: AWS Data Analytic Platform for the City of Vancouver - Part 1
* This project aims to design and implement a Data Analytics Platform (DAP) using Amazon Web Services (AWS) to store, process, and analyze water system permits to ensure public health standards are met and to streamline responses to any identified issues.
## Project Objective:
* Designing & Implementing DAP.
## Methodology:
* The process of DAP designing and implementation is as follows.
### 1. Data Analytical Question Formulation
Key analytical questions driving the project include:
- How many water system operating permits were issued for each department in 2024 and 2025?
- What is the trend in water system permits issued across different departments and over time?-
- How does water quality and system performance differ between the departments? 
### 2. Data Discovery
- The dataset was sourced from the City of Vancouver’s open data portal, containing detailed information on issued operating permits for water systems, along with reports on water quality and conditions. 
![image](https://github.com/user-attachments/assets/5fb7608e-c4c5-4020-808c-b121ff962f9d)
### 3. Storage Design
To efficiently handle data storage, AWS S3 was utilized with the following structure:
- **Raw Bucket**: Stores raw, unprocessed data.
- **Staging Bucket**: Holds preliminary processed data after basic cleaning.
- **Curated Bucket**: Contains final cleaned and transformed data, ready for analysis. 
 ![image](https://github.com/user-attachments/assets/e4be7bc0-21cc-42db-8a2b-7127056128ae)
### 4. Data Preparation
- AWS DataBrew was employed to clean and standardize the data by removing null values, correcting data formats, and eliminating unnecessary data points.
![image](https://github.com/user-attachments/assets/948612a0-40f2-4b91-af27-9afa83b85e5a)
### 5. Data Injection
- Once cleaned, the data was ingested into the S3 Raw bucket for storage and further processing.
![image](https://github.com/user-attachments/assets/7c5369a9-f0fd-48e2-b619-968588a499b0)
### 6. Data Pipeline Design
- AWS Glue was used to create the data pipeline, automating the ETL (Extract, Transform, Load) process.
- The pipeline ensured the smooth flow of data from storage to processing and transformation. 
![image](https://github.com/user-attachments/assets/d24b74ba-d0c0-4187-8d99-545641440b6e)
### 7. Data Cleaning
- AWS DataBrew was again used for in-depth data cleaning, ensuring that the data conformed to necessary formats and was free of null or incomplete entries. 
![image](https://github.com/user-attachments/assets/21321062-ef43-4f8d-ba78-0bcde00bbeab)
### 8. Data Structuring
- The data was restructured according to department and monthly trends, which enabled more focused analysis and answered the key analytical questions. 
![image](https://github.com/user-attachments/assets/87944ecf-44be-45dc-92a5-94690fb62cf0)
### 9. Data Pipeline Implementation
- AWS Glue Jobs were set up to ensure the data was properly transformed and loaded into the final S3 Curated bucket for analysis. 
![image](https://github.com/user-attachments/assets/c8fc0239-628c-4be9-a8c5-8b14a16f49a2)
### 10. Data Analysis
- AWS Athena was utilized to execute SQL queries on the structured data. An example query used in the project is:
```sql
SELECT * FROM "vancouver_water_permits"."issued_operating_permits";
```
- This query helped retrieve information on permits, categorized by department, for the years 2024 and 2025. 
![image](https://github.com/user-attachments/assets/84ed5433-741f-4bc4-a9da-3f8461037bb7)
### 11. Data Visualization
- Data on the number of permits issued per department for 2024 and 2025 was visualized to provide insights into how resources were allocated and how water system performance was monitored over time.
### 12. Data Publishing
- An AWS EC2 instance was deployed to publish the analysis results, providing remote access for stakeholders to view and interact with the data. 
![image](https://github.com/user-attachments/assets/5969a0f5-6a03-43c9-a38e-1576cef61ded)







