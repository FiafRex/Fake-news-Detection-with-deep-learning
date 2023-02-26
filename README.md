# Fake-news-Detection-with-deep-learning
This project will seek to detect fake news articles by looking out for keywords (such as "POPE", "TRUMP" etc.) from news sites (with sufficiently large datasets) and then comparing them to a dataset (from Kaggle). The model has been trained to report an avg accuracy of 90%.

**How to set it up?**
In order to get started with the code-you need to use google collab. Why? Well, google collab is far better for ML codes than other compilers since it executes para-based code i.e instead of executing the whole code at once, it will separate the code into subsections and ask you to choose which ones to run (and if you want to run them all...you can do that too).
Apart from that, Google collab allows you to well...collab-since the whole code is stored in cloud servers-there's no danger of losing code due to power failures etc. Further, you can work with multiple people on the same code.

**Before starting, go to the EDIT option (in the menu bar), click on notebook settings and set the hardware accelarator to GPU-this will save you a lot of time.**

And yeah, that's about it-everything else that you need such as (numpy, pandas etc.) will be installed by command line arguments.

*MODULES USED IN THE PROGRAM*
1-NumPy:A library used in python: specifically made for working with arrays.
It options for working with linear algebra, fourier transforms and matrices.
Reason for usage: NumPy aims to create an array object that is 50 times faster than
traditional Python lists.

2-Pandas: Pandas is an open-source library that is used for analysis of data and high
performance data-manipulation. It is also built on top of the Numpy package.
Reason for usage: Pandas has a fast and efficient algorithm-that allows quick manipulation of data;
and for reshaping and pivoting of data sets.

3-Matplotlib: Matplotlib is a visualization library in Python used for 2D plotting of
arrays. It is a multi-platform data vis-library built over NumPy and is supposed to work over
the broader SciPy stack.

3-wordcloud:Wordcloud or Tag Clouds is a technique for visualizing texts in a way
such that tags and keywords are highlighted from the sites. These keywords are typically
used for single words that depict the content of the webpage the word cloud is made from

4-- TENSORFLOW: While not strictly a type of deep learning-Tensorflow is often used in tandem with it.
It is an open source platform containing a variety of workflow with high-level APIs
that allows creation of machine learning models in numerous languages.

**HOW DOES THE CODE WORK?**
**Step 1- Finding the difference between word clouds of real and fake news:**
Helps us to visualize better like which words are frequently occuring in the dataset.
Real news seems to be published by certain publications that are not present in the case of
fake news. Analyzing the data we could observe -
1]Most of the text contains information such as WASHINGTON (REUTERS)
2]Some text are tweets.
3]Few pieces of texts do not containt any publication info.

**STEP 2-Cleaning the data**
First we will remove the reuters or tweets from the text. Text can be splitted only once at -
which would be always present after mentioning source of publication: giving us the
publication part and the text part. So here, there could be two possiblities like if for some
record, publication details was not there in the dataset itself or if it is a tweet. We create a
function called unknown publishers for this and then append this data into that. In this
process we will also eliminate those news articles which doesn't contain any text in the
dataset. At the end, for both real and fake news we would store the text and title of the news
articles in their respective datasets.

**STEP 3-Preprocessing Text**
We will assign class labels to both real and fake news items. Then in the final dataset we
would combine both real and fake news together along with their text and class.

**STEP 4-Vectorization**
Convert text data into numeric data. With the help of Word2Vec, we will process word
embedding which would help to capture context of word in a text or help us with finding
semantic and syntactic similarity. Here, with the help of this we could find the exact same
word for what we are looking into and also we could get the most similiar words. We can
feed this vectors aa initial inputs on the machine learning models and recreate these vectores
which would help us to increase the accuracy


**HOW TO TEST THE MODEL*
Simply copy and paste any large summary/dataset from a news site into the x=[] field (at the end) and run the code.


e.g sites:
*https://www.moneycontrol.com/news/trends/health-trends/covid-19-dgca-lifts-mask-mandate-for-air-travel-says-its-no-longer-compulsory-9547761.html*
*https://www.moneycontrol.com/news/coronavirus/china-eases-covid-curbs-on-domestic-group-tourism-trips-9539581.html*
*https://www.moneycontrol.com/news/health-and-fitness/how-covid-19-causes-neurological-damage-found-9539591.html*
