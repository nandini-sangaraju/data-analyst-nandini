# Project - Descriptive Analysis

#  3-1-1 Service Requests

# Description:
The project focuses on designing and implementing a Data Analytics Platform (DAP) for the 3-1-1 service requests in Vancouver. The 3-1-1 service is a non-emergency contact center that provides information an assistance to residents and visitors. The platform aims to streamline the process of data ingestion, profiling, cleaning, cataloging, and summarization to derive actionable insights from the service request data.

# Objective:
The primary objective of this project is to develop a robust data analytics platform that can efficiently process and analyze 3-1-1 service request data. The platform will enable the city of Vancouver to improve its call center operations by identifying trends, evaluating performance metrics, and enhancing customer service practices.

*Figure 1 Data Analytics Platform design (Draw.io)*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/objective.png)
# Methodology:

The project follows a structured approach to data analytics, divided into five key steps:

-   **Data Ingestion**:Data is collected from various sources and stored in an Amazon S3 bucket. The data is organized in a structured folder hierarchy for easy access and management. (*Location: /contact-centre/311-service/year=24/month=12/day=31/server=YVR-nan*)

 *Figure 2 AWS S3 Raw data storage (Excel file)*
 ![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/data_ingestion.png)
    
-   **Data Profiling**: AWS Glue DataBrew is used to analyze the quality of the data, identify missing values, and detect inconsistencies. This step ensures that the data is ready for further processing. (*A transfer bucket has been created in the S3 bucket for transferring data*).

*Figure 3 AWS Glue DataBrew updated data profile*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/data_profiling.jpeg)
    
-   **Data Cleaning:** The data is cleaned by standardizing formats, removing inconsistencies, and correcting errors (*changing the date format to yyyy-mm-dd*). This step ensures that the data is accurate and reliable for analysis.

*Figure 4 AWS Glue DataBrew Profiling Job*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/data_cleaning.jpeg)
    
-   **Data Cataloging:** The cleaned data is organized using the AWS Glue Data Catalog. A database named contact-centre-data-catalog-nan was created. AWS Glue Crawlers are used to automatically create schema definitions and populate the catalog, making the data easily accessible for queries and analysis.

*Figure 5 AWS Glue – Data catalog - job creation & run*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/data_cataloging.jpeg)
    
-   **Data Summarization:** The data is processed through an Extract, Transform, Load (ETL) pipeline to derive key insights. This step involves summarizing the data to evaluate call center performance metrics such as the average number of calls offered and abandoned.

*Figure 6 AWS Glue - ETL pipeline visualization*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/pipeline_visualization.jpeg)

*Figure 7 AWS S3 Curated bucket Summarized output - System*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/Summ_out_sys.jpeg)

*Figure 8 AWS S3 Curated bucket Summarized output - User*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/Summ_out_user.jpeg)

*Figure 9 AWS Glue Data Catalog tables*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/Data_catalog_table.jpeg)

# Tools and Technologies:

-   **Amazon S3:** Used for data storage and organization.

-   **AWS Glue DataBrew:** Used for data profiling and cleaning.

-   **AWS Glue Data Catalog:** Used for data cataloging and schema
    management.

-   **AWS Glue ETL:** Used for data transformation and summarization.

-   **Visual ETL:** Used for visualizing the ETL pipeline and summarizing data.

# Deliverables:

-   **Data Ingestion Pipeline:** A fully functional pipeline for ingesting and storing 3-1-1 service request data in an Amazon S3 bucket.
    
-   **Data Profiling Report:** A detailed report generated by AWS Glue DataBrew, highlighting data quality issues and inconsistencies.
    
-   **Cleaned Data Set:** A cleaned and standardized dataset ready for analysis.
    
-   **Data Catalog:** A structured data catalog created using AWS Glue, enabling easy access and querying of the data.

-   **Summarized Insights:** Key insights derived from the data, including metrics such as the average number of calls offered and abandoned.



# Member List

# Description:
The Member List project is designed to manage and maintain comprehensive records of students within an educational institution. It includes critical details such as student demographics, academic performance, and contact information. The primary goal is to establish a centralized system for tracking student progress, facilitating communication, and supporting academic decision-making.

# Objective:
-   To create a reliable and up-to-date database of student records.
-   To monitor academic performance metrics such as GPA and enrollment status.
-   To enable seamless communication with students through email and phone.

*Figure 1 Data Analytics Platform design (Draw.io)*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/draw_io.jpeg)

# Methodology:

The project follows a structured approach to data analytics, divided into five key steps:

-   **Data Collection:** Student data is collected through structured CSV files and stored in Amazon S3

  *Figure 2 AWS S3 Raw data storage (Excel file)*
 ![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/member_s3.jpeg)
    
-   **Data Profiling:** AWS Glue DataBrew is used to profile the dataset, identifying missing values, duplicates, and inconsistencies.

  *Figure 3 AWS Glue DataBrew updated data profile*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/member_profiling.jpeg)
    
-   **Data Cataloging:** The dataset is registered in the AWS Glue Data Catalog to create a searchable metadata repository.


-   **Data Transformation:** AWS Glue ETL jobs are employed to clean and standardize the data (e.g., formatting names, correcting GPA values).

  *Figure 4 AWS Glue – Data catalog - job creation & run*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/member_databrew.jpeg)

-   **Data Storage:** The cleaned data is stored back in Amazon S3 for further analysis or integration with other datasets.
 
-   **Reporting:** AWS Glue is used to generate reports on student demographics, academic trends, and enrollment statistics. 

    *Figure 5 AWS Glue - ETL pipeline visualization*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/member_pipeline.jpeg)

*Figure 6 AWS S3 Curated bucket Summarized output - System*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/member_system.jpeg)

