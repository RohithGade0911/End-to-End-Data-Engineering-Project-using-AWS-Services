# End-to-End Data Engineering Pipeline with AWS 🚀

## Project Overview 🌐

This project is an end-to-end data engineering pipeline aimed at processing and analyzing a comprehensive YouTube dataset from Kaggle. The dataset includes JSON and Excel files, which are categorized by regions including Canada, USA, India, and Russia. Our goal is to leverage AWS services to transform this raw data into actionable insights, providing advanced analytics and visualizations to uncover global content trends on YouTube.
## Dataset Description 📊

The "Trending YouTube Video Statistics" dataset on Kaggle (accessible [here](https://www.kaggle.com/datasets/datasnaek/youtube-new)) provides a detailed look into the videos listed in the trending category by YouTube for several regions. It includes:

- **Video Performance Metrics**: Views, likes, dislikes, comment count.
- **Content Details**: Video title, channel title, publish time, tags, descriptions.
- **Regional Data Files**: Separate JSON and CSV files for countries like Canada, the USA, India, and Russia, etc., allowing for region-specific trend analysis.

This dataset is instrumental in our project, as it serves as the foundational data upon which our data engineering pipeline operates.

## Data Architecture 🏛️

Our data architecture is crafted for scalability and adaptability, ensuring smooth data transformation at each stage:

- **Source Systems**: Bulk ingestion from Kaggle through S3 APIs to reliably and securely transfer YouTube datasets.
- **Data Lake**: A multi-tiered storage strategy in S3:
  - **Landing Area**: Staging area for the raw data.
  - **Cleansed/Enriched**: AWS Glue processes data for cleansing and enrichment.
  - **Analytics/Reporting**: S3 buckets for storing data ready for analysis and reporting.

- **Data Processing**: 
  - **AWS Glue Data Catalog**: Central metadata repository for data assets.
  - **AWS Lambda**: Automated data processing, including format conversion and preprocessing tasks.

- **Data Catalogue & Classification**: AWS Glue for organizing and classifying data to streamline discovery and analysis.

- **Analytical Data Access**:
  - **API**: Programmatically accesses data for analytical tool integration.
  - **AWS Athena**: Provides SQL-based analytics directly on S3-stored data.

- **Analytics**:
  - **QuickSight**: Visualization tool for creating interactive dashboards.

- **Monitoring/Alert**:
  - **AWS CloudWatch**: Monitors AWS services and triggers alerts for operational issues.

## Technical Architecture 🛠️

Our solution employs key AWS services for comprehensive dataset management and analysis:

- **Amazon S3**: Hosts both the raw and processed data.
- **AWS IAM**: Manages secure access across AWS services.
- **AWS Glue**: Data cataloging and ETL service.
- **AWS Lambda**: Automated code execution for data processing.
- **Amazon Athena**: SQL query engine for data analysis.
- **Amazon QuickSight**: Business intelligence and visualization.

## Detailed Workflow 📋

### Data Ingestion and Organization

- **S3 Bucket**: Stores the raw YouTube dataset, categorized by region.
- **IAM & AWS CLI**: Configured for secure and programmatic AWS service access.

### Data Processing

- **AWS Glue Crawler**: Catalogs datasets and manages metadata.
- **Data Preprocessing & ETL**: AWS Glue prepares data for analysis.

### Data Analysis and Visualization

- **Amazon Athena**: Analyzes data through SQL queries.
- **Amazon QuickSight**: Visualizes trends and metrics in an accessible format.

## Challenges and Solutions 🔍

- **Data Format and Schema Variations**: Custom ETL scripts in AWS Glue standardize data structures.
- **Automated Data Processing**: AWS Lambda triggers automate data processing workflows.
