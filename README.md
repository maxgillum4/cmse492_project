# Chicago Rent Alpha Predictor

End-to-end CMSE 492 final project exploring what drives **ZIP-level rent outperformance**
("alpha") in the Chicago metro area.

The goal is to:
- Engineer economic, structural, lifestyle, and safety features at the ZIP × month level
- Train and compare linear vs tree-based models (Ridge, Gradient Boosting, Random Forest)
- Identify which neighborhoods are projected to outgrow the metro baseline, and why

---

## Repository Structure

```text
.
├── data/
│   ├── raw/
│   │   ├── zori_zip.csv                     # Zillow rent index by ZIP (input)
│   │   └── Boundaries_-_ZIP_Codes_*.geojson # Chicago ZIP boundaries (input)
│   └── processed/
│       └── chicago_augmented_12m.csv        # Engineered feature table (output of 01)
├── notebooks/
│   ├── 01_eda_augmented.ipynb               # Data loading, feature engineering, synthetic indices
│   └── 02_models_advanced.ipynb             # Modeling, evaluation, and visualization
├── figures/
│   ├── model_suite.png                      # Multi-panel model/importance figure
│   ├── feature_importance.png               # (exported from 02)
│   ├── gentrification_map.png               # (exported from 02)
│   └── model_performance.png                # (exported from 02)
├── docs/
│   ├── model_metrics.csv                    # Metric table for report
│   └── (LaTeX PDF will live here eventually)
├── requirements.txt
└── README.md
