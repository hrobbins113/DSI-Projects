
Project 4 Summary

Objective: To classify Chicago housing prices into a high and low price scheme.

Data: Some significant data cleaning was required upfront. There were 3662 pieces of missing data from the dataset. This data was dropped since the percentage was low enough that it would not adversely effect the modeling process.  All unnecessary characters were removed and the data was transformed to the appropriate data types. Three new columns were made to compartmentalize the data contained in the ‘bed_bath’ column (bedrooms, bathrooms, square feet). Some data within the ‘bedrooms’ column was unrealistic/likely incorrect (11+ bedrooms), so it was converted to zeros so it would not significantly skew the bedroom data. 

Housing prices that were in the top 25th percentile were considered to be “high-priced”, making the cutoff point $500,000. The price column was converted into a categorical variable based on this cutoff point (above $500,000 and below).

Modeling: A Logistic Regression Model was made using variables ‘bedrooms’, ‘bathrooms’ and ‘square feet’, which rendered a mean accuracy of 0.795. Logistic Regression was chosen as the classification model because of its simplicity and it is more resilient against ‘noise’ in the data than KNN. Train/test/split was used to minimize overfitting.

Conclusion: The model performed well against the hold out data and there does not appear to be significant overfitting. However, there is still room for improvement. . A different approach to data cleaning could yield a slightly different result – instead of dropping the rows that had foreclosure prices in the ‘bed_bath’ column, I could determine how to extract those values from that column and put them into the ‘price’ column. Additional housing data could be included by scraping the Zillow.com website. The model could be improved by performing a Grid Search to test out different parameters. A KNN model could also be made to see how it compares to the Logistic Regression. 

