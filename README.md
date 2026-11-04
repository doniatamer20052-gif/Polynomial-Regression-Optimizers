
# Polynomial Regression – Optimizers Comparison

## Project Overview

This project implements Polynomial Regression using five optimization algorithms from scratch with Python and NumPy.

The objective is to compare the convergence behavior and predictive performance of different optimizers.

## Dataset

**Concrete Compressive Strength Dataset**

Source: https://www.kaggle.com/datasets/elikplim/concrete-compressive-strength-data-set

- Original Samples: 1030
- Samples After Cleaning: 1005
- Input Features: 8
- Target: Concrete Compressive Strength
- Training Samples: 804
- Testing Samples: 201

## Model Configuration

- Model: Polynomial Regression
- Polynomial Degree: 2
- Polynomial Features: 44
- Train/Test Split: 80% / 20%
- Random State: 42
- Feature Scaling: StandardScaler
- Training Epochs: 2000

## Implemented Optimizers

1. Batch Gradient Descent (GD)
2. Stochastic Gradient Descent (SGD)
3. Mini-Batch Gradient Descent
4. RMSprop
5. Adam

Momentum experiments were also implemented to investigate their effects on optimization.

## Experimental Results

| Optimizer | Final Cost | RMSE | R2 |
|---|---|---|---|
| GD | 0.112916 | 8.3541 | 0.7661 |
| SGD | 0.105816 | 8.2682 | 0.7708 |
| Mini-Batch GD | 0.109029 | 8.2992 | 0.7691 |
| RMSprop | 0.105167 | 8.2814 | 0.7701 |
| Adam | 0.104904 | 8.2800 | 0.7702 |

## Key Findings

- All five optimizers successfully reduced the training loss.
- Adam achieved the lowest final training cost.
- SGD achieved the lowest test RMSE and highest test R2.
- Momentum improved convergence in some experiments but did not consistently improve test performance.
- Learning rates and parameter-update counts differed, so equal epoch counts do not imply equal computational effort.

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Kaggle Notebooks

## Conclusion

All five optimization algorithms successfully trained the same Polynomial Regression model.

The results demonstrate how different optimization strategies affect training loss, convergence behavior, and generalization performance.
