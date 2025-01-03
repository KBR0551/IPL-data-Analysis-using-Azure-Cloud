# IPL-data-Analysis-using-Azure-Cloud
In this repo I have utilized Azure Cloud services to Ingest, process & store IPL dataset. I will be developing IPL statistics wich will look like reports/stats @ https://www.iplt20.com/stats/2008 from year 2008 to 2017. <br />

Data is available in https://github.com/KBR0551/IPL-data-Analysis-using-Databricks-SQL/tree/main/data repo. <br />

**Azure Cloud resouces used:** <br /> <br />
*ADLS GEN2:* Store layer (/bronze, silver, gold) <br />
*Data Factory:* To ingest Raw data from external azure environment, and for building and orchestration data pipeline. <br />
*Databricks:* To do Data Processing, SQL analystics and Dashboard. <br />
*Key Vault:* To store secrets and keys for secure access <br />

Below is the steup of the enviroment on Azure and resurces used. <br />

There are few steps in establishing connections, access between services inside Azure environment, which are documented in Azure documentation. <br />

## Azure cloud environment visualization 
<img width="819" alt="Screenshot 2024-12-08 at 2 38 01 PM" src="https://github.com/user-attachments/assets/11338cf0-d5c5-47f6-a927-9bb85341971d"> <br />

**Primary Resources in Resource group**
<img width="1189" alt="Screenshot 2024-12-08 at 5 21 46 PM" src="https://github.com/user-attachments/assets/060b1fe9-a753-486d-9632-6a7116b17f03">


## Data Model
![image](https://github.com/user-attachments/assets/20434fe9-dae7-4aa8-912a-7f7ca96cfa6f)

## Data Factory Pipeline orchestration
<img width="949" alt="Screenshot 2024-12-06 at 6 12 30 PM" src="https://github.com/user-attachments/assets/5fa9e908-89c2-47d1-9b44-3f423ced9022">

## Databricks Data Catalouge
Datasets(*external delta tables*) are registered in azure databrciks data catalog for quring in *Databricks SQL Editor* and creating dashboards within the databrciks workspace in Azure cloud. <br />

  **ipl_data:** Enhanced datasets in adls gen2 silver zone <br />
  **ipl_batting_stats:** Aggregated batting reports calculated and stored in adls gen2 gold zone <br />
  **ipl_bowling_stats:** Aggregated bowling reports calculated and stored in adls gen2 gold zone <br />
  
<img width="485" alt="Screenshot 2024-12-08 at 3 10 57 PM" src="https://github.com/user-attachments/assets/8321ecd1-a77b-4afc-b636-4d51f513c4a4"> 

<img width="344" alt="Screenshot 2024-12-08 at 3 59 09 PM" src="https://github.com/user-attachments/assets/ca68b362-286f-47de-b5d3-4282870e0310"> <img width="356" alt="Screenshot 2024-12-08 at 4 00 12 PM" src="https://github.com/user-attachments/assets/04953eb7-6b28-49a2-b1a0-2eb0cc346a87"> <br />

## SQL analytics using Databrciks SQL editor
<img width="1268" alt="Screenshot 2024-12-08 at 4 57 41 PM" src="https://github.com/user-attachments/assets/4365961f-7b16-4752-b946-33965b37ad6f">

 
## Building Dashboards 
<img width="1214" alt="Screenshot 2024-12-08 at 4 14 23 PM" src="https://github.com/user-attachments/assets/ed405e2b-7614-46f6-817d-abfc9fb5d0bd">
