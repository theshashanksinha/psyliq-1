# Diabetes Prediction Project

## Project Overview

The Diabetes Prediction Project aims to analyze a comprehensive dataset of diabetic patients using MySQL to derive insightful information about their health metrics. The dataset includes various attributes such as patient identifiers, smoking status, HbA1c levels, blood pressure, BMI, and blood glucose levels. This project addresses specific queries and suggests database improvements for better performance and data integrity.

## Project Details

### Data Cleaning
- Standardized the patient date of birth (D.O.B) format.
- Corrected date formatting issues such as invalid dates (e.g., "29-02-1995").

### File Conversion
- Converted the original dataset to CSV format for better compatibility with SQL.

### Table Creation
- Created a SQL table named `employee` with the following schema:
  ```sql
  CREATE TABLE `diabetes`.`employee` (
      `EmployeeName` VARCHAR(45) NOT NULL,
      `Patient_id` VARCHAR(45) NOT NULL,
      `gender` VARCHAR(45) NOT NULL,
      `D.O.B` DATE NOT NULL,
      `hypertension` INT(5) NOT NULL,
      `heart_disease` INT(5) NOT NULL,
      `smoking_history` VARCHAR(45) NOT NULL,
      `bmi` DOUBLE NOT NULL,
      `HbA1c_level` DOUBLE NOT NULL,
      `blood_glucose_level` INT(5) NOT NULL,
      `diabetes` INT(5) NOT NULL,
      PRIMARY KEY (`Patient_id`)
  ) COMMENT = 'Employee Health Data';

### Data Import
- Imported the dataset from Excel into the SQL database using the Table Data Import Wizard.
- Verified the total number of entries in the employee table (100,000 entries).

### SQL Queries
1. Retrieve the Patient_id and ages of all patients.
2. Select all female patients who are older than 30.
3. Calculate the average BMI of patients.
4. List patients in descending order of blood glucose levels.
5. Find patients who have hypertension and diabetes.
6. Determine the number of patients with heart disease.
7. Group patients by smoking history and count smokers and non-smokers.
8. Retrieve the Patient_id of patients with a BMI greater than the average BMI.
9. Find the patient with the highest and lowest HbA1c levels.
10. Calculate the age of patients.
11. Rank patients by blood glucose level within each gender group.
12. Update the smoking history of patients older than 40 to "Ex-smoker."
13. Insert a new patient into the database.
14. Delete all patients with heart disease from the database.
15. Find patients who have hypertension but not diabetes using the EXCEPT operator.
16. Define a unique constraint on the "patient_id" column.
