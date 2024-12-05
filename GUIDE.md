# File Guide for [rfandozzi-dynamic-systems-modeling]

This document provides an overview of the files in the `[rfandozzi-dynamic-systems-modeling]` branch.

---

## Files and Descriptions

### **1. [COVIDbyCounty (1).mat]**
####**Description:** There are 3 key arrays in the file:
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
#### **Usage:** 
- Load this file in MATLAB using:
  ```matlab
  load('COVIDbyCounty (1).mat');


---

### **2. [part1-1.m]**
### **File: [filename.m]**

#### **Description:**
This script analyzes COVID-19 case data and census data to study linear independence and interpret relationships between case trajectories for different counties in the U.S. The key tasks performed are:

1. **Identify the Most Populous County in Each Census Division:**
   - Using the 2021 census data, the script identifies the 9 most populous counties (one per division) and extracts their COVID-19 case data.
   - **Output:** A plot visualizing the COVID-19 case trajectories for these 9 counties.

2. **Check for Linear Independence:**
   - Computes the angles between the COVID case trajectories of the 9 counties to verify linear independence.

3. **Normalize the Trajectories:**
   - Each trajectory vector is normalized so its norm equals 1, resulting in a set of unit vectors denoted as \(d_1, d_2, \ldots, d_9\).

4. **Analyze St. Louis City Data:**
   - Denotes the COVID-19 case data for St. Louis City as \(c\).
   - For each of the 9 unit vectors \(d_i\), computes the residual vector:
     \[
     r_i = c - (c^T d_i)d_i
     \]
   - Computes the norm \(||r_i||_2\) for \(i = 1, \ldots, 9\).
   - **Interpretation of \(r_i\):**
     - \(r_i\) represents the component of \(c\) orthogonal to \(d_i\), meaning the portion of \(c\) that cannot be explained by \(d_i\).
     - The norm \(||r_i||_2\) measures how different St. Louis City's case trajectory is from being explained by the trajectory of the \(i\)-th census division's most populous county.

---

#### **Usage:**
- Run the script in MATLAB to:
  - Identify and visualize the most populous counties' COVID trajectories.
  - Check linear independence of the trajectories.
  - Compute residuals and analyze St. Louis City's relationship to census divisions.

---

#### **Key Insights:**
- The residual \(r_i\) describes how well the trajectory of St. Louis City's case data aligns with that of a census division's most populous county.
- If \(||r_i||_2\) is large for all 9 divisions, it may suggest that St. Louis City's trajectory cannot be accurately represented by the trajectories of the most populous counties in each census division. If \(||r_i||_2\) is small, this indicates greater similarity between St. Louis city and the most populous counties.

---

#### **Dependencies:**
- Requires `COVIDbyCounty (1).mat` for the COVID and census data.

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
