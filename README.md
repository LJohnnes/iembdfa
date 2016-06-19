<p align="center">
  <img src="http://www.bravocapital.es/wp-content/uploads/2015/05/manoel-gadi-300x200.jpg"/>
</p>

# Final Project, Group F
> Innovation and beyond in Big Data System for Model Development

This Python 3 package includes 5 algorithms intended to accelerate data cleaning and model development in financial applications for fraud detection.


## Installing / Getting started

Installation is simple. At the command line type:

```shell
pip install ex3groupf
```

Thereafter you should be able to import the ex3groupf package. This package makes use of the following libraries, that you will need to install if you have not already:
numpy
operator
pandas
re
requests
sklearn
statsmodels
time
warnings

Once the required packages are installed, you can make sure everything is working by executing the samplerun.py code included in the respository.

First, please download the dev.csv and oot0.csv files from github or from the dropbox links below:
dev: https://dl.dropboxusercontent.com/u/28535341/dev.csv
oot0: https://dl.dropboxusercontent.com/u/28535341/oot0.csv


## Features

This package includes 5 functions that allow for make for easy data cleaning and model development in an automated or human-assisted fashion. The algorithms implemented are:

A.1) Automated Data Cleaning. Identifies rows that contain invalid values - Null, NAN, and outliers - and automatically solves the problem. Null values are replaced with the highest frequency values, while NaN values are substituted by 0. Values are identified as outliers if they lie outside of the mean +/- 3 times the standard deviation, and are replaced by the closest (the next highest or lowest) value that is not determined to be an outlier.

A.4.1) Automated Dummy Creation and Transformation with Automated Supervised Binning. This function automatically conducts entropy-based supervised binning for columns of numerical values, according to the feature's relationship with the target variable. It then creates dummy variables to represent the new factors for each of the binned columns.

A.6) Automated method comparison and selection. This function develops three models - GML, Random Forest and SVM - and each model's Gini score and performance. The model with the highest Gini score is selected. If there are two models with equivalent Gini scores, the model with faster performance is selected.

H.1) Human assisted Data Cleaning. Gives the user the option to choose different actions when dealing with NULL, NaN and Outlier values. These are the oprtions:
How do you want to treat the Null values?
     1.Replaced by highest frequency value
     2.Replaced by lowest frequency value
How do you want to treat the NaN values?
     1.Replaced by zero (0)")
     2.Replaced by mean")
How do you want to treat the outliers?
     1.Replaced by threshold
     2.Replaced by mean
     3.Replaced by median

H.5) Human assisted method picking. Provides the user with a list of options for selecting a model:
1) The model with the highest Gini
2) The model with the fastest performance
3) The user can manually select GML
4) The user can manually select Random Forest
5) The user can manually select SVM.
Upon selecting a model, the user will be prompted to complete the necessary parameters, including training and test files. Default values are provided for all parameters, in case the user opts not to choose their own.

## Licensing

The code in this project is licensed under MIT license.