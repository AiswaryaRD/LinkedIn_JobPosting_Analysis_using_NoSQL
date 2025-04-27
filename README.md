# LinkedIn Job Posting Analysis using MongoDB (NoSQL)

## Academic Project:
Course        : DATA225
Group Number  : 8



## Project Overview

This project leverages MongoDB to analyze LinkedIn job posting data, identifying key job market insights such as trending skills, industries, salary ranges, and geographic demand. The project emphasizes NoSQL data modeling, query efficiency, and performance benchmarking.



## Project Objective

- Extract relevant job-related insights from LinkedIn data
- Implement a NoSQL schema using MongoDB with denormalized documents
- Enable filtering of job roles, compensation models, and industries
- Support dynamic querying and performance evaluation



## Dataset Information

- Job postings with metadata (title, description, skills, salary, work type)
- Companies with details (name, size, industry, address, specialties)
- Supporting data: skills, benefits, industries, employee counts

Collections were transformed from **8 raw collections** into:
- `job_postings`
- `companies`



## Data Cleaning

- Removed duplicates across all collections
- Dropped orphaned child records with no valid `job_id` or `company_id`
- Replaced 50+ non-existent company references with `NULL`



## Data Preprocessing

- Embedded `skills`, `benefits`, `industries` inside `job_postings`
- Embedded `specialities`, `industries`, `employee_counts` inside `companies`



## Data Transformation

- Denormalized schema for improved query performance
- Optimized data for aggregation-heavy workloads in MongoDB



## Tools / Technologies Used

- **MongoDB Atlas** (cloud-based NoSQL DB)
- **MongoDB Compass** (GUI + Explain plans)
- **Python** (data cleaning & query scripting)
- **Jupyter Notebooks** (analysis and exploration)
- **Visualization**: Plotly, Matplotlib, Choropleth maps



## Methodologies Used

- NoSQL schema modeling
- Document embedding
- Query optimization with `.explain()`
- Denormalization for read efficiency



## Queries Reference

All MongoDB queries used in this project can be found in the following file:

 **[Click here to view MongoDB Query Scripts](./mongosh_scripts/final_scripts)** 


## Visualizations

- Industry-wise job distribution (Donut chart)
- Location-based job frequency (Bar chart)
- Pay period vs max salary (Line chart)
- Top 10 skills in demand (Bar chart)
- Experience vs Work Type (Stacked chart)
- Country-wise opportunities (GeoMap)
- Top 20 company specialties (Word Cloud)


## Performance Insights

- MongoDB outperformed MySQL for large-scale aggregations
- Explain plan comparison via Compass showed lower execution time and IO cost
- Indexed queries were significantly faster with denormalized structure


## Folder Structure
LinkedIn_JobPostingAnalysis_NoSQL/
├── analysis/                # Notebooks and MongoDB queries
├── raw_data/                 # Original LinkedIn datasets (ignored)
├── staging_data/             # Cleaned intermediate datasets
├── visuals/                  # Visualizations and dashboards
├── README.md                 # Project overview documentation
├── .gitignore                # Git ignore rules

## Contributors:
Aiswarya Raghavadesikan  | Neha Thakur  | Saumya Varshney  | Shikha Singh  | Venkata Sai Sreelekha Gollu  


