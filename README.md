# ETL Pipeline with Apache Airflow, Docker, and PostgreSQL

## Project Overview
This project demonstrates the implementation of an ETL (Extract, Transform, Load) pipeline. The pipeline leverages Apache Airflow for orchestration, Docker for containerization, and PostgreSQL as the target data warehouse. The data is extracted from a source, transformed using Python, and loaded into structured, unstructured, and hybrid storage systems.

## Features
- **Data Extraction**: Extract data from Amazon API and other sources.
- **Data Transformation**: Clean and format the data using Python and SQL.
- **Data Loading**: Load transformed data into PostgreSQL and other target storage systems.
- **Orchestration**: Use Apache Airflow to manage and automate pipeline tasks.
- **Containerization**: Employ Docker for seamless deployment and environment consistency.

## Architecture
### Workflow Diagram
![ETL Pipeline Workflow](./pipeline_design.png)

1. **Source**: Includes structured and unstructured data from Amazon and other APIs.
2. **ETL Pipeline**: Apache Airflow orchestrates the extraction, transformation, and loading process.
   - **Extract**: Pull data from source APIs or databases.
   - **Transform**: Perform data cleaning and processing using Python scripts.
   - **Load**: Store the transformed data into PostgreSQL or other storage systems.
3. **Target**: Data is stored in structured (SQL), unstructured (object storage), or hybrid formats.

## Technologies Used
- **Apache Airflow**: Task orchestration and workflow automation.
- **Docker**: Containerization for consistent and portable environments.
- **Python**: Data transformation and processing.
- **PostgreSQL**: Target data warehouse.
- **Amazon API**: Source for data extraction.

## Prerequisites
- Install Docker and Docker Compose.
- Install Apache Airflow.
- PostgreSQL instance (local or cloud-based).

## Setup and Installation
1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```
2. **Set Up Docker**:
   - Build and run Docker containers:
     ```bash
     docker-compose up --build
     ```
3. **Initialize Airflow**:
   - Start Airflow services:
     ```bash
     airflow db init
     airflow webserver -p 8080
     airflow scheduler
     ```
   - Access the Airflow UI at `http://localhost:8080`.

4. **Configure PostgreSQL**:
   - Update the `connection` settings in Airflow to point to your PostgreSQL database.

5. **Run the Pipeline**:
   - Create and trigger a DAG in the Airflow UI.

## How to Use
- **Start the Pipeline**: Navigate to the Airflow UI and trigger the DAG for the ETL pipeline.
- **Monitor Progress**: View task status and logs in the Airflow dashboard.
- **Access Results**: Query the PostgreSQL database to view the transformed and loaded data.

## Future Enhancements
- Add real-time data streaming capabilities.
- Integrate more data sources (e.g., social media, IoT).
- Implement advanced analytics and visualization tools.
