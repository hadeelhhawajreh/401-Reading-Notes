#### Machine Learning Tasks
Academic machine learning starts with and focuses on individual algorithms. However, in applied machine learning, you should first pick the right machine learning task for the job.

A task is a specific objective for your algorithms.
Algorithms can be swapped in and out, as long as you pick the right task.
In fact, you should always try multiple algorithms because you most likely won't know which one will perform best for your dataset.
The two most common categories of tasks are supervised learning and unsupervised learning. (There are other tasks as well, but the concepts you'll learn in this course will be widely applicable.)

**Supervised Learning
Supervised learning includes tasks for "labeled" data (i.e. you have a target variable).**

In practice, it's often used as an advanced form of predictive modeling.
Each observation must be labeled with a "correct answer."
Only then can you build a predictive model because you must tell the algorithm what's "correct" while training it (hence, "supervising" it).
Regression is the task for modeling continuous target variables.
Classification is the task for modeling categorical (a.k.a. "class") target variables.
![i](https://elitedatascience.com/wp-content/uploads/2017/05/weaker-penalty-noisy-conditional.png)

**Unsupervised Learning
Unsupervised learning includes tasks for "unlabeled" data (i.e. you do not have a target variable).**

In practice, it's often used either as a form of automated data analysis or automated signal extraction.
Unlabeled data has no predetermined "correct answer."
You'll allow the algorithm to directly learn patterns from the data (without "supervision").
Clustering is the most common unsupervised learning task, and it's for finding groups within your data.

![i](https://elitedatascience.com/wp-content/uploads/2017/03/mlmc-cluster-analysis.png)


The Blueprint
Our machine learning blueprint is designed around those 3 elements.

There are 5 core steps:
1
Exploratory Analysis

First, "get to know" the data. This step should be quick, efficient, and decisive.

2
Data Cleaning

Then, clean your data to avoid many common pitfalls. Better data beats fancier algorithms.

3
Feature Engineering

Next, help your algorithms "focus" on what's important by creating new features.

4
Algorithm Selection

Choose the best, most appropriate algorithms without wasting your time.

5
Model Training

Finally, train your models. This step is pretty formulaic once you've done the first 4.

Of course, there are other situational steps as well:
S
Project Scoping

Sometimes, you'll need to roadmap the project and anticipate data needs.

W
Data Wrangling

You may also need to restructure your dataset into a format that algorithms can handle.

P
Preprocessing

Often, transforming your features first can further improve performance.

E
Ensembling

You can squeeze out even more performance by combining multiple models.

