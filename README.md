# Anime Recommendation: MyAniMate

# Introduction/Summary:
After getting the hang of content and collaborative filtering, I thought it’d be cool to build my own anime recommendation system. Crunchyroll’s slow UI and Netflix’s limited anime options were kind of a bummer. So, I made MyAniMate to find new animes for myself. However, the system has a limitation where the dataset only expands up to 2023 user ratings and animes.

## Language used: 
Python

## Libraries used:
Fuzzywuzzy, Ipyplot, Pandas, Matplotlib, Nltk, Numpy, and Scikit-learn

## Development Process:

1.) Downloaded a dataset from Kaggle and loaded it into a DataFrame.

2.) Initiated data cleaning and preprocessing, focusing on handling null values and ensuring data quality.

3.) Used a heatmap to visualize missing values, decided to ignore them to avoid introducing biases.

4.) Performed feature engineering by merging genres, synopsis, and TV ratings into a ‘tags’ column using NLP techniques.

5.) For content-based filtering, calculated similarity scores using TF-IDF and cosine similarity.

6.) For collaborative-based filtering, developed a popularity metric column using weighted overall scores and number of favorites.

7.) Combine the average 'tags' content score with the popularity score, multiplied by the weights.

8.) Implemented a user-input interface allowing users to give an input list of favorite animes which finds the average score and frequent genre.

9.) Subtract the user's average score against the rest of the scores. The top 30 smallest differences in scores will be recommended to the user.

## Future Developments:

Currently testing different weights and use cases of the recommendation system. In addition to that, a website is still under construction.
