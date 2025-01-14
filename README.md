# Titanic Dataset EDA and Visualization

## Overview
This project involves conducting **Exploratory Data Analysis (EDA)** and creating insightful visualizations of the Titanic dataset. The goal is to analyze the dataset, uncover hidden patterns, and present the findings in a visually appealing and informative manner.

## Objectives
- Perform comprehensive EDA on the Titanic dataset.
- Clean and preprocess the data for analysis.
- Visualize key trends, patterns, and relationships within the dataset.
- Generate meaningful insights about the passengers, survival rates, and other variables.

## Dataset
- **Source:** [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)  
- **File Name:** `titanic.csv`  

### Columns in the Dataset
1. **PassengerId**: Unique ID for each passenger.
2. **Survived**: Survival indicator (0 = No, 1 = Yes).
3. **Pclass**: Passenger class (1 = 1st, 2 = 2nd, 3 = 3rd).
4. **Name**: Passenger name.
5. **Sex**: Gender.
6. **Age**: Age of the passenger.
7. **SibSp**: Number of siblings/spouses aboard.
8. **Parch**: Number of parents/children aboard.
9. **Ticket**: Ticket number.
10. **Fare**: Fare paid for the ticket.
11. **Cabin**: Cabin number.
12. **Embarked**: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).

## Steps to Reproduce
### 1. Installation
Ensure you have the required dependencies installed. Use the following command:
```bash
pip install pandas numpy matplotlib seaborn
```

### 2. Load the Dataset
Upload the Titanic dataset (`titanic.csv`) to your working directory and load it in the Jupyter Notebook using:
```python
import pandas as pd

data = pd.read_csv("titanic.csv")
```

### 3. Exploratory Data Analysis
- Check the first few rows of the dataset:
  ```python
  print(data.head())
  ```
- Understand the dataset structure:
  ```python
  print(data.info())
  print(data.describe())
  ```
- Check for missing values:
  ```python
  print(data.isnull().sum())
  ```

### 4. Data Cleaning
- Handle missing values (e.g., fill or drop).
- Convert categorical variables to numerical ones if required.

### 5. Visualizations
Use libraries like `matplotlib` and `seaborn` to create:
- Survival rates by gender:
  ```python
  sns.barplot(x="Sex", y="Survived", data=data)
  ```
- Survival rates by class:
  ```python
  sns.barplot(x="Pclass", y="Survived", data=data)
  ```
- Age distribution:
  ```python
  sns.histplot(data["Age"].dropna(), bins=20)
  ```
- Correlation heatmap:
  ```python
  sns.heatmap(data.corr(), annot=True, cmap="coolwarm")
  ```

## Key Insights
- **Gender and Survival**: Female passengers had a significantly higher survival rate.
- **Class and Survival**: Passengers in 1st class were more likely to survive compared to those in 2nd and 3rd classes.
- **Age Distribution**: Younger passengers had a higher survival probability.

## Directory Structure
```
Titanic_EDA/
|-- README.md
|-- titanic.csv
|-- eda_visualization.ipynb
|-- requirements.txt
```

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/titanic-eda.git
   ```
2. Open the Jupyter Notebook:
   ```bash
   jupyter notebook eda_visualization.ipynb
   ```
3. Run the cells step-by-step to reproduce the analysis.

## Dependencies
- Python 3.7+
- pandas
- numpy
- matplotlib
- seaborn

Install dependencies using:
```bash
pip install -r requirements.txt
```

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements
- [Kaggle](https://www.kaggle.com) for providing the Titanic dataset.
- [Seaborn](https://seaborn.pydata.org) and [Matplotlib](https://matplotlib.org) for visualization tools.

---

Feel free to reach out for questions or contributions!

