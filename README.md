# Titanic Survival Analysis
---------------------------------------
## Overview
This project explores the famous **Titanic dataset** to understand the factors that influenced passenger survival during the disaster.  
Through **data cleaning, exploratory data analysis (EDA), and visualization**, we uncover insights about how gender, class, age, fare, and embarkation port affected survival chances.  

The notebook also includes **statistical plots** and a **correlation matrix** to highlight relationships between variables.

---

## Tech Stack
- **Python**
- **Libraries used**:
  - `pandas`, `numpy` → data manipulation
  - `matplotlib`, `seaborn` → data visualization
  - `statsmodels` → statistical analysis (QQ plots)

---
 
## Exploratory Data Analysis (EDA)
Key steps in the analysis:
1. **Data Cleaning**
   - Filled missing `Age` with median, `Embarked` with mode.
   - Dropped `Cabin` due to too many missing values.

2. **Univariate Analysis**
   - Distribution of survival, passenger class, gender, embarkation port.
   - Age & Fare distributions (histograms, boxplots, violin plots).

3. **Bivariate Analysis**
   - Survival by passenger class, gender, age, fare, and embarkation.
   - Age vs. Fare scatter plot with survival overlay.

4. **Correlation Analysis**
   - Heatmap to visualize correlations between numeric variables.
     
5. **Family Size Analysis (New)**
   - Multiple definitions of family size were tested:
     - **SibSp + Parch** (direct relatives).  
     - **Ticket Group Size** (passengers sharing the same ticket).  
     - **LastName + Ticket (redefined)** – most accurate grouping of true families.  
   - Clear **U-shaped survival trend** was found:
     - **Alone travelers** → lowest survival (~30%).  
     - **Small families (2–4)** → highest survival (~50%).  
     - **Large families (≥5)** → very low survival (<20%).

---

## Visualizations
- **Count plots** of survival by class, gender, and embarkation port.
- **Distribution plots** of age and fare (histograms, KDE, boxplots, violin plots).
- **QQ plots** to check normality of age and fare distributions.
- **Correlation matrix heatmap** to identify key survival predictors.
- **Age vs. Fare scatter plot** colored by survival status.
- **Survival rate by SibSp + Parch** (traditional definition of family size).
- **Distribution of Ticket Group Sizes** (passengers sharing the same ticket).
- **Survival rate by redefined family size (LastName + Ticket)** → most accurate grouping.
- **Survival rate by Family Category (Alone, Small, Large)** showing a clear **U-shaped survival pattern**.
- **Correlation heatmap** comparing different family size definitions with survival.
     
---

## Key Findings
- **Overall survival rate**: ~38% (342 survived out of 891).
- **Gender**: Women survived at much higher rates than men.
- **Class**: 1st-class passengers had the best survival chances, 3rd-class the worst.
- **Fare**: Higher fare strongly associated with higher survival.
- **Age**: Children had better chances; elderly survival was low.
- **Embarkation Port**: Passengers from Cherbourg (C) survived more compared to Southampton (S).
- Alongside gender, class, and age, **family structure was a major survival determinant**.
