# deep-learning-challenge
GTPE Data Science Boot Camp Module 21 Challenge

This repository contains course-provided starter code in the Starter Code folder, the Jupyter notebook that analyzes the dataset, and the exported HDF5 of the neural network model.

Analysis Overview

The analysis was on funded project success data, and the original dataset contained, for example, the following columns:
  EIN
  NAME
  APPLICATION_TYPE
  CLASSIFICATION
  USE_CASE
  ORGANIZATION
  STATUS
  INCOME_AMT
  SPECIAL_CONSIDERATIONS
  ASK_AMT
  IS_SUCCESSFUL

The goal of the analysis was to train a model to be able to predict the success of future projects to fund.

EIN and NAME were discarded as this information was considered irrelevant. 
All remaining non-numerical entries were converted to numerical using get_dummies.

IS_SUCCESSFUL was the target, all remaining columns were used as features.

The dataset was split into training and testing sets and used to train a neural network model. 
The model used 3 hidden layers with decreasing units and RELU activations until the final output layer, which used sigmoid.
The input layer used 37 input dimensions, following the size of the scaled features dataset.
The hidden layers use decreasing units 30, then 20, then 10. The final output layer has only 1 unit, since I want a "yes/no" answer.


Results

Neural Model with scaled dataset came out with a final evaluation of:
Loss: 0.6914709806442261, Accuracy: 0.5295627117156982

Summary

Given that we capped out at an accuracy of 0.5295627117156982, I don't think this was a super successful attempt.
The loss definitely decreased dramatically over time though.
