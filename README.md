
# WATER QUALITY PREDICTION

The purpose of this project is to deliver a machine learning solution to predict the quality of the water for the given sample parameters.This repository contains the code to predict water quality by using various machine learning models. 

# TABLE OF CONTENTS
i) Getting Started

ii) Data Preprocessing 

iii) Data Visualisation

iv) Observing the effect of Outliers

iv)Training with different ML algorithms

v) Training with Deep Learning algorithm

vi) predicting the results

vii) computing the F1 SCORE

viii) Creating a web app using ANVIL app designer

# Getting Started

The training dataset was uploaded in the google drive in the following link:
<p> https://drive.google.com/file/d/1HBbbwZ5cCj_Xp6yR8MTkTgDuSOVo9dj5/view
  
This dataset path was imported into the "GOOGLE COLAB" which is an online based compiler for ML algorithms, which has most of the libraries preinstalled. All the necessary libraries like 'numpy', 'pandas', and 'matplotlib' were imported so that we can use them on our dataset.

# Data Preprocessing 

First we have imported the dataset in the pandas frame using the pandas library that we imported before, and created the matrix of features and the dependent variable vector and we have also observed that there were minority classes in the dataset which might be ignored by our model during prediction. Hence we have applied SMOTE (synthetic minority oversampling technique) to increase the number of minority samples in our data so that our ML model won't ignore them during training part. Further information can be read in the following link
  
<p> https://towardsdatascience.com/smote-fdce2f605729
  

We have also applied the info() method to chech whether there were any missing values in the data and found no missing values and since all the training data was having numerical datatype, we don't need to encode any data as well. 

# Data Visualisation
  
 For visualisation purpose, we have used heatmaps and boxplots to observe the correlation and the outliers in our data respectively. Following are the images we obtained:

  ## HEATMAP WITHOUT SMOTE
![alt text](https://github.com/hs181/IITBBS_GC_Team20_PS03/blob/main/Corrleation_plots/CORR_WITHOUT_SMOTE.png)
  ## HEATMAP WITH SMOTE
![alt text](https://github.com/hs181/IITBBS_GC_Team20_PS03/blob/main/Corrleation_plots/CORR_WITH_SMOTE.png)
  
  ## BOXPLOT FOR SOME PARAMETERS
  
 ![alt text](https://github.com/hs181/IITBBS_GC_Team20_PS03/blob/main/Box-plots-visualisation/Mud.png)
 ![alt text](https://github.com/hs181/IITBBS_GC_Team20_PS03/blob/main/Box-plots-visualisation/P15.png)
  
  
 # OBSERVING THE EFFECT OF OUTLIERS
 
  ![image](https://user-images.githubusercontent.com/84396869/159155069-7fd184fb-358d-414e-91e6-5fc5734920f8.png)

  We have tried to remove the outliers so as to simplify our future ML models but when we observed the box plots we see that outliers mostly consist of the minority class and removing them will mean removing the minority class data which might affect our accuracy of our ML model hence we have decided to not do so.
