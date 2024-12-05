# File Guide for [rfandozzi-dynamic-systems-modeling]

This document provides an overview of the files in the `[rfandozzi-dynamic-systems-modeling]` branch.

---

## Files and Descriptions

### **1. [COVIDbyCounty (1).mat]**
- **Description:** There are 3 key arrays in the file:
1. **CNTY_COVID**  
   - An `m × n` matrix, where `m` is the number of counties and `n` is the number of dates.  
   - Each entry represents the new COVID-19 cases in a county per week, normalized by 100k population.

2. **CNTY_CENSUS**  
   - A table with `m` rows corresponding to counties in the `CNTY_COVID` matrix.  
   - Columns provide summary census data, including:
     - FIPS code
     - Division code
     - Division name
     - State name
     - County name
     - Estimated population (2021).

3. **dates**  
   - A `1 × n` vector containing dates that correspond to the columns in the `CNTY_COVID` matrix.
- **Usage:** 
- Load this file in MATLAB using:
  ```matlab
  load('COVIDbyCounty (1).mat');


---

### **2. [another_file.m]**
- **Description:** Briefly describe the purpose of this file.
- **Usage:** How to run or use this file.
- **Dependencies:** List any required files or libraries.

---

### **3. [writeup.pdf]**
- **Description:** Detailed writeup for the project. Explains the objectives, methods, and results.
- **Format:** PDF
- **Location:** [Link to file, if applicable]

---

## How to Run
1. Open MATLAB and navigate to the folder containing these files.
2. Run the main script (e.g., `main_file.m`).
3. Follow the prompts or documentation for usage instructions.

---

## Additional Notes
- **Author:** Your Name
- **Date:** Date the branch was last updated.
- **Contact:** Email or GitHub username for questions or suggestions.
