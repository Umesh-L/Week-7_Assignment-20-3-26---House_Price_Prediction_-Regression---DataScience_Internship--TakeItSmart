# House Price Prediction (Regression) ML Project

This project builds and evaluates regression models to predict house prices using structured housing features such as square footage, number of rooms, lot size, and neighborhood quality.

## Project Summary

- Project type: Supervised Machine Learning (Regression)
- Main objective: Predict house prices accurately and compare model performance
- Main notebook: House_Price_Prediction_(Regression).ipynb
- Dataset records: 1000 rows
- Algorithms used:
  - Linear Regression
  - K-Nearest Neighbors Regressor (KNN)

## Folder Structure

- House_Price_Prediction_(Regression).ipynb
- Input Dataset and project info pdf/
  - house_price_regression_dataset.csv
  - Machine Learning Task1_new.pdf
- output snapshots/
  - Distribution of House Prices.png
  - Square Footage vs House Price.png
  - Corelation Heatmap.png
  - Boxplot for Square Footage.png
  - Log Transformed House Prices.png
  - Linear Regression and KNN Regression final output.png

## Dataset Details

File: Input Dataset and project info pdf/house_price_regression_dataset.csv

Columns used:

1. Square_Footage
2. Num_Bedrooms
3. Num_Bathrooms
4. Year_Built
5. Lot_Size
6. Garage_Size
7. Neighborhood_Quality
8. House_Price (target, original scale)

## End-to-End Workflow

1. Imported required libraries for data handling, visualization, and modeling
2. Loaded and inspected dataset shape and schema
3. Checked and handled missing values
4. Checked and removed duplicates (if any)
5. Performed EDA:
   - House price distribution
   - Square footage vs house price relationship
   - Correlation heatmap
6. Performed feature engineering:
   - Outlier handling with IQR on Square_Footage
   - Log transformation on target: Log_House_Price = log1p(House_Price)
7. Split data into train and test sets
8. Applied StandardScaler to feature set
9. Trained models:
   - Linear Regression
   - KNN Regressor (n_neighbors=5)
10. Evaluated with:
   - MAE
   - MSE
   - RMSE
   - MAPE
   - R2
   - Adjusted R2

## Key Observations

- Square_Footage shows a very strong positive relationship with House_Price.
- In the latest heatmap snapshot, Square_Footage is highly correlated with House_Price (approximately 0.99), and House_Price is also strongly correlated with Log_House_Price (approximately 0.97).
- Log transformation helped stabilize the target distribution.
- Outlier filtering with IQR did not reduce row count in the saved run output (dataset remained 1000 rows).
- Linear Regression performed better than KNN on this dataset.

## Final Model Comparison (from notebook conclusion)

- Linear Regression:
  - R2 Score: 0.9304
  - Adjusted R2: 0.9279
  - RMSE: 66,971.31
- KNN Regression:
  - R2 Score: 0.8934
  - Adjusted R2: 0.8895
  - RMSE: 82,897.69

Verdict: Linear Regression is the better-performing model than K-Nearest Neighbour Regression.

## Output Visualizations

### 1) Distribution of House Prices
![Distribution of House Prices](output%20snapshots/Distribution%20of%20House%20Prices.png)

### 2) Square Footage vs House Price
![Square Footage vs House Price](output%20snapshots/Square%20Footage%20vs%20House%20Price.png)

### 3) Correlation Heatmap
![Correlation Heatmap](output%20snapshots/Corelation%20Heatmap.png)

### 4) Boxplot for Square Footage
![Boxplot for Square Footage](output%20snapshots/Boxplot%20for%20Square%20Footage.png)

### 5) Log Transformed House Prices
![Log Transformed House Prices](output%20snapshots/Log%20Transformed%20House%20Prices.png)

### 6) Final Model Output Snapshot
![Final Model Output](output%20snapshots/Linear%20Regression%20and%20KNN%20Regression%20final%20output.png)

## Project Explanation Video
https://github.com/user-attachments/assets/87b8bf6c-1817-499c-bd00-adada0272117

## Tech Stack

- Python
- Jupyter Notebook
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## How to Run

1. Clone this repository.
2. Keep dataset path unchanged or update it in the notebook.
3. Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

4. Open House_Price_Prediction_(Regression).ipynb.
5. Run all cells from top to bottom.

## Assignment Reference

- The assignment/problem statement document is included at:
  - Input Dataset and project info pdf/Machine Learning Task1_new.pdf

## Author

- Name: Umesh L
- Internship/Company: DataScience Internship | Take It Smart
- Week: Week-7 Assignment (20-3-26)
