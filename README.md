# Extract Transform Load using SSIS at Bank BTPN Syariah
This repository contains a ETL process using SQL Server Integration Service and scheduler for automation using Apache Airflow for Bank BTPN Syariah credit card customer. The project is designed to get a clean data that is consistent and reliable for analysis.

## Project Overview
This projects perform ETL process using SQL Server Integration Services start from extracting customer data from CSV flat file, then transform the data into clean data that is reliable for analysis and load this data into database and another CSV file to be used for analysis using Tableau.

## Tools and Technologies
- SQL Server Integration Service
- Apache Airflow
- Google Cloud Composer
- PostgreSQL
- Python
- Jupyter Notebook
- Pandas
- Tableau

## File Description
- `data_source/` : Folder containing raw data to be extracted.
- `data_destination/` : Folder containing clean data result of load process.
- `images/` : Folder containing images of data visualization, analysis result and logo of this project.
- `Rakamin_BTPN_Syariah.dtsx` : SQL Server Integration Service Package containing ETL process.
- `etl_btpns.py` : Airflow DAGs containing the code run SSIS package (dtsx) automatically based on the schedule.
- `Final_Project_BTPN_Syariah_Presentation.pptx` : Project Presentation
- `Final Task_Bank BTPN Syariah_Data Engineer_Gilang Wiradhyaksa.pdf` : Rakamin Final Project Task

## SQL Server Integration Service
### Data Flow Task
Data Flow Task for Customer History, transformation process for customer history table and load it into CSV flat file and Microsoft SQL Server Database.
![Data Flow Task](./images/01.png)

### SSIS Package
Multiple Data Flow Task are executed sequentially. Start from Customer History until Customer Status to transform and load data for all table.
![SSIS Package](./images/02.png)