# Movie Recommendation Engine

A simple example version of a movie recommender engine built in Python using the [MovieLens dataset](https://grouplens.org/datasets/movielens/).  

This project demonstrates how to build a **content-based movie recommender** from scratch using **pandas, cosine similarity, and basic validation checks**. The goal is to explore and begin building useful applications at the intersection of data analytics and entertainment — a strong foundation for media/tech/consulting applications.

---

## Project Overview
- **Dataset:** ~650K ratings from the MovieLens dataset (cleaned from the 32M set)  
- **Goal:** Recommend movies to users based on their past ratings. Then build a real time recommender to ask the current user about their preferences.  
- **Approach:**  
  1. Merge user ratings and movie data into a single dataframe.  
  2. Create a user/movie matrix (users as rows, movies as columns).  
  3. Compute cosine similarity between movies.  
  4. Generate recommendations based on movies a user has already rated.  
  5. Validate results with simple checks (sparsity, popularity, neighbors).  

---

## Tech Stack & Setup
- **Python** (pandas, numpy)  
- **scikit-learn** (cosine similarity)  
- **matplotlib** (visualization)  

### Create & activate a virtual environment (macOS/Linux)
python3 -m venv .venv
source .venv/bin/activate

### or Windows PowerShell
python -m venv .venv
.venv\Scripts\Activate.ps1

### Install packages
pip install -r requirements.txt

### Launch Jupyter
jupyter notebook

---

## Key Features
- **User–Movie Matrix Construction**  
  Put ratings into a sparse matrix, sort for the most full section of data, and then handle missing values.

- **Cosine Similarity Engine**  
  Measure similarity between movies based on user rating patterns. See which movies that are rated high are correlated with each other. 

- **Recommendation Function**  
  Suggests new titles by using similarity scores from the broader data to make recommendations to single users. 

- **Simple Evaluation Checks**  
  - Ratings shape & sparsity check  
  - See Top 10 most rated movies  
  - Nearest neighbors for a chosen (ideally esoteric) title  

---

## Example Outputs

### Top 10 Most Rated Movies
| Title                                                     | Similarity |
|-----------------------------------------------------------|------------|
| Shawshank Redemption, The (1994)                          | 102929     |
| Forrest Gump (1994)                                       | 100296     |
| Pulp Fiction (1994)                                       | 98409      |
| Matrix, The (1999)                                        | 93808      |
| Silence of the Lambs, The (1991)                          | 90330      |
| Star Wars: Episode IV - A New Hope (1977)                 | 85010      |
| Fight Club (1999)                                         | 77332      |
| Jurassic Park (1993)                                      | 75233      |
| Schindler's List (1993)                                   | 73849      |
| Lord of the Rings: The Fellowship of the Ring, The (2001) | 73122      |


### Nearest Neighbors of *Toy Story (1995)*
| Title                  | Similarity |
|-------------------------|------------|
| A Bug's Life (1998)     | 0.91       |
| Monsters, Inc. (2001)   | 0.88       |
| Finding Nemo (2003)     | 0.85       |

---

## Business Relevance
Streaming and media companies leverage more advanced types of these recommenders to:
- **Improve content discovery** (personalized “Because you viewed…” suggestions)  
- **Guide marketing campaigns** (bundle popular titles with related niche content)  
- **Optimize catalog strategy** (identify clusters of substitutable movies)  

Even this simple cosine similarity model shows how analytics can provide immediate, actionable insights without requiring deep learning or large infrastructure.

---

## Project Structure



    project-root/
    │── data/                  # MovieLens dataset (ratings.csv, movies.csv)
    │── notebooks/             
    │   └── 01_eda.ipynb       # Main Jupyter Notebook (exploration & modeling)
    │── README.md              # Project documentation (this file)
    │── requirements.txt       # Python dependencies


---

## Wrap Up
As a creative development professional pivoting into analytics, I built this project to connect interest and domain experience in entertainment with data science tools. By creating a simple recommender, I'm exploring how analytics can support content strategy, personalization, and audience engagement; key areas for media and technology companies.

---

## Next Steps
Potential future improvements:
- Create a program for users to ask for recommendations based on a specific movie
- Create profiles or Id numbers so users can update their ratings as they watch, and get more recs.
- Incorporate genres / metadata into recommendations.  


---

## Contact
Created by **Emmet Andrews** | UCLA MSBA (2026)  
📩 [LinkedIn](https://www.linkedin.com/in/emmet-andrews/) | [GitHub](https://github.com/emmetand)




Data License: This project uses the public MovieLens dataset by GroupLens. Please see their site for license and citation instructions. Data is downloaded by users at runtime; it is not redistributed in this repository.
