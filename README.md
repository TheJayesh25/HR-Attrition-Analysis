# HR Attrition Analysis: Uncovering Key Insights for Employee Retention 📊

## 🔍 Project Overview

This repository contains a comprehensive analysis of HR attrition within an organization, leveraging survey data to identify key factors influencing employee turnover. The goal of this project is to provide actionable insights that can help the organization improve employee retention strategies.

The analysis delves into various demographic and satisfaction-related aspects of employees, including age, gender, department, job role, education, work-life balance, job satisfaction, environment satisfaction, and more. By understanding these correlations, the organization can proactively address potential issues and foster a more engaging and supportive work environment.

## 💾 Data Source

The analysis is based on the `HR DATA` Excel file, which includes:

* Demographic information (age, gender, education, etc.)
* Job-related details (job role, department, wages, performance rating, work hours, training time, etc.)
* Employee survey data on job satisfaction, relationship satisfaction, environment satisfaction, work-life balance, etc.

## 🛠️ Tools Used

* **PostgreSQL:** For efficient data storage, cleaning, transformation, and in-depth analysis using SQL queries.
* **Tableau:** For creating insightful and visually appealing dashboards and reports to communicate the findings (visualizations not included in this repository).

## ⚙️ Setup and Execution

1.  **Database Setup:** Ensure you have a PostgreSQL database set up.
2.  **Load Data:** Import the `HR DATA` Excel file into a PostgreSQL table named `hr_data`.
3.  **Connect via Jupyter Notebook:** The provided Jupyter Notebook (`hr_attrition_analysis.ipynb`) contains the SQL queries and analysis steps. Update the database connection details within the notebook:

    ```python
    %load_ext sql
    import os
    host = "localhost"
    database = "hr_attrition"
    user = 'your_user_name'  # Replace with your PostgreSQL username
    password = 'your_password'  # Replace with your PostgreSQL password
    connection_string = f"postgresql://{user}:{password}@{host}/{database}"
    %sql $connection_string
    ```

4.  **Run the Notebook:** Execute the cells in the Jupyter Notebook sequentially to perform the data cleaning, transformation, and analysis.

## 📊 Key Findings

The analysis reveals several significant factors associated with employee attrition:

* **Overall Attrition Rate:** The organization experienced an attrition rate of **16.12%**.
* **Departmental Insights:** While the **R&D** department had the highest number of departing employees, the **Sales (20.63%)** and **HR (19.05%)** departments exhibited higher attrition rates.
* **Job Role Impact:** The **Laboratory Technician** role had the highest attrition count.
* **Age Demographics:** Employees in the **25-34 age group** contributed the most to attrition.
* **Satisfaction Matters:** A clear inverse relationship was observed between attrition rates and employee satisfaction levels:
    * Lower **environment satisfaction** scores strongly correlated with higher attrition.
    * Lower **job satisfaction** scores were also linked to increased employee turnover.
* **Engagement is Crucial:** Employees with **very low job involvement** had a significantly higher attrition rate (33.73%).
* **Work-Life Balance:** Employees reporting a **poor work-life balance** (score of 1) showed the highest likelihood of leaving (31.25%).
* **Other Factors:** No clear trends were identified based solely on the distance from home. Employees who **travel rarely** had a higher attrition count compared to frequent travelers.

## 💡 Key Takeaways and Recommendations

The analysis strongly suggests that focusing on improving employee satisfaction (both job and environment), fostering greater job involvement, and promoting better work-life balance are critical for reducing attrition. Further investigation into the specific drivers of dissatisfaction and low involvement within different departments and job roles is recommended.

## 🚀 Future Enhancements

* Incorporate the Tableau visualizations into the repository for a complete picture.
* Perform more advanced statistical analysis to identify the most significant predictors of attrition.
* Develop predictive models to forecast potential attrition risks.
* Analyze qualitative data (e.g., exit interviews) to gain deeper insights into the reasons for leaving.
* Track the impact of implemented retention strategies over time.

## ✍️ Author

[Jayesh Suryawanshi](https://github.com/TheJayesh25)

#### I have created a dashboard in tableau to view these findings at a glance and filter them out based on different data points.  
#### I have attached an image of the dashboard below OR you can click here to view the Dashboard: [HR Attrition Analysis dashboard](https://public.tableau.com/app/profile/jayesh25/viz/HRAttritionAnalysis_16866548755520/Dashboard1)  



![Dashboard](images/Dashboard.png)
