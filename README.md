## Loan Data Analysis

This project analyzes a loan data set (`loan_data.csv`) to explore factors potentially influencing loan approval, interest rates, and repayment behavior. 

**Libraries Used:**

* pandas (pd)
* numpy (np)
* matplotlib.pyplot (plt)
* seaborn (sns)

**Data Exploration:**

* **Data Loading:** The script reads the CSV file (`loan_data.csv`) using pandas.
* **Data Overview:** Initial data is displayed using `head()` and `info()` methods to understand data structure and presence of missing values.
* **Data Cleaning:** Missing values are not explicitly handled in this code, but you can add steps to address them if necessary.

**Analysis Steps:**

1. **Loan Purposes:**
    * The script identifies the distribution of loan purposes using `value_counts()`.
    * A bar chart visualizes the number of loans for each purpose (using `plot(kind='bar')`).

2. **Credit Policy and FICO Score:**
    * The script calculates the average FICO score for loans with different credit policy outcomes (`credit.policy`).
    * The results are displayed, suggesting a potential correlation between credit policy and FICO score.

3. **Interest Rate by Purpose:**
    * The script calculates the average interest rate for each loan purpose.
    * A bar chart visualizes the average interest rate by purpose.

4. **Loan Repayment Status:**
    * A new binary variable `not.fully.paid` is created to categorize loans as "Fully Paid" or "Not Fully Paid."
    * The script displays the distribution of loans across these categories.
    * A bar chart visualizes the distribution of fully and not fully paid loans.

5. **Loan Repayment by Purpose:**
    * The script analyzes the repayment status (fully paid or not) for each loan purpose using `groupby()`.
    * The results are displayed as a table (crosstabulation).
    * The repayment rates are further presented as percentages.
    * A heatmap visualizes the repayment rates by purpose (using seaborn).

6. **Interest Rate and Repayment:**
    * The script calculates the average interest rate for fully and not fully paid loans.
    * The results are displayed, suggesting a potential correlation between repayment status and interest rate.
    * The percentage difference in interest rate between these groups is calculated and displayed.

7. **Revolving Credit Utilization and Interest Rate:**
    * The correlation coefficient between revolving credit utilization (`revol.util`) and interest rate (`int.rate`) is calculated.
    * The results are displayed, suggesting a moderate positive correlation.
    * A scatter plot visualizes the relationship between revolving credit utilization and interest rate (using seaborn).

8. **FICO Score and DTI by Repayment:**
    * The script calculates the average FICO score and DTI ratio for fully and not fully paid loans.
    * The results are displayed, suggesting potential correlations between these factors and repayment behavior.

**Findings:**

* The analysis reveals potential relationships between loan purposes, creditworthiness (FICO score), debt-to-income ratio (DTI), revolving credit utilization, interest rates, and loan repayment behavior.
* Borrowers with higher FICO scores and lower DTI ratios seem more likely to repay loans fully.
* Loans for specific purposes (e.g., small business) might have higher average interest rates.
* There appears to be a positive correlation between revolving credit utilization and interest rates, suggesting borrowers with higher credit utilization might receive higher interest rates.

