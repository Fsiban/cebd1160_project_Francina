# cebd1160_project_Francina
Instructions and template for final projects.

| Name | Date |
|:-------|:---------------|
|Francina Sibanda| 14 June 2019|

-----

### Resources
Your repository should include the following:

- Python script for your analysis
- Results figure/saved file
- Dockerfile for your experiment
- runtime-instructions in a file named RUNME.md

-----

## Research Question

1 sentence description of your research question.
- Which feature values distinctly indicate a malignant diagnosis. 


### Abstract

4 sentence longer explanation about your research question. Include:

- opportunity (what data do we have)
- challenge (what is the "problem" we could solve with this dataset)
- action (how will we try to solve this problem/answer this question)
- resolution (what did we end up producing)


To answer the research question i needed to understand the characteristics of each feature based and how each feature differs in a malignant compared to benign diagnosis. Using the breast cancer dataset form sklearn, used the pairplot to visualise the data and identified positive correlations. By comparing the values of each of the main features with a malignant and Benign diagnosis to understand the feature reading for each diagnosis, I woul be able to determine which feature values distinctly indicate a malignant diagnosis.  

The mean of the ten main features were compared to the Diagnosis are listed below:

Radius
Texture
Perimeter
Area
Smoothness
Compactness
Concavity
Concave_Points
Symmetry
Fractal_Dimension

### Introduction

Brief (no more than 1-2 paragraph) description about the dataset. Can copy from elsewhere, but cite the source (i.e. at least link, and explicitly say if it's copied from elsewhere).


The detailed decription of the dataset is from Kaggle and Slearn website. 
The data set is from the sklearn website, the features are computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. They describe characteristics of the cell nuclei present in the image. The sample size is 569 and there are 32 variables. The 32 variables comprise of an ID variable, a diagnosis variable indicating a benign or malignant, and 30 measurement variables detailing the size and shape of the cell nuclei. The diagnosis, a categorical variable, is our response variable and the 30 measurement variables, all of which are continuous, are our potential explanatory variables for our model. The 30 measurement variables are actually only 10 different features of the nucleus, but with 3 different measurements of each; the mean, the standard error and the ‘worst’ or largest (mean of the three largest values). The 10 features included are indicated below:

Data Set Characteristics:
Number of Instances:
 	569
Number of Attributes:
 	30 numeric, predictive attributes and the class

Attribute Information:
 	
- radius (mean of distances from center to points on the perimeter)
- texture (standard deviation of gray-scale values)
- perimeter
- area
- smoothness (local variation in radius lengths)
- compactness (perimeter^2 / area - 1.0)
- concavity (severity of concave portions of the contour)
- concave points (number of concave portions of the contour)
- symmetry
- fractal dimension (“coastline approximation” - 1)
- The mean, standard error, and “worst” or largest (mean of the three largest values) of these features were computed for each image, resulting in 30 features. For instance, field 3 is Mean Radius, field 13 is Radius SE, field 23 is Worst Radius.
- class:
WDBC-Malignant
WDBC-Benign

Sources:
https://www.kaggle.com/shravank/predicting-breast-cancer-using-pca-lda-in-r
https://scikit-learn.org/stable/datasets/index.html#breast-cancer-wisconsin-diagnostic-dataset

### Methods

Brief (no more than 1-2 paragraph) description about how you decided to approach solving it. Include:

- pseudocode for this method (either created by you or cited from somewhere else)
- why you chose this method

I determined that this is a clasification problen, and i would need to use logistic regression classifier model because the dataset has two categories for the output values, Malignant and Begnin. First to understand the how the attributes of the features relate to each other and their values to the diagnosis predictions, I used decided to perform exploratory analysis first by visualising the data using a pairplot. I selected the 10 mean attributes first to identify the correlation.I identified that the mean radius has a positive correlation with the area and perimeter. To now understand the relationship betwen the rean radius in a benign and malignant diagnosis reading, I generated a distribution plot to understand if these the two classes can be seperated so that I can develop a machine learning model. Then I developed a logistic regression model to determine the class to evaluate if the diagnosis can be predicted with accuracy. I identified the target variable as the class. For comparison, i also used KNeighbors and determined that the logistic regression model was more accurate.

I performed the steps below:

- Imported the dataset from sklearn library
- Imported other necessarry libraries (Matplotlib,Numpy,Pandas,Seaborn)
- Exploratory analysis 
   - Used the describe function to have a look at the description of the dataset
   - Dropped the features for the standard error and the worst so that that I could use the mean values to generate the pairplot)
- Train the logistic regression model
   - Split the data into a training and test set
   - Create and Train the Model
- Evaluate the Logistic regression model by looking at the generated results after running the model.
- Train the K-Neigbours
- Evaluate the K-Neighbours model by looking at the generated results after running the model.



### Results

Brief (2 paragraph) description about your results. Include:

- At least 1 figure
- At least 1 "value" that summarizes either your data or the "performance" of your method (classification - show the F1 score)
- A short explanation of both of the above  9if you solved the project or not and what you could have done to makeit better)

The results indicate that the Logistic regression model performs better as it produced more accurate results compared to the KNeighbours.

- I imported the data from sklearn 


### Discussion
Brief (no more than 1-2 paragraph) description about what you did. Include:

- interpretation of whether your method "solved" the problem
- suggested next step that could make it better.
Make it iteration eg using the average
KNeighbours Cross validation score:[0.87826087 0.92173913 0.94690265 0.9380531  0.91150442]

KNeighbours ShuffleSplit val_score:[0.94736842 0.94736842 0.87719298 0.94736842 0.92982456]


you can remove the ones with the lowest coefifient to keep the ones that have higher one to remove the noise..


### References
All of the links

- Source1:https://www.kaggle.com/shravank/predicting-breast-cancer-using-pca-lda-in-r
- Source2:https://scikit-learn.org/stable/datasets/index.html#breast-cancer-wisconsin-diagnostic-dataset


-------
