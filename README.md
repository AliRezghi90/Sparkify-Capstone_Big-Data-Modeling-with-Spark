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
- [Methodology](#methodology)
- [Results](#results)
- [Blogpot](#blogpost)
- [Installation - Packages](#installation)
- [File Descriptions](#files)
- [Licensing, Authors, and Acknowledgements](#licensing)


## Introduction <a name="introduction"></a>
This is the Capstone Project for the Data Scientist Nanodegree by Udacity. In this project, the interactions that users have with an imaginary music streaming app named *Sparkify* are analyzed. Sparkify database is potentially similar to the popular streaming service [Spotify](https://open.spotify.com/). Different Machine Learning (ML) models of [PySpark's Machine Learning Library](https://spark.apache.org/mllib/) are used to predict customer churn.

## Motivation <a name="motivation"></a>
Customer churn entails the termination of a service by a customer. Businesses aim to proactively identify potential users who may leave their service before they actually do so. Therefore, predicting customer churn in advance can help the company to provide enticing offers to unsatisfied customers to convince them to stay active. 
Sparkify users can have different interactions with the app, including but not limited to, playing songs, liking or disliking a song, adding songs to playlists, adding friends, upgrading to Premium with a monthly rate, downgrading to free mode, watching advertisements, and canceling the service. All of this information is stored in Sparkify's data set with timestamps of each interaction. The complete dataset has a size of 12 GB, while a mini-dataset is also available with a size of 128 MB. The large data set (12 GB) is a big data modeling problem, which is highly demanded. The mini-dataset is used here for modeling and the large dataset will be analyzed for future work. 


## Methodology <a name="methodology"></a>
The churn prediction is created by implementing the following steps:
###### I. Exploratory Data Analysis
The mini-dataset is first explored to find some insights about the data. The behaviors of churned and active users are compared in detail. Next, the data sets are cleansed and prepared for classification models.

###### II. Feature Engineering
Based on the insights gained from the previous step, suitable features are chosen. Non-binary features are scaled and vectorized with binary features. A complete list of these features can be found in the Notebook. The final dataset has 53 features and a target (label) column.

###### III. Modeling
First, the dataset is split to train and test datasets. Pipelines with scaled vectors of features are created using [VectorAssembler](https://spark.apache.org/docs/3.1.3/api/python/reference/api/pyspark.ml.feature.VectorAssembler.html) and [StandardScaler](https://spark.apache.org/docs/latest/api/python/reference/api/pyspark.ml.feature.StandardScaler.html) tools. Cross-validation is performed for several methods of Logistic Regression, Random Forest, Gradient Boosted Trees, and Linear SVC. The metrics of the best models from each method is found and the final model is chosen based on the F1-score (higher the better) and calculation time (lower the better). Finally, the perfomance of the best model is evaluated on the test dataset.

## Results <a name="results"></a>

From the cross-validation on the training dataset, the following scores and calculation time is obtained for the best model of each ML method. It is clear that Random Forest can provide the F1-score of 1.0 with the lowest calculation time. 
| Model                  | F1-score | Calculation Time (second) |
| ------------------     | -------- | ----------------          |
| LogisticRegression     | 0.806   | 362.14                     |
| Random Forest          | 0.814   | 332.99                     |
| Gradient Boosted Trees | 0.790   | 1815.89                    |
| LinearSVC              | 0.783   | 564.89                     |


## Blogpot <a name="blogpost"></a>

Further information and results about this project can be found in [this article](https://medium.com/@a.rezghi90/58f4af05946a) on the medium platform.


## Installation - Packages <a name="installation"></a>
Use pip to install The following packages:
* Pandas
* Numpy
* Matplotlib
* Jupyter
* Pysaprk
* folium
* device-detector
* geopy
* Seaborn

The program was appropriately run using Python 3.11., however, older versions might work as well.


## File Descriptions - Packages <a name="files"></a>
Sparkify.ipynb : Jupyrt notebook of the project

mini_sparkigy_event_data.josn: JSOn file containing the data

SparkifyLogo: Logo (jpg file)


## Licensing, Authors, and Acknowledgements <a name="licensing"></a>
Credit must be given to [Udacity](https://www.udacity.com/) for the excellent Udacity Data Scientist Nanodegree program and for the provided dataset. 


