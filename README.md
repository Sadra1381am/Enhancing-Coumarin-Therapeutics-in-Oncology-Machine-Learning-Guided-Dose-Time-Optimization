# Enhancing Coumarin Therapeutics in Oncology: Machine Learning-Guided Dose-Time Optimization and Experimental Validation

This repository contains the complete computational pipeline for optimizing coumarin-based cancer therapeutics using machine learning. The framework identifies optimal dose-time combinations across different cancer types to achieve target viability (≈50%) while ensuring reliability through Gaussian Mixture Model filtering.

## Repository Structure:
├── Machine_Learning_Models/          # Core ML implementation
│   ├── HistGradientBoostingRegressor.py
│   ├── VotingRegressor.py           # Ensemble (CatBoost, XGBoost, LGBM)
│   ├── CatBoostRegressor.py
│   ├── RandomForestRegressor.py
│   └── Weighted_Median_Aggregation.py
├── Visualization/                    # Plotting and analysis
│   ├── Dose_Time_Regressors/        # Regression analysis per coumarin
│   ├── Bubble_Plots/                # Dose-time-viability relationships
│   ├── Flowchart/                   # Workflow visualization
│   └── Treemaps/                    # Data composition analysis
└── Data/                            # Dataset

## Key Features:
Multi-Model Approach: Implements 4 robust ML models with cross-validation
Reliability Filtering: Gaussian Mixture Model for cancer type selection
Dose-Time Optimization: Predicts optimal combinations for target viability
Weighted Consensus: Aggregates predictions across all models
Comprehensive Visualization: Multiple plotting techniques for result interpretation

## Supported Coumarins:
Auraptene (24, 48, 72, 96h time points)
Umbelliprenin (24, 48, 72h)
Galbanic Acid (24, 48, 72h)
Esculetin (24, 48, 72h)

## Models Used:
HistGradientBoostingRegressor
VotingRegressor (CatBoost + XGBoost + LightGBM)
CatBoostRegressor
RandomForestRegressor

## Evaluation Metrics:
MSE, MAE, Median Absolute Error, R² Score
5-fold cross-validation
Feature importance analysis

## Outputs:
Trained model files (.pkl)
Evaluation reports (CSV)
Feature importance plots (TIFF)
Prediction reports with optimal dose-time combinations
Consensus results via weighted median aggregation

## Usage
Prepare your dataset in Total_Data.csv format
Run individual model scripts or the complete pipeline
Review generated reports in Result/Reports/
Use trained models for new predictions

## Citation:
If you use this work in your research, please cite our accompanying paper (reference to be added).