*Figure 7 AWS S3 Curated bucket Summarized output - User*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/member_user.jpeg)

*Figure 8 AWS Glue Data Catalog tables*
![Alt text](https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/member_table.jpeg)

# Tools and Technologies:

-   **Data Storage:** Amazon S3 for storing raw and processed student records.
-   **Data Profiling:** AWS Glue DataBrew for data quality checks and profiling.
-   **Data Catalog:** AWS Glue Data Catalog for metadata management.
-   **Data Transformation:** AWS Glue ETL jobs for cleaning and transforming data.
-   **Reporting:** AWS Glue for generating reports and insights.

# Deliverables:

-   **Data Ingestion Pipeline:** A fully functional pipeline for ingesting and storing student records in an Amazon S3 bucket.
  
-   **Data Profiling Report:** A detailed report generated by AWS Glue DataBrew, highlighting data quality issues such as missing values, duplicates, and inconsistencies in student records.
  
-   **Cleaned Data Set:** A cleaned and standardized dataset of student records, ready for analysis and integration with other datasets.
  
-   **Data Catalog:** A structured data catalog created using AWS Glue, enabling easy access and querying of student data.
  
-   **Summarized Insights:** Key insights derived from the data, including metrics such as average GPA, enrollment trends, and demographic breakdowns.



# Advisor List:

# Description:
The Advisor List project is designed to manage advisor records, including their specialization, availability, and contact details. The goal is to ensure that students are assigned the most suitable advisor based on their needs and the advisor's expertise, while also tracking advisor workload and performance.

# Objective:
-   To maintain an accurate and up-to-date database of advisor records.
-   To assign advisors to students based on specialization and availability.
-   To monitor advisor workload and performance metrics.

# Methodology:
-   **Data Collection:** Advisor data is collected through structured CSV files and stored in Amazon S3.
  
-   **Data Profiling:** AWS Glue DataBrew is used to profile the dataset, ensuring data quality and consistency (e.g., checking for missing values, duplicates, and inconsistencies).
  
-   **Data Cataloging:** The dataset is registered in the AWS Glue Data Catalog to create a searchable metadata repository.
  
-   **Data Transformation:** AWS Glue ETL jobs are employed to clean and transform the data (e.g., standardizing formats, enriching data with additional fields).
  
-   **Data Storage:** The cleaned data is stored back in Amazon S3 for further analysis or integration with other datasets.
  
-   **Reporting:** AWS Glue is used to generate reports on advisor workload, performance, and availability.

# Tools and Technologies:
-   **Data Storage:** Amazon S3 for storing raw and processed advisor records.
-   **Data Profiling:** AWS Glue DataBrew for data quality checks and profiling.
-   **Data Catalog:** AWS Glue Data Catalog for metadata management.
-   **Data Transformation:** AWS Glue ETL jobs for cleaning and transforming data.
-   **Reporting:** AWS Glue for generating reports and insights.

# Deliverables:
-   **Data Ingestion Pipeline:** A fully functional pipeline for ingesting and storing advisor records in an Amazon S3 bucket.

-   **Data Profiling Report:** A detailed report generated by AWS Glue DataBrew, highlighting data quality issues such as missing contact details, duplicate entries, and inconsistencies in advisor records.

-   **Cleaned Data Set:** A cleaned and standardized dataset of advisor records, ready for analysis and integration with other datasets.

-   **Data Catalog:** A structured data catalog created using AWS Glue, enabling easy access and querying of advisor data.

-   **Summarized Insights:** Key insights derived from the data, including metrics such as advisor workload, specialization distribution, and availability trends.



#  Complaint List:

# Description:
The Complaint List project focuses on managing and resolving student complaints efficiently. It includes details such as complaint type, description, status, and assigned advisor. The goal is to streamline the complaint resolution process, improve response times, and enhance student satisfaction.

# Objective:
-   To establish a system for tracking and resolving student complaints.
-   To assign the most suitable advisor based on complaint type and severity.
-   To monitor and reduce complaint resolution times.

# Methodology:
-   **Data Collection:** Complaint data is collected through structured CSV files and stored in Amazon S3.
  
-   **Data Profiling:** AWS Glue DataBrew is used to profile the dataset, identifying common complaint types, trends, and data quality issues.
  
-   **Data Cataloging:** The dataset is registered in the AWS Glue Data Catalog to create a searchable metadata repository.
  
-   **Data Transformation:** AWS Glue ETL jobs are used to clean and transform the data (e.g., standardizing complaint types, linking complaints to students and advisors).
  
-   **Data Storage:** The cleaned data is stored back in Amazon S3 for further analysis or integration with other datasets.
  
-   **Reporting:** AWS Glue is used to generate reports on complaint resolution times, advisor performance, and common issues.

# Tools and Technologies:
-   Data Storage: Amazon S3 for storing raw and processed complaint records.
-   Data Profiling: AWS Glue DataBrew for data quality checks and profiling.
-   Data Catalog: AWS Glue Data Catalog for metadata management.
-   Data Transformation: AWS Glue ETL jobs for cleaning and transforming data.
-   Reporting: AWS Glue for generating reports and insights.

# Deliverables:
-   **Data Ingestion Pipeline:** A fully functional pipeline for ingesting and storing student complaints in an Amazon S3 bucket.

-   **Data Profiling Report:** A detailed report generated by AWS Glue DataBrew, highlighting data quality issues such as missing complaint descriptions, unresolved statuses, and inconsistencies.

-   **Cleaned Data Set:** A cleaned and standardized dataset of student complaints, ready for analysis and integration with other datasets.

-   **Data Catalog:** A structured data catalog created using AWS Glue, enabling easy access and querying of complaint data.

-   **Summarized Insights:** Key insights derived from the data, including metrics such as average resolution time, most common complaint types, and advisor performance.
