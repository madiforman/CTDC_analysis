### LICENSE

This analysis uses the Counter-Trafficking Data Collaborative (CTDC) Global Synthetic Dataset, accessed under the CTDC Terms of Use [terms of use](https://www.ctdatacollaborative.org/page/terms-use). The data are synthetic and created for research and illustration purposes; they do not contain identifiable victim records.

Counter-Trafficking Data Collaborative (CTDC). 2025. CTDC Global Synthetic Dataset and accompanying codebook. Available at [CTDC](https://www.ctdatacollaborative.org/).

### Relevant Resources


* [Data](https://www.ctdatacollaborative.org/dataset/global-synthetic-data-and-resources/resource/microdata)

* [Codebook](https://www.ctdatacollaborative.org/dataset/global-synthetic-data-and-resources/resource/codebook)

* [About Page](https://www.ctdatacollaborative.org/page/global-synthetic-dataset)


### Abstract

This study uses the Counter-Trafficking Data Collaborative (CTDC) Global Synthetic Dataset to examine how victim demographics, recruiter relationships, and means of control are associated with two main forms of human trafficking exploitation: sexual exploitation and forced labour. I constructed a cleaned analytic dataset, engineered predictors from the CTDC codebook, and fit regularized logistic regression models to estimate odds ratios for each exploitation type while controlling for overlapping risk factors. The results show that sexual exploitation is strongly concentrated among women and transgender/non‑conforming victims, citizens, and individuals controlled with drugs and alcohol and recruited by intimate partners or friends. In contrast, forced labour is concentrated among men and non‑citizens who experience work‑ and immigration‑related control tactics such as excessive work hours, debt bondage via earnings, denial of basic needs, threats, and document withholding, often through “other” recruiter types like brokers or employers. These findings highlight that different forms of trafficking operate through distinct, but overlapping, vulnerability profiles and suggest that prevention, identification, and protection efforts should be tailored to the specific patterns of risk associated with each exploitation type. These findings should not be used to disclude a specific demographic from intervention in either form of exploitation, but is intended to highlight major risk factors amongst vulnerable populations. 

### Project Structure:
.
├── README.md               # Project overview, abstract, methods, findings
├── LICENSE                 # Project license
├── analysis.ipynb          # Modeling, results, and visualizations
├── process_data.ipynb      # Data cleaning and feature engineering
├── notebook_pdfs/                         
│   ├── analysis.pdf
│   └── process_data.pdf
├── data/                  
│   ├── Codebook_CTDC_global_synthetic_data_v2024.pdf  # CTDC variable definitions
│   ├── CTDC_global_synthetic_data_v2025.csv           # Raw CTDC synthetic data
│   └── final_data.csv                                 # Cleaned analysis dataset
└── figures/               
    ├── forest_plot.png
    ├── feature_correlation.png
    └── roc_curves.png