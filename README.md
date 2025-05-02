![](UTA-DataScience-Logo.png)

# PCOS Diagnosis Prediction Project

This repository outlines my process to use a linear regression model to predict PCOS diagnoses using "PCOS Diagnosis Dataset" from Kaggle, found [here](https://www.kaggle.com/datasets/samikshadalvi/pcos-diagnosis-dataset?resource=download)

## Overview

The task, as defined by the Kaggle challenge is to use a dataset containing PCOS patient data containing 6 features, to predict PCOS diagnosis. The approach in this repository follows a simple linear regression model and an iteration of this model with hyperparameter adjustments. This model was able to identify 95% of women with a PCOS diagnosis. As of the time this was written, the best recall performance on Kaggle is 96%. 

## Summary of Workdone

### Data

* Data:
  * Type: CSV file of entirely numerical features
  * Size: 1000 rows of unique entries
  * Instances (Train, Test, Validation Split): 800 patients for training, 200 for testing, none for validation

#### Preprocessing / Clean up

* Data was scaled for normalization purposes

#### Data Visualization

![](histograms.png)
The histograms show that there are a couple binary categories, such as Menstrual_Irregularity. Upon further examination, the features are relatively well spread out across their respective ranges.


### Problem Formulation

* Define:
  * Input: features in dataset ('Age', 'BMI', 'Menstrual_Irregularity', 'Testosterone_Level(ng/dL)', 'Antral_Follicle_Count')
  * Output: PCOS diagnosis prediction
  * Models:
    * I attemped only a linear regression model, since the data was too simple for more complex models
  * I chose to adjust the class_weight hyperparameter, since there is a noticable imbalance between class_0 and class_1

### Training

* Describe the training:
  * How you trained:
    * Software: I trained the model using Python within a Jupyter Notebook environment. The libraries used include:
      * pandas and numpy to manipulate data
      * sci-kit learn to build models
      * matplotlib and seaborn to create visualizations
    * Hardware: All training and testing was done on my personal MacBook Air
  * Training was incredibly quick, since the dataset was so small
  * There were no significant difficulties I encountered, since the initial dataset was clean and well-prepared

### Performance Comparison

* I chose recall as my key performance metric
* Show/compare results in one table.
* Show one (or few) visualization(s) of results, for example ROC curves.

### Conclusions

* State any conclusions you can infer from your work. Example: LSTM work better than GRU.

### Future Work

* What would be the next thing that you would try.
* What are some other studies that can be done starting from here.

## How to reproduce results

* In this section, provide instructions at least one of the following:
   * Reproduce your results fully, including training.
   * Apply this package to other data. For example, how to use the model you trained.
   * Use this package to perform their own study.
* Also describe what resources to use for this package, if appropirate. For example, point them to Collab and TPUs.

### Overview of files in repository

* Describe the directory structure, if any.
* List all relavent files and describe their role in the package.
* An example:
  * utils.py: various functions that are used in cleaning and visualizing data.
  * preprocess.ipynb: Takes input data in CSV and writes out data frame after cleanup.
  * visualization.ipynb: Creates various visualizations of the data.
  * models.py: Contains functions that build the various models.
  * training-model-1.ipynb: Trains the first model and saves model during training.
  * training-model-2.ipynb: Trains the second model and saves model during training.
  * training-model-3.ipynb: Trains the third model and saves model during training.
  * performance.ipynb: loads multiple trained models and compares results.
  * inference.ipynb: loads a trained model and applies it to test data to create kaggle submission.

* Note that all of these notebooks should contain enough text for someone to understand what is happening.

### Software Setup
* List all of the required packages.
* If not standard, provide or point to instruction for installing the packages.
* Describe how to install your package.

### Data

* Point to where they can download the data.
* Lead them through preprocessing steps, if necessary.

### Training

* Describe how to train the model

#### Performance Evaluation

* Describe how to run the performance evaluation.


## Citations

* Provide any references.







