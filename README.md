### Objective:
To create an azure data pipeline deployment architecture for the walmart sales data


![img1](https://github.com/bsathyamur/Walmart-Sales-Data---Deployment-Architecture/blob/main/architecture.png)


### Data pipeline design

1. Input files from external business applications will push the input files to the blob storage
2. The data pipeline configured in data factory will run on a daily basis and pick the files staged in the blob storage for data ingest
3. Once the data files are ingested, the same is processed and transformed via azure databricks
4. Then the processed data is stored in MS SQL server
5. The power BI will display the data to the front end business users

*** Deployment templates from azure resource group

ExportedTemplate-Microsoft.DataFactory-20210512165847
ExportedTemplate-Microsoft.SQLDatabase.newDatabaseNewServer_c61f8a26038d47beb0935
ExportedTemplate-walmartsalesacct_1620863517202
