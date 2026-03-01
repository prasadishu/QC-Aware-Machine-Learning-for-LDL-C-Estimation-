qc-aware-ldl-prediction
📌 Overview This project presents a quality control (QC)–aware machine learning framework for estimating low-density lipoprotein cholesterol (LDL-C) using routine lipid profile parameters (Total Cholesterol, Triglycerides, HDL-C).

The framework compares four supervised ML algorithms: Random Forest XGBoost CatBoost Support Vector Regression (SVR)

against established LDL-C calculation formulas: Friedewald equation Martin–Hopkins method Sampson–NIH equation

A post-prediction QC validation layer is integrated to enhance analytical safety and laboratory applicability

🎯 Objectives Improve LDL-C estimation accuracy using machine learning Compare ML models with conventional calculation-based formulas Evaluate triglyceride-stratified performance (especially TG ≥400 mg/dL) Integrate laboratory-inspired QC logic into ML predictions Bridge computational modeling with real-world laboratory workflows

🏥 Clinical Relevance LDL-C is a central biomarker in cardiovascular risk assessment. Traditional calculation methods deteriorate in hypertriglyceridemic samples.

This framework: Improves performance in elevated TG states Reduces extreme analytical deviations Aligns ML predictions with laboratory quality control principles Supports implementation in ISO 15189–compliant laboratories

⚙️ Installation
1️⃣ Clone the repository git clone (https://github.com/prasadishu/qc-aware-ldl-prediction.git) 2️⃣ Install dependencies pip install -r requirements.txt ▶️ How to Run Place your dataset inside: data/LDL_Internal_Training_Test_Dataset1.xlsx data/LDL_Secondary_Internal_Validation_Dataset1.xlsx

Required columns: TC TG HDL_C LDL_direct Then run: python src/main.py ** 📊 Outputs Generated** The script automatically generates:

📁 Predictions results/predictions_internal.csv results/predictions_Secondary_internal.csv

📈 Figures Actual vs Predicted plots Residual vs Predicted plots ML vs Formula comparison QC vs Non-QC residual overlay

All saved under: results/figures/

🧠 Methodology Summary 🔹 Machine Learning Models Random Forest (ensemble-based variance reduction) XGBoost (regularized gradient boosting) CatBoost (ordered boosting) SVR (kernel-based regression)

🔹 Traditional Formulas Friedewald Martin–Hopkins Sampson–NIH

🔹 QC Module A post-prediction validation layer: Flags extreme predictions Constrains outliers within biologically plausible limits Mimics Westgard-style QC logic Does NOT interfere with model training

🔬 Key Findings ML models outperform conventional formulas Ensemble methods show highest stability Performance advantage increases at TG ≥400 mg/dL QC module reduces extreme analytical deviations Demographic robustness maintained without including age/gender in training

📄 Publication This repository supports the manuscript: “Quality Control–Aware Machine Learning for LDL-Cholesterol Estimation: A Comparative Study with Established Calculation Methods.”

⚠️ Disclaimer This project is intended for research and educational purposes only. It is not intended to replace clinical judgment or direct LDL-C measurement when clinically indicated.

📬 Contact

For academic collaboration or inquiries:

D V Prasad Vengaladasu AIG Hospitals vdvprasad.24@gmail.com# QC-Aware-Machine-Learning-for-LDL-C-Estimation-
