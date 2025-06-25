# -KiTS19-Kidney-Tumor-Imaging-and-Clinical-Analysis-Pipeline
🧠 KiTS19 Kidney Tumor Imaging and Clinical Analysis Pipeline
This project implements a full end-to-end pipeline for the KiTS19 dataset. It supports preprocessing, visualization, statistical analysis, machine learning modeling, and survival analysis of kidney tumor cases derived from CT scans and metadata.

📌 Key Features
✅ Automated preprocessing: resampling, metadata cleaning
✅ Visualizations: slices with overlays, metadata-augmented images
✅ Tumor volume, kidney-to-tumor ratio, heterogeneity analysis
✅ Demographic and tumor characteristic analysis
✅ Survival modeling (Kaplan-Meier, Cox)
✅ ML models for predicting malignancy & complications
✅ Export of analysis figures, reports, and case summaries
🛠 Pipeline Overview
1. Data Preprocessing
Resample all CT scans and segmentations to isotropic spacing (1.5×1.5×1.5 mm³)

Flatten and clean metadata from kits.json

Normalize numeric fields, encode categorical fields

2. Visualization
Generate middle slice overlays (volume + segmentation)

Annotate slices with metadata

Save slice-wise PNGs for all cases

3. Analysis Modules
Demographics
Age & gender distributions

BMI analysis by malignancy

Comorbidity prevalence

Tumor Characteristics
Histologic subtype frequencies

Radiographic vs pathologic size comparisons

TNM staging and ISUP grade analysis

Imaging Features
Tumor & kidney volumes (cm³)

Volume ratios

Tumor heterogeneity metrics (entropy, range, std)

Survival Outcomes
Kaplan-Meier plots

Cox Proportional Hazards modeling

eGFR tracking across timepoints

Predictive Models
Random Forest & Logistic Regression

Predicting:

Tumor malignancy

Post-operative complications

📈 Outputs
All results are saved under kits19_analysis_results/, including:

Figures (PDF/PNG)

Summary reports

Machine learning evaluation metrics

Case-wise visual summaries (integrated_analysis/)
📊 Sample Figures
Age Distribution by Gender

Tumor Volume vs Radiographic Size

Survival Curves

Feature Importance for Random Forest

ISUP Grade Distribution by Tumor Type

📎 References
KiTS19 Dataset: https://kits19.grand-challenge.org/

SimpleITK: https://simpleitk.readthedocs.io/

Lifelines Survival Library: https://lifelines.readthedocs.io/

Nibabel: https://nipy.org/nibabel/
