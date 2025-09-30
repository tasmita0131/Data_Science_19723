# USA Car Accident Analysis (500k records, 46 features)

A portfolio project analyzing U.S. car accidents to uncover patterns in **severity**, **timing**, **weather**, and **geography**, and to explore **baseline ML models** for severity classification.  

> Built as part of my *Introduction to Data Science* coursework at **San Francisco Bay University (SFBU)**.

---

## Objectives
- Explore accident patterns by **time of day**, **day of week**, **weather**, and **location**  
- Engineer simple **risk categories** for decision support  
- Train baseline **classification models** (Decision Tree, Random Forest) on a cleaned subset  
- Communicate insights with **clear visualizations** and a short slide deck  

---

## Dataset
- **Source:** [US_Accidents (March 2023 snapshot)](https://www.kaggle.com/sobhanmoosavi/us-accidents) – sampled **500,000 rows** with **46 columns**  
- **Examples of features:**  
  - `Severity`, `Start_Time`, `City`, `State`, `Weather_Condition`  
  - `Temperature(F)`, `Wind_Speed(mph)`, `Junction`, `Traffic_Calming`  

> The notebook reads `US_Accidents_March23_sampled_500k.csv` and performs exploratory analysis plus lightweight modeling.

---

## Methods & Tools
- **Languages & Libraries:** Python, pandas, numpy, matplotlib, seaborn, scikit-learn, folium  
- **Data Cleaning:** Dropped high-missing columns, imputed numerics (median) & categoricals (mode)  
- **Visualization:** Distributions, correlation heatmaps, commute-time analysis, folium mapping  
- **Modeling:** Baseline classifiers — Decision Tree, Random Forest (basic tuning)  

---

## Key Findings
- **Weak weather–severity link** → Weather variables show *very weak* correlation with severity (highest: wind speed ≈ 0.04)  
- **Daytime volume dominates** → Most accidents occur in the **day**, with **Severity=2** as the most common level  
- **Peak hours & weekdays** → Accidents peak during **7–8 AM** and **4–5 PM**; **Fridays** highest, weekends lower  
- **Risk categories** → Derived risk labels (based on weather, hour, traffic calming) → majority are **Low Risk**  
- **Geography** → Clusters in large metros/highways; East Coast denser overall  
- **Baseline ML** → Decision Tree ≈ **81–82%** accuracy; Random Forest ≈ **77–78%**  

---

## Repository Contents
- `USA_Accident.ipynb` → Full exploratory analysis (cleaning, visuals, baseline models)  
- `USA_Car_accidents_final_presentation.pdf` → Slide deck with insights & recommendations  
- `Paper_Car_Accident.pdf` → Full written report (objectives, methods, findings, recommendations)  
- `data_Visualization_part.pdf` → Supporting charts & figures  
- `part_02_ds_model_accuracy.pdf` → Model evaluation notes  
- `USA_Car_Accident_dataset.pdf` → Dataset overview/context  
- `US_Accidents_March23_sampled_500k.csv` — dataset

---


