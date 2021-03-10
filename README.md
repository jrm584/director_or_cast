# director_or_cast
Task as part of MSc module: establishing whether director or cast makes a stronger contribution to the success of a movie.

Mean director rating and sum of mean cast ratings are the input variables, 'vote average' is the target variable, taken as the measure of the success of the movie. 

The approach used was to train a machine learning algorithm on the data set, once trained use it to establish which attribute is the primary contributor to the predicition of the rating. 

In this instance SKlearn decision tree is used, with the target variable discretized. GridSearch Cross validation used to tune the the cost complexity parameter, avoiding overfitting the tree and optimising generalisation performance. Disappointing overall test/train score (c.65 at best) attributed to the limited range of variables used (only 2, other variables may be better predictors of performance, e.g. budget). But insofar as these two attributes can predict the success of a movie, Director is shown to overwhelmingly be the better predictor, in that it is almost always offers the greatest minimisation of entropy at each node of the tree (shown in the SKlearn feature_importances_ score).  
