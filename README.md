# Plagiarism Project, Machine Learning Deployment

This repository contains code and associated files for deploying a plagiarism detector using AWS SageMaker.

## Project Overview

In this project, you will be tasked with building a plagiarism detector that examines a text file and performs binary classification; labeling that file as either *plagiarized* or *not*, depending on how similar that text file is to a provided source text. Detecting plagiarism is an active area of research; the task is non-trivial and the differences between paraphrased answers and original work are often not so obvious.

This project will be broken down into three main notebooks:

**Notebook 1: Data Exploration**
* Load in the corpus of plagiarism text data.
* Explore the existing data features and the data distribution.
* This first notebook is **not** required in your final project submission.

**Notebook 2: Feature Engineering**

* Clean and pre-process the text data.
* Define features for comparing the similarity of an answer text and a source text, and extract similarity features.
* The features explored were _Containment Score_ and _LCS score_ . The _Containment Score_ was calculated on n-grams where n ~ range(1, 11)
* Select "good" features, by analyzing the correlations between different features. The features with the lease correlation was chosen to train the model.
* Create train/test `.csv` files that hold the relevant features and class labels for train/test data points.

**Notebook 3: Train and Deploy Your Model in SageMaker**

* Upload train/test feature data to S3.
* Define a binary classification model and a training script. 
* I tried out _SVM and Random Forest_ models and RF seemed to perform better
* Train Randon Forest model and deploy it using SageMaker.
* The accuracy of the model turned out to be 96%


---

Please see the [README](https://github.com/udacity/ML_SageMaker_Studies/tree/master/README.md) in the root directory for instructions on setting up a SageMaker notebook and downloading the project files (as well as the other notebooks).

