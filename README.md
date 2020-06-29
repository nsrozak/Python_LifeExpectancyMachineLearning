# Prediction of Life Expectancy

## Introduction

This project uses Python and Pandas to predict the life expectancy of a country. 

## File Descriptions

***Life_Expectancy_Data.csv:*** Main data source for this project.

***Country.csv:*** Secondary data source for this project.

***DataPreprocessing.ipynb:*** Data cleaning and splitting dataset into train and test.

***DataExploration.ipynb:*** Data visualization and principal component analysis.

***MachineLearning.ipynb:*** Training regression machine learning models with `sklearn`.

***AnalyzeResults.ipynb:*** Analyze results of Gradient Boosted Tree model.

***Charts:*** Graphs used in each of the files.

## Viewing Graphs

Altair charts do not display on GitHub. However, I included these graphs in the *Charts* folder. Also, charts can be viewd by going to https://nbviewer.jupyter.org/ and inputting the URL of the project.
 
## Limitations

I assumed that the data was uncorrelated in time. This dataset ranged from 2000 to 2014, so life expectancy only slightly increased with time. However, over a longer time frame, there is definitely a correlation between life expectancy and time as new medicines and technologies get created. Therefore, my models should not be used for dates that are far from the range of values that the model got trained with. 

Furthermore, the model is biased towards the life expectancy values that it was trained on. I believe that the `Region` variable will become inaccurate as more nations gain access to new technology and better medicines. Eventually, life expectancy will become uniform throughout the globe and there will be no need to differentiate it by country so this model will not be useful. 

## Findings

Exploratory data analysis showed that developed countries typically had higher life expectancies than developing countries. Countires in Europe, Asia, and North America also typically have higher life expectancies. Moreover, life expectancy had large, positive correlations with schooling and income composition of resources. HIV/AIDS and thinness had large, negative correlations with life expectancy. 

All of the machine learning models performed very well on the train and test datasets. The best model was Gradient Boosted Tree with an RMSE of 2.0291 years. Important features for the GBT model were the income composition of resources and HIV/AIDS prevalance. The model performed best for North America and South Asia, and it had difficulty predicting regions such as Sub-Sahara Africa, the Middle East and North Africa, and Europe and Central Asia. The regions with larger RMSE values have countries with a broad range of life expectancy, which could have contributed to the miscalculations by the model. Additionally, the model did a very good job of predicting large values of thinness, population size, and BMI.
