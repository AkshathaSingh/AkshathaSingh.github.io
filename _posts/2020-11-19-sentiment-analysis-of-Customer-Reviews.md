---
published: true
---
![alex-motoc-iImF3APdKmk-unsplash.jpg]({{site.baseurl}}/images/alex-motoc-iImF3APdKmk-unsplash.jpg)

<span>Photo by <a href="https://unsplash.com/@alexmotoc?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Alex Motoc</a> on <a href="https://unsplash.com/t/experimental?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span>


Enormous amount of data is generated on digital platforms, especially in an unstructured format and mostly in text format like Reviews, Comments, Tweets, Captions, and Posts. 

It is difficult to shift through every piece of content to understand the opinion of the writer and the sentiment behind it and gather insights to make informed decisions. 

That’s where the process of Sentiment Analysis comes into the picture, it helps us understand the emotion and opinion of a wider range of audience about a product or topic of interest by identifying the sentiment behind it. 

The two important parts of the process of sentiment Analysis is **Natural Language Processing** and **Machine Learning**, and the sentiments are classified as Positive, Neutral and Negative.

## Overview:

In this project we are implementing a 3-way Sentiment Analysis of the customer reviews of the Amazon’s Grocery and Gourmet Food Platform. We will classify the reviews as positive, negative or neutral with the help of machine learning and preprocess our data in an unstructured text format using natural language processing.

The data has been taken from Amazon Reviews Data, Julian McAuley UCSD. The dataset consists of 5000 reviews with ratings on the scale of 1-5. The implementation of the project is divided into the following parts, Data Collection and Cleaning, Data Preprocessing, Classification using machine learning and Model Evaluation.  

## Data Collection:

The customer reviews data of Amazon's Grocery and Gourmet Food platform is in json format and the data is unstructured. There are around 5 million reviews, I have collected a set of 5000 reviews to implement the project. I followed the following steps to complete the process of Data Collection.

- Created a dataframe by converting the unstructured data in a structured format and saved the data as a csv file.
- Removed the columns not relevant for our project.
- Renamed the columns as ‘Reviews’ and ‘Rating’.
- Checked for the presence of missing values and dropped the rows with missing values.

## Data Preprocessing:

As our data is in text format, the preprocessing step has been carried out with the help of Natural Language Processing, this step is done to **transform the data in a format which is compatible with our machine learning model to train on.**

![wc.PNG]({{site.baseurl}}/images/wc.PNG)


- Using the Regular Expression (re) package, substituted the special characters in our reviews with a space.
- Transformed all the characters to lowercase.
- Then split sentences to words.
- Removed stopwords and converted each word into its root form.
- Combined all the reviews and created a corpus, a list of reviews.
- Finally, converted the data into a document matrix where sentences are replaced by a vector which gives the count of each word's occurrence in the corpus, this is referred as **Bag of words**.
- Then the dataset is **split into a training set**, which is used by our machine learning model to learn on and a **test set**,which is used to evaluate the performance of our model.

## Classification and Evaluation:

Here, three classification algorithms have been used to train the model, Naive Bayes Classifier, Decision Trees and Support Vector Machines. The performance of all the three models is compared and the one with highest is selected for predictions on new data.

The algorithms are trained using the **training dataset** and are evaluated by comparing the predictions of the model on the test set with the actual values of the **test set**.

- Naive Bayes Classifier:

![nbc.PNG]({{site.baseurl}}/images/nbc.PNG)


The accuracy in predictions of **Naive Bayes Classifier is 82%**

- Decision Tree Classifier: 

![dt.PNG]({{site.baseurl}}/images/dt.PNG)


The accuracy in predictions of **Decision Tree is 76%**

- Support Vector Machine: 

![svm.PNG]({{site.baseurl}}/images/svm.PNG)


The accuracy in predictions of **Support Vector Machine is 79%.**

## Conclusion:

**The classifier which is performing well on our data among the three is Naive Bayes Classifier with an Accuracy of 82%.** 

This Concludes our project of Sentiment Analysis with a note that the accuracy of our models can be improved by creating a more **balanced dataset**.
