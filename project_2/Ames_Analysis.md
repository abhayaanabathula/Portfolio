### Overview

Ames is a town in Iowa with a population of more than 65,000 residents. Ames is also the home of Iowa State University, with a student population of 35,000. Ames has been described as a growing city and an attractive location for new businesses to move to and and for existing businesses to expand. In 2015, Ames was named one of the “15 Cities That Have Done the Best Since the Recession” by Bloomberg Business and one of the top 25 “Best Places for STEM Grads.” Ames ranked No. 8 by Niche Ranking for “Best Towns for Millennials in America.” Additionally, USA Today named Ames as the healthiest city in America. ([*source*](https://www.cityofames.org/about-ames/about-ames)). 

---

### Problem Statement

As a realtor, my job is to help my clients find their perfect home. Along with certain other variables/features the clients are looking for, the most important thing is that the home falls within their budget. Ames is also a bustling and growing city, so new homes are coming on the market all the time. My goal is to see if I can predict how much the house will cost in order to provide my customers with viable options. These predictions will help improve customer service and hopefully also increase closing rates for the firm. 

---

### Datasets

* [`test.csv`](datasets/test.csv): test data with 82 features 
* [`train.csv`](/datasets/train.csv): train data with 82 features and target variable 

---

### Data Dictionary

|Feature|Type|Description|
|---|---|---|
|Order|Discrete|Observation number|
|PID|Nominal|Identifies the type of dwelling involved in the sale|
|MS SubClass|Nominal|Identifies the type of dwelling involved in the sale|
|MS Zoning|Nominal|Identifies the general zoning classification of the sale|
|Lot Frontage|Continuous|Linear feet of street connected to property|
|Lot Area|Continuous|Lot size in square feet|
|Street|Nominal|Type of road access to property|
|Alley|Nominal|Type of alley access to property|
|Lot Shape|Ordinal|General shape of property|
|Land Contour|Nominal|Flatness of the property|
|Utilities|Ordinal|Type of utilities available|
|Lot Config|Nominal|Lot configuration|
|Land Slope|Ordinal|Slope of property|
|Neighborhood|Nominal|Physical locations within Ames city limits|
|Condition 1|Nominal|Proximity to various conditions|
|Condition 2|Nominal|Proximity to various conditions|
|Bldg Type|Nominal|Type of dwelling|
|House Style|Nominal|Style of dwelling|
|Overall Qual|Ordinal|Rates the overall material and finish of the house|
|Overall Cond|Ordinal|Rates the overall condition of the house|
|Year Built|Discrete|Original construction date|
|Year Remod/Add|Discrete|Remodel date|
|Roof Style|NominalType of roof|
|Roof Matl|Nominal|Roof material|
|Exterior 1|Nominal|Exterior covering on house|
|Exterior 2|Nominal|Exterior covering on house|
|Mas Vnr Type|Nominal|Masonry veneer type|
|Mas Vnr Area|Continuous|Masonry veneer area in square feet|
|Exter Qual|Ordinal|Evaluates the quality of the material on the exterior|
|Exter Cond|Ordinal|Evaluates the present condition of the material on the exterior|
|Foundation|Nominal|Type of foundation|
|Bsmt Qual|Ordinal|Evaluates the height of the basement|
|Bsmt Cond|Ordinal|Evaluates the general condition of the basement|
|Bsmt Exposure|Ordinal|Refers to walkout or garden level walls|
|BsmtFin Type 1|Ordinal|Rating of basement finished area|
|BsmtFin SF 1|Continuous|Type 1 finished square feet|
|BsmtFinType 2|Ordinal|Rating of basement finished area|
|BsmtFin SF 2|Continuous|Type 2 finished square feet|
|Bsmt Unf SF|Continuous|Unfinished square feet of basement area|
|Total Bsmt SF|Continuous|Total square feet of basement area|
|Heating|Nominal|Type of heating|
|HeatingQC|Ordinal|Heating quality and condition|
|Central Air|Nominal|Central air conditioning|
|Electrical|Ordinal|Electrical system|
|1st Flr SF|Continuous|First Floor square feet|
|2nd Flr SF|Continuous|Second floor square feet|
|Low Qual Fin SF|Continuous|Low quality finished square feet|
|Gr Liv Area|Continuous|Above grade ground living area square feet|
|Bsmt Full Bath|Discrete|Basement full bathrooms|
|Bsmt Half Bath|Discrete|Basement half bathrooms|
|Full Bath|Discrete|Full bathrooms above grade|
|Half Bath|Discrete|Half baths above grade|
|Bedroom|Discrete|Bedrooms above grade|
|Kitchen|Discrete|Kitchens above grade|
|KitchenQual|Ordinal|Kitchen quality|
|TotRmsAbvGrd|Discrete|Total rooms above grade|
|Functional|Ordinal|Home functionality|
|Fireplaces|Discrete|Number of fireplaces|
|FireplaceQu|Ordinal|Fireplace quality|
|Garage Type|Nominal|Garage location|
|Garage Yr Blt|Discrete|Year garage was built|
|Garage Finish|Ordinal|Interior finish of the garage|
|Garage Cars|Discrete|Size of garage in car capacity|
|Garage Area|Continuous|Size of garage in square feet|
|Garage Qual|Ordinal|Garage quality|
|Garage Cond|Ordinal|Garage condition|
|Paved Drive|Ordinal|Paved driveway|
|Wood Deck SF|Continuous|Wood deck area in square feet|
|Open Porch SF|Continuous|Open porch area in square feet|
|Enclosed Porch|Continuous|Enclosed porch area in square feet|
|3-Ssn Porch|Continuous|Three season porch area in square feet|
|Screen Porch|Continuous|Screen porch area in square feet|
|Pool Area|Continuous|Pool area in square feet|
|Pool QC|Ordinal|Pool quality|
|Fence|Ordinal|Fence quality|
|Misc Feature|Nominal|Miscellaneous feature not covered in other categories|
|Misc Val|Continuous|Value of miscellaneous feature|
|Mo Sold|Discrete|Month Sold 𝑀𝑀|
|Yr Sold|Discrete|Year Sold 𝑌𝑌𝑌𝑌|
|Sale Type|Nominal|Type of sale|
|Sale Condition|Nominal|Condition of sale|
|SalePrice|Continuous|Sale price $$|

---

### Analysis

Initial results were definitely not great. Looking at the predicted sale prices vs. actual sale prices, the models were not close. This suggests that the models had low bias and high variance. The models did not perform well on the test data, suggesting the models focused too much on the training data and did not generalize well. 
Based on the multiple linear regression analysis, a one unit increase in overall quality suggests an increase of 227875.35 in the sale price, while holding all else constant. A one unit increase in square feet for the above grade ground living area suggests an increase of 48.88 in the sale price, while holding all else constant. A one unit increase in square feet for the garage area suggests an increase of 76.78 in the sale price, while holding all else constant. The lasso regression with polynomial features added predicted very different results. The coefficients were very large and may suggest problems with the models. There could be issues in teh splitting or maybe the refitting to the test data. The second lasso regression without adding polynomial features was similar in the first lasso regression in that the coefficients were very large. 

---

### Conclusions/Recommendations 

I would definitely not use this model to make predictions for sale prices in Ames. The linear model provided some insight, but I would look to restructure my models and run further analysis. 



