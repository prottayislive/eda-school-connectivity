### Report on Data Cleaning Process of School-Age Digital Connectivity Dataset

#### Overview
The data cleaning process was applied to the "School-Age-Digital-Connectivity-A1data.csv" dataset. The primary goal was to prepare the dataset for further analysis by addressing various data quality issues. The dataset contains information about the digital connectivity of children in school attendance age, with internet connection at home.

#### Data Cleaning Steps

1. **Initial Data Loading and Inspection**:
   - The dataset was loaded into a pandas DataFrame using `pd.read_csv`. 
   - Initial examination of the data was performed using `df.head()` to understand the structure and content.

2. **Whitespace Trimming**:
   - Whitespaces were stripped from column names and string values within the dataset. This step is crucial for consistency and to avoid errors during data manipulation caused by unnoticed trailing or leading spaces.

3. **Missing Values Analysis**:
   - Missing values in the dataset were identified using `df.isnull().sum()`. Addressing missing values is vital for ensuring the integrity of statistical analyses.

4. **Column Statistics Compilation**:
   - Each column's unique values and data types were analyzed to understand the data's diversity and structure. This step helps in identifying data inconsistencies and errors.

5. **Data Type Conversion**:
   - Percentage columns were converted from string to float types after stripping the '%' character. Accurate data type representation is crucial for numerical computations.

6. **Handling Missing Values**:
   - Missing values in specific columns were replaced with the respective column's median. This method is a standard practice for dealing with missing numeric data, as it preserves the overall distribution of the data.

7. **Conversion to Integer Types**:
   - After handling missing values, certain columns were converted to integers for consistency and ease of analysis.

8. **Duplicate Rows Removal**:
   - Duplicate rows were identified and removed. This step is essential to prevent skewed analysis results due to repeated entries.

9. **Typo Correction in 'Income Group' Column**:
   - A typo was corrected in the 'Income Group' column to ensure consistency in categorical data.

10. **Extraction and Conversion of 'Time period' Column**:
    - The 'Time period' column was extracted and converted to an integer type. This step ensures that time-related data is in a consistent and analyzable format.

11. **Removal of Rows with Impossible Time Periods**:
    - Rows with time periods beyond 2023 were removed as they are not possible and could represent data entry errors.

12. **Irrelevant Columns Removal**:
    - Columns not relevant to the analysis ('ISO3', 'Region', 'Sub-region', 'Data source', 'Time period') were dropped. Removing irrelevant data simplifies the dataset and focuses analysis on pertinent information.

13. **Final Dataset Description**:
    - A descriptive statistics summary of the cleaned dataset was obtained using `df.describe()` to provide an overview of the data's distribution post-cleanup.

14. **Saving the Cleaned Data**:
    - The cleaned dataset was saved to a new CSV file "cleaned_A1data.csv" for further analysis. This step is crucial for documenting the data cleaning process and providing a clean dataset for subsequent tasks.

