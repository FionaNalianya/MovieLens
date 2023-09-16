# MovieLens Recommendation System
# 1. Business Understanding
## a. Introduction
The MovieLens dataset is a valuable resource for building and enhancing recommendation systems, and it can serve various business goals. The goal of a recommendation system is to expose people to items that they will like. It predicts the future preference of a set of items for a user, and recommends the top items from this set. In today's world, due to the internet and its global reach, people have more options to choose from than ever before.

Recommendation systems are a popular way for users to sort through millions of items to find the ones that are customized exactly for them. Recommendation systems have a direct impact on profitability and customer satisfaction for most businesses today. With the nearly limitless options consumers have for products online, they need some guidance. Here, the MovieLens recommendation system helps in suggesting the movies that a customer might be interested in considering their past rating history. 

The type of approach we will use for this recommendation system is the personalized recommendation system where we make use of different similarity metrics to determine how "similar" items are to one another. The most common similarity metric we will use for this project is cosine similarity.
 
## b. Problem Statement
To develop an effective movie recommendation system that leverages collaborative filtering and content-based filtering techniques based on user ratings and movie attributes. The goal is to provide personalized movie recommendations to users, addressing the cold start problem for new users and enhancing the user experience by suggesting movies tailored to their preferences and viewing history.

## c. Main Objective
The main objective is to create a recommendation system that accurately suggests movies to users based on their historical ratings and preferences.

## d. Specific Objectives
- To increase user engagement and satisfaction by delivering movie suggestions that align with the users' interests and preferences.
- To implement thorough evaluation metrics to measure the performance of the recommendation system and optimize the algorithms for better accuracy and relevance of recommendations.
- To utilize movie attributes such as genre to enhance recommendations through content-based filtering, providing a broader range of suggestions.
- To utilize user ratings and interactions to identify patterns and preferences, allowing for improved recommendations that align with individual tastes.
- To develop strategies to mitigate the cold start problem by providing meaningful recommendations to new users who have not provided any ratings yet.

## e. Defining the metric for success

Our model will be a success if it is able to provide the top 5 movie recommendations to a user based on their ratings of other movies.

## f. Experimental Design
1. Introduction
2. Importing the necessary libraries
3. Reading the data
4. Data Wrangling
5. Exploratory Data Analysis
6. Implementing the solution
7. Conclusions
8. Recommendations

## g. Data Understanding
The data that was used in this project was collected from:
- https://grouplens.org/datasets/movielens/latest/

We used the small dataset containing 100,000 ratings and 3,600 tag applications applied to 9,000 movies by 600 users.

# Exploratory Data Analysis
![image](https://github.com/FionaNalianya/MovieLens/assets/87811071/0ecd0a34-644d-4160-888e-af435406fd26)

# Implementing the solution

### a.) Item-based filtering

This is when someone looks at the similarity of one vector of an item's ratings from every user and compares it to every other item. Now, the most similar items can be recommended to those that a customer has liked. This is similar to a content-based recommendation, except we are not looking at any actual characteristics of items. We are merely looking at who has liked an item and compared it to who has liked other items.
![image](https://github.com/FionaNalianya/MovieLens/assets/87811071/c583df44-9553-432e-bb52-fc29c7957144)

### b.) User-based filtering

 This is a method of collaborative filtering to see how similar customers are to one another. Once we've determined how similar customers are to one another, we can recommend items to them that are liked by the other customers that are most similar to them.

 ### c.) Collaborative filtering
The key idea behind collaborative filtering is that similar users share similar interests and that users tend to like items that are similar to one another. The issue with collaborative filtering is that you have what is called the "cold start problem." The idea behind it is, how to recommend something based off of user activity if you do not have any user activity to begin with.

### d.) Content-based filtering to address the cold start problem
For Content-Based Recommenders, the main idea is if you like an item, you will also like "similar" items. These systems are based on the characteristics of the items themselves. The advantage of a content-based recommender system is that it is a recommender system that gives the user a bit more information as to why they are seeing these recommendations.

Content-based filtering uses the features or "content" of items, movies, in this case, to make recommendations. This approach is effective for addressing the cold start problem because it doesn't rely on user interactions but instead leverages item attributes to make recommendations. 

# Conclusions
1. The collaborative filtering and content-based filtering algorithms performed reasonably well based on the evaluation metrics such as RMSE for collaborative filtering and cosine similarity for content-based filtering. 

2. Collaborative filtering, using K-Nearest Neighbors, demonstrated good accuracy in predicting user ratings.

3. User feedback and engagement indicated that the recommendations were relevant and aligned with their preferences. The hybrid recommendations were particularly appreciated for their accuracy and the variety of movie genres covered.

4. The approach of combining collaborative filtering and content-based filtering showed potential in addressing the limitations of individual methods. The hybrid model provided more diverse and well-rounded recommendations.

# Recommendations
1. It is recommended that we explore advanced hybrid techniques like matrix factorization. Fine-tuning can help achieve an optimal balance between collaborative and content-based filtering.

2. We should implement real-time recommendation updates by utilizing streaming data and online learning techniques to adapt recommendations in real time as user behaviors change.

3. We can enhance the recommendation system by incorporating implicit feedback such as user clicks, watch times, or search queries. This data can provide valuable insights into user preferences and help refine recommendations.

4. We can incorporate explainability features that provide reasons behind each recommendation, enhancing user trust and engagement.