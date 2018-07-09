# Prediction-of-job-interview-performance-by-extracting-prosody-features
Analysis done on verbal and non-verbal features of interviewee in the interview.

**Work Done:-**
* quantify the relative inﬂuences of diﬀerent low level features on the interview performance.
* used regression models to predict interview ratings and the likelihood of hiring using extracted features.
* predicts several other high-level personality traits such as engagement, friendliness, and excitement.

`The objective of the project is to extract the various prosody features responsible for diﬀerent personality traits and predict scores for various personality traits given a interview sound file.`

# Dependencies:
* Numpy
* Pandas
* NLTK
* Matplotlib
* sklearn
* Python3

Use [pip](https://pypi.org/project/pip/) to install any missing dependencies.

```Here we use MIT Dataset. The research paper followed was ```[Automated Prediction and Analysis of Job Interview Performance](https://ieeexplore.ieee.org/document/7579163/)

# Overview:
**To accomplish our objective ,the work is completed in the following steps:-**
* i) Raw data set
It contains 138 sound file(.wav file). We are not using mp3 and other data
compression format as some data is lost which can be crucial in speech analysis
for detecting some features.

* ii) Pre-processing
In pre-processing, noise is removed from sound files. Praat(Open Source pro-
gram for scientific analysis of speech in phonetics.) is used for removal of noise.
In noise removal, spectral subtraction method was used to remove noise. The
filter frequency range was 80Hz to 10 KHz.

* iii) Extracting Sound Features
To verify the csv file containing extracted features, Praat and MATLAB were
used.

* iv) Feature Selection
Relevant features based on Information Gain measures for respective response
were selected for further processing. The Mutual Information of all features for each personality traits was calculated. Top seven feature is selected based on Mutual Information .`Mutual information (MI) between two random variables is a non-negative value, which measures the dependency between the variables. It is equal to zero if and only if two random variables are independent, and higher values mean higher dependency.`

* v) Regression Method
Two regression methods were used:
1) Lasso Regression 2)Random Forest Regression
The K-Fold cross validation was applied to both the algorithm. `K-Folds cross-validator provides train/test indices to split data in   train/test sets. Split dataset into k consecutive folds (without shuffling by default). Each fold is then used once as a validation while the k - 1 remaining folds form the training set.`
* vi) Result analysis
Comparing two different algorithms of predicitng the scores and then the accuracies of those two algorithms.
Then comparing the accuracy of each model. We also compared prosody features with the lexical features for different personalty traits.


