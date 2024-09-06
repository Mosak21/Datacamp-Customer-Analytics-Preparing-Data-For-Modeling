# Training Data Ltd. - Student Job Change Prediction

## Overview

This project is focused on creating a more efficient storage solution for **Training Data Ltd.**, a major online data science training provider. The company aims to use its large customer dataset to predict whether students are seeking a new job based on anonymized information. This GitHub repository contains a **proof-of-concept** for efficiently storing and cleaning the provided dataset to improve model performance.

The dataset, `customer_train.csv`, includes various features about students and their job-seeking behavior. The goal is to clean and preprocess this dataset to ensure it can be efficiently used in predictive modeling.

## Dataset Information

The dataset contains the following columns:

| Column                   | Description                                                   |
|---------------------------|---------------------------------------------------------------|
| `student_id`              | A unique identifier for each student.                         |
| `city`                    | A code representing the student's city of residence.          |
| `city_development_index`  | A scaled index indicating the development level of the city.  |
| `gender`                  | The student's gender.                                         |
| `relevant_experience`     | An indicator of the student's relevant work experience.       |
| `enrolled_university`     | The type of university course enrolled in (if any).           |
| `education_level`         | The student's education level.                                |
| `major_discipline`        | The educational discipline of the student.                    |
| `experience`              | The student's total work experience (in years).               |
| `company_size`            | The number of employees at the student's current company.      |
| `company_type`            | The type of company employing the student.                    |
| `last_new_job`            | The years between the student's current and previous jobs.     |
| `training_hours`          | The number of hours of training completed.                    |
| `job_change`              | An indicator of whether the student is seeking a new job (1) or not (0). |

## Objective

The main objective is to **optimize storage** and **clean the dataset** to allow for efficient use in future predictive modeling. This work will support the company's broader aim of predicting student job changes and linking them with prospective recruiters.

## Key Tasks

1. **Data Cleaning**: 
   - Handle missing values
   - Normalize and standardize data where applicable
   - Ensure consistency in categorical variables (e.g., `gender`, `relevant_experience`)

2. **Storage Optimization**:
   - Use efficient data types to minimize storage space
   - Optimize data format for fast loading and processing

3. **Feature Engineering**:
   - Create new features from existing columns where appropriate
   - Ensure features are ready for machine learning models

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/student-job-change-prediction.git
   ```
2. Install the necessary Python packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

After installation, you can explore and preprocess the dataset using the provided Jupyter notebook (`data_preprocessing.ipynb`). Here's how to load the data and begin cleaning it:

```python
import pandas as pd

# Load dataset
df = pd.read_csv('data/customer_train.csv')

# Example of cleaning missing values
df.dropna(subset=['gender', 'major_discipline'], inplace=True)
```

## Conclusion

This project lays the groundwork for a scalable and efficient solution for **Training Data Ltd.'s** predictive modeling tasks. The preprocessing and storage optimization techniques will enable faster model training and deployment in production.

---

Feel free to contribute or provide feedback through pull requests or issue reports.
