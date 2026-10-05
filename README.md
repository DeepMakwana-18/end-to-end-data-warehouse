# Data Warehouse and Analytics Project

This project demonstrates an end-to-end data warehousing and analytics solution built with SQL Server. It covers data ingestion, transformation, dimensional modeling, data quality validation, and analytical reporting using ERP and CRM source data.

## Data Architecture

The warehouse follows the **Medallion Architecture**, with separate Bronze, Silver, and Gold layers:

See the [High Level Architecture diagram](docs/High%20Level%20Architecture.drawio) for the project architecture.

1. **Bronze Layer**: Stores raw data loaded from the source CSV files.
2. **Silver Layer**: Cleans, standardizes, and integrates data from the ERP and CRM systems.
3. **Gold Layer**: Provides business-ready dimensional models for reporting and analytics.

## Project Overview

The project includes:

- Designing a modern data warehouse using SQL Server
- Loading ERP and CRM data through SQL-based ETL procedures
- Cleaning and standardizing source data
- Building fact and dimension tables for analytical queries
- Creating data quality checks for the Silver and Gold layers
- Documenting the data flow, architecture, and data model

This repository is intended to demonstrate practical skills in:

- SQL development
- Data engineering and ETL pipelines
- Dimensional data modeling
- Data quality and validation
- Data analytics and reporting

## Tools and Technologies

- **SQL Server** for database storage and transformation
- **SQL Server Management Studio (SSMS)** for database development
- **Draw.io** for architecture, data flow, and data model diagrams
- **CSV files** as the source-system datasets

## Project Structure

```text
Data Warehouse Project/
├── datasets/                      # ERP and CRM source CSV files
├── docs/                          # Architecture, flow, model, and catalog documentation
│   ├── data_catalog.md
│   ├── Data Flow.drawio
│   ├── DATA INTEGRATION.drawio
│   ├── data model.drawio
│   └── High Level Architecture.drawio
├── scripts/                       # Database initialization and warehouse scripts
│   ├── init_database.sql
│   ├── bronze/
│   │   ├── ddl_bronze.sql
│   │   └── proc_load_bronze.sql
│   ├── silver/
│   │   ├── ddl_silver.sql
│   │   └── proc_load_silver.sql
│   └── gold/
│       └── ddl_gold.sql
├── tests/                         # Data quality validation scripts
│   ├── quality_checks_silver.sql
│   └── quality_checks_gold.sql
├── LICENSE
└── README.md
```

## Getting Started

1. Install SQL Server Express and SQL Server Management Studio.
2. Create the project database by running `scripts/init_database.sql`.
3. Create the Bronze, Silver, and Gold schemas and tables using the DDL scripts in `scripts/`.
4. Update the source file paths in the Bronze loading procedure for your local environment.
5. Run the Bronze load procedure to import the CSV files.
6. Run the Silver load procedure to clean and integrate the data.
7. Create the Gold-layer objects and run the quality checks in `tests/`.

## Project Requirements

### Data Engineering

- Import data from the provided ERP and CRM CSV files.
- Resolve data quality issues before analytical use.
- Integrate both source systems into a consistent warehouse model.
- Focus on the latest available dataset; historization is outside the current scope.
- Maintain clear documentation for business and analytics users.

### Analytics and Reporting

The warehouse supports analysis of:

- Customer behavior
- Product performance
- Sales trends

## About Me

Hi, I’m **Deep Makwana**, an aspiring data engineer passionate about building reliable data pipelines, scalable data warehouses, and useful analytical solutions.

This project is part of my learning portfolio and reflects my hands-on practice with SQL Server, ETL development, data modeling, and data quality engineering.

## License

This project is licensed under the [MIT License](LICENSE).
