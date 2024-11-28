# Greenhouse Gas Emissions Forecasting with LSTM
This project predicts greenhouse gas emissions by sector using Long Short-Term Memory (LSTM) models. The model is trained on historical emissions data and predicts future emissions for each sector. The project was completed in three phases, starting with simple Linear Regression and transitioning to advanced LSTM-RNN models. This progression allowed us to better understand the data, refine our approach, and improve predictive accuracy.

This document provides instructions on how to run the program, along with the required dependencies and setup steps.

## Table of Contents
* Dataset Overview
* Project Phases 
* Prerequisites
* Installation
* Running the Notebooks/script

## Dataset Overview  
We began with a dataset containing greenhouse gas emissions from various sectors across multiple countries, recorded annually from 1990 to 2020.  

To gain insights into global trends, the data was grouped by year, aggregating emissions across all countries to create a worldwide emissions dataset for each sector. However, global aggregation presented challenges, such as:  
- **Loss of Specificity**: Summing up data blurred country-specific patterns and regional differences important for accurate forecasting.  
- **Localized Patterns**: Each country exhibited unique emissions trends, better captured by training separate models for each country.  

This motivated the development of country-specific models to enhance forecasting accuracy and capture localized trends.  

## Project Phases  

### Phase 1: Data Exploration and Preprocessing  
- Conducted exploratory data analysis (EDA) to examine trends and patterns in the dataset.  
- Preprocessed the data, including handling missing values, normalizing features, and preparing it for model development.  

### Phase 2: Initial Model Development  
1. **Linear Regression**  
   - Chosen for its simplicity and ability to establish a baseline performance.  
   - Provided insights into data relationships and patterns.  

2. **LSTM-RNN 1**  
   - Transitioned to LSTM-RNN to capture temporal correlations in time-series data.  
   - Demonstrated improved predictive accuracy over Linear Regression by leveraging the sequential nature of the dataset.  

### Phase 3: Advanced Modeling and Country-Specific Analysis  
1. **LSTM-RNN 2**  
   - Enhanced version of the initial LSTM-RNN, featuring refined hyperparameters.  
   - Addressed overfitting and improved the robustness of predictions.  

2. **Country-Specific Modeling (`country.py`)**  
   - Trained separate models for each country to overcome limitations of global aggregation.  
   - Key motivations:  
     - **Preservation of Specificity**: Captured country-specific patterns and regional trends.  
     - **Localized Insights**: Allowed flexibility to fine-tune models per country.  
     - **Improved Suitability for Small Datasets**: LSTM-RNNs effectively handled 30 years of single-country data, improving temporal relationship modeling.  

## Results  
- **Linear Regression vs. LSTM-RNN**: Transitioning to LSTM-RNN significantly improved the model's ability to capture time-series patterns.  
- **Country-Specific Models**: Training individual models for each country enhanced accuracy and highlighted unique regional trends that were obscured in global data aggregation.  
- **Refinements in LSTM-RNN**: Hyperparameter tuning in LSTM-RNN 2 mitigated overfitting, delivering robust predictions.  

## Files  
- **Linear_regression.ipynb**: Notebook implementing and analyzing the Linear Regression model.  
- **LSTM-RNN.ipynb**: Initial LSTM-RNN implementation (Phase 2).  
- **LSTM-RNN 2.ipynb**: Refined LSTM-RNN model with optimized hyperparameters (Phase 3).  
- **country.py**: Script for country-specific modeling, training separate models for each country.  

## Prerequisites

To run this project, ensure you have the following installed:

* Python 3.6 or higher
* pip for managing Python packages
* Jupyter Notebook or JupyterLab
* Required Python libraries (listed below)
* import pandas as pd
* import numpy as np
* import os
* from tensorflow import keras
* from keras.models import Sequential
* from keras.layers import LSTM, Dense
* from sklearn.preprocessing import MinMaxScaler
* from sklearn.metrics import mean_squared_error
* import matplotlib.pyplot as plt
* from tqdm import tqdm

## Installation
1. Clone the repository:
   * git clone https://github.com/pranathy-ms/Carbon-Emissions-Projections.git
2. Install required dependencies:
      * ```pip install jupyter```
      * ```pip install -r requirements.txt```
3. Download the dataset:
  * Ensure the dataset ghg-emissions-by-sector-stacked.csv is located in the same directory as the Jupyter Notebooks. This dataset contains historical greenhouse gas emissions data by sector.

### How to Run the Jupyter Notebooks
1. Start Jupyter Notebook:
  * After installing the dependencies, start the Jupyter Notebook server:
"jupyter notebook"
2. Open the Notebooks:
  * Navigate to the .ipynb files in the Jupyter interface and open the notebooks to run.
3. Run the Cells:
Once the notebook is open, you can run the cells sequentially. Make sure to run the initial setup cells first (e.g., importing libraries and loading the dataset), followed by the cells containing the model definition, training, and evaluation code.

### How to Run the country.py Script
1. Navigate to the folder containing the script. For example: ```cd /path/to/your/project```
2. Run the script: ```python country.py```

