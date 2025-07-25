# movie-recommender
Rule-based movie recommendation system

Title: Rule-Based Movie Recommendation System

Objective:
To build a simple movie recommendation system that suggests top-rated movies based on user-selected genres using logic-based filtering, without machine learning.

Tech Stack:

Component
Tool / Library
Language
Python
Libraries
pandas, json
Dataset Source
Kaggle (MovieLens)
Execution Env
Google Colab / Jupyter Notebook
Version Control
Git + GitHub


Architecture

Workflow Diagram:-

[User Input: Genres] 
        ↓
[Filter Movies with Matching Genres] 
        ↓
[Group by Movie Title → Average Rating] 
        ↓
[Sort by Rating Descending] 
        ↓
[Return Top 5 Recommendations]




Data Flow:-
Load & Clean Data


Merge Movies and Ratings


Parse and Explode Genres


User selects genre(s)


Filter, group & 
recommend


Key Features & Modules:-



Genre-based filtering
Users choose one or more genres as input


📊 Rating aggregation
Calculates average ratings from ratings.csv


🧠 No ML required
Uses only logic and pandas operations


📄 CSV Parsing
Handles JSON-like genre strings in metadata


🔁 Exploded Genres
Allows filtering by each genre individually


🧼 Cleaned Data
Handles invalid or missing IDs in metadata


📋 Console Interface
Simple CLI input and output (interactive)


Challenges Faced
Parsing Genre JSON Strings
 The genres column in movies_metadata.csv is stored as strings that look like JSON. Handling this with proper parsing was tricky.


Invalid or Missing Movie IDs
 Some id fields in movies_metadata.csv were not numeric. This was resolved using pd.to_numeric(..., errors='coerce') and dropping NaN.


Mismatch Between Datasets
 Matching movieId from ratings and id from movies required careful conversion to integers and type consistency.

Screenshots of the working project:-




Learnings
Gained hands-on experience with:


Merging datasets using keys (merge())


Cleaning and transforming messy data


Filtering DataFrames using isin() and explode()


Grouping and sorting for recommendation logic


Understood how to structure rule-based recommender systems before diving into ML-based ones.


Improved modular thinking by separating logic into reusable functions.

Benefits of the Rule-Based Movie Recommendation System:- 
1. Simple and Lightweight 
2. User-Friendly 
3. Fast and Responsive 
4. Educational Value 
5. Customizable 
6. No Cold Start Problem 
7. No User Data Required 
8. Modular Design

