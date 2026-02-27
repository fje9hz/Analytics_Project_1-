# Analytics Project 1  
Mustafa, Thomas, Yusuf  

## Overview  

This project analyzes NHANES 1999–2000 survey data along with the CDC Linked Mortality File to study long-term mortality outcomes. We combine demographic, dietary, and mortality follow-up data to explore patterns in survival and build predictive models.

The project is divided into two main parts:

- **Notebook 1** – Data wrangling and exploratory data analysis  
- **Notebook 2** – K-Nearest Neighbors (KNN) classification and regression  

---

## Data Sources  

- **NHANES 1999–2000**
  - Demographic file (`DEMO.xpt`)
  - Dietary recall file (`DRXTOT.xpt`)

- **CDC Linked Mortality File**
  - Public-use mortality follow-up through December 31, 2019

Each row represents one NHANES participant. All datasets are merged using the unique identifier `SEQN`.

---

## Research Goals  

We focus on two response variables:

- **MORTSTAT** – Whether the participant died during the follow-up period  
- **PERMTH_INT** – Follow-up time in months from interview to death or censoring  

Our goals are to:

1. Clean and merge the datasets correctly  
2. Explore distributions and relationships in the data  
3. Examine how demographic and dietary factors relate to mortality  
4. Build and evaluate KNN models for both classification and regression  

---

## Repository Structure  

- `notebook1_wrangling_eda.ipynb`  
  Data loading, merging, cleaning, missing value analysis, and exploratory analysis  

- `notebook2_knn.ipynb`  
  KNN classification for mortality and KNN regression for follow-up time  

- `data/`  
  Contains NHANES and mortality data files  

---

## Methods Used  

- Data wrangling and merging using `pandas`  
- Exploratory data analysis using `seaborn` and `matplotlib`  
- K-Nearest Neighbors classification  
- K-Nearest Neighbors regression  
- Model evaluation using accuracy, confusion matrix, and RMSE  

---

## Notes  

- Only participants eligible for mortality linkage (`ELIGSTAT == 1`) are included in modeling.  
- Dietary recall data is merged using a left join to retain the full mortality-eligible sample.  
- Missing values are handled explicitly during preprocessing.

## Work Distribution
- EDA and Wrangling - Yusuf and Mustafa
- KNN - Mustafa and Thomas 

## AI Acknowledgement

- AI (Claude, ChatGPT 5.2. and Gemini) was used to help with coding, formatting, structure, and checking work. AI usage is properly cited where needed. AI was used to help create and structure the README.
  
```
