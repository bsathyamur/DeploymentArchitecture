### Objective: To create an azure data pipeline deployment architecture for the walmart sales data 

![img1](https://github.com/bsathyamur/DeploymentArchitecture/blob/main/pipeline%20orchestration.png)


### The architecture consists of two data pipelines. The data will get received as input files and stored in blob container in azure. The data pipeline will be orchestrated in azure data factory. First the raw input files will get retrieved from the blob container and processed via a HDInsight spark activity and transformed and stored in a output folder in the blob container. Then another pipeline will get invoked which will perform the ETL load to the azure SQL Server DW.


