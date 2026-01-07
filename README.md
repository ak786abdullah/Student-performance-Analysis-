# Student Performance Analysis & Grading Automation

##  Project Overview
This project is a data analysis workflow built with Python to process raw student exam scores. It automates the data cleaning process, calculates performance metrics (percentages and grades), and generates statistical insights into student performance across different grade levels.

##  Files Description
* **`Student_Performance_EDA.ipynb`**: The main Jupyter Notebook containing the Python code for data loading, cleaning, feature engineering, and analysis.
* **`student_exam_scores.csv`**: The raw dataset containing original student records (Name, Class, Total Marks, Obtained Marks).
* **`cleaned_student_performance.csv`**: The processed output file containing cleaned data with added `Percentage` and `Grade` columns.

##  Tech Stack
* **Python**
* **Pandas** (Data manipulation and analysis)
* **Matplotlib** (Data visualization)

##  Data Processing Workflow

### 1. Data Cleaning
The raw dataset (`student_exam_scores.csv`) initially contained **2,050** records. The cleaning process involved:
* **Handling Missing Values:** Identified and removed rows with missing `Name` values (17 records).
* **Removing Duplicates:** Detected and dropped duplicate entries (52 records).
* **Final Data Shape:** The dataset was reduced to **1,983** clean records for accurate analysis.

### 2. Feature Engineering
Two new columns were generated to standardize performance metrics:
* **Percentage:** Calculated as `(Obtained_Marks / Total_Marks) * 100`.
* **Grade:** Assigned based on the following custom threshold logic:
    * **A**: Percentage ≥ 80%
    * **B+**: 75% ≤ Percentage < 80%
    * **B**: 70% ≤ Percentage < 75%
    * **C+**: 65% ≤ Percentage < 70%
    * **C**: 60% ≤ Percentage < 65%
    * **Fail**: Percentage < 60%

## Key Insights
* **Overall Performance:** The average percentage across all students is **73.2%**.
* **Top Performing Class:** The **8th Grade** achieved the highest average performance (**74.1%**).
* **Grade Distribution:** The majority of students achieved an **'A'** grade (1,063 students), while **527** students fell into the 'Fail' category, highlighting areas for potential academic intervention.

##  How to Run
1.  Ensure you have Python and the required libraries installed:
    ```bash
    pip install pandas matplotlib
    ```
2.  Place the `student_exam_scores.csv` file in the same directory as the notebook.
3.  Open and run `Student_Performance_EDA.ipynb`.
4.  The script will generate the cleaned dataset: `cleaned_student_performance.csv`.

## 📜 License
This project is open-source and available for educational purposes.

