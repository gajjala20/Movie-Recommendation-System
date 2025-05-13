# Movie-Recommendation-System(INTERNSHIP PROJECT)
📌 Project Objective
The objective of this project is to build a movie recommendation system that suggests movies to users based on their interests. The system utilizes two primary techniques:

Content-Based Filtering – recommends movies based on their genre similarity.

Collaborative Filtering – recommends movies based on user preferences and patterns using the SVD algorithm.

📚 Dataset Used
We use the MovieLens 100k dataset which contains:

movies.csv – Movie metadata like movieId, title, and genres.

ratings.csv – User rating data including userId, movieId, rating, and timestamp.

You can download the dataset here: https://grouplens.org/datasets/movielens/100k/

🧠 Recommendation Techniques
1. 🎯 Content-Based Filtering
Approach:

Each movie has associated genres like "Action", "Comedy", etc.

Using TF-IDF vectorization, genres are converted into numerical features.

Cosine similarity is used to compute similarity between movies.

Steps:

Preprocess genres (convert "Action|Adventure" to "Action Adventure").

Convert genre text into vectors using TfidfVectorizer.

Compute pairwise similarity (cosine similarity) between movies.

Recommend top N similar movies based on similarity scores.

Example:

Input: 'Toy Story (1995)'
Output: List of similar movies like 'A Bug's Life (1998)', 'Shrek (2001)' etc., based on genre similarity.

2. 🤝 Collaborative Filtering (Matrix Factorization using SVD)
Approach:

Based on user-item interactions (ratings).

Uses Surprise library and Singular Value Decomposition (SVD) for matrix factorization.

Learns latent factors for users and movies.

Steps:

Load rating data into Surprise using Reader.

Split data into training and test sets.

Train an SVD model on the training set.

Predict ratings on the test set and compute RMSE (Root Mean Squared Error).

Generate Top-N recommendations for each user.

Example:

Input: User ID = 1
Output: Top 5 movies predicted to be liked by the user based on other similar users' preferences.

🧪 Evaluation
Metric Used:

RMSE (Root Mean Squared Error) on the test set to evaluate the collaborative filtering model's accuracy.

🛠️ Technologies & Libraries
Tool	Purpose
Python	Core programming language
pandas	Data manipulation
scikit-learn	TF-IDF, cosine similarity
Surprise	Collaborative filtering (SVD)
Jupyter/Colab	Interactive environment (optional)

🔍 Key Features
Dual recommendation logic: Content-based + Collaborative.

Easy-to-use functions for getting recommendations.

Scalable to larger datasets or hybrid systems.

🧠 Possible Enhancements
✅ Add a GUI using Tkinter or Streamlit.

✅ Create a web app using Flask/Django.

✅ Implement hybrid filtering (combine both systems).

✅ Add more features like tags, directors, etc.

✅ Deploy to cloud (e.g., Render, Heroku).

📝 Conclusion
This project demonstrates how to build a basic movie recommender system using two popular techniques:

Content-Based Filtering (based on genres)

Collaborative Filtering (based on user ratings)

It’s a strong foundation for any internship or academic project, showcasing both data processing and machine learning concepts in a practical setting.


