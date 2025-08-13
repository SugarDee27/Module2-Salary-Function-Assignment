# Module 2 Assignment — Salary Function

## Overview
This Jupyter Notebook performs salary data processing, employee lookups, file export, and integration with R.  
It includes:
- Data import from CSV.
- Python function to search employee details.
- Dictionary-based data processing for faster lookups.
- Error handling for missing or invalid inputs.
- Export of employee details to CSV inside a zipped folder.
- R code to unzip the folder and display the CSV contents.

---

## Files
- **Salary_Function_Assignment.ipynb** — Main Jupyter Notebook containing all Python & R code.
- **Total.csv** — Salary dataset provided.
- **Employee_Profile.zip** — Generated zip file containing the employee’s profile.
- **README.md** — This instruction file.

---

## Requirements

### Python
- Python 3.x  
- pandas  
- rpy2 (for R integration in Jupyter)  
- zipfile (built-in)  
- csv (built-in)  

Install Python dependencies:
```bash
pip install pandas rpy2

## R
 - R installed on your system (Download here)
 - No extra R packages required for this assignment.

### How to Run
Open the Jupyter Notebook:

bash
Copy
Edit
jupyter notebook Salary_Function_Assignment.ipynb
Step 1: Import the salary dataset Total.csv (must be in the same folder as the notebook).

Step 2 & 3: Use:

python
Copy
Edit
get_employee_details_safe("EMPLOYEE NAME")
to search for an employee.

Step 5: Export an employee’s details to CSV and zip:

python
Copy
Edit
export_employee_profile("EMPLOYEE NAME")
This will create:

Employee Profile/EMPLOYEE_NAME.csv

Employee_Profile.zip

Step 6: Run the R cell in the notebook to unzip and display the data:

r
Copy
Edit
%%R
unzip("Employee_Profile.zip", exdir = "Unzipped_Employee_Profile")
employee_data <- read.csv("Unzipped_Employee_Profile/Employee Profile/EMPLOYEE_NAME.csv")
print(employee_data)
Notes
Replace "EMPLOYEE NAME" with the exact name from the dataset.

The R cell will only work if R and rpy2 are correctly installed and configured.

Keep Total.csv in the same directory as the notebook.
