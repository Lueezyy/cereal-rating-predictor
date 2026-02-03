# Cereal Nutrition Rating Predictor

Machine learning project comparing regression models to predict consumer ratings of breakfast cereals based on nutritional content.

## Overview
Built and compared Decision Tree and Random Forest Regression models to analyze how nutritional factors influence cereal ratings. Demonstrates model comparison, hyperparameter tuning, and train/validation split methodology.

**Note:** This project uses a classic ML dataset for educational purposes. While some nutritional values may be outdated, the machine learning techniques and model comparison approach remain valid and transferable to real-world applications.

## Dataset
- **Size:** 78 breakfast cereals
- **Features:** 8 nutritional attributes
  - Calories, Protein, Fat
  - Sodium, Fiber, Carbohydrates
  - Sugars, Vitamins
- **Target:** Consumer rating (continuous variable)

**Dataset Source:** [80 Cereals Dataset](https://www.kaggle.com/datasets/crawford/80-cereals) - Kaggle  

## Technologies
- **Python**
- **Pandas** - Data manipulation and analysis
- **Scikit-Learn** - Machine learning algorithms
  - DecisionTreeRegressor
  - RandomForestRegressor
  - train_test_split
  - mean_absolute_error
- **Jupyter Notebook** - Development environment

## Model Performance

### Decision Tree Regressor
- Tested multiple max_leaf_nodes values: [5, 25, 50, 100, 250, 500]
- Best performance: **MAE of 4.70** (max_leaf_nodes=50)
- Validation MAE: 5.15 (baseline without max_leaf_nodes)

### Random Forest Regressor (Final Model)
- **Mean Absolute Error: 3.94**
- Ensemble method combining multiple decision trees
- Better generalization than single decision tree

## Key Learning Outcomes
- Implemented train/validation split to prevent overfitting
- Performed hyperparameter tuning (max_leaf_nodes optimization)
- Compared single model vs. ensemble methods
- Evaluated models using Mean Absolute Error metric
- Demonstrated proper ML workflow: load → split → train → validate → optimize

## Future Improvements
- Feature importance analysis (which nutritional factors matter most?)
- Additional models: Gradient Boosting, XGBoost
- Cross-validation for more robust evaluation
- Visualization of predictions vs actual ratings
- Feature engineering (ratios like sugar/fiber)
