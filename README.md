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

a) Lasso Regression b)Random Forest Regression

The K-Fold cross validation was applied to both the algorithm. `K-Folds cross-validator provides train/test indices to split data in   train/test sets. Split dataset into k consecutive folds (without shuffling by default). Each fold is then used once as a validation while the k - 1 remaining folds form the training set.`

* vi) Result analysis

Comparing two different algorithms of predicitng the scores and then the accuracies of those two algorithms.
Then comparing the accuracy of each model. We also compared prosody features with the lexical features for different personalty traits.

# Analysis :
`Comparison of Random forest and LASSO on same personality
trait`
![accuracy](https://user-images.githubusercontent.com/22328407/42433489-325b2770-836d-11e8-9a17-6d8ebca00d27.png)

`Relative proportion of prosodic and lexical features after applying
LASSO`

![engaging_tone_3](https://user-images.githubusercontent.com/22328407/42433657-efd51d06-836d-11e8-95ff-2291f38d82b7.png)
![engaged_3](https://user-images.githubusercontent.com/22328407/42433658-f03e2378-836d-11e8-87c1-9cc397922fb4.png)

`Relative proportion of prosodic and lexical features after applying
Random forest`

![engaging_tone_4](https://user-images.githubusercontent.com/22328407/42433718-29fdf5ca-836e-11e8-950b-fe9194781e97.png)
![engaged_4](https://user-images.githubusercontent.com/22328407/42433719-2a8a0448-836e-11e8-93e9-0f801f79da7c.png)
