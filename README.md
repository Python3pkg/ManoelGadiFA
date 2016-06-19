Auto Clean Data : autocleandata.py 
This library will assisst the user with data cleaning tasks by asking for the following:
1) Asking the user what to do with the outliers; the user has two options to keep or to remove
2) Asking the user what to do with the Nans; the user has three options to remove the rows with nans; replacing them with zeros or the mean of the column

to user just type : from ManoelGadiFA import autocleandata and then call the function autocleandata(x) with a dataframe.

######################################

Data clean : dataclean.py
This library will clean a datafra,e by automatically dropping the nulls;duplicates; and outliers values 
to user just type : from ManoelGadiFA import dataclean and then call the function cleandata(x) with a dataframe.


######################################
Human Assisted Method Picking: H5_Method_picking.py
Get accuracy scores for 3 algorithms once. The library take 2 inputs; a dataset and a target variable.
The following parameters will be set by default:
testSize=0.25, randomState=0, peceptronIteration = 20, perceptronLearningRate = 0.01, svmCost = 10, rfTrees = 10

to user just type : from ManoelGadiFA import H5_Method_picking and then call the function mp(x,y) with a dataframe.

######################################
Automated Dummy Creation and Transformation: supervised2.py 

This library takes all continuous variables and bins them seperately based on how their information value is maximised
information value is calculated through the entropy in the target variable corresponding to each bin
furthermore, all string columns are transformed to dummies and all int columns are kept the same

to user just type : from ManoelGadiFA import supervised2 and then call the function binning1(x) with a dataframe.


######################################
Automated Variable Creation - PCA & Decision Trees - supervisedPCA.py

This function works as following: 
    1) extracting the name of the columns from the data frame
    2) using those names to filter the data frame by the columns to be 
    analyzed and generating another one with the columns to be discarded
    (e.g. the TARGET variable)
    3) Run PCA on the selected data frame
    4) Identify the number of columns required to achieve the desired accuracy
    and run PCA again only with those columns as output
    5) Concatenate the result of PCA analysis and data frame with filtered
    columns and return it


Inputs:
    - df: DATA FRAME subject of the PCA analysis
    - colstodiscard: LIST of columns of df excluded from PCA analysis
    - accuracy: NUMERIC value to indicate the selected accuracy of PCA
Output: 
    - df2: DATA FRANE that combines the output of the PCA analysis with the
    columns that were discarded from the analysis


to user just type : from ManoelGadiFA import supervisedPCA and then call the function PCAfunction(df, colstodiscard, accuracy) with the input variables explained earlier.


