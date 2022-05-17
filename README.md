# Surgre-Pricing-Algorithm-with-Neural-Network

On this project, i want to share how problem of car availbility on Uber can be solved using surge pricing. To apply surge pricing, i use data analytics to describe the pattern using Tableau and predict fare amount each customer based on particular condition using Neural Network regression method (Deep Learning).
![absent](Img/uber.jpg)
<br>
For full report of this project, please visit <a href="https://github.com/Juantonios1/Absenteeism-Analysis-to-Improve-Work-Performance/blob/main/Absenteeism%20Analysis%20ipynb/Absenteeism%20Analysis%20to%20Improve%20Work%20Performance.ipynb">Surge pricing algorithm with neural network</a>.

## Summary Process
<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Content</summary>
  <ol>
    <li><a href="#business-background">Business Background</a></li>
    <li><a href="#data-understanding">Data Understanding</a></li>
    <li><a href="#feature-engineering">Feature Engineering</a></li>
    <li><a href="#exploratory-data-analysis">Exploratory Data Analysis</a></li>
    <li><a href="#data-preprocessing">Data Preprocessing</a></li>
    <li><a href="#data-analytics">Data Analytics</a></li>
    <li><a href="#model-selection">Model Selection</a></li>
    <li><a href="#explainable-and-interpretable-machine-learning">Explainable and Interpretable Machine Learning</a></li>
    <li><a href="#preprocessing-new-dataset">Preprocessing New Dataset</a></li>
    <li><a href="#prediction-result">Prediction Result</a></li>
    <li><a href="#conclusion">Conclusion and Recommendation</a></li>
    <li><a href="#contributors">Contributors</a></li>
  </ol>
</details>

## Business Background
**Context :**  
Uber is an American app-based transportation platform headquartered in San Francisco, California who develop an app that connects drivers to users who need a ride, using a smartphone as a tool. The Uber Business Model is also known as a Multisided Platform Business Model, as it connects drivers (offer) and passengers (demand), in order to offer cheaper transportation and an additional source of income. The customer must use the Uber app to book a ride and then enter the customer's destination before the trip takes place. When the customer arrives at the destination, the journey ends. Fares are automatically calculated and charged to the payment method the customer connects to the Uber account.

**Problem Statement :**  
One of the biggest problem from Uber as ride hailing company is availability of drivers at certain times (rush hours or bad weather conditions) and certain locations in some cities. The best way to solve that problems is use Surge Pricing. Surge Pricing / Dynamic Pricing (Flexible Pricing) is where prices change constantly based on market fluctuations. For that, Uber need system and algorithm to make prediction for fare amount based on some feature on history data.

**Goals :**  
The goals of this analysis are to know the price per transaction according to particular conditions (the time, distance traveled, etc) so surge pricing can be applied.

## Data Understanding

| Feature      	     | Description                                                      |
|--------------------|------------------------------------------------------------------|
| Key        	       | Unique ID for customer                          	                |
| Fare Amount        | The cost of each trip in USD.                                  	|
| Pickup Datetime    | Date and time when the meter was engaged.                        |
| Passanger Count    | The number of passengers in the vehicle (driver entered value).  |
| Pickup Longitude   | The longitude where the meter was engaged.                    	  |
| Pickup Latitude    | The latitude where the meter was engaged.                        |
| Dropoff Longitude  | The longitude where the meter was disengaged.                    |
| Dropoff Latitude   | The latitude where the meter was disengaged.                     |
                                                                                                   
## Feature Engineering
At this stage, to enrich the information from the existing data, a feature engineering process can be carried out, with results:
| Feature      	     | Description                                                      |
|--------------------|------------------------------------------------------------------|
| Year        	     | The year when the meter was engaged.                          	  |
| Month              | The month when the meter was engaged..                           |
| Day                | The day when the meter was engaged.                              |
| Day Name           | Day name when the meter was engaged.                             |
| Hour               | The hour when the meter was engaged..                            |
| Minute             | The minute when the meter was engaged.                           |
| Week               | The week when the meter was engaged.                             |
| Weekend            | Determine the day is weekend or weekday.                         |
| Distance           | The distance from start point to end point(in km).               |

## Exploratory Data Analysis
At this stage, a brief analysis of the data will be carried out, as follows:
* Distribution Data
* Normal Test
* Data Cardinalities
* Identify Missing Values
* Data Correlation

![correlation](Image/Correlation.png)

## Data Preprocessing
At this stage, data preparation and processing will be carried out before being used as a data model, as follows:
* Casting Data Type
* Encode
* Categorization
* Extract Date Feature
* Splitting

## Data Analytics
At this stage, another information analysis will be carried out, as follows:
* Information Abseenteism in Company <br>
![Information Abseenteism in Company](Image/Dashboard_1.png) <br>
* Personal Information of Employee <br>
![Personal Information of Employee](Image/Dashboard_2.png) <br>
* Daily Work <br>
![Daily Work](Image/Dashboard_3.png) <br>
You can also see full dashboard of analysis at <a href="https://public.tableau.com/app/profile/juan1691/viz/AnalysisAbseenteismProject/AnalysisAbseenteism">Analysis Tableau</a>.  

## Model Selection
At this stage will be done making and optimizing the machine learning model, as follows:
* Model Benchmark (Linear Regression, Ridge, KNN Regression, Lasso, and Decision Tree Regression)
* Hyperparameter Tuning
For summary can see on picture below:

## Explainable and Interpretable Machine Learning
At this stage there will be an explanation in the decision making of the machine learning model, in the following ways:
* Feature Importance
* SHAP <br>
![SHAP](Image/SHAP.png)

## Preprocessing New Dataset
At this stage, preprocessing stage will apply to new data set which want to predict

## Prediction Result
At this stage, new data set will predict with selected model before, in the following ways:
* Predict New Dataset
  * For view the result of prediction, please visit <a href="https://github.com/Juantonios1/Performance-Improvement-Absenteeism-at-Work/blob/main/Data_set/Absenteeism_data_predict.csv">Prediction Dataset</a>.  

![prediction](Image/prediction.png)

* Import to CSV File
* Prediction Analysis
  * For view the full analysis of prediction dataset, please visit <a href="https://public.tableau.com/app/profile/juan1691/viz/PredictedAbsenteeismProject/PredictedInformation">Prediction Tableau</a>.  

## Conclusion 
We conclude our result and give recommendation based on it
* Summary Model <br>
![Daily Work](Image/summary.png) <br>
* Business Insight
  * January & February have the less average abseenteism beside that March, April, and June have most average abseenteism time. Maybe in this month spirit of employee is down and they use the reason to absent
  * BMI and Age dont have specific pattern with Abseenteism
  * Employee with 2 Children and 1 or 2 pets have more abseenteism time then the others
* Recommendation
  * The company need to mantain employee spirit. They can make some event to keep employee spirit like gathering or eat together for every division
  * For every director or supervisor can reduce the workload for every senior employee so they can mantain their health and prevent absenteeism time
  * Every supervisor need to remind their employee to do their task even they need to look after their children or pet.
 
For full report of this project, please visit <a href="https://github.com/Juantonios1/Absenteeism-Analysis-to-Improve-Work-Performance/blob/main/Absenteeism%20Analysis%20ipynb/Absenteeism%20Analysis%20to%20Improve%20Work%20Performance.ipynb">Absenteeism at Work</a>.

## Contributors:
Juan Antonio Suwardi - antonio.juan.suwardi@gmail.com  

