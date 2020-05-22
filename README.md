##COMP6200 Data Science Portfolio 
========================================================================
Name:Nakul Soni
Student ID:46153640

The repository contains all the portfolio projects.I have worked on three analysis task and explain each portfolio below explicitly.

Portfolio projects

1. Analysis of CSV data for cycling 
2. Analysing COVID-19 Data
3. Predicting the Genre of Books from Summaries

##Analysis of CSV data for cycling
=========================================================================
**Introduction**
The portfolio is all about to analyse the Cycle data.We are analyzing the data from two different location, one dataset comes from the online platform and other dataset come from application.We will be analysing the some important variable and explore the relationship among these variables of the dataset.

**Getting data**
We have two dataset, one comes from [Strava](https://strava.com/), this website contains cycling and other sports data, other dataset comes from
application [GoldenCheetah](https://www.goldencheetah.org/) that contains the other rides data.
We will be extracting the data in the CSV format, so that we can easily understand the data.

**Exploring the data**
While exploring the data we find out that the two dataset are in different time zone, so we have done some conversion that will convert the data in the local time zone.
There are some important variable that we have explain in the portfolio, few are e.g. given below
*Duration* - overall duration of the ride, should be same as elapsed_time
*Time Moving* - time spent moving (not resting or waiting at lights), should be the same as moving_time
*Elevation Gain* - metres climbed over the ride
*=*Average Speed* - over the ride
*Average Power* - average power in watts as measured by a power meter, relates to how much effort is being put in to the ride, should be the same as  * average_watts' from Strava
**Methods**
We haven't use any specific methods in this portfolio, we have just learnt in exploring the data at more granular level and plot the data of the column of the dataset.
We have first combine the  two dataset into single dataset and keeps only those rows of dataset that appears in both the dataframe so that we have complete data for one row.
So, once we got the data we have done some small techniques in finding the relationship among the variables, we have plot the summary data and calculate the distance of a ride for a month over a period of time.
**Correlation**
Next we have find the correlation among the key variables.Correlation is the process of finding the statistical relationship between two variables.Correlation can be positive, negative and neutral correlation.
**Distribution**
The other method we have used is skew method.skew method is used to measure the distribution on its mean.The skewness value can be positive, zero, negative, or undefined.We have depict the distribution of data of some specific variables and find which variable has symmertric distribution and which have asymmetric distribution.
**Conclusion**
In this Portfolio, we have learnt how to generate graph for a specific and also learnt some technqiues that are helpful in exploring the data set and can also help us in visualising the dataset.We have learnt about correlation and distribution of data among the variables of the dataset.The techniques and methodologies we have learnt in this portfolio will help us in prediction and modelling of data. 


##Analysing COVID-19 Data
=========================================================================
**Introduction**
The portfolio is all about to analyse the global spread of COVID-19 in the world.COVID-19 is a respiratory illness caused by a new virus, it Symptoms include fever, coughing, a sore throat and shortness of breath. The virus can spread from person to person, but a person having good hygiene can prevent this infection.

Our aim is to explore the dataset,plot the exponential increases in the cases and build a model that will help us to understood in creating a technique to prevent the coronavirus disease, there are number of  open dataset and stories available that show number of cases in the country, total death caused by coronavirus , or number of recovered cases in the coronavirus.

**Getting data**
We are only focusing on the increase number of coronavirus cases in the country, we are extracting the data from [ArcGIS Dashboard](https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6) Johns Hopkins university and will do analysis on this data.The data we get from the story are breakup on the state or territory bases, so we combine the data on based of country and then start our anaysis.

**Exploring the data**
Now after getting the number of cases on country basis, our first task is to compare the number of cases on the country basis and plot the data  for the countries.Next we are extracting only that part of time series that have cross 100 number of cases and then compare these countries to find out which country had first crossed the 100 number of cases in the world.It is an important visualization as it helps us in comparing the countries and we can also find out the present number of cases of these countries.
**Method**
We have used normalization method in computing the cases per million for each in the world.Normalization is the process of reorganizing data in a database so our data is stored in only one place and we extract the data from the location, and data dependencies are logical.

To calculate cases per million, we need population data so we will be using the data from [United Nations Population Dynamics page](https://population.un.org/wpp/Download/Standard/CSV/)  and calculate cases per million.

**Model**
We are building linear regression model to predict the  exponential increases in the coronavirus cases.We are building this model to satisfy the 
equation y = e^{mx}, we will taking log values of this equation and predicting the exponential curve. In this way we can find predict those countries that have find their way to control the number of cases in their region.
**Conclusion**
So by using various method we have plot the data of different countries and analyze their situation in this pandemic, we are successfull in predicting the future number of cases by using linear regression model and can use this analysis to warn the country about the future increase in the number of cases.

##Predicting the Genre of Books from Summaries
=========================================================================
**Introduction**
This portfolio is all about predicting the genre tag of book by building a model that will depict the genre tags from summary.so, we will develops an approach to understanding multi-label classification in NLP.
Our goal in this portfolio is to take this data and build a predictive model to classify the books into one of the five target genres.  We will extract suitable features from the summary and build a suitable model to predict the genre the of the book.

**Getting data**
We'll use a set of book summaries from the [CMU Book Summaries Corpus](http://www.cs.cmu.edu/~dbamman/booksummaries.html) in this experiment.   Each book can have more than one genre and there are 227 genres listed in total.To simplify the problem of genre prediction we will select a small number of target genres that occur frequently in the collection and select the books with these genre labels. This will give us one genre label per book. 
**Exploring the data**
Our first task is to read the data. It is available in tab-separated format with no column headings.We will use read_csv to read the data and used '\t' (tab) separator to and supply the column names.The field names we get from the ReadMe file.
**Model**
We are building multilabel classification model to predict the genre tags from the summary field.Our First task is to clean the data and the target features by removing numerical characters and special characters from the list.After cleaning the summary data, we will remove stopwords from the summary columns and store the clean the data in a column of the genre_book dataframe.
**LabelBinarizer**
We will start building our model by converting the genre into the features.Since we have single column data so we will use LabelBinarizer that will convert the summary genre into the features.LabelBinarizer makes our process easy by using the transform method.
**tfidfVectorizer**
After that we will use TfidfVectorizer that computes the word counts, IDF values, and Tf-idf scores all in one step in the  same dataset.
**Conclusion**
So, we have created a model that will predict book genre from the summary feature, we have also compute accuracy score of the dataset to find out the accuracy of the model, our model can predict 52% of the genre tag on train dataset and 40% of the genre tag on test dataset.

    





