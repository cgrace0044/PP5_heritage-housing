# Heritage Housing Issues

Analyze how home attributes influence sale price in Ames, Iowa (USA), and build a model to forecast prices for four inherited properties—plus any other Ames home. The project delivers a simple dashboard that visualizes key price drivers and generates predictions from user-entered features.

## Dataset Content

* The dataset is sourced from [Kaggle](https://www.kaggle.com/codeinstitute/housing-prices-data). We then created a fictitious user story where predictive analytics can be applied in a real project in the workplace.
* The dataset has almost 1.5 thousand rows and represents housing records from Ames, Iowa, indicating house profile (Floor Area, Basement, Garage, Kitchen, Lot, Porch, Wood Deck, Year Built) and its respective sale price for houses built between 1872 and 2010.

|Variable|Meaning|Units|
|:----|:----|:----|
|1stFlrSF|First Floor square feet|334 - 4692|
|2ndFlrSF|Second-floor square feet|0 - 2065|
|BedroomAbvGr|Bedrooms above grade (does NOT include basement bedrooms)|0 - 8|
|BsmtExposure|Refers to walkout or garden level walls|Gd: Good Exposure; Av: Average Exposure; Mn: Minimum Exposure; No: No Exposure; None: No Basement|
|BsmtFinType1|Rating of basement finished area|GLQ: Good Living Quarters; ALQ: Average Living Quarters; BLQ: Below Average Living Quarters; Rec: Average Rec Room; LwQ: Low Quality; Unf: Unfinshed; None: No Basement|
|BsmtFinSF1|Type 1 finished square feet|0 - 5644|
|BsmtUnfSF|Unfinished square feet of basement area|0 - 2336|
|TotalBsmtSF|Total square feet of basement area|0 - 6110|
|GarageArea|Size of garage in square feet|0 - 1418|
|GarageFinish|Interior finish of the garage|Fin: Finished; RFn: Rough Finished; Unf: Unfinished; None: No Garage|
|GarageYrBlt|Year garage was built|1900 - 2010|
|GrLivArea|Above grade (ground) living area square feet|334 - 5642|
|KitchenQual|Kitchen quality|Ex: Excellent; Gd: Good; TA: Typical/Average; Fa: Fair; Po: Poor|
|LotArea| Lot size in square feet|1300 - 215245|
|LotFrontage| Linear feet of street connected to property|21 - 313|
|MasVnrArea|Masonry veneer area in square feet|0 - 1600|
|EnclosedPorch|Enclosed porch area in square feet|0 - 286|
|OpenPorchSF|Open porch area in square feet|0 - 547|
|OverallCond|Rates the overall condition of the house|10: Very Excellent; 9: Excellent; 8: Very Good; 7: Good; 6: Above Average; 5: Average; 4: Below Average; 3: Fair; 2: Poor; 1: Very Poor|
|OverallQual|Rates the overall material and finish of the house|10: Very Excellent; 9: Excellent; 8: Very Good; 7: Good; 6: Above Average; 5: Average; 4: Below Average; 3: Fair; 2: Poor; 1: Very Poor|
|WoodDeckSF|Wood deck area in square feet|0 - 736|
|YearBuilt|Original construction date|1872 - 2010|
|YearRemodAdd|Remodel date (same as construction date if no remodelling or additions)|1950 - 2010|
|SalePrice|Sale Price|34900 - 755000|

## Business Requirements

You are requested by your friend, who has received an inheritance from a deceased great-grandfather located in Ames, Iowa, to help in maximising the sales price for the inherited properties.

Although your friend has an excellent understanding of property prices in her own state and residential area, she fears that basing her estimates for property worth on her current knowledge might lead to inaccurate appraisals. What makes a house desirable and valuable where she comes from might not be the same in Ames, Iowa. She found a public dataset with house prices for Ames, Iowa, and will provide you with that.

* 1 - The client is interested in discovering how the house attributes correlate with the sale price. Therefore, the client expects data visualisations of the correlated variables against the sale price to show that.
* 2 - The client is interested in predicting the house sale price from her four inherited houses and any other house in Ames, Iowa.

## Hypothesis and how to validate?

* TO BE UPDATED

## The rationale to map the business requirements to the Data Visualisations and ML tasks

* **Business Requirement 1:** Data Visualization and Correlation study
  * We will inspect the data related to the houses prices in Amnes, Iowa.
  * We will conduct a correlation study (Pearson and Spearman) to understand better how the variables are correlated to house price.
  * We will plot the main variables against house price to visualize insights.

* **Business Requirement 2:** Classification/Regression
  * Build a model to forecast prices for four inherited properties—plus any other Ames, Iowa homes using regression/classification.

## ML Business Case

| **Question** | **Answer** |
|--------------|------------|
| **1. What are the business objectives?** | The client is interested in knowing how house attributes correlate with house price and expects visualisations of this. The client is also interested in predicting the house sale price for her four inherited houses and any other house in Ames, Iowa. |
| **2. Can any business objectives be answered with conventional data analysis?** | Yes, we can use conventional data analysis to discover house pricing patterns in the dataset. |
| **3. Does the client need a dashboard or an API endpoint?** | The client has requested a dashboard. |
| **4. What does the client consider a successful project outcome?** | A running dashboard that meets the business requirements. This includes a study showing the main variables that influence house price and a reliable prediction model for house prices in the Ames, Iowa area. |
| **5. Can you break down the project into Epics and User Stories?** | Yes, these are mapped to the ML lifecycle: <br> 1. Information gathering and data collection <br> 2. Data visualisation, cleaning, and preparation <br> 3. Model training, validation, and optimisation <br> 4. Dashboard planning, design, and development <br> 5. Dashboard deployment and release |
| **6. Ethical or privacy concerns?** | None in this case, as the client is using a public dataset. |
| **7. Does the data suggest a particular model?** | The data suggests using a regressor where sales price is the target. |
| **8. What are the model inputs and intended outputs?** | **Input:** A public dataset with house prices for Ames, Iowa. <br> **Output:** Predictions of house prices. |
| **9. What are the performance criteria for the predictions?** | Regressor with an R² score ≥ 0.7. This value is a common rule of thumb for regression. |
| **10. How will the client benefit?** | Data-driven insights: the client wants to maximise the sales price of her inherited properties. |

## Dashboard Design (Streamlit App User Interface)

### Page 1: Quick project summary

    - Quick project summary
	- Project Terms & Jargon
	- Describe Project Dataset
	- State Business Requirements

### Page 2: House Prices Study

    - Before the analysis, we knew we wanted this page to answer business requirement 1, but we couldn't know in advance which plots would need to be displayed.
    - After data analysis, we agreed with stakeholders that the page will: 
    	- State business requirement 1
    	- Checkbox: data inspection on house prices (display the number of rows and columns in the data, and display the first ten rows of the data)
    	- Display the most correlated variables to house price and the conclusions
    	- Checkbox: Individual plots showing the house price levels for each correlated variable

### Page 3: Prediction of House Prices

* **Business Requirement 2**  
  Define the second business requirement related to predicting house prices.

* **Widget Inputs**  
  Provide a set of input fields describing the house for which the price prediction is required.

* **Run Predictive Analysis Button**  
  Uses the entered data to run the ML pipeline and:  
  * Predict the price of the specified house.

### Page 4: Project Hypothesis and Validation

* Before the analysis, we knew we wanted this page to describe each project hypothesis, the conclusions, and how we validated each. After the data analysis, we can report that:
* 1 - TO BE UPDATED

* 2 - TO BE UPDATED

### Page 5: Predict Sales price

* Considerations and conclusions after the pipeline is trained.
* Present ML pipeline steps
* Feature importance
* Pipeline performance

## Unfixed Bugs

* You will need to mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a big variable to consider, paucity of time and difficulty understanding implementation is not valid reason to leave bugs unfixed.

## Deployment

### Heroku

* The App live link is: <https://YOUR_APP_NAME.herokuapp.com/>
* Set the .python-version Python version to a [Heroku-24](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack currently supported version.
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. At the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click the button Open App on the top of the page to access your App.
6. If the slug size is too large then add large files not required for the app to the .slugignore file.

## Main Data Analysis and Machine Learning Libraries

* TO BE UPDATED

## Credits

* TO BE UPDATED

### Content

* To BE UPDATED

### Media

* TO BE UPDATED

## Acknowledgements (optional)

* TO BE UPDATED
