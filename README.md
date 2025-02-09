# NYC_Taxi_Azure_DE_Project

##  **Project Overview**

1. **Ingestion**: Collect raw data from NYC Taxi and Limousine Commission (TLC) for Green Taxis and store it. (Tool used - ADF)
2. **Transformation**: Clean, process, and transform the data. (Tool used - ADB)
3. **Serving**: Save the transformed data in a serving layer for further analysis and use the data in Reporting Layer. (Tool used - Azure Delta Lake)

## **Architecture**

1. **Source Data**
   
   - **API LINK** https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
   - **Sample File Link** https://d37ci6vzurychx.cloudfront.net/trip-data/green_tripdata_2023-01.parquet
     
3. **Ingestion Layer** 

   - Ingested the raw data into **Azure Data Lake Gen2**.
   - Stored the data in **Parquet format** for efficient storage and processing.

4. **Transformation Layer** 

   - Used **Azure Databricks** to clean and transform the data.
   - Converted the raw data into a meaningful format using Spark and saved it back to **Azure Data Lake Gen2**.

5. **Serving Layer** 

   - The cleaned, transformed data was saved as a **Delta Table** in the serving layer for analytics and reporting.

6. **Security** 

   - Secured access to all Azure services using **Azure Active Directory** and role-based access control (RBAC).
  

  ## **Technologies Used**

| **Tool/Service**           | **Purpose**                                       |
| -------------------------- | ------------------------------------------------- |
| **Azure Data Factory**     | Ingesting data from APIs.                         |
| **Azure Data Lake Gen2**   | Storage for raw, transformed, and served data.    |
| **Databricks**             | Processing and transforming the data using Spark. |
| **Parquet**                | Storage format for raw and transformed data.      |
| **Delta Lake**             | Optimized format for serving clean data.          |
| **Azure Active Directory** | Security and access management.                   |


## **Folder Structure**

Here’s how I organized my data in **Azure Data Lake Gen2**:

```
DataLakeGen2/
│
├── bronze/          <- Raw data in Parquet format
│
├── silver/          <- Cleaned and transformed data
│
└── gold/            <- Final Delta Tables for analytics
```

## **How to Run the Project**

Follow these steps to run the project:

1. **Set up Azure Resources**:

   - Create Azure Data Lake Gen2, Azure Databricks, and Azure Data Factory.

2. **Ingest Data**:

   - Use **Azure Data Factory** to collect data and store it in **Data Lake Gen2**.

3. **Transform Data**:

   - Use Databricks to clean and transform the data.

4. **Store Data**:

   - Write the transformed data as Delta Tables to the serving layer.

5. **Analyze the Data**:

   - Query the Delta Tables for reporting and insights.
  

## **Conclusion**

This project shows how you can build an end-to-end data engineering solution using **Azure tools**. It covers everything from **ingesting data** to **transforming** it and saving it securely for analysis.

## **Next Steps**

- Add more transformations in Databricks.
- Use **Power BI** or **Synapse Analytics** to visualize the data.
- Automate pipelines further using triggers.
