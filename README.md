# 🎬 Machine-Learning-Project-Movie_Recommendation_System

http://localhost:8501/

**📌 Project Overview :**

This project is a content-based movie recommendation system built using machine learning techniques. It recommends similar movies to a user-selected title based on textual features such as genres, keywords, cast, and crew.

Two datasets were used:

**Movies Dataset** – contains metadata such as genres, overview, etc.

**Credits Dataset** – includes cast and crew details.

**🔧 Tools & Libraries Used :**

Python

Pandas – data manipulation

NumPy – numerical operations

scikit-learn – machine learning (CountVectorizer, cosine similarity)

Jupyter Notebook

**🔄 Workflow Summary :**

🧹 1.**Data Preprocessing**

Merged movies.csv and credits.csv on the appropriate key.

Removed duplicates and handled missing values.

Selected and combined key textual features: genres, keywords, cast, crew, and overview.

Processed text by lowering case, removing spaces and special characters, and standardizing formatting.

**🧠 2. Feature Engineering**

Created a new column named tags by combining all the important text features.

Used **CountVectorizer** to convert text into a matrix of token counts (bag-of-words model).

Reduced dimensionality by limiting the number of features (max_features=5000) and removing English stopwords.

**📈 3. Similarity Calculation**

Applied **cosine similarity** to compute the similarity score between movies based on the tags.

Built a recommendation function that:

Takes a movie name as input.

Finds the most similar movies using cosine similarity.

Returns the top 5 or 10 recommendations.

💡 **Key Insights :**

Combining multiple metadata fields into a single bag-of-words helps improve the relevance of recommendations.

Cosine similarity is a simple but powerful method for content-based filtering.

This model doesn't require user history or ratings – it purely relies on content, making it ideal for cold-start scenarios.

The model is scalable and can easily be extended to include more complex NLP techniques like TF-IDF, stemming, or even deep learning approaches.

