# Reproducible Regression Workflow

This repository contains a reproducible regression analysis using the pollution dataset. The aim is to investigate the relationship between poverty and mortality and to demonstrate how a statistical analysis can be organised as a reproducible workflow following FAIR principles.

## Analysis

The dataset contains 60 observations and several demographic, environmental, and pollution-related variables.

In this analysis:

- `POOR` is the percentage of families with income below $3000.
- `MORT` is the total age-adjusted mortality rate per 100,000 people.

Local linear regression is used to model the relationship between `POOR` and `MORT`. Leave-one-out cross-validation (LOOCV) is used to select the number of neighbouring observations, \(k\).

The cross-validation procedure selected **k = 15**.

## Repository Contents

- `Regression.ipynb` – Jupyter Notebook containing the complete analysis
- `pollution_cleaneddata.csv` – dataset used in the analysis
- `pollution_metadata.txt` – information about the dataset and variables
- `requirements.txt` – required Python packages and pinned versions
- `LICENSE` – license for the repository

## Requirements

The workflow was run using:

- Python 3.13.9
- NumPy 2.3.1
- pandas 2.3.3
- Matplotlib 3.10.6

The exact package versions are specified in `requirements.txt`.

## How to Run

1. Clone or download this repository.
2. Install the required packages:

```bash
pip install -r requirements.txt
```

3. Open `Regression.ipynb` using Jupyter Notebook or JupyterLab.
4. Run the notebook cells from top to bottom.

## Reproducibility

The repository includes the data, metadata, analysis code, dependency information, and documentation required to reproduce the analysis.

Exact package versions are pinned to reduce the risk that future package updates change the behaviour of the workflow.

## FAIR Principles

The workflow considers the FAIR principles of **Findability, Accessibility, Interoperability, and Reusability**.

A more detailed discussion of the FAIR principles and how they relate to this project is included in `Regression.ipynb`.

## Data Source

The pollution dataset originates from:

McDonald, G. C. and Schwing, R. C. (1973), *Instabilities of regression estimates relating air pollution to mortality*, Technometrics, 15, 463–482.

Additional information about the variables is provided in `pollution_metadata.txt`.

## License

The analysis code and documentation in this repository are provided under the MIT License. See the `LICENSE` file for details.
