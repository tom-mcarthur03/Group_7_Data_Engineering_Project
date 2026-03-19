# CIVE70122 Data Engineering Group Project

**Project title:** Prediction and Classification of Vehicle Fuel Consumption Using Vehicle Specifications  
**Module:** CIVE70122 Data Engineering  
**Institution:** Imperial College London  
**Group 7:** Xilong Fang, Zudi Huang, Xiaoyang Lin, Tom McArthur, Andrew Patton, John Peng, Yi Zhu

## Project overview

This repository contains the notebooks and data for our CIVE70122 Data Engineering group project on vehicle fuel-consumption analysis. Using the Canadian vehicle emissions dataset, the project investigates which combinations of vehicle characteristics are associated with stronger fuel efficiency across broad vehicle groupings.

The work covers:
- exploratory data analysis and feature engineering
- data cleaning and deduplication
- feature selection
- predictive modelling
- neural network modelling
- clustering analysis
- classification modelling

The core business question addressed is:

> Which combinations of vehicle components and characteristics are associated with the highest possible fuel efficiency for different general vehicle groupings?

## Repository URL

GitHub repository: `https://github.com/tom-mcarthur03/Group_7_Data_Engineering_Project`

To clone the repository:

```bash
git clone https://github.com/tom-mcarthur03/Group_7_Data_Engineering_Project.git
cd Group_7_Data_Engineering_Project
```

## Repository structure

```text
Group_7_Data_Engineering_Project/
│
├── README.md
├── .gitignore
├── requirements.txt
│
├── Data/
│   ├── CO2 Emissions_Canada.csv
│   ├── Clean dataset.csv
│   ├── Model dataset.csv
│   └── clean_data_with_predictions.csv
│
└── Notebooks/
    ├── Sect_2_and_3_EDA_Feature_Selection.ipynb
    ├── Sect_4_Predictive Models.ipynb
    ├── Sect_4_Neural_Network_Models.ipynb
    ├── Sect_4_Clustering_models_DBSCAN_and_K_means.ipynb
    └── Sect_5_Classification_Models.ipynb
```

## Files included in this submission

### Notebooks

**`Sect_2_and_3_EDA_Feature_Selection.ipynb`**  
Performs exploratory data analysis, basic cleaning, deduplication, and feature selection. This notebook reads the raw dataset and writes `Clean dataset.csv` to the `Data/` folder.

**`Sect_4_Predictive Models.ipynb`**  
Builds the predictive modelling workflow. It reads `Clean dataset.csv`, performs additional feature engineering, writes `Model dataset.csv`, and also exports `clean_data_with_predictions.csv` for downstream analysis.

**`Sect_4_Neural_Network_Models.ipynb`**  
Builds neural-network regression models for fuel-consumption prediction using the processed modelling dataset.

**`Sect_4_Clustering_models_DBSCAN_and_K_means.ipynb`**  
Runs the clustering analysis, including DBSCAN and k-means, using the cleaned dataset.

**`Sect_5_Classification_Models.ipynb`**  
Builds the classification modelling workflow using the processed modelling dataset.

### Data

**`CO2 Emissions_Canada.csv`**  
Raw source dataset used as the starting point for the project.

**`Clean dataset.csv`**  
Deduplicated and de-identified base dataset produced from the raw file after removing `Make` and `Model` and dropping duplicate rows.

**`Model dataset.csv`**  
Feature-engineered modelling dataset created from `Clean dataset.csv` for downstream training and analysis.

**`clean_data_with_predictions.csv`**  
An enriched output dataset containing the cleaned data plus prediction results from the predictive modelling stage.

## Notebook path conventions

The notebooks are set up to use relative paths from the `Notebooks/` folder to the `Data/` folder. For example:

```python
from pathlib import Path
import pandas as pd

df_raw = pd.read_csv(Path("../Data/CO2 Emissions_Canada.csv"))
```

This means the notebooks should be run from within the repository structure without moving files out of their folders.

## Recommended running order

For the clearest reproduction of the workflow, run the notebooks in the following order:

1. `Sect_2_and_3_EDA_Feature_Selection.ipynb`
2. `Sect_4_Predictive Models.ipynb`
3. `Sect_4_Neural_Network_Models.ipynb`
4. `Sect_4_Clustering_models_DBSCAN_and_K_means.ipynb`
5. `Sect_5_Classification_Models.ipynb`

## Setup instructions

1. Clone the repository:

```bash
git clone https://github.com/tom-mcarthur03/Group_7_Data_Engineering_Project.git
cd Group_7_Data_Engineering_Project
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

4. Launch Jupyter Notebook or JupyterLab and open the notebooks in the `Notebooks/` folder:

```bash
jupyter notebook
```

## Main Python packages used

The project uses the following main libraries:

- numpy==2.1.3
- pandas==2.2.3
- matplotlib==3.10.0
- seaborn==0.13.2
- scikit-learn==1.6.1
- ipython==8.30.0
- jupyter==1.1.1
- torch==2.10.0
- optuna==4.1.0

## Reproducibility note

Some datasets in the `Data/` folder are generated by earlier notebooks. To fully reproduce the workflow from scratch, begin with `Sect_2_and_3_EDA_Feature_Selection.ipynb` and then run the later notebooks in order.

## Submission note

This repository is intended to accompany the final submission for the CIVE70122 Data Engineering module and provide a clear, reproducible record of the project workflow.
