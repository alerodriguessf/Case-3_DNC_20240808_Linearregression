
# USA Housing Price Analysis and Prediction

This repository contains a Python script designed to analyze and predict housing prices in the USA based on various demographic and regional factors. The project utilizes a combination of data exploration, visualization, and machine learning techniques to achieve accurate predictions.

## Table of Contents

- [Project Overview](#project-overview)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Running the Script](#running-the-script)
- [Data Exploration](#data-exploration)
  - [Dataset Overview](#dataset-overview)
  - [Feature Renaming](#feature-renaming)
  - [Visualizations](#visualizations)
- [Data Preprocessing](#data-preprocessing)
  - [Feature Selection](#feature-selection)
  - [Train-Test Split](#train-test-split)
- [Modeling and Prediction](#modeling-and-prediction)
  - [Linear Regression Model](#linear-regression-model)
  - [Performance Evaluation](#performance-evaluation)
  - [Model Visualization](#model-visualization)
  - [Custom Predictions](#custom-predictions)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

The main objective of this project is to build a predictive model for housing prices in the USA using a linear regression approach. The analysis begins with data exploration and visualization to understand the relationships between variables, followed by the application of machine learning techniques to predict housing prices based on features like average area income, house age, and number of rooms.

## Getting Started

### Prerequisites

To run the script, you need to have the following Python libraries installed:

```bash
pip install pandas seaborn matplotlib plotly cufflinks chart-studio scikit-learn
```

### Running the Script

1. **Data File**: Ensure that the dataset file `USA_Housing.csv` is available in the same directory as the script.
2. **Execution**: The script can be executed in any Python environment, such as Jupyter Notebook or VSCode. It processes the data, performs exploratory data analysis, trains a linear regression model, and makes predictions.

## Data Exploration

### Dataset Overview

The dataset used in this analysis (`USA_Housing.csv`) contains the following key features:
- **Avg. Area Income**: Average income of the area.
- **Avg. Area House Age**: Average age of houses in the area.
- **Avg. Area Number of Rooms**: Average number of rooms per house in the area.
- **Avg. Area Number of Bedrooms**: Average number of bedrooms per house in the area.
- **Area Population**: Population of the area.
- **Price**: Dependent variable representing the house price.
- **Address**: Address of the house (not used in the analysis).

### Feature Renaming

To make the feature names more accessible for analysis, the following renaming was performed:
- **Avg. Area Income** -> **Avg_Area_Income**
- **Avg. Area House Age** -> **Avg_Area_House_Age**
- **Avg. Area Number of Rooms** -> **Avg_Area_Number_of_Rooms**
- **Avg. Area Number of Bedrooms** -> **Avg_Area_Number_of_Bedrooms**
- **Area Population** -> **Area_Population**

Additionally, the `Address` column was dropped as it is not relevant to the analysis.

### Visualizations

The script includes various visualizations to explore the data:
- **Box Plots**: Used to examine the distribution of `Avg_Area_Income` and `Price`.
- **Pair Plots**: Generated using `seaborn` to visualize relationships between multiple features.
- **Correlation Heatmap**: Displays the correlation matrix of the features, highlighting relationships between variables.
- **Histogram**: Shows the distribution of house prices.

## Data Preprocessing

### Feature Selection

The analysis focuses on the following features as independent variables (X):
- **Avg_Area_Income**
- **Avg_Area_House_Age**
- **Avg_Area_Number_of_Rooms**
- **Avg_Area_Number_of_Bedrooms**
- **Area_Population**

The dependent variable (Y) is `Price`.

### Train-Test Split

The dataset is split into training and testing sets using an 70-30 split ratio:
- **Training Set**: 70% of the data used to train the model.
- **Testing Set**: 30% of the data used to evaluate model performance.

## Modeling and Prediction

### Linear Regression Model

A linear regression model is trained on the training dataset to predict house prices. The model is implemented using `scikit-learn`'s `LinearRegression` class.

### Performance Evaluation

The performance of the model is evaluated using the R-squared metric (`r2_score`), which measures the proportion of variance in the dependent variable that is predictable from the independent variables.

### Model Visualization

To visualize the model's performance, a comparison between actual and predicted prices is plotted:
- **Blue Line**: Represents actual house prices from the testing set.
- **Red Line**: Represents predicted house prices.

### Custom Predictions

The script allows for custom predictions by inputting specific values for the features. For example:
- **Avg_Area_Income = 50**
- **Avg_Area_House_Age = 30**
- **Avg_Area_Number_of_Rooms = 7**
- **Avg_Area_Number_of_Bedrooms = 5**
- **Area_Population = 200**

The model predicts the house price based on these inputs.

## Contributing

Contributions are welcome! If you have any suggestions or improvements, please feel free to open an issue or submit a pull request.
