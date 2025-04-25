# Movie Recommender System

This repository implements a complete pipeline for building, analyzing, and evaluating a movie recommendation system using the MovieLens dataset and enriched metadata.

## 📁 Project Structure

- **data/**
  - `movies_metadata.csv` &nbsp;&nbsp; Preprocessed movie metadata (title, genres, director, actors, language, country, year)  
  - `users.csv` &nbsp;&nbsp; User demographics (gender, age, occupation, zip code)  
  - `train.txt` &nbsp;&nbsp; User–item interactions for training  
  - `test.txt` &nbsp;&nbsp; User–item interactions for testing  
- **scripts/**
  - `01_preprocess_data.ipynb` &nbsp;&nbsp; Load raw data, split train/test, fetch metadata  
  - `02_eda.ipynb` &nbsp;&nbsp; Exploratory data analysis and visualizations  
  - `03_models.ipynb` &nbsp;&nbsp; Feature engineering, model training & evaluation  
- `.gitignore` &nbsp;&nbsp; Specifies files/folders to ignore in Git  
- `requirements.txt` &nbsp;&nbsp; Python package dependencies  
- `README.md` &nbsp;&nbsp; This file  

## ⚙️ Prerequisites

- Python 3.7 or higher  
- (Recommended) Use a virtual environment  

Install dependencies:
```bash
pip install -r requirements.txt
```

## 🚀 Notebooks Workflow

### 01_preprocess_data.ipynb
- **Load** MovieLens interactions via KaggleHub  
- **Remove** cold-start users and items  
- **Split** interactions into `train.txt` and `test.txt`  
- **Query** additional movie metadata (director, actor, country, language) via DBpedia SPARQL  
- **Save** processed metadata and interaction files under `data/`  

### 02_eda.ipynb
- **Analyze** rating distribution and sparsity  
- **Visualize** top genres, languages, actors, and directors  
- **Examine** user demographics (gender, age distribution)  

### 03_models.ipynb
- **Encode** user and item IDs for modeling  
- **Build** content-based and collaborative filtering features  
- **Define** evaluation metrics (Precision@K, Recall@K, NDCG)  
- **Train & Compare** multiple recommenders:  
  - Popularity baseline  
  - User-based CF  
  - Item-based CF  
  - Implicit ALS  
  - LightFM hybrid model  

## 📚 References

- [MovieLens dataset](https://www.kaggle.com/datasets/odedgolden/movielens-1m-dataset/data)
- [MappingMovielens2DBpedi](https://github.com/sisinflab/LODrecsys-datasets)
- [DBpedia SPARQL endpoint](http://dbpedia.org/sparql)  
- [LightFM library](https://github.com/lyst/lightfm)  
- [Implicit library for ALS](https://github.com/benfred/implicit)  


