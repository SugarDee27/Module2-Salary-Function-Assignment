# Module 2 Assignment — Salary Function

## Overview
This Jupyter Notebook performs salary data processing, employee lookups, file export, and integration with R.  
It includes:
1. Data import from CSV.
2. Python function to search employee details.
3. Dictionary-based data processing for faster lookups.
4. Error handling for missing or invalid inputs.
5. Export of employee details to CSV inside a zipped folder.
6. R code to unzip the folder and display the CSV contents.

---

## Files
- `Salary_Function_Assignment.ipynb` — Main Jupyter Notebook containing all Python & R code.
- `Total.csv` — Salary dataset provided.
- `Employee_Profile.zip` — Generated zip file containing the employee’s profile.
- `README.md` — This instruction file.

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
