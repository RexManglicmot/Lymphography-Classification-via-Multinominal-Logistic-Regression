# Lymphography Classification via Multinomial Logistic Regression

## Continuing Working document

Things still need to do:

* How to run code chunks on Python Markdown...I may need help on this bit. I Googled and Overstacked the heck out of it.
  I still unable to figure it out.
* Flush out intro
* Add more content to the MLR section such as what is it, applications, pros and cons
* Grammar
* Get feedback on work and incorporate

## Introduction

![](https://healthjade.net/wp-content/uploads/2019/12/lymph-node-infection.jpg)

The lymph nodes are a specialized organ that is responsible for our bodies immune response. They are primary sites where
many immune cells like T-cells and B-Cells, and Natural Killer cells are made to ward of microbial infections.

## Loading the Libraries

```python
# load libraries
import pandas as pd
import seaborn as sns
import numpy as np
```

## Loading the Data

```python
# load the data from the UCI website into an object
data_source = "https://archive.ics.uci.edu/ml/machine-learning-databases/lymphography/lymphography.data"

# store into a panda dataframe
data_orig = pd.read_csv(data_source)
mouse = pd.read_csv('mouse.csv')

# show data
print(data_orig)
print(mouse)

```

## Cleaning the Data

```python
 data_orig.tail()


```

## Exploratory Data Analysis

```
hmmm

```

## Multinomial Logistic Regression

Multinomial Logistic Regression (MLR) modeling is used a type of supervised learning that is used to classify a
categorical dependent variable from one or more independent variables. In essence, MLR uses the same concept of
Logistical Regression, but determining the probability a dependent variable is and classifying it accordingly. Here,
with MLR, instead of a binomial classification, it is now multiclass.

Examples of MLR range from a multitude of industries. Classifying a particular plant from a set of numerical independent
variables. Another is classifying whether a person has Stage 1, 2, or 3 cancer. Lastly, in terms of business, it can be
used to classfiy a customer's product preference amongst a sea of products. The usage of MLR are widerange and
encompassing.

To further elaborate, we can ask the question of, which bank would a person choose to deposit their savings?

Dependent Variable:
(again, this variable can have two or more possible outcomes)

* Goldman Sachs
* JP Morgan
* Deutsche Bank

Independent Variable:

* Age
* Gender
* Income
* Occupation

The Logistic Regression uses a Sigmoid function to determine whether an observation (y) is classified in one class or
another. Here, it is binary class where y ∈ {0, 1}. In the case of Multinomial Logisitic Regression it uses a Softmax
regression for classification. Here, we can have up to K classes, where y ∈ {1, 2, 3, ...k}. In Softmax, it predicts the
class of an observation by calculating the probability among all the K classes.

![](https://d1m75rqqgidzqn.cloudfront.net/wp-data/2021/03/26140357/Screenshot-2021-03-26-140320.png)

There are 3 classifications; A, B, and C. In the exhibit above, each observation will have 3 models each with each own
probability and the model with the highest probability, then that observation is categorized as such.
If P(A) > P(B) and P(A) > P(C), then the observation is classified as A.

# Pros

* Easy to implement and understand. It builds slightly upon the Logistic Regression concept.

# Cons

* Inapplicable to an ordinal dependent variable. In some data sets the dependent variables tend to have a natural
  ordering amongst them such as least likely to most likely. In datasets such as this, a different model is more
  appropiate (Ordinal Regression).

```python
#build out the model
```

## Limitations

## Conclusion

## Inspiration for this project



