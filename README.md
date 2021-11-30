# -AI-2-Convolutional-Neural-Network
NN used in flights dataset to predict whether the flights would be delayed. CNN on Kannada MNIST dataset to classify between 1 and 0 digit.
Model interpretation and predictive intervals in NN
Overview and Data Description In this problem, you will be building and interpreting models to predict whether a flight was delayed for its arrival based on features 
that could be measured as the flight takes off. We will also estimate the predictive intervals of the model using bootstrapping. We will utilize those predictive 
intervals to build a new kind of model: a model that refrains from making a prediction when it is not confident. 
The included variables are: **ARRIVAL_DELAY**: the difference between scheduled arrival and actual arrival, in minutes (positive is late, negative is early). 
**DISTANCE**: the distance between arrival and departure airports, in miles. **SCHEDULED_TIME**: the flight's scheduled travel time. 
**MONTH**: the month the flight took off, 1 = January, 2 = February, etc. **SCHED_DEP_HOUR**: the scheduled departure time (the hour of the day).
**SCHED_ARR_HOUR**: the scheduled arrival time (the hour of the day). **FLIGHT_COUNT**: the number of flights flying out of that airport before noon on a typical day. 
**DAY_OF_WEEK**: the day of the week, 1 = Monday, 2 = Tuesday, etc. **ORIGIN_AIRPORT**: the airport the flight took off from. 
**DESTINATION_AIRPORT**: the airport the flight was scheduled to land at. 
For the airport codes, see: https://www.bts.gov/topics/airlines-and-airports/world-airport-codes 
To sucessfully complete this part, you will proceed by fitting a NN model, evaluating its accuracy, interpreting the predictors' importance, 
and finally evaluating the predictive intervals. **NOTE:** The observations were sampled so that roughly half of the observations were delayed
and half of the observations were not delayed.

CNN Problem Statement
ANNs can be prone to overfitting, where they learn specific patterns present in the training data, but the patterns do not generalize to new data.
There are several methods used to improve ANN generalization. One approach is to use an architecture just barely wide or deep enough to fit the data.
The idea here is that smaller networks are less expressive and thus less able to overfit the data.
However, it is difficult to know a priori the correct size of the ANN, and it is computationally costly to hunt for the correct size. 
Given this, other methodologies are used to prevent overfitting and improve ANNs' generalizability. 
These methodologies, like other techniques that combat overfitting, fall under the umbrella term of "regularization". 

In this problem, you are asked to regularize a network of a given architecture.
The Kannada MNIST Dataset
 For this problem, we will be working with a modified version of [Kannada MNIST dataset](https://arxiv.org/pdf/1908.01242.pdf) , 
 which is a large database of handwritten digits in the indigenous language *Kannada*. 
 This dataset consists of 60,000 28x28 grayscale images of the ten digits, along with a test set of 10,000 images. 
 For this homework, we will simplify the problem by only use the digits labeled `0` and `1` owing to the similarity of the two symbols, 
 and we want to use a total of 1200 samples for training (this includes the data you will use for validation). 
 To understand the dataset better, we recommend this [article](https://towardsdatascience.com/a-new-handwritten-digits-dataset-in-ml-town-kannada-mnist-69df0f2d1456) by Vinay Prabhu, the curator of the dataset.
