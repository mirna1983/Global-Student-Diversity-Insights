# Academic Diversity Analysis

## Overview

Welcome to the "Global Student Diversity Insights" project repository. This project aims to analyze and understand trends related to student diversity on a global scale. The analysis encompasses various aspects, including academic details, field of study, origin, funding sources, and demographic information. The insights derived from this project aim to provide valuable information to educational institutions, policymakers, and researchers.

## Table of Contents

- [Installation Directions](#installation-directions)
- [Contributors](#contributors)
- [Methods Used](#methods-used)
- [Technologies](#technologies)
- [Project Introduction](#project-introduction)
- [Data Analysis](#data-analysis)
- [Hypothesis Testing](#hypothesis-testing)

## Installation Directions

1. **Download Datasets:**
   - Download the international-student-demographics datasets from Kaggle [here](https://www.kaggle.com/datasets/webdevbadger/international-student-demographics?select=academic.csv).
   - Ensure you have the following datasets: `academic_detail_modified.csv`, `academic_modified.csv`, `field_of_study_modified.csv`, `origin_modified.csv`, `source_of_fund_modified.csv`, and `status_modified.csv`.

2. **Create Database:**
   - In your SQL environment, create a database named `Global_Student_Diversity_Insights`.

```sql
-- Example SQL commands for creating the database
CREATE DATABASE Global_Student_Diversity_Insights;
USE Global_Student_Diversity_Insights;
```

3. **Load Datasets:**
   - Load the datasets into the database tables with corresponding names:

```bash
# Example commands for loading datasets into SQL tables
sqlcmd -S localhost -d Global_Student_Diversity_Insights -U your_username -P your_password -Q "BULK INSERT academic_detail_modified FROM 'academic_detail_modified.csv' WITH(FIELDTERMINATOR = ',', ROWTERMINATOR = '\n', FIRSTROW = 2)"
# Repeat for other tables
```

## Contributors

Contributors to the "Global Student Diversity Insights" project include Mirna Philip, Parisa Kamizi, and Arya Shahbaz.

## Methods Used

- Exploratory Data Analysis (EDA)
- Data Cleaning and Transformation
- Data Visualization
- SQL Queries

## Technologies

- VSCode
- PySQL
- Python via Jupyter Notebook

## Project Introduction

The goal of the "Global Student Diversity Insights" project is to analyze and understand trends related to student diversity on a global scale. The project encompasses various aspects, including academic details, field of study, origin, funding sources, and demographic information. The insights derived from this project aim to provide valuable information to educational institutions, policymakers, and researchers.

## Data Analysis

The data analysis process involves exploring, cleaning, and transforming the datasets.

## Hypothesis Testing

The hypothesis under investigation suggests a gradual increase in the representation of females in academic programs over the last decade. The `hypothesis_testing.ipynb` notebook details the methodologies used for testing this hypothesis.

## Deployment

### Manual Processes

If there are any manual processes involved in the deployment process, document them here:

- **Step 1: Clone the Repository**
  ```bash
  gh repo clone mirna1983/Global-Student-Diversity-Insights
  ```

- **Step 2: Update Project.ipynb**
  ```bash
  cd Global-Student-Diversity-Insights
  git add Project.ipynb
  git commit -m "Updated Project.ipynb with XYZ changes"
  ```

- **Step 3: Push Changes to GitHub**
  ```bash
  git push
  ```

### Infrastructure as Code (Optional)

If you want to set up infrastructure as code (IaC), refer to the `terraform` directory for the Terraform scripts. Adjust the variables in `main.tf` and run:

```bash
cd terraform
terraform init
terraform apply
```
