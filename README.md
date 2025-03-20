<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Project: Descriptive Analysis -- 3-1-1 Service Requests</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            margin: 0;
            padding: 20px;
        }
        h1, h2 {
            color: #2c3e50;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            margin: 10px 0;
        }
        .section {
            margin-bottom: 30px;
        }
        .section h2 {
            border-bottom: 2px solid #2c3e50;
            padding-bottom: 10px;
        }
        .section p {
            line-height: 1.6;
        }
        .tools-list {
            list-style-type: none;
            padding: 0;
        }
        .tools-list li {
            background-color: #e9ecef;
            margin: 5px 0;
            padding: 10px;
            border-radius: 4px;
        }
        .deliverables-list {
            list-style-type: square;
            padding-left: 20px;
        }
        .deliverables-list li {
            margin: 10px 0;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Project: Descriptive Analysis -- 3-1-1 Service Requests</h1>

        <div class="section">
            <h2>Project Description</h2>
            <p>The project focuses on designing and implementing a Data Analytics Platform (DAP) for the 3-1-1 service requests in Vancouver. The 3-1-1 service is a non-emergency contact center that provides information and assistance to residents and visitors. The platform aims to streamline the process of data ingestion, profiling, cleaning, cataloging, and summarization to derive actionable insights from the service request data.</p>
        </div>

        <div class="section">
            <h2>Objective</h2>
            <p>The primary objective of this project is to develop a robust data analytics platform that can efficiently process and analyze 3-1-1 service request data. The platform will enable the city of Vancouver to improve its call center operations by identifying trends, evaluating performance metrics, and enhancing customer service practices.</p>
            <img src="https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/objective.png" alt="Data Analytics Platform design">
        </div>

        <div class="section">
            <h2>Methodology</h2>
            <p>The project follows a structured approach to data analytics, divided into five key steps:</p>
            <ul>
                <li><strong>Data Ingestion:</strong> Data is collected from various sources and stored in an Amazon S3 bucket. The data is organized in a structured folder hierarchy for easy access and management. (<em>Location: /contact-centre/311-service/year=24/month=12/day=31/server=YVR-nan</em>)</li>
                <img src="https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/data_ingestion.png" alt="AWS S3 Raw data storage">
                <li><strong>Data Profiling:</strong> AWS Glue DataBrew is used to analyze the quality of the data, identify missing values, and detect inconsistencies. This step ensures that the data is ready for further processing. (<em>A transfer bucket has been created in the S3 bucket for transferring data</em>).</li>
                <img src="https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/data_profiling.jpeg" alt="AWS Glue DataBrew updated data profile">
                <li><strong>Data Cleaning:</strong> The data is cleaned by standardizing formats, removing inconsistencies, and correcting errors (<em>changing the date format to yyyy-mm-dd</em>). This step ensures that the data is accurate and reliable for analysis.</li>
                <img src="https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/data_cleaning.jpeg" alt="AWS Glue DataBrew Profiling Job">
                <li><strong>Data Cataloging:</strong> The cleaned data is organized using the AWS Glue Data Catalog. A database named contact-centre-data-catalog-nan was created. AWS Glue Crawlers are used to automatically create schema definitions and populate the catalog, making the data easily accessible for queries and analysis.</li>
                <img src="https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/data_cataloging.jpeg" alt="AWS Glue – Data catalog - job creation & run">
                <li><strong>Data Summarization:</strong> The data is processed through an Extract, Transform, Load (ETL) pipeline to derive key insights. This step involves summarizing the data to evaluate call center performance metrics such as the average number of calls offered and abandoned.</li>
                <img src="https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/pipeline_visualization.jpeg" alt="AWS Glue - ETL pipeline visualization">
                <img src="https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/Summ_out_sys.jpeg" alt="AWS S3 Curated bucket Summarized output - System">
                <img src="https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/Summ_out_user.jpeg" alt="AWS S3 Curated bucket Summarized output - User">
                <img src="https://raw.githubusercontent.com/nandini-sangaraju/data-analyst-nandini/main/Images/Data_catalog_table.jpeg" alt="AWS Glue Data Catalog tables">
            </ul>
        </div>

        <div class="section">
            <h2>Tools and Technologies</h2>
            <ul class="tools-list">
                <li><strong>Amazon S3:</strong> Used for data storage and organization.</li>
                <li><strong>AWS Glue DataBrew:</strong> Used for data profiling and cleaning.</li>
                <li><strong>AWS Glue Data Catalog:</strong> Used for data cataloging and schema management.</li>
                <li><strong>AWS Glue ETL:</strong> Used for data transformation and summarization.</li>
                <li><strong>Visual ETL:</strong> Used for visualizing the ETL pipeline and summarizing data.</li>
            </ul>
        </div>

        <div class="section">
            <h2>Deliverables</h2>
            <ul class="deliverables-list">
                <li><strong>Data Ingestion Pipeline:</strong> A fully functional pipeline for ingesting and storing 3-1-1 service request data in an Amazon S3 bucket.</li>
                <li><strong>Data Profiling Report:</strong> A detailed report generated by AWS Glue DataBrew, highlighting data quality issues and inconsistencies.</li>
                <li><strong>Cleaned Data Set:</strong> A cleaned and standardized dataset ready for analysis.</li>
                <li><strong>Data Catalog:</strong> A structured data catalog created using AWS Glue, enabling easy access and querying of the data.</li>
                <li><strong>Summarized Insights:</strong> Key insights derived from the data, including metrics such as the average number of calls offered and abandoned.</li>
            </ul>
        </div>
    </div>
</body>
</html>
