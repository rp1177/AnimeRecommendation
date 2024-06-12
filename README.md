# Anime Recommendation - MyAniMate (Notebook version)

### Introduction
This project is a weighted hybrid Anime Recommendation System. The goal is to provide users with anime recommendations based on their viewing history and preferences. A user has to input a list of anime or movies they like and the recommendation system will return the top 30 results. 

### Features
Personalized Recommendations: The system provides personalized anime recommendations based on the user’s past list of watched animes, and the corresponding scores overall that are associated with them.

Hybrid: This system uses content-based and collaborative filtering techniques (a weighted hybrid recommendation system), considering the features of animes such as genre, synopsis and tv rating, score, and number of favorites.


### Development Process:

1. Downloaded a dataset from Kaggle and loaded it into a DataFrame.
2. Initiated data cleaning and preprocessing, focusing on handling null values and ensuring data quality.
3. Used a heatmap to visualize missing values for genre and synopsis columns, and decided to ignore them to avoid introducing potential biases. (Null values for synopsis were over 10%)
4. Performed feature engineering by merging genres, synopsis, and TV ratings into a 'tags' column using NLP techniques.
5. Calculated similarity scores using TF-IDF and cosine similarity as the content-based portion and calculated the average similarity score comparison for each anime.
6. Adjusted features through trial and error to balance the number of differences and similarities.
7. Developed a popularity metric for the collaborative filtering portion, using weighted overall scores and the number of favorites for an anime.
8. Combined the popularity metric score with the similarity scores as one Dataframe normalized them, and used the weighted hybrid formula (final score = w * popularity score + w * similarity score)
9. Used Fuzzywuzzy library to implement leniency in search results within the data frame when converting input into a dictionary with keys as the anime names and their final scores. Compute the average final score, calculate the absolute difference, and find within the results list animes that the user did not watch and have the smallest absolute difference. 


### Technologies Used: 
Python (Jupyter Notebook), Matplotlib, Pandas, Scikit-Learn, and FuzzyWuzzy

### Dataset Used:
https://www.kaggle.com/datasets/dbdmobile/myanimelist-dataset/data

### Next steps:
The project is still under development. The goal is to implement an accessible and interactive website. Updates are made via CI/CD

