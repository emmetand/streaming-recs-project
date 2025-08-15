# streaming-recs-project
Streaming Content Recommendation Engine (Python)

This project is a filtering movie recommendation program using the MovieLens 32M dataset. 

OVERVIEW
Goal of the project is to:
-Load and explore a large movie rating data set. 
-Create a user/item rating matrix 
-Find item to item similarity
-Generate persoinalized recommendations for a given user
-Evaluate the recommendation results.

DATASET
Source: MovieLens32M
Files Used:
-ratings.csv for user ratings of movies
-movies.csv for movie titles and genres

This data set for filtered to include the 500 most active users and 500 most popular movies.
(In a true moment of learning in a project I created oversized matrices a few times before realizing I needed these caps).

INSTALLATION & SETUP
git clone https://github.com/emmetand/streaming-recs-project.git
cd streaming-recs-project

place ratings.csv and movies.csv into: data/ml32/

STRUCTURE

streaming-recs-project/
│
├── data/                  # Dataset storage (not in repo)
│   └── ml32/
│       ├── ratings.csv
│       └── movies.csv
│
├── notebooks/             # Jupyter notebooks
│   └── 01_eda.ipynb       # Main analysis & recommendation code
│
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation


WORKFLOW