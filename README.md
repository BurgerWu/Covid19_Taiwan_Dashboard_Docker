# Covid19_Taiwan_Dashboard_Docker
## Introduction
This is the docker-compose version of my previous projects: <a href='https://github.com/BurgerWu/airflow_covid19_tw'>airflow_covid19_tw</a> and <a href='https://github.com/BurgerWu/Covid19_Django_Webapp'>Covid19_Django_Webapp</a>.
Instead of making an online website, this project provides a solution to deploy the website in a easy way on any platform any machine as long as there is docker engine installed. This tutorial is based on Windows Docker desktop.

- **airflow_covid19_tw:**<br>
Apply apache airflow to collect and write covid19 data of Taiwan into local MYSQL database. The data includes cases , suspects and vaccination statistics.

- **Covid19_Django_Webapp:**<br>
Apply Django framework to demonstrate transformed covid19 Taiwan data from previous project. This project contains a one page webpage containing interactive Dash Plotly visualizations.

## Files and Directory
### Directories:
- **Covid19_Django_Webapp:** Contains files required for django website

- **airflow_covid19_tw:** Contains files required for Apache airflow system

### Files:
- **af_mysql.Dockerfile:** Dockerfile for mysql container image
- **airflow.Dockerfile:** Base image for apache airflow
- **cases.sql:** SQL script for initiating covid19 cases table
- **django.Dockerfile:** Dockerfile for Django framework
- **django_requirements.txt:** Requirements for Django environment
- **mysql_setting.sql:** A startup script for MYSQL initiation
- **source.sql:** SQL command line script for initiating MYSQL databases
- **suspects.sql:** SQL script for initiating covid19 suspects table
- **vacc.sql:** SQL script for initiating covid19 vaccination table

## How to deploy this project
- **Download this project via Github:**<br>
You may git clone this project or download zip file directly from Github

- **Have docker engine install on your machine:**<br>
Check out <a href='https://www.docker.com/products/docker-desktop/'>Docker official site </a> for more information.

- **Install docker-compose:**<br>
Check <a href='https://docs.docker.com/compose/install/'>here </a>for more information. If you already install docker desktop, docker-compose should come along with the installation.
This is the combination docker version of my previous project airflow_covid19_tw and Covid19_Django_Webapp.

- **Run docker-compose command**<br>
Direct your working directory or specify the full path to which this project was downloaded. Run the following command.<br>
```docker-compose -f path_to_docker_compose_yaml up ```

This will create required images according to yaml file specified and up the containers.

- **You may need to run previous command twice for unknown reason**<br>
For some unknown reason, the initiation of airflow container will fail for the first time, and you may need to run the same command again so that the docker system will be successfully up.

- ****<br>

- ****<br>

- ****<br>
