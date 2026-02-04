🦟 Rainfall–Dengue Relationships Across Climatic Zones
A Study in Ratnapura District, Sri Lanka (2020–2025)

📋 Project Overview
This repository contains the code and analysis for my Final Year Project (FYP) submitted in partial fulfillment of the requirements for the BSc (Hons) Data Science and Analytics at the University of Westminster.
🎯 Aim
To quantify and compare the temporal associations between weekly rainfall patterns and dengue case incidence in two climatologically distinct Medical Officer of Health (MOH) areas in Sri Lanka over the period 2020–2025, contributing to the development of climate-informed dengue surveillance strategies.
📍 Study Areas
MOH AreaClimatic ZoneAnnual RainfallBalangodaWet Zone 2,500–3,000 mmUdawalawaDry Zone 1,200–1,800 mm

🔬 Research Objectives

✅ Analyse rainfall and dengue trends to identify seasonal variations and outbreak periods
✅ Determine lag periods between rainfall and dengue case increases using cross-correlation analysis
⏳ Develop statistical models (Negative Binomial Regression) linking rainfall to dengue incidence
⏳ Compare model outcomes across zones to assess rainfall impacts and public health implications


📊 Key Findings (To Date)
Cross-Correlation Analysis Results
MOH AreaOptimal LagCorrelation (r)InterpretationBalangoda (Wet Zone)18 weeks0.0450Weak positiveUdawalawa (Dry Zone)17 weeks0.2168Moderate positive
Key Insight

Udawalawa (dry zone) shows a stronger rainfall-dengue correlation than Balangoda (wet zone), suggesting that rainfall events have more distinct impacts in drier regions where water accumulation is less frequent.

Descriptive Statistics
StatisticBalangodaUdawalawaMean Dengue Cases/Week3.051.06Max Cases2814Mean Rainfall (mm)46.1629.08Variance/Mean Ratio5.841.98

🛠️ Methodology
┌─────────────────────────────────────────────────────────────────┐
│                    METHODOLOGY WORKFLOW                         │
├─────────────────────────────────────────────────────────────────┤
│  1. Data Collection                                             │
│     └── Dengue: Epidemiology Unit, MOH (2020-2025)             │
│     └── Rainfall: Dept. of Meteorology (2020-2025)             │
│                              ↓                                  │
│  2. Data Preprocessing                                          │
│     └── Reshape, clean, merge datasets                         │
│     └── Weekly aggregation                                      │
│                              ↓                                  │
│  3. Exploratory Data Analysis                                   │
│     └── Descriptive statistics                                  │
│     └── Time series visualization                               │
│                              ↓                                  │
│  4. Stationarity Testing                                        │
│     └── Augmented Dickey-Fuller (ADF) Test                     │
│                              ↓                                  │
│  5. Cross-Correlation Analysis                                  │
│     └── Identify optimal lag periods                            │
│                              ↓                                  │
│  6. Statistical Modeling                                        │
│     └── SARIMAX (Failed - documented)                          │
│     └── Negative Binomial Regression (Planned)                 │
│                              ↓                                  │
│  7. Visualization & Dashboard                                   │
│     └── Power BI Interactive Dashboard                          │
└─────────────────────────────────────────────────────────────────┘

📁 Repository Structure
📦 FYP-Rainfall-Dengue-Analysis
├── 📄 README.md                    # Project documentation (this file)
├── 📓 SARIMAX.ipynb                # Main analysis notebook
├── 📊 Data/
│   ├── Rainfall_data.xls           # Raw rainfall data
│   └── Dengue_Data.xlsx            # Raw dengue case data
├── 📈 Outputs/
│   ├── 01_time_series_balangoda.png
│   ├── 02_time_series_udawalawa.png
│   ├── 03_distribution_comparison.png
│   ├── 04_yearly_trends.png
│   ├── 09_acf_pacf_balangoda.png
│   ├── 10_acf_pacf_udawalawa.png
│   ├── 11_cross_correlation_balangoda.png
│   ├── 12_cross_correlation_udawalawa.png
│   ├── 13_cross_correlation_comparison.png
│   ├── 14_diagnostics_balangoda.png
│   ├── 15_diagnostics_udawalawa.png
│   ├── 16_predictions_balangoda.png
│   └── 17_predictions_udawalawa.png
└── 📋 Reports/
    └── IPD_Report.pdf              # Interim Progress Demonstration

