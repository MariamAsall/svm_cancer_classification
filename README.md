## Overview

This project focuses on the initial data analysis and preprocessing of the Wisconsin Breast Cancer dataset. The primary goal is to clean the data and perform Exploratory Data Analysis (EDA) to understand the feature distributions. This notebook serves as the foundational step before building a machine learning model to predict whether a tumor is malignant or benign.

The analysis is performed in a Jupyter Notebook and utilizes standard Python libraries for data science, including Pandas, NumPy, and Matplotlib.

---

## Table of Contents

- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Technologies Used](#technologies-used)
- [Setup and Usage](#setup-and-usage)
- [Results & Outcome](#results--outcome)

---

## Dataset

-   **Source:** The project uses the **Wisconsin Breast Cancer dataset**, which is available on Kaggle.
-   **File:** `Cancer_Data.csv`
-   **Description:** The dataset contains features computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. The features describe characteristics of the cell nuclei present in the image.
-   **Key Columns:**
    -   `id`: Patient ID
    -   `diagnosis`: The target variable (M = malignant, B = benign)
    -   `radius_mean`, `texture_mean`, `perimeter_mean`, etc.: 30 real-valued numerical features used for prediction.

---

## Project Workflow

The notebook follows a structured approach to data analysis:

1.  **Data Loading:** The `Cancer_Data.csv` file is loaded into a Pandas DataFrame.
2.  **Initial Inspection:**
    -   The data's structure, shape, and data types are examined using `.head()` and `.info()`.
    -   Checks for duplicate rows and missing values are performed using `.duplicated().sum()` and `.isnull().sum()`.
3.  **Data Cleaning:**
    -   An empty and unnecessary column, `Unnamed: 32`, is identified and dropped from the DataFrame.
4.  **Exploratory Data Analysis (EDA):**
    -   Histograms are generated for all 30 numerical features to visualize their distributions. This helps in understanding the scale, skewness, and range of each feature.

---

## Technologies Used

-   **Language:** Python 3
-   **Libraries:**
    -   [Pandas](https://pandas.pydata.org/): For data manipulation and analysis.
    -   [NumPy](https://numpy.org/): For numerical operations.
    -   [Matplotlib](https://matplotlib.org/): For data visualization.
-   **Environment:** Jupyter Notebook

---

## Setup and Usage

To run this project locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone 
    cd 
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install pandas numpy matplotlib jupyterlab
    ```

4.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    Then, open and run the notebook file to see the analysis.

---

## Results & Outcome

-   **Cleaned Dataset:** The primary outcome is a cleaned DataFrame, ready for feature engineering and model training.
-   **Data Insights:** The histograms provide a clear visual summary of the data, showing that many features have a right-skewed distribution. This insight can inform decisions about feature scaling or transformation in the subsequent modeling phase.
