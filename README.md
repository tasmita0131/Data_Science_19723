USA Car Accident Analysis (500k records, 46 features)

A portfolio project analyzing U.S. car accidents to uncover patterns in severity, timing, weather, and geography, and to explore baseline ML models for severity classification.

Built as part of my Introduction to Data Science coursework at SFBU.

Objectives

Explore accident patterns by time of day, day of week, weather, and location.

Engineer simple risk categories for decision support.

Train baseline classification models (Decision Tree, Random Forest) on a cleaned subset.

Communicate insights with clear visualizations and a short slide deck.

Dataset

Source: US_Accidents (March 2023 snapshot) – sampled 500,000 rows with 46 columns.

Examples of features:
Severity, Start_Time, City, State, Weather_Condition, Temperature(F),
Wind_Speed(mph), Junction, Traffic_Calming, etc.

The notebook reads US_Accidents_March23_sampled_500k.csv and performs exploratory analysis plus lightweight modeling.

Methods & Tools

Python: pandas, numpy, matplotlib, seaborn, scikit-learn, folium

Cleaning & prep: Dropping high-missing columns, imputing numerics (median) and categoricals (mode), feature simplifications (e.g., weather groupings)

Visualization: Distributions, correlation heatmaps, time-of-day & weekday bar charts, map sampling with folium

Models: Decision Tree, Random Forest (baseline, simple tuning)

Highlights (Selected Findings)

Weak weather–severity link. Weather variables show very weak correlation with severity; wind speed is the highest but still only ~0.04.

Daytime volume dominates. Accidents are more frequent in the day than at night; Severity=2 is the most common class overall.

Peak hours & weekdays. Peaks around 7–8 AM and 4–5 PM (commute hours). Fridays are highest; weekends are lower.

Risk categories. A derived risk label (based on weather, hour, traffic-calming) shows the majority as Low Risk.

Geography. Densest clusters appear in large metros and along major highways; East Coast shows higher density overall.

Baseline ML. Decision Tree ≈ 81–82% accuracy; Random Forest ≈ 77–78% on the subsample.

Repository Contents

USA_Accident.ipynb → Full exploratory analysis (cleaning, visuals, basic models).

USA_Car_accidents_final_presentation.pdf → Slide deck summarizing insights and recommendations.

Paper_Car_Accident.pdf → Written report (objectives, methods, findings, recommendations).

data_Visualization_part.pdf → Visual analysis outputs.

part_02_ds_model_accuracy.pdf → Model accuracy and preprocessing notes.

USA_Car_Accident_dataset.pdf → Dataset overview and context.

(CSV not included here) US_Accidents_March23_sampled_500k.csv — expected path used by the notebook.

Reproducibility

Environment

pip install pandas numpy matplotlib seaborn scikit-learn folium


Data
Place US_Accidents_March23_sampled_500k.csv in the project root (or update the notebook path).

Run
Open USA_Accident.ipynb in Jupyter or Google Colab and run all cells in order.

One-hot encoding over many categorical levels can produce a large sparse matrix; a subsample is used for faster modeling during iteration.

Results (Short)

Preprocessing eliminated high-missing columns and imputed the rest.

Decision Tree delivered strong baseline accuracy with straightforward interpretability.

Random Forest performed slightly lower but remains a robust baseline.

Visual analyses suggested commute-time safety measures, junction/roundabout planning, and targeted monitoring in high-density corridors.
