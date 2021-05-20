### Objective:
To create an azure data pipeline deployment architecture for the walmart sales data


![img1](https://github.com/bsathyamur/Walmart-Sales-Data---Deployment-Architecture/blob/main/architecture.png)


### Data pipeline design

1. Input files from external business applications will push the input files to the blob storage
2. The data pipeline configured in data factory will run on a daily basis and pick the files staged in the blob storage for data ingest
3. Once the data files are ingested, the same is processed and transformed via azure databricks
4. Then the processed data is stored in MS SQL server
5. The power BI will display the data to the front end business users

### Azure Resource deployment templates

#### 1. ADF:
ExportedTemplate-Microsoft.DataFactory-20210512165847

#### 2. MS SQL Server database
ExportedTemplate-Microsoft.SQLDatabase.newDatabaseNewServer_c61f8a26038d47beb0935

#### 3. Azure Storage account
ExportedTemplate-walmartsalesacct_1620863517202

### Unit testing

The unit_testing is performed using pytest. Below is the unit testing metrics:
1. Total test cases: 12
2. Total passed: 12
3. Total failed: 0

Below are the test cases performed:
1. Verify the NA column is replaced with Guest value for Customer ID field (2 test cases)
2. Verify the NA is replaced with Unlisted value for description field (2 test cases)
3. Verify the new column Quarter is populated as expected (2 test cases)
4. Verify the new column InvoiceType is populated as expected with Purchase and return (3 test cases)
5. Verify the dataframe is split based on country - United Kingdom vs. Others (3 test cases)

### Process followed to convert from test code to final code

![img2](https://github.com/bsathyamur/WalmartSalesData-Deployment-Architecture/blob/main/flow.png)

### Final code is available in the main branch in the below repo

https://github.com/bsathyamur/WalmartSales-DataFactory
https://github.com/bsathyamur/walmartSales-Databricks

### Monitoring Dashboard

![img1](https://github.com/bsathyamur/WalmartSalesData-Deployment-Architecture/blob/main/walmartSales-MonitorDashboard.png)
