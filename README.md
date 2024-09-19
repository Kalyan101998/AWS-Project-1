<h1 align="center">AWS Project 1</h1>


# Project Description: Implementation and Analysis of Animal Control Data
* This project involves setting up a comprehensive data analytics platform using AWS services to manage the City of Vancouver’s animal control data.

## Project Title: AWS Data Analytic Platform for the City of Vancouver - Part 1
* This project goal was to streamline data sourcing, storage, cleaning, transformation, and analysis, all while maintaining high standards of data security and governance. The platform was built with a focus on handling large datasets, securing sensitive information, and providing real-time insights through data visualization.
## Project Objective:
* The objective of this project is to design and implement a secure AWS-based Data Analytics Platform (DAP) for processing and analyzing the City of Vancouver’s Animal Control Lost and Found inventory data. The platform ensures data protection, efficient processing, and the provision of actionable insights to assist city officials in better managing animal-related cases.
## Methodology:
* The process of DAP designing and implementation is as follows.
### 1. Data Analytical Question Formulation
Key analytical questions driving the project include:
- What are the trends in lost and found animals over the years?
- Which breeds or colours are most commonly reported as lost or found?
### 2. Data Discovery
- The data is sourced from external datasets. For example, the dataset for animal control inventory lost and found is accessed via an open data portal. This involves identifying and accessing relevant datasets that will be used for analysis.
![image](https://github.com/user-attachments/assets/e6f8f460-7dd7-463c-a2a4-2ba59a483269)

### 3. Storage Design
The storage design phase involves setting up a system to efficiently store and manage the data. 
- **Raw Bucket**: Stores raw, unprocessed data.
- **Staging Bucket**: Holds preliminary processed data after basic cleaning.
- **Curated Bucket**: Contains final cleaned and transformed data, ready for analysis. 
 ![image](https://github.com/user-attachments/assets/3286dd09-d2c7-45de-9c0e-a85568d611a7)

### 4. Data Preparation
- AWS DataBrew was employed to cleaning and transforming the data to ensure  that there is no null values, correcting data formats, and eliminating unnecessary data points.
![image](https://github.com/user-attachments/assets/1f4ed4d5-e308-46aa-b69d-060075fb3b5a)

### 5. Data Injection
- Once cleaned, the cleaned data is transferred into the designated storage location, such as a raw data bucket for further processing.
![image](https://github.com/user-attachments/assets/d27b45fa-350f-40c2-ba54-21ac2f280c22)

### 6. Data Pipeline Design
- AWS Glue is used to create the data pipeline, automating the ETL process.
- The data pipeline is designed to facilitate the smooth flow and transformation of data throughout the system.
![image](https://github.com/user-attachments/assets/7920194e-3cf5-45d2-8f8a-7e0cfde1d526)

### 7. Data Cleaning
- Data cleaning involves removing any inconsistencies or errors in the data to improve its quality. and was free of null or incomplete entries. 
![image](https://github.com/user-attachments/assets/dbb801a1-dfe5-48f6-b45f-d1a360ca930b)

### 8. Data Structuring
- Data is organized in a way that aligns with the analytical questions being addressed, making it easier to analyze.
![image](https://github.com/user-attachments/assets/cadee02f-bfd7-4abd-bbb6-e540c29993d8)

### 9. Data Pipeline Implementation
- AWS Glue Jobs were set up to ensure the data was properly transformed and loaded into the final S3 Curated bucket for analysis.
- The data pipeline is implemented to ensure data is processed and loaded correctly, using tools like AWS Glue.
![image](https://github.com/user-attachments/assets/33f5b481-cd4a-4506-94e4-7e2a2a84317a)
![image](https://github.com/user-attachments/assets/0162ae05-d76f-4ed0-946c-b267f3bac78f)

### 10. Data Analysis
- AWS Athena was utilized to execute SQL queries on the structured data. An example query used in the project is:
![image](https://github.com/user-attachments/assets/1715ff90-b443-4141-8bbb-3588589cb12c)
- This query helped retrieve information on found animal differnece in 2023 and 2024

### 11. Data Visualization
- Based on the output data recorded from the table created a data visualization where it show the difference in the year the number of found animal in year 2024 and 2023.
![image](https://github.com/user-attachments/assets/5d49a1be-057f-499d-91eb-031dc3c793c1)
### 12. Data Publishing
- The final step involves publishing the analysis results, making them accessible to stakeholders through a server setup like AWS EC2. This rewritten version maintains the original content's meaning while using different wording and structure.
![image](https://github.com/user-attachments/assets/2b9c68de-290c-4a65-b5ac-80fe67a138c7)