💻 Technologies & Tools
CategoryToolsProgramming LanguagePython 3.8+IDE/EnvironmentGoogle Colab, Jupyter NotebookData Manipulationpandas, NumPyStatistical Analysisstatsmodels (SARIMAX, ADF, CCF)VisualizationMatplotlib, SeabornMachine Learning Metricsscikit-learn (MAE, RMSE, R²)DashboardPower BIStatistical SoftwarePSPP v1.6

🚀 How to Run
Option 1: Google Colab (Recommended)

Open Google Colab
Upload SARIMAX.ipynb
Upload data files to Colab
Run all cells sequentially

Option 2: Local Jupyter Notebook
bash# Clone the repository
git clone https://github.com/Analytics-By-Kalpitha/FYP-Rainfall-Dengue-Relationships-Across-Climatic-Zones-2020-2025.git

# Navigate to directory
cd FYP-Rainfall-Dengue-Relationships-Across-Climatic-Zones-2020-2025

# Install dependencies
pip install pandas numpy matplotlib seaborn statsmodels scikit-learn

# Launch Jupyter
jupyter notebook SARIMAX.ipynb

📦 Dependencies
python# Required Libraries
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
statsmodels>=0.12.0
scikit-learn>=0.24.0
openpyxl>=3.0.0      # For Excel file handling
xlrd>=2.0.0          # For .xls file handling

📈 Sample Outputs
Time Series Analysis
The analysis generates time series plots showing weekly dengue cases overlaid with rainfall patterns for both MOH areas.
Cross-Correlation Plots
Cross-correlation analysis identifies the optimal lag period between rainfall events and subsequent dengue case increases.
ADF Test Results
All four time series (dengue and rainfall for both areas) were confirmed stationary (p < 0.05), enabling direct time series modeling.

⚠️ SARIMAX Model Failure Documentation
The initial SARIMAX modeling approach failed due to:
IssueDescriptionData Type MismatchSARIMAX designed for continuous data; dengue cases are discrete countsInsufficient Sample Size52-week seasonality requires more complete annual cyclesOverdispersionVariance >> Mean (ratios: 5.84 and 1.98)
Solution: Methodology revised to Negative Binomial Regression (implementation in progress).

📅 Project Timeline
PhaseTaskStatusPhase 1Data Collection & Preprocessing✅ CompletePhase 2Exploratory Data Analysis✅ CompletePhase 3Stationarity & Cross-Correlation✅ CompletePhase 4SARIMAX Modeling✅ Complete (Failed)Phase 5Negative Binomial Regression⏳ In ProgressPhase 6Power BI Dashboard⏳ PlannedPhase 7Thesis Writing⏳ In Progress

👨‍🎓 Author
A. Kalpitha Prabhasha Perera
🎓 Student IDw1985754 / 20222130🏫 UniversityUniversity of Westminster📚 ProgrammeBSc (Hons) Data Science and Analytics👨‍🏫 SupervisorMr. Daham Alwis📅 Academic Year2025/2026

📚 References

Goto, K., et al. (2013). "Analysis of effects of meteorological factors on dengue incidence in Sri Lanka using time series data." PLoS One, 8(5).
Withanage, G.P., et al. (2018). "A forecasting model for dengue incidence in the District of Gampaha, Sri Lanka." Parasites & Vectors, 11.
Ehelepola, N.D.B., et al. (2015). "A study of the correlation between dengue and weather in Kandy City, Sri Lanka." Infectious Diseases of Poverty, 4.
Edirisinghe, G. (2017). "Contribution of rainfall patterns for increased dengue epidemic in Sri Lanka." ASRJETS, 35(1).


📄 License
This project is submitted for academic purposes as part of the BSc (Hons) Data Science and Analytics program at the University of Westminster.

🙏 Acknowledgements

Epidemiology Unit, Ministry of Health, Sri Lanka - For providing dengue surveillance data
Department of Meteorology, Sri Lanka - For providing rainfall data
Mr. Daham Alwis - Project Supervisor
University of Westminster - School of Computer Science & Engineering
