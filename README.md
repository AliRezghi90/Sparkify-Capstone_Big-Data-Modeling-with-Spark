<p align="center">
  <a href="https://www.udacity.com/">
    <img src='https://course_report_production.s3.amazonaws.com/rich/rich_files/rich_files/5511/s300/udacity-logo.png' alt="Udacity logo" height = 200px>
   </a>


  <a href="https://www.udacity.com/">
    <img src='https://github.com/AliRezghi90/Sparkify-Capstone_Big-Data-Modeling-with-Spark/blob/13975ca5ef5c3a1ca303608875b8e168b3aaf568/SpakifyLogo.jpg' alt="Spakify logo" height = 200px>
   </a>

</p>
<h3 align="center"><a href='https://www.udacity.com/course/data-scientist-nanodegree--nd025'>Udacity Data Scientist Nanodegree Program</a></h3>
<h1 align="center"> Capstone Project: Churn Prediction Using PySpark (Sparkify Big data) </h1>

The project files can be found [here](https://github.com/AliRezghi90/Sparkify-Capstone_Big-Data-Modeling-with-Spark.git) 

## Table of Contents
- [Introduction](#introduction)
- [Motivation](#motivation)
- [Summary - Methodology](#summary)
- [Results](#results)
- [Installation - Packages](#installation)
- [File Descriptions](#files)
- [Licensing, Authors, and Acknowledgements](#licensing)


## Introduction <a name="introduction"></a>
This is the Capstone Project for the Data Scientist Nanodegree by Udacity. In this project, the interactions that users have with an imaginary music streaming app named *Sparkify* are analyzed. Sparkify database can be similar to the popular streaming service [Spotify](https://open.spotify.com/). Different Machine Learning models are used to predict customer churn.

## Motivation <a name="motivation"></a>
Customer churn entails the termination of a service by a customer. Businesses aim to proactively identify potential users who may leave their service before they actually do so. Therefore, predicting customer churn in advance can help the company to provide enticing offers to unsatisfied customers to convince them to stay active. 
Sparkify users can have different interactions with the app, including but not limited to, playing songs, like or dislike a song, add songs to playlists, add friends, upgrade to Premium with a monthly rate, downgrade to free mode, watch advertisements, and cancel the service. All of this information is stored in the Sparkify's data-set with timestamps of each interaction. The complete dataset has a size of 12 GB, while a mini-dataset is also available with size of 128 MB. The large data set (12 GB) is a big data modeling problem, which is highly demanded. The mini-dataset is used here for modeling and the large dataset will be analyzed in the future. 


## Summary - Methodology <a name="summary"></a>
The recommendation engine is created by implementing the following steps:
###### I. Exploratory Data Analysis
The data sets for articles cimmunity and user-item interactions are first explored to find some insights about the data. Next, the data sets are cleansed and prepared for recommendation models.

###### II. Rank Based Recommendations
Articels with most interactions are chosen as the most popular articles. The popular articles are especially used for new users as they do not present any interaction with the article community.

###### III. User-User Based Collaborative Filtering
To recommend article to users similar to other users, the user-user based collaborative filtering is an appropriate approach. A user-item matrix is created, which is used to find the users with highest similarities and the coreesponding articles. 

###### IV. Matrix Factorization
The Singular Value Decomposition (SVD) method is a well-known machine learning approach to build recommendation engines. Using the SVD, we will get an idea of how well we can predict new articles an individual might interact with. Since the user-item matrix does not have any NaN, there is no need to perform Funk SVD. 


