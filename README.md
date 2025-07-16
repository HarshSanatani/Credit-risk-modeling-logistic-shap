# README for EDA Credit Loan Analysis

## Project Overview
This project involves an Exploratory Data Analysis (EDA) of credit loan data to identify key attributes that differentiate defaulters (TARGET=1) from non-defaulters (TARGET=0). The analysis is based on two datasets: `Application.csv` and `Previous_Application.csv`.

## Objective
- Conduct EDA to uncover trends and patterns in the data.
- Identify attributes strongly associated with loan defaulters.
- Provide actionable insights for risk assessment and loan approval processes.

## Datasets
1. **Application.csv**: Contains current loan application data with a `TARGET` variable indicating default status.
2. **Previous_Application.csv**: Contains historical loan application data.

## Approach
1. **Data Import**: Datasets were imported into a Jupyter Notebook for analysis.
2. **Meta Data Check**: Initial inspection of data dimensions, missing values, and general structure.
3. **Data Cleaning**: Handling missing values using imputation (mode, mean, median).
4. **Data Imbalance Check**: Analyzed the distribution of defaulters vs. non-defaulters.
5. **Outlier Detection**: Identified and analyzed outliers in numerical columns.
6. **Univariate & Multivariate Analysis**: Explored trends and correlations among variables.

## Key Findings
### Data Imbalance
- Both datasets exhibited a 9:1 imbalance between non-defaulters and defaulters.

### Outliers
- Columns like `AMT_GOODS_PRICE`, `AMT_CREDIT`, and `AMT_APPLICATION` had higher distribution values for defaulters, with noticeable outliers.

### Segmented Univariate Analysis
- **Previous Application**:
  - Loan rejections were primarily due to 'HC' and 'LIMIT' codes.
  - Defaulters were more prevalent in categories like 'Refusal to give reason', 'Money for third Person', and 'Hobby'.
- **Application**:
  - Clients with more children and family members had higher default rates.
  - Married (non-civil) or single clients formed the majority.

### Correlation Analysis
- **Previous Application**:
  - `AMT_APPLICATION` was highly correlated with `AMT_CREDIT`, `AMT_GOODS_PRICE`, and `AMT_ANNUITY`.
- **Application**:
  - `AMT_CREDIT` and `AMT_GOODS_PRICE` were directly correlated.
  - `AMT_INCOME_TOTAL` showed no significant correlation with other financial variables.

### Multivariate Analysis
- Defaulters often received higher loan amounts for goods in categories like 'Additional Service', 'Direct Sales', and 'Education'.

## Conclusions
- The data imbalance suggests the need for techniques like resampling or weighted models in predictive modeling.
- Outliers in financial columns highlight the importance of robust risk assessment for high-value loans.
- Specific loan purposes and client demographics (e.g., family size) are strong indicators of default risk.
- Correlations between financial variables can simplify feature selection for predictive models.

## Repository Structure
- **Notebooks**: Contains the Jupyter Notebook with the full EDA code.
- **Data**: Directory for the datasets (`Application.csv` and `Previous_Application.csv`).
- **Results**: Summary of findings and visualizations.

## How to Use
1. Clone the repository.
2. Ensure the datasets are placed in the `Data` folder.
3. Run the Jupyter Notebook to reproduce the analysis.

## Dependencies
- Python 3.x
- Libraries: Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

## Author
Harshraj Chavda  
Email: harshchavda439@gmail.com  

## License
This project is open-source and available under the MIT License.
