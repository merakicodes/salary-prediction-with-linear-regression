# Salary Prediction with Linear Regression

A beginner machine learning project that uses years of experience to predict salary. I adapted a linear regression practice notebook to work with a CSV dataset from Kaggle.

## Dataset

Source: [Salary Data — Simple Linear Regression on Kaggle](https://www.kaggle.com/datasets/karthickveerakumar/salary-data-simple-linear-regression)

The dataset contains two columns:

- **YearsExperience:** the input used to make predictions.
- **Salary:** the numerical value the model tries to predict.

## How It Works

1. Load `Salary_Data.csv` using pandas.
2. Separate the input (`X`) from the target (`y`).
3. Split the data into 80% training data and 20% test data, using `random_state=1`.
4. Train a scikit-learn `LinearRegression` model.
5. Predict salaries for the test rows.
6. Compare predictions with actual salaries and calculate mean squared error (MSE).

## Results

The model produced these example predictions on the test set:

| Years of experience | Actual salary | Predicted salary |
|---|---:|---:|
| 5.3 | 83,088 | 75,074.51 |
| 7.1 | 98,273 | 91,873.81 |
| 3.9 | 63,218 | 62,008.38 |
| 6.0 | 93,940 | 81,607.57 |
| 4.5 | 61,111 | 67,608.15 |
| 6.8 | 91,738 | 89,073.92 |

**Test MSE:** 51,338,023.49

The square root of this MSE gives an **RMSE of approximately 7,165.06**, expressed in the same units as salary. Lower MSE and RMSE indicate smaller prediction errors.

These results show that the model learned a relationship between experience and salary, although its predictions do not exactly match the recorded salaries.

## What I Learned

- Linear regression predicts numerical outputs.
- Training data teaches the model; test data helps evaluate predictions on unseen examples.
- pandas DataFrames and NumPy arrays have different methods and shapes.
- Inputs should be two-dimensional, while the target can be one-dimensional.
- Prediction errors are expected, and their size helps assess model performance.

## Run the Project

You will need Python, Jupyter Notebook, and these libraries:

```bash
pip install pandas numpy scikit-learn jupyter
```

Download `Salary_Data.csv` from the linked Kaggle dataset and place it in the same folder as the notebook. Open the notebook in Jupyter and run the cells in order.

## Limitations

This is an educational project using a small dataset and a single input feature. Salary also depends on factors such as job role, location, and qualifications, which this model does not include.

The results come from one train/test split and should not be treated as a reliable estimate of real-world salary prediction performance.

## Next Steps

- Plot actual and predicted salaries.
- Calculate mean absolute error (MAE).
- Compare the model against a baseline that predicts the average training salary.
- Explore a dataset with additional relevant features.

## Acknowledgments

This project started from the provided `LinearRegressionExemplar.ipynb` practice notebook. I adapted it to load the Kaggle salary dataset and explored how to interpret its predictions and errors.

Credit for the dataset belongs to its contributor on Kaggle.
