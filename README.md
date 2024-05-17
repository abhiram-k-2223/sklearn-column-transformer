# Using ColumnTransformer in sklearn for Data Preprocessing

## Introduction
This repository demonstrates the usage of `ColumnTransformer` from the `sklearn.compose` module for preprocessing data in a machine learning pipeline. Additionally, it provides a manual coding approach to achieving similar preprocessing steps for comparison.

## Dependencies
- Python 3.x
- pandas
- numpy
- scikit-learn (sklearn)

## File Structure
- `columntransformer.ipynb`: Jupyter notebook containing code for demonstrating the usage of `ColumnTransformer` for data preprocessing.
- `covid_toy.csv`: Sample dataset used for demonstration.
- `README.md`: This markdown file providing an overview of the repository.

## Usage

### 1. Dataset
Ensure that your dataset is in a compatible format (e.g., CSV) and accessible from your working directory or provide the correct path to the dataset in the code.

### 2. Jupyter Notebook
Open `columntransformer.ipynb` in a Jupyter notebook environment. This notebook contains the code demonstrating two approaches:
- **Ordinary Approach:** Manually coding the preprocessing steps.
- **ColumnTransformer Approach:** Utilizing `ColumnTransformer` for streamlined preprocessing.

### 3. Manual Coding Approach
In the manual coding approach:
- Data is loaded using `pandas.read_csv()`.
- Missing values are imputed using `SimpleImputer`.
- Nominal categorical variables are encoded using `OneHotEncoder`.
- Ordinal categorical variables are encoded using `OrdinalEncoder`.
- Labels are encoded using `LabelEncoder`.
- Finally, data is concatenated to form the transformed feature set.

### 4. ColumnTransformer Approach
In the ColumnTransformer approach:
- A `ColumnTransformer` object is initialized with a list of transformers.
- Each transformer specifies the preprocessing steps for a subset of columns.
- The `transformers` argument accepts a tuple containing a name, a transformer, and the columns it operates on.
- The `remainder` parameter specifies what to do with columns not specified in transformers (e.g., 'passthrough' to keep them unchanged).
- Data is transformed using `fit_transform()` for training data and `transform()` for test data.

## Conclusion
Both approaches achieve the same preprocessing tasks, but the ColumnTransformer approach offers a more concise and scalable solution, especially for datasets with multiple types of features. It enhances code readability and simplifies the integration of preprocessing into a machine learning pipeline.
