# Automated, Weighted, Monotonic Weight of Evidence (WoE) Transformation Module in Credit Risk Modeling

## Overview
This project implements an **Automated, Weighted, Monotonic Weight of Evidence (WoE) Transformation Module** designed for **credit risk modeling**. It enhances the transformation of both **categorical** and **continuous features** into monotonic WoE values, supporting downstream modeling tasks.

The algorithm aims to automate the transformation of both categorical and numerical variables into monotonic WoE values, which are essential for making the relationship between an attribute and credit risk more interpretable, regulatory-compliant, and accurate.

Data Disclaimer:
1. All data utilized in this project is simulated and does not contain any sensitive or proprietary information.
1. This project serves as a theoretical study to illustrate how the Weight of Evidence (WoE) methodology works.
1. No actual code or proprietary algorithms are shared in this repository to comply with intellectual property policies.

## Features
- **Automated Transformation**: Automatically converts any input variable (categorical or numerical) into WoE values.
- **Monotonicity Enforcement**: Ensures WoE values follow a consistent monotonic trend with risk, improving the interpretability and stability of models.
- **Weighted Data Handling**: Incorporates weights for data points, a novel feature not commonly found in existing WoE transformation methods.
- **Dual-Direction Algorithm**: Provides flexibility by generating WoE values both forward and backward, allowing the modeler to choose the result with the higher Information Value (IV).

## Introduction to Weight of Evidence (WoE)
In credit risk modeling, accurately capturing the relationship between predictive attributes (e.g., age, credit card type) and the likelihood of credit events (e.g., delinquency, default) is essential. Naive methods often fail to represent risk accurately due to the over-emphasis on larger data segments, data imbalance, or non-linearity in the relationship between variables.

The **Weight of Evidence (WoE)** transformation offers a robust solution by converting categorical and continuous variables into log-odds, which simplifies their use in models like **logistic regression**. WoE serves as an effective **pre-processing step** that provides several advantages:
1. **Handling of Categorical Variables**: WoE transforms categories into continuous values, avoiding one-hot encoding and reducing model complexity.
2. **Improved Risk Representation**: WoE expresses predictor-event relationships in odds, offering clearer risk interpretation and reducing overfitting on sparse data.
3. **Addressing Data Imbalance**: WoE adjusts for imbalances, preventing high-frequency, low-risk categories from dominating the model.
4. **Handling Non-Linearity**: WoE bins continuous variables, capturing non-linear patterns missed by untransformed logistic regression models.
5. **Monotonicity**: Ensures a consistent, interpretable relationship between predictor values and risk, improving model accuracy and compliance.

Incorporating monotonicity in WoE transformations further enhances model **accuracy**, **interpretability**, and **regulatory compliance** by ensuring a consistent relationship between predictor values and risk. This module automates the WoE transformation process, accounting for weighted data points, ensuring that the transformation is both efficient and aligned with best practices for credit risk modeling.

## Project Structure
- `code/`  
  Contains example scripts simulating the workflow. The actual code isn't shared due to IP restrictions; these examples are for illustration only.
- `plots/`  
  Includes visualizations generated from simulation data to illustrate outcomes.
- `data/`  
  Contains example datasets for simulations, used purely for demonstration.

## Algorithm Flowchart
Here is the algorithm flowchart:
![Algorithm Flowchart](plots/flowchart.png)

## Figures


## Demo
Introduction to the WoE Algorithm - Explore how the monotonic WoE algorithm operates through a mountaineering analogy.
![Introduction to the WoE Algorithm](plots/demo/WoE_demo.003.png)
Identifying the Trend - The algorithm identifies the overall trend, which is upward in this case, allowing for the transformation of complex data into numerical values.
![Introduction to the WoE Algorithm](plots/demo/WoE_demo.003.png)
Sampling the Data: Running the Algorithm from Left to Right
Data points are sampled from left to right, representing utilization and delinquency rates.
Initializing the WoE Bins
Bins for the Weight of Evidence are initialized while maintaining numerical flexibility.
Backtracking to Ensure Monotonicity
To ensure monotonic WoE values, a new bin is created when values follow the trend; otherwise, bins are merged. If the trend is not followed, backtracking occurs to combine the last two bins and restore monotonicity.
Combining Bins to Ensure Sufficient Data
Bins are combined to ensure that each contains sufficient data for reliable analysis.
Final Result: Forward Pass
The final result displays monotonic WoE values in the forward direction, represented as base camps on the data.

## Requirements
- Python 3.x
- `pandas`, `numpy`, `scipy`, `matplotlib`, `pyspark`
