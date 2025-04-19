# 🎬 Movie Knowledge Graph Recommender

This project builds a knowledge graph-based recommender system by enriching the [MovieLens 1M Dataset](https://grouplens.org/datasets/movielens/) with external metadata from [DBpedia](https://dbpedia.org/). The system learns from user–item interactions, movie genres, and DBpedia attributes like directors, actors, country, and language to generate more personalized recommendations.

---

## 📌 Project Highlights

- ✅ Mapped MovieLens movies to DBpedia URIs
- ✅ Queried DBpedia to extract rich metadata (director, actor, country, language)
- ✅ Constructed a knowledge graph with users, movies, and entities
- ✅ Exported KG as triplets for graph-based recommender models (e.g., KGAT, KGCN)
- ✅ Compatible with libraries like RecBole, PyTorch Geometric, or Neo4j

---

## 🗂️ Dataset Used

- `movies.dat`, `ratings.dat`, `users.dat` from **MovieLens 1M**
- `MappingMovielens2DBpedia.tsv` from [LODRecSys GitHub Repo](https://github.com/sisinflab/LODrecsys-datasets)
- DBpedia SPARQL endpoint for metadata enrichment

---



