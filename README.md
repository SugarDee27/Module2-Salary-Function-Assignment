# Module 2 Assignment — Salary Function

## Overview
This project processes employee salary data, performs lookups, handles errors, exports data to CSV, and integrates with R for further processing.  

The workflow includes:
1. Importing salary data from CSV.
2. Creating a Python function to search employee details.
3. Processing data with a dictionary for faster lookups.
4. Implementing error handling for invalid or missing inputs.
5. Exporting employee details to CSV inside a zipped folder.
6. Using R to unzip the folder and display the CSV contents.

---

## Files in This Project
- **`Salary_Function_Assignment.ipynb`** — Main Jupyter Notebook (Python + R code).
- **`Total.csv`** — Provided salary dataset. Please note: Total.csv is provided in a compressed format due to its large size (over  GitHub’s 25 MB upload limit). Extract the CSV file and place it in the same directory as the other project files before running the notebook.
- **`Employee_Profile.zip`** — Example zipped output of an employee profile.
- **`README.md`** — Instructions for setup and usage.

---

## 🛠 Requirements

### **Python**
- Python 3.x  
- Required libraries:
  ```bash
  pip install pandas rpy2
  ```
- Built-in modules: `os`, `csv`, `zipfile`

### **R**
- [Install R](https://cran.r-project.org/) on your system.
- No extra R packages are required.

---

## How to Run

### Open the Notebook
In your terminal:
```bash
jupyter notebook Salary_Function_Assignment.ipynb
```

### Step-by-Step in the Notebook
- **Step 1:** Import `Total.csv`  
  Make sure `Total.csv` is in the same directory as the notebook.  
- **Step 2 & 3:** Search for an employee:
  ```python
  get_employee_details_safe("EMPLOYEE NAME")
  ```
- **Step 5:** Export an employee profile:
  ```python
  export_employee_profile("EMPLOYEE NAME")
  ```
  This creates:
  - `Employee Profile/EMPLOYEE_NAME.csv`
  - `Employee_Profile.zip`

### Step 6 — R Code in Jupyter
Run the following in an R cell:
```R
%%R
unzip("Employee_Profile.zip", exdir = "Unzipped_Employee_Profile")
employee_data <- read.csv("Unzipped_Employee_Profile/Employee Profile/EMPLOYEE_NAME.csv")
print(employee_data)
```

---

## 📝 Notes
- Replace `"EMPLOYEE NAME"` with an exact match from the dataset.
- Ensure R is installed and `rpy2` is configured before running R cells in Jupyter.
- Keep all files in the same directory for smooth execution.

---
