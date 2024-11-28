# Greenhouse Gas Emissions Forecasting with LSTM
This project predicts greenhouse gas emissions by sector using Long Short-Term Memory (LSTM) models. The model is trained on historical emissions data and predicts future emissions for each sector. This document provides instructions on how to run the program, along with the required dependencies and setup steps.

## Table of Contents

* Prerequisites
* Installation
* Running the Notebooks

## Prerequisites

To run this project, ensure you have the following installed:

* Python 3.6 or higher
* pip for managing Python packages
* Jupyter Notebook or JupyterLab
* Required Python libraries (listed below)

## Installation
1. Clone the repository:
   * git clone https://github.com/pranathy-ms/Carbon-Emissions-Projections.git
2. Install required dependencies: ```pip install -r requirements.txt```
3. Download the dataset:
  * Ensure the dataset ghg-emissions-by-sector-stacked.csv is located in the same directory as the Jupyter Notebooks. This dataset contains historical greenhouse gas emissions data by sector.

## Running the Notebooks
1. Start Jupyter Notebook:
  * After installing the dependencies, start the Jupyter Notebook server:
"jupyter notebook"
2. Open the Notebooks:
  * Navigate to the .ipynb files in the Jupyter interface and open the notebooks to run.
3. Run the Cells:
Once the notebook is open, you can run the cells sequentially. Make sure to run the initial setup cells first (e.g., importing libraries and loading the dataset), followed by the cells containing the model definition, training, and evaluation code.
