# 🎬 Movie Recommendation System — Collaborative Filtering

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![ML](https://img.shields.io/badge/ML-Collaborative%20Filtering-blueviolet?style=flat-square)
![Dataset](https://img.shields.io/badge/Dataset-MovieLens%20100K-yellow?style=flat-square)

> Personalized movie recommendation engine built using User-User Collaborative Filtering and Cosine Similarity on the MovieLens 100K dataset.

---

## 📌 Problem Statement
With thousands of movies available, users struggle to find content they'll enjoy. This project solves the cold-start discovery problem by recommending movies based on the viewing history of similar users.

## 🎯 Key Features
| Feature | Detail |
|---------|--------|
| Algorithm | User-User Collaborative Filtering |
| Similarity Metric | Pairwise Cosine Distance |
| Dataset | MovieLens 100K |
| Output | Top-N personalized movie recommendations |

## 🛠️ Tech Stack
- **Language:** Python
- **ML:** Scikit-learn, Surprise
- **Data Processing:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Environment:** Jupyter Notebook

## 📂 Project Structure
```
movie-recommendation-collaborative-filtering/
├── Movie_recomendation_project/
│   ├── data/      # MovieLens dataset
│   ├── python/    # Notebooks & scripts
│   └── README.md
└── README.md
```

## 🚀 How to Run
```bash
# 1. Clone the repo
git clone https://github.com/shreesneha056-gif/movie-recommendation-collaborative-filtering.git
cd movie-recommendation-collaborative-filtering

# 2. Install dependencies
pip install pandas numpy scikit-learn scikit-surprise matplotlib seaborn jupyter

# 3. Launch Jupyter
jupyter notebook
```

## 📊 Pipeline Overview
1. **Data Loading** — Load MovieLens 100K ratings data
2. **User-Item Matrix** — Build user × movie rating matrix
3. **Similarity Computation** — Calculate cosine similarity between users
4. **Neighbor Selection** — Find K nearest similar users
5. **Recommendation** — Suggest unseen movies liked by similar users

---
📫 [Connect on LinkedIn](https://www.linkedin.com/in/sneha-shree-mu/) | [Portfolio](https://shreesneha056-gif.github.io/portfolio_website/)
