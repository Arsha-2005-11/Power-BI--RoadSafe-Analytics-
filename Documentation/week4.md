# Road Safety Analytics Data Cleaning

This project focuses on cleaning and preparing **Road Safety Analytics Data** for analysis and visualization.

---

## 1. Overview

The dataset contains records of **road accidents**, including details such as:

- Accident type (Minor, Serious, Fatal)
- Road type (State Highway, National Highway, Urban Road, Village Road)
- Driver information (Age, Gender, Alcohol involvement)
- Weather and lighting conditions
- Date, time, and location of accidents

The raw data had several issues that needed cleaning before analysis.

---

## 2. Common Issues in the Raw Data

1. **Missing Values**
   - Some records had missing **driver age, gender, or alcohol involvement**.
   - Weather or road type sometimes missing.

2. **Duplicates**
   - Certain accident records were repeated.

3. **Inconsistent Formatting**
   - Dates in different formats (`DD/MM/YYYY` vs `YYYY-MM-DD`)
   - Road type and weather names had inconsistent spelling (`State Hwy` vs `State Highway`, `Rainy` vs `rain`)

4. **Incorrect Data Types**
   - Age stored as text
   - Accident date stored as string

5. **Outliers**
   - Driver age values like `-5` or `150` which are impossible

6. **Extra Spaces and Typos**
   - Fields like ` Male `, `female `, and `Unknown ` had trailing spaces.

---

## 3. Steps Taken to Clean the Data

1. **Handled Missing Values**
   - Filled missing **categorical values** with `"Unknown"`.
   - Filled missing **numerical values** (age) with median or removed if necessary.

2. **Removed Duplicates**
   - Identified repeated rows and removed them.

3. **Standardized Formats**
   - Converted all dates to `YYYY-MM-DD`.
   - Standardized road type, weather, and accident severity text.

4. **Corrected Errors and Typos**
   - Fixed inconsistent spellings and removed extra spaces.

5. **Handled Outliers**
   - Removed impossible driver ages (<0 or >120).

6. **Converted Data Types**
   - Age → integer
   - Date → datetime
   - Categorical columns → category type for analysis

7. **Validated Data**
   - Ensured all fields now have **logical and consistent values**.
   - Confirmed road types, accident severity, and weather categories are correct.

---

## 4. Outcome

After cleaning:

- Dataset is **consistent, complete, and ready for analysis**.
- Visualizations and analytics (like accident counts by road type, driver age, or alcohol involvement) can now be accurately generated.
- Enables better insights for **road safety policy and awareness**.

---

**Tip:** Always document the cleaning steps so the dataset remains **reproducible and trustworthy**.
