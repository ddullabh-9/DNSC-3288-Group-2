# Basic information: 
* **John, john@grp2.com, Arjun, arjun@grp2.com, Darshan, darshan@grp2.com, Martin, martin@grp2.com 
* **December 9th 2024
* **Model 0.1
* **License: MIT
* **Model implementation code: https://colab.research.google.com/drive/1s4KHqa7oZ6zvu8oNIp4UOOGSXbFfxC6q#scrollTo=D06vOZTmifBZ 
* **Intended Use:
* **Intended uses: Predict sale price of a piece of Real Estate
* **Intended users: Zillow.com, Homes.com
* **Out-of-scope uses: None

###Training data:
Source of training data
File called train.csv downloaded kaggle dataset
How training data was divided into training and validation data
The decided split between training and validation data was 80% training and 20% validation
Number of rows in training and validation data
There are 1,460 rows in total and 81 columns, and given the 80% and 20% split between training and validation, a result of 1,168 rows for training and 292 rows for validation data was devised
Data dictionary; for each column in the training dataset include:
Name
Modeling role
Measurement level
Description
Note: This is in a csv file 
Test data:
Source of test data
A file named test.csv downloaded from kaggle dataset 
Number of rows in test data
There are 1,459 rows of data with 80 columns
State any differences in columns between training and test data
We dropped SalePrice from the training data because it is the target variable trying to be predicted 
Model details:
Columns used as inputs in the final model: 
RF and XgBoost: OverallQual, GrLivArea, TotalBsmtSF, 2ndFlrSF, 1stFlrSF, LotArea, GarageArea, YearBuilt, BsmtFinSF1, GarageCars
Column(s) used as target(s) in the final model: 
RF and XgBoost: SalePrice
 Type of model: 
RF: Random Forest Regressor 
XgBoost model 
Software used to implement the model: 
RF: scikit-learn and 
XgBoost: xgboost 
Version of the modeling software: 
RF: 1.5.2
XgBoost: xgboost version: 2.1.3
Hyperparameters or other settings of your model
RF: n_estimators=100, random_state=42, max_depth=None, min_samples_split=2, min_samples_leaf=1, bootstrap=True
XgBoost: After doing an grid search: eta = 0.05, depth = 3, min_child = 4
Note: our final submission was an average of the predictions from both the models. We did not stack them. 

Random Forest: 


Quantitative analysis:


Metrics used to evaluate your final model (AUC and AIR)
RF: AUC - 
XgBoost: AUC
State the final values, neatly -- as bullets or a table, of the metrics for all data:
training, validation, and test data
RF: 



XgBoost: Image Below 

Provide any plots related to your data or final model -- be sure to label the plots!




Ethical considerations: 

○ Describe potential negative impacts of using your model: 
■ Math or software problems 
Based on the data, if certain neighborhoods are underrepresented, the calculated predictions may systematically disadvantage specific groups 
Any missing or incorrectly imputed data could result in unwanted bias, especially in key variables such as LotFrontage or GarageType
■ Real-world risks: who, what, when or how 
As mentioned previously, with any potential unwanted biases, these biased predictions could influence areas such as property valuation, which would in turn affect underrepresented or minority communities 
Additionally, the misuse of these predictions could distort market prices or favor certain buyers/sellers
○ Describe potential uncertainties relating to the impacts of using your model:
■ Math or software problems 
There could also be transparency issues. For example, complex models like XGBoost or neural networks may act as "black boxes," making it difficult to explain predictions.
Prediction ranges could also be skewed or not calibrated properly, leading to overconfidence in results 
 	■ Real-world risks: who, what, when or how?
On the economic side of things, property market conditions such as inflation or a potential recession may change or make certain predictions obsolete 
Zoning changes and new legislations in different areas could also impact key predictors such as MSZoning 
○ Describe any unexpected or results
There may be a presence of data anomalies such as outliers which can skew model performance and lead to erratic predictions
Variables could also be misinterpreted, meaning certain variables that have been classified to have lower importance could be perceived as playing a significant role due to the complexity of the data and different variables.

