### Next purchase pridiction

This is a competition notebook for [SberMarket Inclass challenge](https://www.kaggle.com/c/sbermarket-internship-competition).

The dataset is the purchase history of twenty thousand customers for a couple of years. The data contains statistics for each purchase (without specifying the quantity of purchased goods), there are only the list of purchased categories (a total of 881 categories).

The challenge is to predict the next order, **regardless of the time of the next order** and regardless of the number of purchased items of each category.<br>

In the basic ranking tutorial, we trained a model that can predict ratings for user/categories pairs. The model was trained to minimize the mean squared error of predicted ratings.

We do not need ranking models to predict scores with great accuracy. Instead, we care more about the ability of the model to generate an ordered list of items that matches the user's preference ordering.

Instead of optimizing the model's predictions on individual query/item pairs, we can optimize the model's ranking of a list as a whole. This method is called listwise ranking.

In this tutorial, we will use TensorFlow Recommenders to build listwise ranking models. To do so, we will make use of ranking losses and metrics provided by TensorFlow Ranking, a TensorFlow package that focuses on learning to rank.
