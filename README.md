# Airbnb New Users Challenge on kaggle
You can find the Jupyter notebook on google colab [here](https://colab.research.google.com/drive/1H6mTaO9bERyjZSp9yzfIQcnm3J6mySlA?usp=sharing)
## Data Visiualizations
I began with visualizing the data on the csv files to get a sense of what the data looks like and discover useful features. Usually, after this step I would develop hypothesis on the features and test them; however, I did not find one feature that correlates to the destination country output more than the others. So, I only noted some useful insights that I found (available on the [presentation](https://docs.google.com/presentation/d/1AJm09x3saScGr_yw8N0qMDjO262uK-gOh8hJz6AhS80/edit?usp=sharing))
## Feature Extraction
To make use of the available session data, I summed up the total time each user performed on each unique action and added those actions as new features to the training and testing set. It's worth noting that there are some actions that are only performed by the users on the training set and others only by users on the test set. I used the intersection of the set of actions by test users and train users as added features. This improved the submission score from 0.86 (without added features) to 0.88(with added features).
## The Model
I used a XGboost classifier. XGboost is a tree based ensemble classifier that uses boosting which is a technique in which each model trains with more emphasis on improving on the mistake of the prevous model. Tree based classifiers are well suited for tabular data due to the fact that they can extract rules for classification. 
## Results
Private score on kaggle (0.883)
Public score on Kaggle (0.8786)
