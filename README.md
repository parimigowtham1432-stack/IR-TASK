
# TF-IDF and Vector Space Model for News Document Retrieval

## 📌 Project Overview

This project implements a News Document Retrieval System using **TF-IDF (Term Frequency–Inverse Document Frequency)** and the **Vector Space Model (VSM)**.

It demonstrates how text documents can be converted into numerical vectors using TF-IDF and how cosine similarity can identify documents that are most relevant to a user's search query.

The project also compares Basic TF-IDF and Improved TF-IDF techniques to understand their impact on document representation and similarity scores.

## 🎯 Objectives

- Generate and analyze a dataset containing 300 news documents.
- Perform text preprocessing.
- Implement Basic TF-IDF.
- Implement Improved TF-IDF.
- Represent documents as TF-IDF vectors.
- Apply the Vector Space Model.
- Calculate cosine similarity between documents.
- Retrieve the most relevant documents for custom search queries.
- Compare Basic TF-IDF and Improved TF-IDF results.

## 📂 Dataset Description

The dataset contains 300 news documents distributed across five categories.

| Category | Number of Documents |
|---|---:|
| Technology | 60 |
| Sports | 60 |
| Business | 60 |
| Politics | 60 |
| Entertainment | 60 |
| **Total** | **300** |

Each document contains the following fields:

- ID
- Title
- Text
- Category

**Note:** The generated dataset is synthetic news text, not a collection of verified real-world news articles.

## ⚙️ Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Regular Expressions (Regex)

## 🔄 Project Workflow

1. Dataset Generation
2. Text Preprocessing
3. Basic TF-IDF Calculation
4. Improved TF-IDF Calculation
5. Document Vector Representation
6. Vector Space Model
7. Cosine Similarity Calculation
8. Document Similarity Comparison
9. Custom Query Search
10. Result Visualization

## 📖 Methodology

### 1. Text Preprocessing

The preprocessing stage includes:

- Converting text into lowercase.
- Removing punctuation and special characters.
- Removing numerical values.
- Removing common English stopwords.
- Tokenizing the cleaned text.

### 2. Basic TF-IDF

Basic TF-IDF assigns weights to terms based on their frequency in a document and their distribution across the document collection.

Configuration:

- Unigram representation.
- Raw term frequency.
- No IDF smoothing.
- L2 normalization.

### 3. Improved TF-IDF

Improved TF-IDF uses additional weighting techniques to improve term representation.

Configuration:

- Unigram and bigram representation.
- Smoothed IDF.
- Sublinear term frequency.
- L2 normalization.

The sublinear term frequency transformation is:

**TF(t,d) = 1 + log(tf(t,d))**

The smoothed IDF used by Scikit-learn is:

**IDF(t) = log((1 + N)/(1 + df(t))) + 1**

Where:

- N = Total number of documents.
- df(t) = Number of documents containing term t.
- tf(t,d) = Frequency of term t in document d.

### 4. Vector Space Model (VSM)

The Vector Space Model represents each document as a numerical vector based on its TF-IDF weights.

Each document is represented in a multidimensional vector space.

### 5. Cosine Similarity

Cosine similarity measures the similarity between two document vectors.

Formula:

Cosine Similarity(A,B) = (A · B) / (||A|| × ||B||)

Where:

- A and B are document vectors.
- A · B represents the dot product.
- ||A|| and ||B|| represent vector magnitudes.

A higher cosine similarity score indicates greater similarity between two documents.

## 🚀 How to Run the Project

### Step 1: Open Google Colab

Visit:

https://colab.research.google.com/

### Step 2: Create a Notebook

Create a new Python notebook.

### Step 3: Add the Project Code

Copy the project implementation into the notebook cells.

### Step 4: Install Required Libraries

```python
!pip install pandas numpy scikit-learn matplotlib seaborn
```

### Step 5: Execute the Notebook

Run all cells sequentially.

### Step 6: Explore the Results

The implementation generates:

- News dataset.
- Preprocessed text.
- Basic TF-IDF vectors.
- Improved TF-IDF vectors.
- Top important terms.
- Cosine similarity matrices.
- Similar document results.
- Custom query search results.
- Basic vs Improved TF-IDF comparison.

## 📊 Expected Outputs

1. Dataset with 300 news documents.
2. Preprocessed news documents.
3. Basic TF-IDF matrix.
4. Improved TF-IDF matrix.
5. Top weighted terms.
6. Document similarity heatmap.
7. Top 5 similar documents.
8. Custom search results.
9. Comparison of Basic and Improved TF-IDF.

## 📁 Project Structure

```text
TF-IDF-Vector-Space-Model/
│
├── README.md
├── TFIDF_Vector_Space_300_Documents.ipynb
│
├── data/
│   └── news_dataset.csv
│
├── outputs/
│   ├── basic_tfidf_matrix.csv
│   ├── improved_tfidf_matrix.csv
│   ├── basic_similarity_matrix.csv
│   ├── improved_similarity_matrix.csv
│   └── comparison_results.csv
│
└── requirements.txt
```

*The structure above describes the intended organization; individual output files are created when the corresponding code is executed.*

## 🔍 Applications

- News article retrieval.
- Search engines.
- Document similarity analysis.
- Information retrieval systems.
- Text mining.
- Content recommendation.
- Duplicate document identification.

## 🔮 Future Enhancements

- Use a larger real-world news dataset.
- Implement stemming and lemmatization.
- Add a web-based search interface.
- Improve search result ranking.
- Support document uploads.
- Extend the system to multilingual documents.

## 👨‍💻 Project Focus

This project focuses exclusively on **TF-IDF, Improved TF-IDF, Vector Space Model, and Cosine Similarity** for document representation and retrieval.

It does not implement machine learning classification algorithms.

## 📜 License

This project is intended for academic and educational purposes.
