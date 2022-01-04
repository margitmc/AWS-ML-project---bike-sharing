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
My model didn't perform. I tried various things in terms of actual hyperparameters after getting the submission feedback that I hadn't done this properly before. I tried NN and GBM hyperparameters, but then NN still seemed to score low, so I tried some variations on GBM hyperparameters including adding a couple. I also extended the allowed time. However, I never got the scores better than just with the new featuures and no HPO. I'm a bit fumbling in the dark with these hyperparameters and how to get them all to be explored properly.

### If you were given more time with this dataset, where do you think you would spend more time?
I might do more exploratory data analysis to see if there may be other features that could be generated that could help. (The feedback on my first submission had some interesting ideas - thanks!) I guess also further exploring hyperparameter optimization could help. At this point I need to move onto the other modules in this nanodegree so I'll leave it here for now.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
![image](https://user-images.githubusercontent.com/1861163/147995091-f3da494b-3567-493b-b0cc-912b31608cad.png)


### Create a line plot showing the top model score for the three (or more) training runs during the project.
![image](https://user-images.githubusercontent.com/1861163/147906074-153ff116-0f75-48c8-abd2-3fa6cfe6be06.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![image](https://user-images.githubusercontent.com/1861163/147995134-207b4acb-867d-450b-adec-3b0ddbc9f1e0.png)

## Summary
I enjoyed this exercise and it gave me an appreciation for the importance of exploratory data analysis and feature creation, as well as for the power of AutoGluon in finding an effective model.
