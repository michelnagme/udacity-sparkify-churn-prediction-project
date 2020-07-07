# Predicting churn with PySpark

## Table of Contents

1. [Motivation](#motivation)
2. [File descriptions](#filesdescriptions)
3. [Libraries](#libraries)
4. [Results](#results)
5. [Licensing](#licensing)
6. [Resources](#resources)

## Motivation <a name="motivation"></a>

Customer churn is when an existing customer, user, subscriber or any kind of return client stops doing business or ends the relationship with a company or service. Not surprisingly, Churn Rate is one of the most important KPIs for many services and is a good measurement of business' health. Predicting churn is a fundamental task to help Customer Success teams take action and avoid loss of customers and revenue.

## Files descriptions <a name="filesdescriptions"></a>

* `Sparkify.ipynb` is a jupyter notebook with the analysis and results for this project.
* `Sparkify.html` is a HTML version of the above notebook.

## Libraries <a name="libraries"></a>

* Spark 3.0.0
* PySpark 3.0.0
* Pandas 1.0.5
* NumPy 1.18.5
* Matplotlib 3.0.3
* Seaborn 0.10.1
* HTTPAgentParser 1.9.0
* FindSpark 1.4.2

## Results <a name="results"></a>

Our task was to build a binary classifier, using Machine Learning techniques and the Spark engine through PySpark library, that was able to efficiently predict from user's access logs which customers were about to cancel their subscriptions of a music streaming service, going through the whole process of building a machine learning algorithm (data exploration and analysis using helpful visualizations, feature engineering, model engineering and finally evaluation). The dataset used for this project was a 128MB subset of a larger dataset (with more than 12GB) that could only be processed using Big Data tools like Spark. All steps here could be easily applied to the full dataset using a real Spark cluster deployed in a cloud service.

The most challenging part of this project was certainly the generation of new features through creative engineering of the original input. As the initial data set consisted of activity logs and not user information itself, several transformations needed to be made. In addition, to ensure that our model was not influenced by implicit information, such as customer lifetime, which would not be available in production and also so that it could be applied over a configurable observation window, we needed to make sure that the features were time-independent. The solution was to create features based on usage frequencies and trends.

Some further steps could be taken to improve our results, like: perform further investigation on how sessions are structured and how they could be used to generate new features like session time length, songs per session, etc; use songs and artists' names to generate some insight about users' musical preferences and how this could affect churn rate; and, mainly, train and test the shortlisted models on the full 12GB dataset.

After all, the model we've built could be successfully used to identify in advance users with a high churn risk and thus allow the music streaming company to take appropriate measures to reverse the situation, keep customers and also the business' health.

## Licensing <a name="licensing"></a>

This repository is licensed under the MIT License.

## External Resources <a name="resources"></a>

1. [Guide to install Spark and use PySpark from Jupyter in Windows](https://bigdata-madesimple.com/guide-to-install-spark-and-use-pyspark-from-jupyter-in-windows/)
2. [Apache Spark 3.0.0 Machine Learning Library (MLlib) Guide](https://spark.apache.org/docs/latest/ml-guide.html)
3. [Httpagentparser by shon](http://shon.github.io/httpagentparser/)
