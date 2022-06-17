# Project 2 - Ames Housing Data and Kaggle Challenge

### Problem Statement
Personal property tax revenue is very important for municipal operations in Ames.  Citizens need to have confidence that they will be taxed accurately and fairly, and the city of Ames cannot waste unnecessary resources on determining this assessment every year.

This presentation aims to create a reliable model to predict a real property assessment based on the sale price of homes in the Ames, Iowa area.  It will first analyze the data to look for correlation, then explore different models, and finally choose the most appropriate one.  The conclusion will also address limits on the application of this data to other cities/regions.


### Data used

The Ames Housing Dataset is an exceptionally detailed and robust dataset with over 70 columns of different features relating to houses.  It is used by the Ames Assessor's Office to compute assessed vales for individual residential properties sold in Ames, IA from 2006 to 2010.  More information about this data, including a data dictionary, can be found here:

http://jse.amstat.org/v19n3/decock/DataDocumentation.txt





### The Modeling Process

After data cleaning, the first step in the modeling process was to look for correlation between quantitative variables and sales price.  Secondly, categorical features were perused, grouped, and checked for mean differences.  Ones with large variances in mean were considered for inclusion in the model.  Models of increasing complexity were tried, starting with simple linear regression to LASSO models with tens of variables.

### Conclusion

Using r-squared values, multiple models can quickly be designed and tested for accuracy on our dataset.  We were easily able to increase model complexity to reach an r-squared value of 92%.  As this is being used solely for tax assessment data, this value is within acceptable levels.  It would be recommended to round each property's assessed value to the nearest $10,000 for the sake of simplicity and to take out any arbirtrary variance in the model which is not accurately reflected in the property data itself.  As any tax is subject to legal and Constitutional challenges, it should be safe to allow public viewing of this algorithm in the case of any suit or FOIA request.  The categories themselves are numerous and were not motivated by any real or perceived bias - rather, they were chosen almost completely on correlation statistics.  Additionally, the weight of each of these numerous categories was done entirely by automated LASSO regression and is consistent with real-life sales figures.

Additionally, this model is easy and inexpensive to maintain.  With slight adjustments - and depending on the exact format of data-keeping - it can easily be expanded to other similar markets.  