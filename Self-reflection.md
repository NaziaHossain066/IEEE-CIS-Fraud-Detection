<h1>Preamble:<\h1>

Through this project I embarked on my journey of exploring Machine Learning. As I am new to this sector having no prior experience, my initial goal was to build a running model. Having majored in Electrical and Electronic Engineering, this wasn't easy. It was the first time I was implementing my theoretical knowledge in pratical application.

##The Challenges I faced:

####1) I had a hard time deciding which platform to choose. The datasets in this competition are huge, and working with them in kaggle and google collab seemed impossible without hitting the limit, which lead to sudden restart of the notebook.

<strong>Fix</strong>:

The data usage has to be truncated manually. For example, whenever we load a CSV into a column in a dataframe, it will assign 64 bytes to store 1 numerical value. We can reduce that and use other int formates to save some memory.

int8 can store integers from -128 to 127

int16 can store integers from -32768 to 32767

####2) Dealing with so many features was a daunting task.

<strong>Fix</strong>:

 In the Discussion section of the competition in kaggle, some insights about the features were provided. There were in total 433 features, and 1 target. Of the 433 features, after droping the features with more than 80% null value, I worked with 359 features. Of the total features, 26 were categorical and the others were numerical.
####Categorical Features:
Replaced the null values with a single term 'un' and finally label encoded them along with scaling.

####Numerical Feature:
As there were 333 columns, to reduce the dimension, I used PCA.

###3)The provided dataset is highly imbalanced, with more than 99% normal transaction and less than 1% fraud transaction.

<strong>Fix</strong>:

To tackle this problem I used SMOTE upsampling to increased fraud transaction instances. Finally used Lightgbm to create the model.

##Takeaway from the project:

 My takeaway from the project is, only through applying the theoretical knowledge in practical instances, an individual will get better in this sector. I will have to dive deeper into the theory part to understand the actual use of different algorithms. Enjoyed every bit of the project.
