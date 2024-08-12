# Analytical Data Engineering Project
<img width="1114" alt="Screenshot 2024-08-12 at 8 09 20 PM" src="https://github.com/user-attachments/assets/ff53b4e7-3f9c-4443-adad-d70cb812c9e7">

## Step 1: AWS Lambda Function

1. download 'inventory.csv' from a public AWS S3 URL.
2. upload the 'inventory.csv' file to the Snowflake table.
3. create a schedule for every night 2 am (Riyadh time).

## Step 2: Airbyte Installation

1. Install Airbyte on EC2 instance.
2. Connect to the Postgres database in AWS RDS.
3. Create connections to data sources and set up replication pipelines.

## Step 3: Data Modeling

1. Create an analytics schema within the Snowflake database to hold the data model.
2. Develop an integrated customer dimension table from multiple related tables.

     ![customer dimension](https://github.com/user-attachments/assets/89af2874-b144-4dd4-ac8f-f156522625f8)

3. Design a weekly fact table containing sales and inventory metrics.
   
     ![SCD2](https://github.com/user-attachments/assets/d7b41307-36e8-4afa-8f90-f32966c2c7f3)

## Step 4: ETL and Data Loading

1. Implement merge scripts for integrating customer dimensions and daily sales records.
2. Create SQL queries for joining daily sales and updated inventory tables to generate the weekly sales and inventory fact table.
3. To realize the requirements from the Metabase BI purpose, we also need the Date_dim, Warehouse, and Item tables in the Prod schema.

> [!NOTE]
> More information is available within the presentation file.


## Step 5: Metabase

1. Install and configure Metabase for data visualization and report generation.
2. Connect Metabase to the Snowflake database.
3. Fix field names, and assign types to the columns to ensure proper visualization.
4. Generate reports based on business requirements using dashboards.


   
