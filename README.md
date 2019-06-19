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


To answer the research question i needed to understand the characteristics of each feature based and how each feature differs in a malignant compared to benign diagnosis. Using the breast cancer dataset form sklearn, used the seaborn pairplot to visualise the and identified intersting correlations.
By comparing the values of each of the main features with a malignant and Benign diagnosis to understand the feature reading for each diagnosis, I was able to determine which feature values distinctly indicate a malignant diagnosis.

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


Features are computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. They describe characteristics of the cell nuclei present in the image. Our dataset consists of 569 observations and 32 variables. There is an ID variable, a diagnosis variable revealing if they were benign or malignant, and 30 measurement variables detailing the size and shape of the cell nuclei. The diagnosis, a categorical variable, is our response variable and the 30 measurement variables, all of which are continuous, are our potential explanatory variables for our model. The 30 measurement variables are actually only 10 different features of the nucleus, but with 3 different measurements of each; the mean, the standard error and the ‘worst’ or largest (mean of the three largest values). The 10 features included are:

radius - mean of distances from center to points on the perimeter
texture - standard deviation of gray-scale values
perimeter
area
smoothness - local variation in radius lengths
compactness - perimeter^2 / area - 1.0
concavity - severity of concave portions of the contour
concave points - number of concave portions of the contour
symmetry
fractal dimension - “coastline approximation” - 1

Source:https://www.kaggle.com/shravank/predicting-breast-cancer-using-pca-lda-in-r


Data Set Characteristics:
Number of Instances:
 	
569
Number of Attributes:
 	
30 numeric, predictive attributes and the class
Attribute Information:
 	
radius (mean of distances from center to points on the perimeter)
texture (standard deviation of gray-scale values)
perimeter
area
smoothness (local variation in radius lengths)
compactness (perimeter^2 / area - 1.0)
concavity (severity of concave portions of the contour)
concave points (number of concave portions of the contour)
symmetry
fractal dimension (“coastline approximation” - 1)
The mean, standard error, and “worst” or largest (mean of the three largest values) of these features were computed for each image, resulting in 30 features. For instance, field 3 is Mean Radius, field 13 is Radius SE, field 23 is Worst Radius.
class:
WDBC-Malignant
WDBC-Benign



### Methods

Brief (no more than 1-2 paragraph) description about how you decided to approach solving it. Include:

- pseudocode for this method (either created by you or cited from somewhere else)
- why you chose this method

### Results

Brief (2 paragraph) description about your results. Include:

- At least 1 figure
- At least 1 "value" that summarizes either your data or the "performance" of your method (classification - show the F1 score)
- A short explanation of both of the above  9if you solved the project or not and what you could have done to makeit better)

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

-------
