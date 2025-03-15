Project Description:
The project focuses on designing and implementing a Data Analytics Platform (DAP) for the 3-1-1 service requests in Vancouver. The 3-1-1 service is a non-emergency contact center that provides information and assistance to residents and visitors. The platform aims to streamline the process of data ingestion, profiling, cleaning, cataloging, and summarization to derive actionable insights from the service request data.

Project Title:
Design and Implementation of a Data Analytics Platform for 3-1-1 Service Requests in Vancouver

Objective:
The primary objective of this project is to develop a robust data analytics platform that can efficiently process and analyze 3-1-1 service request data. The platform will enable the city of Vancouver to improve its call center operations by identifying trends, evaluating performance metrics, and enhancing customer service practices.

Methodology:
The project follows a structured approach to data analytics, divided into five key steps:

Data Ingestion:

Data is collected from various sources and stored in an Amazon S3 bucket. The data is organized in a structured folder hierarchy for easy access and management.

Data Profiling:

AWS Glue DataBrew is used to analyze the quality of the data, identify missing values, and detect inconsistencies. This step ensures that the data is ready for further processing.

Data Cleaning:

The data is cleaned by standardizing formats, removing inconsistencies, and correcting errors. This step ensures that the data is accurate and reliable for analysis.

Data Cataloging:

The cleaned data is organized using the AWS Glue Data Catalog. AWS Glue Crawlers are used to automatically create schema definitions and populate the catalog, making the data easily accessible for queries and analysis.

Data Summarization:

The data is processed through an Extract, Transform, Load (ETL) pipeline to derive key insights. This step involves summarizing the data to evaluate call center performance metrics such as the average number of calls offered and abandoned.

Tools and Technologies:
Amazon S3: Used for data storage and organization.

AWS Glue DataBrew: Used for data profiling and cleaning.

AWS Glue Data Catalog: Used for data cataloging and schema management.

AWS Glue ETL: Used for data transformation and summarization.

Visual ETL: Used for visualizing the ETL pipeline and summarizing data.

Deliverables:
Data Ingestion Pipeline: A fully functional pipeline for ingesting and storing 3-1-1 service request data in an Amazon S3 bucket.

Data Profiling Report: A detailed report generated by AWS Glue DataBrew, highlighting data quality issues and inconsistencies.

Cleaned Data Set: A cleaned and standardized dataset ready for analysis.

Data Catalog: A structured data catalog created using AWS Glue, enabling easy access and querying of the data.

Summarized Insights: Key insights derived from the data, including metrics such as the average number of calls offered and abandoned.

Screenshots:
Note: Please insert the relevant screenshots from the project at the designated spaces below.

Figure 1: Data Analytics Platform design (Draw.io)
![Insert Figure 1 Screenshot Here]

Figure 2: AWS S3 Raw data storage (Excel file)
![Insert Figure 2 Screenshot Here]

Figure 3: AWS Glue DataBrew updated data profile
![Insert Figure 3 Screenshot Here]

Figure 4: AWS Glue DataBrew Profiling Job
![Insert Figure 4 Screenshot Here]

Figure 5: AWS Glue -- Data catalog - job creation & run
![Insert Figure 5 Screenshot Here]

Figure 6: AWS Glue - ETL pipeline visualization
![Insert Figure 6 Screenshot Here]

Figure 7: AWS S3 Curated bucket Summarized output - System
![Insert Figure 7 Screenshot Here]

Figure 8: AWS S3 Curated bucket Summarized output - User
![Insert Figure 8 Screenshot Here]

Figure 9: AWS Glue Data Catalog tables
![Insert Figure 9 Screenshot Here]
