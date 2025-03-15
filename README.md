# Project

## Descriptive Analysis -- 3-1-1 Service Requests

# Project Description:
The project focuses on designing and implementing a Data Analytics Platform (DAP) for the 3-1-1 service requests in Vancouver. The 3-1-1 service is a non-emergency contact center that provides information an assistance to residents and visitors. The platform aims to streamline the process of data ingestion, profiling, cleaning, cataloging, and summarization to derive actionable insights from the service request data.

# Objective:
The primary objective of this project is to develop a robust data analytics platform that can efficiently process and analyze 3-1-1 service request data. The platform will enable the city of Vancouver to improve its call center operations by identifying trends, evaluating performance metrics, and enhancing customer service practices.

*Figure 1 Data Analytics Platform design (Draw.io)*
<img src='./src/welcome-friends-prism.gif'>
# Methodology:

The project follows a structured approach to data analytics, divided into five key steps:

-   **Data Ingestion**:Data is collected from various sources and stored in an Amazon S3 bucket. The data is organized in a structured folder hierarchy for easy access and management. (*Location: /contact-centre/311-service/year=24/month=12/day=31/server=YVR-nan*)

 *Figure 2 AWS S3 Raw data storage (Excel file)*
 ![.c](https://github.com/nandini-sangaraju/data-analyst-nandini/blob/main/Images/data_ingestion.png)
    
-   **Data Profiling**: AWS Glue DataBrew is used to analyze the quality of the data, identify missing values, and detect inconsistencies. This step ensures that the data is ready for further processing. (*A transfer bucket has been created in the S3 bucket for transferring data*).

*Figure 3 AWS Glue DataBrew updated data profile*
![.c](https://github.com/nandini-sangaraju/data-analyst-nandini/blob/main/Images/data_profiling.jpeg)
    
-   **Data Cleaning:** The data is cleaned by standardizing formats, removing inconsistencies, and correcting errors (*changing the date format to yyyy-mm-dd*). This step ensures that the data is accurate and reliable for analysis.

*Figure 4 AWS Glue DataBrew Profiling Job*
![.c](https://github.com/nandini-sangaraju/data-analyst-nandini/blob/main/Images/data_cleaning.jpeg)
    
-   **Data Cataloging:** The cleaned data is organized using the AWS Glue Data Catalog. A database named contact-centre-data-catalog-nan was created. AWS Glue Crawlers are used to automatically create schema definitions and populate the catalog, making the data easily accessible for queries and analysis.

*Figure 5 AWS Glue – Data catalog - job creation & run*
![.c](https://github.com/nandini-sangaraju/data-analyst-nandini/blob/main/Images/data_cataloging.jpeg)
    
-   **Data Summarization:** The data is processed through an Extract, Transform, Load (ETL) pipeline to derive key insights. This step involves summarizing the data to evaluate call center performance metrics such as the average number of calls offered and abandoned.

*Figure 6 AWS Glue - ETL pipeline visualization*
![.c](https://github.com/nandini-sangaraju/data-analyst-nandini/blob/main/Images/pipeline_visualization.jpeg)

*Figure 7 AWS S3 Curated bucket Summarized output - System*
![.c](https://github.com/nandini-sangaraju/data-analyst-nandini/blob/main/Images/Summ_out_sys.jpeg)

*Figure 8 AWS S3 Curated bucket Summarized output - User*
![.c](https://github.com/nandini-sangaraju/data-analyst-nandini/blob/main/Images/Summ_out_user.jpeg)

*Figure 9 AWS Glue Data Catalog tables*
![.c](https://github.com/nandini-sangaraju/data-analyst-nandini/blob/main/Images/Data_catalog_table.jpeg)

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
    
    
