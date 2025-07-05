# 📚 Book Recommendation System using KNN

This project builds a simple yet effective **book recommendation system** using the **K-Nearest Neighbors (KNN)** algorithm. It uses collaborative filtering on user ratings to suggest similar books.

---

## 📌 Overview

- **Algorithm**: K-Nearest Neighbors (KNN)
- **Approach**: Item-based collaborative filtering
- **Dataset**: Book-Crossing dataset from [Kaggle](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset)
- **Libraries**: `pandas`, `scikit-learn`, `scipy`

---

## 📁 Dataset Description

The dataset contains three CSV files:

- `Books.csv`: Book details like title, author, and publisher.
- `Users.csv`: User demographic data.
- `Ratings.csv`: User ratings of books (0–10 scale).

After cleaning:
- Removed implicit ratings (`Book-Rating` = 0)
- Filtered to keep popular books and active users (≥ 10 ratings)

---

## 🧠 How It Works

1. **Preprocessing**:
   - Clean CSVs
   - Strip column names and drop irrelevant data
   - Merge `ratings` with `books`

2. **Filtering**:
   - Keep only books/users with ≥ 10 ratings to reduce sparsity

3. **User-Book Matrix**:
   - Built a matrix where rows = books, columns = users, values = ratings

4. **KNN Model**:
   - Used cosine similarity with `NearestNeighbors` from `scikit-learn`
   - Recommend books by finding similar ones based on user rating patterns

---

