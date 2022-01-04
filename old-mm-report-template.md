# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Margit

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
Well I realized given the Jupyter notebook that we needed to put the predictions into the submissions.csv format. Much later, I realized I'd made an error with how I was putting the predictions into the submissions dataframe, so my scores improved, especially with the new features added, once I'd fixed that.

### What was the top ranked model that performed?
The weighted ensemble tended to do best.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
Datetime wasn't as useful as it could be because it was single points spread out over time - no aggregation by hour or month or day. Some features were more continuous, such as temp, humidity, windspeed, and some were more categorical such as season, holiday, and working day. I added additional features by parsing hour, month, and day out of the datetime feature, and I also modified a couple of features to be categorical in type.

### How much better did your model preform after adding additional features and why do you think that is?
The model performed much better with the new features, probably because being able to analyze how bike sharing usage varied with time of day or day of week or month of year ended up improving predictions.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
My model didn't perform that much better, in part because I haven't had much time to really dig into the various hyperparameters (including model specific ones) that could be useful.

### If you were given more time with this dataset, where do you think you would spend more time?
I might do more exploratory data analysis to see if there may be other features that could be generated that could help. I guess also further exploring hyperparameter optimization could help.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
	initial	add_features	hpo
num_bag_folds	0	0	5
num_bag_sets	0	0	1
num_stack_levels	0	0	1
score	1.39719	0.47173	0.047068
![image](https://user-images.githubusercontent.com/1861163/147906453-eac276b7-1d50-419f-8a1b-cedd6776e28e.png)


### Create a line plot showing the top model score for the three (or more) training runs during the project.
![image](https://user-images.githubusercontent.com/1861163/147906074-153ff116-0f75-48c8-abd2-3fa6cfe6be06.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![image](https://user-images.githubusercontent.com/1861163/147906082-291a1ef2-ff58-4f3a-b270-3399cc3cc3bc.png)

## Summary
I enjoyed this exercise and it gave me an appreciation for the importance of exploratory data analysis and feature creation, as well as for the power of AutoGluon in finding an effective model.
