# Data Cleaning using Python

## 📌 Project Overview

This project focuses on identifying and cleaning common data-quality issues in a public dataset. The Titanic dataset was selected for this task and cleaned using Python and Pandas.

The main objectives were to identify:

- Missing values
- Duplicate records
- Incorrect data types
- Inconsistent values
- Invalid values

## 📊 Dataset

**Dataset:** Titanic Dataset

**Source:** Publicly available Titanic passenger dataset

The dataset contains information about Titanic passengers, including passenger class, age, gender, fare, ticket information, cabin information, and survival status.

## 🛠️ Tools Used

- Python
- Pandas
- NumPy
- Jupyter Notebook
- GitHub

## 🔍 Data Quality Issues Identified

### 1. Missing Values

Missing values were checked using:

```python
df.isnull().sum()
```

Missing values were identified mainly in:

- `Age`
- `Cabin`
- `Embarked`

### 2. Duplicate Records

Duplicate records were identified using:

```python
df.duplicated().sum()
```

Duplicate records, if present, were removed using:

```python
df.drop_duplicates(inplace=True)
```

### 3. Incorrect Data Types

The dataset data types were inspected using:

```python
df.dtypes
```

Numeric fields such as `Age` and `Fare` were converted to appropriate numeric data types.

### 4. Inconsistent Values

Text and categorical fields were standardized.

For example:

```python
df['Sex'] = df['Sex'].str.strip().str.lower()
```

and:

```python
df['Embarked'] = df['Embarked'].str.strip().str.upper()
```

This helped maintain consistent formatting.

## 🧹 Data Cleaning Performed

| Issue | Cleaning Method |
|---|---|
| Missing Age | Replaced with median age |
| Missing Embarked | Replaced with mode |
| Missing Cabin | Replaced with `Unknown` |
| Duplicate records | Removed |
| Extra spaces | Removed using `str.strip()` |
| Inconsistent capitalization | Standardized |
| Numeric data types | Converted using `pd.to_numeric()` |
| Invalid values | Checked using validation conditions |

## ✅ Validation

After cleaning, the dataset was checked again for:

- Missing values
- Duplicate records
- Data types
- Invalid values
- Consistency of categorical fields

## 📁 Repository Structure

```text
task-1-data-cleaning/
│
├── data/
│   ├── titanic_raw.csv
│   └── titanic_cleaned.csv
│
├── notebook/
│   └── data_cleaning.ipynb
│
├── README.md
│
└── requirements.txt
```

## 📌 Output

The cleaned dataset is available as:

`titanic_cleaned.csv`

The complete cleaning process is documented in:

`data_cleaning.ipynb`

## 👨‍💻 Author

**Ayush Pathak**

B.Tech Computer Engineering Student


