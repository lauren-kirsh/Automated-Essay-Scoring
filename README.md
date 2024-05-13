# Automated-Essay-Scoring

## Background

We were tasked in conducting a fairness audit on an Automated Decision System (ADS) in order to determine whether or not it should be used in real life applications. We audited an automated essay scoring system created for a Kaggle competition.

## Overview
The William and Flora Hewlett Foundation (Hewlett) sponsored the Automated Student Assessment Prize (ASAP). Hewlett is appealed to data scientists and machine learning specialists to help create a fast, effective and affordable solutions for automated grading of student-written essays. Hewlett provided the training, validation, and test data and challenged developers to create the automated scoring algorithm. The data has been preprocessed using the Named Entity Recognizer (NER) developed by the Stanford Natural Language Processing group to help hide personally identifying information in the essay data.

Link to competition on Kaggle: https://www.kaggle.com/c/asap-aes/overview

All the sections in the Audit_Automated_Essay_Scoring Jupyter Notebbok are copied from Kaggle (https://www.kaggle.com/irfanmansuri/the-havelett-foundation-automated-scoring) except the "Outcomes" section. The "Outcomes" section demonstrates our exploration of the fairness quality of the Automated Essay Scoring. 

## Study

We used two models, k-nearest neighbors and logistic regression, to model fairness. Fairness measurements were challenging due to the absence of typical sensitive attributes; therefore, grade level was used as a proxy. Both models exhibited skewed score distributions, with logistic regression performing slightly better. Despite low accuracies, disparities favoring the unprivileged group were observed, indicating potential bias. Analysis using SHAP explainers on the k-nearest neighbors model revealed problematic predictions outside the score range, highlighting the ADS's shortcomings in accurately scoring essays.

## Outcome

In conclusion, deploying the Automated Essay Scoring System in the public sector is not advisable due to several critical issues. Firstly, the provided data lacks proper ground truth data, hindering the ability to assess fairness effectively. Secondly, both machine learning models used in the ADS exhibit extremely low accuracy, rendering them unreliable for grading essays accurately. Moreover, the models fail to account for crucial aspects of human grading, such as punctuation and grammar, leading to further inaccuracies. Lastly, the Automated Essay Scoring System demonstrates a disparity in outcomes favoring the unprivileged group, undermining the principle of group fairness. Consequently, deploying this ADS for automated essay scoring is not recommended due to its shortcomings and potential biases.
