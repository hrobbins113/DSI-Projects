
Project 6 Executive Summary

Problem Statement: Predict, based on information retrieved from the IMDB API about the top 250 movies of all time, what factors lead to high movie ratings.

Data: The data was mostly clean to begin with. There were no null values, so no rows of data were dropped. Columns were cleared of unnecessary characters and converted to the appropriate data types. For my chosen variables (Top_Directors, Decade, Runtime, Popular_Genre, Movie Rating), I performed necessary data transformations to convert categorical data to numerical data. Movie Years were binned into decades. Dummy variables were created for the ‘Rated’ column. Using dummy variables ‘Drama’ was chosen to be set against other genres since it was exceedingly prevalent. Similarly, the top 5 directors were set against the other directors because they directed an equal number of movies in the data set (7 each).

Several other features were present in the data set, but were ultimately eliminated for various reasons. For instance, Awards and Metascore were dropped because they are indicators of movie rating, not predictors. Other columns such as ‘Poster’ and ‘ Website’ have no bearing on movie ratings and were therefore dropped. More complex columns such as ‘Actors’ and ‘Writers’ were also dropped because each movie had different values and they therefore wouldn’t have significant meaning within the model. 

Modeling: Two models were compared -- a Random Forest Classifier and a Random Forest Regressor. The Random Forest Classifier far out-performed the Random Forest Regressor by approximately 0.2-0.25 points in mean accuracy – enough that I was comfortable focusing only on the Random Forest Classifier. 
Testing on a hold-out sample after the modeling process rendered a mean accuracy score of 0.158. I performed a Grid Search to improve accuracy and saw a modest increase in score. The Grid Search rendered a mean accuracy score of 0.238, suggesting that on data the model had never seen before, I was able to predict approximately 23.8% of the movie scores correctly.

Conclusion: This model does not perform exceedingly well against hold-out data, so there are several areas for improvement. The data could have been collected and transformed differently. I could have chosen the dummy variables differently and I could have gathered more information from the IMDB API to include more features. I could have also tried other ensemble methods such as Extra Trees or Ada Boosting to improve the accuracy of the model.  



