Wanna see something cool ? Check `figures/habitat_types_map.jpeg`

```
   \\                       /""\      ,                       __                         ,_,  
   (o>                     <>^  L____/|                      /'{>                       (O,O)
\\_//)                       `) /`   , /                ____) (____                     (   )
 \_/_)                        \ `---' /               //'--;   ;--'\\                   -"-"---
  _|_                          `'";\)`                ///////\_/\\\\\\\
                                _/_Y                        m m
```

LEONARDI Raphael (raphael.leonardi@universite-paris-saclay.fr) ; 22208912

PRAS Baptiste (baptiste.pras@universite-paris-saclay.fr) ; 22201371

# Reproducibility Instructions

## 1. Create the environment

To reproduce the analysis, create a Python environment and install all required libraries using the `requirements.txt` file.

`pip install -r requirements.txt`

All dependencies (NumPy, pandas, matplotlib, seaborn, scikit-learn, pygam, statsmodels, GeoPandas, etc.) will be installed automatically.

## 2. Input data

Always use our dataset: `Observations 2012-2025.xlsx`

Do not use another version of the dataset (we modified some mistakes in it).

The preprocessing pipeline was designed exclusively for our cleaned version of the dataset and expects its structure.

## 3. Notebooks execution order (important)

There are three Jupyter notebooks, and they must be executed in this exact order:

1) `data_preparation.ipynb` (Cleans the raw Excel sheet and generates processed tables. Vizualize some data.)
2) `multi_years_indicators.ipynb` (Computes multi-year indicators.)
3) `species_evolution.ipynb` (Compute species-level trends.)

Mandatory rules:

You must run all cells of `data_preparation.ipynb` before running notebooks 2 or 3.

When using a notebook, always execute the cells in order — do not skip any.

## 4. Output files

All generated figures are saved inside the folder: `figures/`

Cleaned datasets are exported as three CSV tables (one per sheet of the Excel file) inside: `data/processed/`

## 5. Folder structure summary

```
data/
|  processed/
|     observations.csv
|     sites.csv
|     species.csv
|  raw/
|     Observations 2012-2025.xlsx
figures/
|  ...
requirements.txt
data_preparation.ipynb
multi_year_indicators.ipynb
species_evolution.ipynb
Technical_Report.pdf
```

This ensures full reproducibility of the data cleaning, indicator computation, and modeling.
