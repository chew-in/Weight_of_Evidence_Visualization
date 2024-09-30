# Automated, Weighted, Monotonic Weight of Evidence (WoE) Transformation Module in Credit Risk Modeling

## Overview
This project implements an **Automated, Weighted, Monotonic Weight of Evidence (WoE) Transformation Module** designed for **credit risk modeling**. It enhances the transformation of both **categorical** and **continuous features** into monotonic WoE values, supporting downstream modeling tasks.

## Features
- **Automated binning**: Automatically determines bins for continuous features.
- **Weighted WoE transformation**: Incorporates optional weighting for feature transformation.
- **Monotonicity constraint**: Ensures that WoE transformation follows a monotonic trend.
- **Supports categorical and continuous variables**: Handles different data types seamlessly.

## Requirements
- Python 3.x
- `pandas`, `numpy`, `scipy`, `matplotlib`
- `optbinning` (optional but recommended for optimal binning)

## Installation
To install the required packages, run:
```bash
pip install pandas numpy scipy matplotlib optbinning
