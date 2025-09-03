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

| Question |  |
|---|---|
| 1. What are the business objectives? | The client is interested in knowing how house attributes correlate with house price and expects visualisations of this. The client is also interested in predicting the house sale price from her four inherited houses and any other house in Ames, Iowa. |
| 2. Is there any business objectives that can be answered with conventional data analysis? | Yes we can use conventional data analysis to discover house pricing patterns in the housing dataset. |
| 3. Does the client need a dashboard or an API endpoint? | In this case the client has requested a dashboard. |
| 4. What does the client consider as a successful project outcome? | A running dashboard meeting the business requirements. This includes a study showing the main variables which influence house price and a reliable prediction model of house prices in the Amnes, Iowa area. |
| 5. Can you breakdown the project into Epics and User Stories? | Yes and these are mapped to the ML life cycle. 1. Information gathering and data collection. 2. Data visualisation, cleaning and preparation. 3. Model training, validation and optimisation. 4. Dashboard planning, designing and development. 5. Dashboard deployment and release.  |
| 6. Ethical or Privacy concerns? | Not in this case as the client found a public dataset. |
| 7. Does the data suggest a particular model? | The data suggests a regressor where sales price is the target. |
| 8. What are the model inputs and intended outputs? | The input is a public dataset with house prices for Ames, Iowa. The output is a prediction of house prices. |
| 9. What are the criteria for the performance goal of the predictions? | Regressor 0.7 R2 score. This value is a common rule of thumb for regression. |
| 10. How will the client benefit? | Datadriven insights: the client would like to maximise the sales price on her given inherited properties. |

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
- State business requirement 2
- Set of widgets inputs, which relates to the prospect profile. Each set of inputs is related to a given ML task to predict prospect Churn, Tenure and Cluster.
- "Run predictive analysis" button that serves the prospect data to our ML pipelines and predicts if the prospect will churn or not, if so, when. It also shows to which cluster the prospect belongs and the cluster's profile. For the churn and tenure predictions, the page will inform the associated probability for churning and tenure level.

### Page 4: Project Hypothesis and Validation
- Before the analysis, we knew we wanted this page to describe each project hypothesis, the conclusions, and how we validated each. After the data analysis, we can report that:
- 1 - We suspect house prices are are churning with low tenure levels
	- Correct. The correlation study at Churned Customer Study supports that.
- 2 -  A customer survey showed our customers appreciate Fibre Optic.
	- A churned user typically has Fiber Optic, as demonstrated by a Churned Customer Study. The insight will be taken to the survey team for further discussions and investigations.

### Page 5: Predict Sales price

  * Considerations and conclusions after the pipeline is trained.
* Present ML pipeline steps
* Feature importance
- Pipeline performance

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

* Here you should list the libraries you used in the project and provide example(s) of how you used these libraries.

## Credits

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism.
* You can break the credits section up into Content and Media, depending on what you have included in your project.

### Content

* The text for the Home page was taken from Wikipedia Article A
* Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
* The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

* The photos used on the home and sign-up page are from This Open Source site
* The images used for the gallery page were taken from this other open-source site

## Acknowledgements (optional)


* In case you would like to thank the people that provided support through this project.

