---
layout: post
title: Introduction to Scikit-learn’s Ensemble Methods
---

Hey! Are we all set to learn something about Ensemble methods?!
Hahaha! We sure are! Well, I am assuming you guys have some background or prior knowledge of basic Data Mining classification, clustering and regression algorithms, like Naive Bayes, Decision Trees, KNN, K-Means etc.

So, without further ado, lets get to it.

Ensemble Methods, talk about combining predictions from several “base estimators”. Now, this base predictor could be a K Nearest Neighbor classifier, a Decision Tree or I guess practically anything under the sun! (Kidding! Wont that be great though?!)

There are 2 broad types of Ensemble Methods-

Averaging Methods : Yep, you guessed it! These build the estimators independently and then compute an average score from those estimators and predict that! Eg : Random Forests
Boosting Methods : Here, we sequentially build estimators and try to reduce the bias of the combined estimator. What we are trying to achieve is to combine several weak models to produce a powerful ensemble. Eg : AdaBoost, Gradient Tree Boosting
RANDOM FORESTS

So how do Random Forests work?! As the name suggests, these are forests of randomly constructed Decision Trees.

Why are these called random you may ask? Because when splitting a node during construction of the Tree, the split that’s chosen is no longer the best among ALL the features. Instead the split that is chosen os the best split among the RANDOM subset of features.

Stuff to keep in mind about RFs :-

Bias of the forest increases
But due to averaging, its variance decreases
Overall due to decrease in variance, we get a better model.

In order to get a Random Forest up and running, make sure you have sci-kit learn up and running along with numpy. You can test out the following code to see how RF is built in python in just 6lines of code!!

from sklearn.model_selection import cross_val_score
from sklearn.ensemble import RandomForestClassifier
classifier = RandomForestClassifier(n_estimators=10, max_depth=None,min_samples_split=2, random_state=0)
scores = cross_val_score(classifier, X, y)
scores.mean()

Here, n_estimators is the number of Decision Trees that will be used(#trees in the forest). The more the merrier :P LOL Kidding! The more, implies more time complexity, better variance. Though obviously results will stop getting better beyond a critical number of trees.

Have my end semester examinations from Monday 11th December’17, so gotta go(though this has been fun! :)). Will write a post soon on AdaBoost and GradientTreeBoosting!

Please share if you enjoyed this! :D
