# Food_Sales_Predictions
![sales-forecasting](https://github.com/HibaBargaoui/Food_Sales_Predictions/assets/135720154/2ba3400f-85c9-4cf3-b7ef-b5d1a4db341f)

# Examining Data to enhance sales

**Author**: Hiba Bargaoui 

## Business problem: 

Data scientists has gathered a large amount of sales data that includes information about products sold in various stores located across different cities. The goal is to create a special kind of model that can make predictions, helping retailers increase the sales of individual products at specific retail outlets. 

## Data: 
Data Science food sales predictions: https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/#ProblemStatement

For this dataset, we have 8523 rows and 12 columns. 

## Data Dictionary:
<img width="599" alt="Data_Dictionary" src="https://github.com/HibaBargaoui/Food_Sales_Predictions/assets/135720154/68ed84fe-cd37-4a0a-886a-410e1c63b229">

In order to get this data ready, we first cleaned it and then carried out the following steps:

## Exploratory Data Analysis:
Established a strong foundational understanding of both numeric and categorical columns by:
- Visualizing numeric datatype columns with boxplots and histograms.
- Employing barplots for categorical columns.
  
![EDA_1](https://github.com/HibaBargaoui/Food_Sales_Predictions/assets/135720154/f1ff044d-e963-4a61-af03-e456d8fadd7e)

- The histogram indicates that the most common weight for products is approximately 12.5.
- The boxplot shows that there are no outliers.
  
![EDA_2](https://github.com/HibaBargaoui/Food_Sales_Predictions/assets/135720154/e68212d9-b81b-4bff-9a0a-0d7cdafe4592)

The graph represents the frequency of 'Low Fat' item.

## Explanatory Data Analysis:
For the purpose of visualization and explanation, we have created:
- Bar graphs that provide a clear comparison between the categories.
- A line graph that illustrates the sales trend across three distinct locations.
  
![EDA_3](https://github.com/HibaBargaoui/Food_Sales_Predictions/assets/135720154/bbb8a0c3-09b1-479d-8690-53052e95164d)

The 'OUT027' outlet stands out as the leader, boasting sales exceeding 3500.

![EDA_4](https://github.com/HibaBargaoui/Food_Sales_Predictions/assets/135720154/d0dae4df-b789-4ae1-ab48-190d60b20a2d)

Starchy foods are in the forefront in terms of sales.

![EDA_5](https://github.com/HibaBargaoui/Food_Sales_Predictions/assets/135720154/d9c8591e-f6fb-4350-97ee-b3e1d545cccc)

The outlet located in 'Tier3' holds the top position in terms of sales.

## Maching Learning Models:
#### Linear Regression Model: 
- Evaluation for the testing set:
  
  MAE: 199,554,574,368.15
  
  MSE: 7,130,647,480,125,906,057,428,992.00
  
  RMSE: 2,670,327,223,417.74
  
  R2: -2,584,525,618,112,160,256.00

- Coefficients of the Linear Regression Model
![Coefficients](https://github.com/HibaBargaoui/Food_Sales_Predictions/assets/135720154/8daef960-89e2-4cc4-9bd0-d1a65a8d9f9f)

  Outlet_Type_Supermarket Type2, Outlet_Identifier_OUT045 and Outlet_Identifier_OUT017 
  are the most impactful features. 
#### Decision Tree Model: 
- Evaluation for the testing set:

  MAE: 995.41
  
  MSE: 2,140,427.72
   
  RMSE: 1,463.02
  
  R2: 0.22
#### Tuned Decision Tree Model:
- Evaluation for the testing set:

  MAE: 736.88 

  MSE: 1,114,471.12 

  RMSE: 1,055.69 

  R2: 0.60
#### Random Forest Model: 
- Evaluation for the testing set:
  
  MAE: 771.82
  
  MSE: 1,239,094.55
   
  RMSE: 1,113.15
  
  R2: 0.55

- Feature importances
![Importances](https://github.com/HibaBargaoui/Food_Sales_Predictions/assets/135720154/db7f6cdb-7615-4a55-ae41-83b015a8e5a5)

  - pipeline-1__Item_MRP, pipeline-2__Outlet_Type_Grocery Store, pipeline-1__Item_Visibility, pipeline- 
     2__Outlet_Identifier_OUT027 and pipeline-1__Item_Weight are the top 5 most important features.
  - pipeline-1__Item_MRP is the most important feature for predicting Item_Outlet_Sales.
  - pipeline-2__Outlet_Type_Grocery Store is the second most important feautre.
  - pipeline-1__Item_Visibility, pipeline-2__Outlet_Identifier_OUT027, pipeline-1__Item_Weight, pipeline- 
     2__Outlet_Type_Supermarket Type3 and pipeline-1__Outlet_Establishment_Year are somewhat important.
  - The rest of the features are unimportant.
#### Tunned Random Forest Model: 
- Evaluation for the testing set:
  
  MAE: 728.09
  
  MSE: 1,091,575.17
  
  RMSE: 1,044.78
  
  R2: 0.60
  
--> To make the best predictions, the Tunned Random Forest Model is chosen with the n_estimators tuned to 200.
- When assessing the model's performance on the testing set, it is able to account for 60% of the variability in y using x.
- The Mean Absolute Error (MAE) shows a discrepancy of around 728.09.
- The Mean Squared Error (MSE) yields a value of 1,091,575.17.
- The Root Mean Squared Error (RMSE) is calculated to be 1,044.78.

## Recommendations:
To enhance the sales of individual products, retailers should consider the following strategies:
- Prioritize the sale of starchy foods, given their high frequency in demand among customers.
- Channel a significant portion of sales efforts through the 'OUT027' outlet, as it has demonstrated leadership in terms of total item outlet sales.
- Concentrate a considerable share of sales activities on outlets situated in 'Tier3', recognizing their potential for driving substantial sales volumes.
  
By aligning their sales approach with these guidelines, retailers can optimize their efforts to boost overall product sales.

## For further information


For any additional questions, please contact **bargaoui.hiba42@gmail.com**
