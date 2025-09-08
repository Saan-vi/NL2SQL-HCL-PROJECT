# NL2SQL-HCL-PROJECT

# Overview

This project is a Proof of Concept (POC) that allows users to query defect data stored in a database using natural language questions.
It demonstrates how LLMs (Gemini) can be integrated with a structured database to automatically generate and execute SQL queries.

The focus is on:

- Making database querying easy for end users without SQL knowledge.

- Enabling schema-aware SQL generation using few-shot examples.

- Providing a Streamlit-based UI for user interaction.

# Features

- Streamlit Web UI for natural language query input.

- Schema Extraction: Reads DB schema dynamically and displays it.

- SQL Generation: Uses Google Gemini LLM to generate SQL queries.

- Safe Execution: Only allows SELECT queries (blocked INSERT/UPDATE/DELETE).

- Results Display: Query results shown as tables or metrics (for COUNT/AVG/SUM).

- Dataset Preparation: Cleans raw defect dataset and loads into SQLite DB.

# Architecture

<img width="252" height="970" alt="Screenshot 2025-09-08 200320" src="https://github.com/user-attachments/assets/d569a340-7299-4dd8-bfb9-f5b252c2e001" />

# File Structure

├── app.py     # Streamlit frontend for user interaction

├── data_prep.py       # Cleans CSV and creates SQLite DB

├── db_exec.py         # Safe SQL execution logic

├── llm_sql.py         # LLM-based SQL generation

├── schema_utils.py    # Extracts schema info from DB

├── defects_data.csv   # Sample dataset

├── defects.db         # Generated SQLite DB

├── requirements.txt   # Python dependencies

└── README.md

# Future Enhancements

- Multi-table joins with schema grounding.

- Error correction loop using execution feedback.

- Multi-agent architecture for query generation, validation, and optimization.

- Support for enterprise-grade databases (PostgreSQL, MySQL, etc.).
