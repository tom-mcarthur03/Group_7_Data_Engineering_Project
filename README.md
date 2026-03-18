# CIVE70122 Data Engineering Group Project

**Project title:** Prediction and Classification of Vehicle Fuel Consumption Using Vehicle Specifications  
**Module:** CIVE70122 Data Engineering  
**Institution:** Imperial College London  
**Group 7:** Xilong Fang, Zudi Huang, Xiaoyang Lin, Tom McArthur, Andrew Patton, John Peng, Yi Zhu

## Project overview

This repository contains the notebooks, data, and report for our Data Engineering group project on vehicle fuel-efficiency analysis. The project uses the Canadian vehicle emissions dataset to investigate which combinations of vehicle characteristics are associated with stronger fuel efficiency across different vehicle groupings.

The work covers:
- exploratory data analysis and feature engineering;
- feature selection;
- predictive modelling;
- clustering analysis;
- classification modelling;
- final reporting and interpretation.

The core business question addressed is:

> Which combinations of vehicle components and characteristics are associated with the highest possible fuel efficiency for different general vehicle groupings?

## Repository structure

A recommended repository structure is shown below.

```text
data-engineering-group-project/
│
├── README.md
├── .gitignore
├── requirements.txt
│
├── data/
│   ├── CO2 Emissions_Canada.csv
│
└── notebooks/
    ├── Sect_2_and_3_EDA_Feature_Selection.ipynb
    ├── Sect_4_Predictive Models.ipynb
    ├── Sect_4_Clustering_models_DBSCAN_and_K_means.ipynb
    └── Sect_5_Classification_Models.ipynb
```

## Files included in this submission

### Notebooks
- `Sect_2_and_3_EDA_Feature_Selection.ipynb`  
  Covers data exploration, data cleaning, feature engineering, and feature selection.

- `Sect_4_Predictive Models.ipynb`  
  Develops the predictive models used to analyse fuel consumption patterns across vehicle groups.

- `Sect_4_Clustering_models_DBSCAN_and_K_means.ipynb`  
  Covers clustering analysis, including DBSCAN and k-means workflows.

- `Sect_5_Classification_Models.ipynb`  
  Builds the classification framework used to identify vehicles that are more fuel-efficient than expected relative to category-specific baselines.

### Data
- `CO2 Emissions_Canada.csv`  
  Raw dataset used throughout the notebooks.

## Dataset note

The notebooks reference a CSV file named `CO2 Emissions_Canada.csv`.

```python
from pathlib import Path

data_path = Path("data/raw/CO2 Emissions_Canada.csv")
```

## Recommended setup instructions

### Run with pip

1. Clone the repository:

```bash
git clone <your-repository-url>
cd data-engineering-group-project
```

2. Create and activate a virtual environment:

```bash
python -m venv venv
```

On Windows:

```bash
venv\Scripts\activate
```

On macOS/Linux:

```bash
source venv/bin/activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Launch Jupyter:

```bash
jupyter notebook
```

## Suggested running order

For the clearest reproduction of the workflow, run the notebooks in the following order:

1. `Sect_2_and_3_EDA_Feature_Selection.ipynb`
2. `Sect_4_Predictive Models.ipynb`
3. `Sect_4_Clustering_models_DBSCAN_and_K_means.ipynb`
4. `Sect_5_Classification_Models.ipynb`

This order follows the project pipeline from data preparation through modelling and final analysis.

## Main Python packages used

The project uses the following main libraries:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- jupyter
- ipython

## Submission note

This repository is intended to accompany the final group report for the CIVE70122 Data Engineering module and provide a transparent, reproducible record of the analysis workflow.
