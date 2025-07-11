# PTB XL Dataset ECG Data Wrangling

This repository contains a Jupyter notebook for wrangling and preparing the **PTB XL ECG Dataset**. The notebook performs exploratory data analysis, data wrangling, and visualization for the dataset, which includes electrocardiogram (ECG) signals from a large number of patients.

## Overview

The PTB XL dataset is a publicly available dataset for ECG classification. The goal of this project is to clean, preprocess, and visualize the data for further analysis or modeling. The notebook loads raw ECG signals, processes them, and aggregates diagnostic data from the dataset to prepare for machine learning tasks.

## Steps Involved

1. **Import Kaggle Data**: The notebook imports the dataset from Kaggle using the `kagglehub` library.
2. **Exploratory Data Analysis (EDA)**:

   * Load and examine raw ECG signals.
   * Visualize the distribution of diagnostic superclasses and subclasses across the dataset.
   * Perform various statistical analyses on the data, including age, sex, height, weight, and other features correlated with diagnostic labels.
3. **Data Preparation**:

   * Aggregate diagnostic information.
   * Format the data into a suitable structure for machine learning, including train, validation, and test sets based on stratified 10-fold splits.
4. **Data Splitting**:

   * The dataset is split into training (folds 1-8), validation (fold 9), and test (fold 10) sets, as recommended by the source of the dataset.
5. **Data Export**:

   * Export the train, validation, and test sets to CSV files for easy access and further analysis.

## Data Sources

* **PTB XL ECG Dataset**: [Dataset link](https://physionet.org/content/ptb-xl/1.0.1/)
* The dataset contains 12-lead ECG signals and associated diagnostic information from patients.

## Requirements

Ensure that the following libraries are installed to run the notebook:

```bash
pip install pandas numpy wfdb tqdm matplotlib seaborn kagglehub
```

## Dataset Files

* `train_meta.csv`: Metadata for the training set.
* `train_signal.csv`: ECG signal data for the training set.
* `valid_meta.csv`: Metadata for the validation set.
* `valid_signal.csv`: ECG signal data for the validation set.
* `test_meta.csv`: Metadata for the test set.
* `test_signal.csv`: ECG signal data for the test set.

## Usage

1. **Import Data**: Run the first code cell to import data from Kaggle.
2. **Run EDA**: Use the EDA sections to analyze the distribution of various diagnostic superclasses and subclasses across the dataset.
3. **Data Wrangling**: Clean and process the data, including feature extraction and aggregation.
4. **Data Splitting**: Split the data into training, validation, and test sets for use in machine learning models.
5. **Export Data**: Export processed data to CSV files for later use.

## Example Visualizations

* **Diagnostic Superclass Distribution**: Visualize the distribution of different diagnostic superclasses (e.g., NORM, MI, STTC, HYP).
* **Age Distribution by Superclass**: Analyze how age correlates with different diagnostic superclasses.
* **Height and Weight Distributions**: Visualize the distribution of patient height and weight across different superclasses.
* **ECG Signal Plots**: Visualize ECG signal data for various superclasses.

## Reference

* **Paper**: Wagner, P., Strodthoff, N., Bousseljot, R.-D., Kreiseler, D., Lunze, F.I., Samek, W., Schaeffter, T. (2020), PTB-XL: A Large Publicly Available ECG Dataset. [DOI](https://doi.org/10.1038/s41597-020-0495-6)
