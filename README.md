# Ensemble Learning and Random Forests

#### Most popular Ensemble methods:
- bagging and pasting
    - Use the same training algorithm for every predictor and train them on different random subsets of the training set.
    - When sampling is performed with replacement, the method is bagging (bootstrapping aggregating). In statistics, resampling with replacement is called bootstrapping.
    - When sampling is performed without replacement, the method is pasting.

![download](https://user-images.githubusercontent.com/44503223/126904459-3a1846e2-0174-4030-813e-98b30c972586.png)

- boosting
    - Train predictors sequentially, each trying to correct its predecessor. 
    - **AdaBoost**: The algorithm then increases the relative weight of misclassified training instances. Then it trains a second classifier, using the updated weights, and again makes predictions on the training set, updates the instance weights.
    - **Gradient Boosting**: instead of tweaking the instance weights at every iteration like AdaBoost does, this method tries to fit the new predictor to the residual errors made by the previous predictor.
    - **XGBoost**: a scalable tree boosting system and an optimized implementation of Gradient Boosting. 
- stacking
    - instead of using trivial functions (such as hard voting) to aggregate the predictions of all predictors in an ensemble, stacking trains a model to perform this aggregation.

#### Voting Classifiers
- Hard Voting Classifiers (predict the class that gets the most votes)
- Soft Voting Classifier (predict the class based on the highest class probability, averaged over all the individual classifiers.)

#### Random Forest
- Train a group of Decision Tree classifiers, each on a different random subset of the training set.
- Instead of searching for the very best feature when splitting a node, it searches for the best feature among a random subset of features.
- Obtain the predictions of all the individual trees, then predict the class that gets the most votes.

#### Extra-Trees
- Extra-Trees makes trees even more random by also using random thresholds for each feature rather than searching for the best possible thresholds (like regular Decision Trees do).

#### Feature Importance
- Feature Importance calculates how much the tree nodes that use that feature reduce impurity on average (across all trees in the forest).


## Learn More

To learn more, please visit the Project Portfolio page at https://tingting0618.github.io

## Reference

This repo is my learning journal following:
- Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow, 2nd Edition, by Aurélien Géron (O’Reilly). Copyright 2019 Kiwisoft S.A.S., 978-1-492-03264-9.
- StatQuest: Decision Trees https://statquest.org/statquest-decision-trees/
