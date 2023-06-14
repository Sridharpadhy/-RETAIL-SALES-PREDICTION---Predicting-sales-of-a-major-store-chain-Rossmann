# -RETAIL-SALES-PREDICTION---Predicting-sales-of-a-major-store-chain-Rossmann

![image](https://github.com/Sridharpadhy/-RETAIL-SALES-PREDICTION---Predicting-sales-of-a-major-store-chain-Rossmann/assets/120051156/e7096a12-b49f-435f-9c16-d52afead4f68)


Explainatory Video : https://drive.google.com/drive/u/2/folders/16Hq2p7zH4X_dl19hfNUDrYbjcH0LiM1d

FILE DETAILS:

1. Data and Resources - Csv zip file of the raw data provided.
2. Collab : The main google collab containing all the project work.

Overview:

Rossmann operates over 3,000 drug stores in 7 European countries.Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. The task is to forecast the "Sales" column for the test set.

Problem Statement :

"Develop a machine learning model to predict the sales of the Rossmann store chain based on historical data and relevant features. The objective is to accurately forecast the future sales of each store in order to optimize inventory management, staffing, and promotional strategies. The model should consider factors such as store-specific information, promotional activities, competition, seasonality, and other relevant variables. The predictions will help Rossmann make informed decisions to maximize revenue, minimize costs, and improve overall business performance."

Variables Description :

*Rossmann Stores Data.csv - historical data including Sales 
*store.csv - supplemental information about the stores

##Data fields

Most of the fields are self-explanatory. The following are descriptions for those that aren't.

Id - an Id that represents a (Store, Date) duple within the test set

Store - a unique Id for each store

Sales - the turnover for any given day (this is what you are predicting)

Customers - the number of customers on a given day

Open - an indicator for whether the store was open: 0 = closed, 1 = open

StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None

SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools

StoreType - differentiates between 4 different store models: a, b, c, d

Assortment - describes an assortment level: a = basic, b = extra, c = extended

CompetitionDistance - distance in meters to the nearest competitor store

CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened

Promo - indicates whether a store is running a promo on that day

Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating

Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2

PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store


Process and Result ::

During the time of our analysis, we initially did EDA on all the features of our datset. We first analysed our dependent variable, 'Sales' and also transformed it. Next we analysed categorical variable and dropped the variable who had majority of one class, we also analysed numerical variable, found out the correlation, distribution and their relationship with the dependent variable using corr() Function and for multicollinearity we use VIF Function defined by us. We also removed some numerical features who had mostly 0 values and hot encoded the categorical variables.

Next we implemented 8 machine learning algorithms Linear Regression,lasso,ridge,elasticnet,decission tree, Random Forest and XGBoost and Gredient Boosting. We did hyperparameter tuning to improve our model performance.

The Important Features are

Customers
Competition Distance
Store Type
Promo
we can conculed that ❗

- The sales in the month of December is the highest sales among others.
- The Sales is highest on Monday and start declining from Tuesday to Saturday and on Sunday Sales almost near to Zero.
- Those Stores who takes participate in Promotion got their Sales increased.
- Type of Store plays an important role in opening pattern of stores. All Type ‘b’ stores never closed except for refurbishment or other reason.
- We can observe that most of the stores remain closed during State holidays. But it is interesting to note that the number of stores opened during School Holidays were more than that were opened during State Holidays.
- The R Squared score of all Liner Regression Algorithm with or without Regularization are quit good which is 0.76.
- The R Squared score of the Decision Tree Regressor model we got 0.83 on test set which is also good.The Random Forest regressor model perform very well amoung the others it was around test 0.96 and train 0.99 which can be considerd as the ideal match .
- The Gradient Boosting Regressor model perform well and give 0.88 R Squared on test set . After Applying GridSearchCV which is a optimal algorithm search tool improve our R Squared score from 0.88 to 0.94 which almost nearly the random forest regression model.
- There is no such over fitting seen.
- We can say that random forest regressor model is our optimal model and can be deploy.
- We can say that random forest regressor model is our optimal model with important feature of customers , competion distance , store_type etc .

WITH VALUES OF ✅

MSE of train dataset: 46652.97111825779

MSE of test dataset: 315640.9403535632

RMSE of train dataset : 215.99298858587468

RMSE of test dataset : 561.81931290546

MAE of train dataset: 140.02035214231896

MAE of test dataset: 368.35857426139705

Train R2 : 0.9951528171957928

Test R2 : 0.9673979592088858

Adjusted R2 : train dataset 0.9951527310874381

Adjusted R2 of test dataset: 0.9673956424341088
