# Churn modelling
The customer churn model dataset has 10000 rows with 15 columns, each representing a unique customer.
14 features and target features (completed). The data consist of both numerical and categorical characteristics.

Target column:


Exited - Whether the customer has exited.
Numeric functions:


Customer number:
Unique ID of the customer.
Credit score:
customer credibility,
Year:
your age,
Term:
The number of months the customer has been with the company.
balance:
any remaining credit in the customer account,
Number of products:
The number of products sold by the customer. Estimated Salary:
Client's estimated salary.
Category features:


Surname:
Customer last name.
Geography:
Customer's country.
sex:
man and woman
HasCrCard:
Whether the customer has a credit card.
IsActiveMember:
Whether the customer is active.
First we import necessary libraries to do the logistic regression analysis for the churn model. After we read the dataset then we start the process of the exploratory data analysis.  
We univariate plots of different numerical variables.
The first plot is a boxplot of the creditscore and the second boxplot is for the age variable.
The next plot present is the violin plot of tenure and balance.
The other plot used is the distribution plot with the number of products as its variables.
The Kernel destiny estimation plot is used for the estimated salary.
After univariating plots, we preprocess data. In summary the things we are doing is: Discard the RowNumber column.
Also discard the customer ID, as it contains no additional information. Each row belongs to a unique customer.
Traits can be classified into non-essential, numeric, categorical and target variables based on the above.
In general, CustomerID is a convenience function that can be used to compute many user-centric functions. The dataset here is insufficient to compute additional customer characteristics. 
Since this is the only data available, we keep a set of tests to evaluate the model at the end and use the unseen data to estimate the performance of the selected model. It also creates a validation set that the base model uses to evaluate and optimize the model as a way of splitting our dataset.
For the categorical variable encoding we are using:
Label encoding:
Converts non-numeric labels to numbers. This works for binary categorical and ordinal variables.
One-hot encoding:
Encode the categorical features as a one-hot numeric array. Available for non-ordered categorical variables of low to medium cardinality (< 5 > 10 levels).
HasCrCard and IsActiveMember are already label coded.
For gender, you can use simple label encoding. Since there are 3 levels of geography, one-hot encoding is sufficient.
For the surname, I'm trying to encode the destination/frequency. 
To represent the decision boundaries of a classification model in 2D space, we first need to train the model in 2D space. The best option is to take existing data (with 2 or more features), apply a dimensionality reduction technique (such as PCA) to it, then reduce the number of features and train a model on this data .
Create an image in Meshgrid where each pixel represents a grid cell in her 2D feature space. This image creates a grid over the 2D feature space. Classifiers are used to classify image pixels by assigning a class label to each grid cell. The identified image is used as the background for a scatterplot containing data points for each class. 
In the decision tree classifier we:
Create a model and train it.
The export_graphviz() function creates her GraphViz representation of the decision tree.
A system command can convert points to PNG using the subprocess.run() method command.
Visualize the image by calling the Image(filename = 'tree.png') function.
Entropy is a measure of the unpredictability of processed information. The higher the entropy, the more difficult it is to draw conclusions from the information.
This decision tree shows that the model consists of a series of logical questions and answers. This is similar to what humans come up with when making predictions. 
