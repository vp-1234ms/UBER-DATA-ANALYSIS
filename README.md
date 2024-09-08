# Uber Data Analytics | Modern Data Engineering GCP Project

## Introduction

The goal of this project is to perform data analytics on Uber data using various tools and technologies, including GCP Storage, Python, Compute Instance, Mage Data Pipeline Tool, BigQuery, and Looker Studio.

## Architecture 
<img src="architecture.jpg">

## Technology Used
- Programming Language - Python

Google Cloud Platform
1. Google Storage
2. Compute Instance 
3. BigQuery
4. Looker Studio

Modern Data Pipeine Tool - https://www.mage.ai/

Contibute to this open source project - https://github.com/mage-ai/mage-ai


## Dataset Used
TLC Trip Record Data
Yellow and green taxi trip records include fields capturing pick-up and drop-off dates/times, pick-up and drop-off locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger counts. 

More info about dataset can be found here:
1. Website - https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
2. Data Dictionary - https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_yellow.pdf

## Data Model
<img src="data_model.jpeg">



# Uber Data Analysis with Mage-AI Flow::
## Overview
The project focuses on building an ETL (Extract, Transform, Load) pipeline using Mage-AI for Uber trip data. The pipeline extracts the data, applies transformations and modeling (fact and dimension tables), loads the data into Google BigQuery for analysis, and concludes with visualization using Looker Studio.

## 1. Setup and Installation
Environment Setup
Start by setting up a virtual environment using a tool like Anaconda or your system’s terminal.
Ensure that all the required libraries for data analysis (such as pandas, NumPy, and visualization tools) are installed. These libraries will help in handling, analyzing, and visualizing data.
Tool Installation
Install Mage-AI, which will be used to handle the ETL pipeline.
Set up access to Google Cloud services, particularly Google Cloud Storage and BigQuery, to store and analyze your data.
## 2. Data Extraction
Dataset Information
The dataset you are working with contains Uber trip records (e.g., pickup/dropoff locations, fare amount, trip distance, passenger count, etc.).
Before proceeding with extraction, review the data dictionary to understand the columns and the structure of the dataset. This helps in ensuring correct data mapping during analysis.
Loading the Dataset
The dataset is stored as a CSV file, which is typically large and may need to be hosted in a cloud environment for accessibility during processing. In this project, Google Cloud Storage is used for this purpose.
You will upload the dataset to Google Cloud Storage and make it publicly accessible so that it can be referenced during the extraction phase of the ETL process.
## 3. Data Transformation & Modeling
Creating Fact and Dimension Tables
After loading the dataset, you’ll move on to data transformation. This involves cleaning and reformatting the raw data.

Fact Tables: These tables contain quantitative data or metrics related to Uber trips, such as total fare, trip distance, and trip duration.

Dimension Tables: These tables contain descriptive or categorical information related to the entities involved, such as:

Customer Dimension: Passenger-related information.
Driver Dimension: Information about the Uber drivers.
Location Dimension: Pickup and drop-off locations.
Date Dimension: Trip dates and times.
Modeling the Data
You will use tools like Lucidchart or draw.io to create diagrams that illustrate the relationships between your fact and dimension tables.
By visualizing the data model, you can easily see how different pieces of data connect and interact with each other.
## 4. Data Loading
Google Cloud Storage
The cleaned and transformed data will be uploaded to Google Cloud Storage.

The purpose of storing the data here is to ensure that it can be easily accessed by Mage-AI and later loaded into Google BigQuery for further processing.

BigQuery for Data Storage
Google BigQuery is a data warehousing solution that will be used to store your transformed Uber data.
The fact and dimension tables that you’ve created will be uploaded into BigQuery, where you can perform SQL-based analysis.
## 5. Data Analysis in BigQuery
Exploring the Data
Once the data is in BigQuery, you can start querying it using SQL.
Typical analysis might include:
Calculating the average fare for trips.
Analyzing trip distance trends over time.
Finding correlations between different metrics (e.g., trip distance and fare amount).
Query Optimization
While working in BigQuery, you will need to ensure that your queries are optimized to handle the size of the dataset efficiently. Using proper indexing, partitioning, and selecting only necessary columns for analysis helps improve performance.
## 6. Data Visualization in Looker Studio
Dashboard Creation
After the data analysis in BigQuery, you’ll move to Looker Studio to create dashboards.

Looker Studio allows you to build visual representations of your analysis, making it easier to identify trends and insights. The dashboards can include:

Charts showing the number of rides per day, average fare, or trip distance trends.
Heatmaps showing Uber trip density across different locations and times.
Filters to allow dynamic changes, such as viewing data for specific months, locations, or drivers.
Integration with BigQuery
Looker Studio is directly integrated with BigQuery, so it can pull in real-time data and refresh your visualizations as the data changes.
## 7. Project Tools
Technologies Used
Jupyter Notebook: Used for initial setup, data manipulation, and analysis before loading the data into the pipeline.

Mage-AI: The primary tool for managing the ETL pipeline, handling extraction, transformation, and loading tasks.

Google Cloud Storage: Cloud storage for raw and transformed data.

Google BigQuery: Used for storing the cleaned data and running SQL queries for analysis.

Looker Studio: Visualization and reporting tool for creating dashboards and visual representations of data.

## 8. Project Workflow Summary
Data Extraction: Extract data from Uber dataset and load it into Google Cloud Storage.

Data Transformation: Create fact and dimension tables and transform the dataset for analysis.

Data Loading: Load transformed data into Google BigQuery.

Data Analysis: Perform SQL queries to extract insights from the data.

Data Visualization: Create interactive dashboards in Looker Studio using the analyzed data.

## Conclusion
This project shows how a combination of Mage-AI, Google Cloud services, and Looker Studio can be used to efficiently process, analyze, and visualize large datasets. The ETL process ensures the data is ready for in-depth analysis, while the tools used provide flexibility in scaling and visualization.
