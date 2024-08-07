# postgres-airflow-snowflake-dbt-looker
Project End to End
# Project End to End: PostgreSQL, Dockerm Airflow, AWS, Snowflake, DBT, Looker Studio

![alt text](image.png)

## Requirements
- AWS, Snowflake, DBT Cloud, and Looker Studio accounts
- Basic knowledge of SSH keys
- Implementation and configuration of EC2 instances
- Knowledge of Python, SQL, and Airflow
  

## Project
The objective of this project was to create a complete pipeline for extracting, transforming, and loading data incrementally, as well as a data visualization dashboard. The following technologies were used: PostgreSQL, Docker, Airflow, AWS, Snowflake, dbt, and Looker Studio.

## Development
Airflow was implemented on an EC2 instance in AWS. Generally, a DAG with two tasks, "get_max_id" and "load_incremental_data", was created to perform the incremental load process considering the highest unique key. Additionally, the connection to the read-only (RO) instance of the PostgreSQL database and Snowflake was configured.

DBT was used to perform data transformations in the data warehouse and to apply simple business rule tests. Configuring the connection to Snowflake was necessary for this step.

Finally, Looker Studio was integrated and configured with Snowflake, and a dashboard was created in the tool to visualize the data.

