# cmsc408-sp2025-hw8 ## Homework 8 - World Bank Indicator Analysis

### Project Overview

This repository contains the work for Homework 8, focusing on analyzing World Development Indicator (WDI) data from the World Bank using SQL queries within a Quarto document. The project involves connecting to a database containing WDI country information, performing various data exploration and analysis tasks, and presenting the results in a structured report.

### Purpose

The primary goals of this project are to:

1.  Practice connecting to and querying a relational database using Python and SQLAlchemy.
2.  Explore and analyze real-world data (WDI country indicators).
3.  Reinforce SQL skills, including filtering, aggregation, grouping, joins, subqueries, and Common Table Expressions (CTEs).
4.  Generate a reproducible report documenting the analysis process and findings using Quarto.

### Features

* **Database Connection:** Securely connects to a MySQL database using environment variables (`.env` file).
* **Data Cleaning/Preparation:** Creates a working copy of the country data, filtering out non-country aggregates.
* **Data Exploration:** Uses SQL queries to investigate table structures, unique values, and data distributions (e.g., countries per region, income group counts).
* **Data Analysis:** Employs various SQL techniques (joins, subqueries, CTEs, CASE statements) to answer specific analytical questions about country classifications and relationships.
* **Report Generation:** Uses Quarto to combine narrative text, code, and query results into a publishable HTML report.

### Technologies Used

* **MySQL:** Database system used to store and query the WDI data.
* **Python:** Scripting language used within Quarto for database interaction.
* **SQLAlchemy:** Python library for database abstraction and connection.
* **PyMySQL:** MySQL database driver for SQLAlchemy.
* **Pandas:** Used by helper functions for handling query results as DataFrames.
* **python-dotenv:** For loading database credentials from the `.env` file.
* **Quarto:** System for creating the final reproducible report.

### Database Structure

* **Source Data:** The analysis primarily uses the `world_bank_data.wdi_country` table provided in the database.
* **Working Table:** A temporary table named `wdi_country` is created within the user's schema during the report execution to hold only country-specific records for analysis.

### Getting Started

1.  **Clone Repository:** Clone this repository to your local machine.
2.  **Setup Environment:** Ensure you have Python and Poetry installed. Navigate to the repository directory in your terminal and run `poetry install` to install dependencies. Activate the virtual environment using `poetry shell`.
3.  **Configure Database:** Create a `.env` file in the root directory and add the necessary key-value pairs for your HW8 database connection (`CMSC408_HW8_USER`, `CMSC408_HW8_PASSWORD`, `CMSC408_HW8_HOST`, `CMSC408_HW8_DB_NAME`).
4.  **Render Report:** Run `quarto render reports/report.qmd` from the root directory to execute the analysis and generate the HTML report.

### Setup Instructions

Detailed instructions for setting up the Python environment, database connections, and necessary tools are available at: [VCU SSG Quarto Python Setup](https://github.com/cmsc-vcu/cmsc-vcu-ssg-templates/blob/main/quarto-scaffolds/python/setup/SETUP_PYTHON.md) (or provide the specific link used in your course).

### Project Structure

├── .env                  # Environment variables for database connection (Create this file)├── .gitignore            # Git ignore file├── README.md             # This file: Project documentation└── reports/├── helpers.py        # Python helper functions for DB interaction└── report.qmd        # Quarto document containing the analysis and report
### Requirements

* Python 3.8+
* Access credentials for the specified MySQL database (CMSC408_HW8)
* Quarto publishing system
* Required Python packages (installed via `poetry install`):
    * `pandas`
    * `SQLAlchemy`
    * `PyMySQL`
    * `python-dotenv`
    * `tabulate` (if used by helpers)
