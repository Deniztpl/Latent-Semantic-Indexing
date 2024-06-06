
# Latent Semantic Indexing (LSI)

Latent semantic indexing (LSI) is an indexing and retrieval method that uses a mathematical technique called singular value decomposition (SVD) to identify patterns in the relationships between the terms and concepts contained in an unstructured collection of text.

# Data
The data is taken fom comcast and it is csv file having columns of: 
- author: Name of the customer
- posted_on: The date of complaint
- rating: Rating (Not exactly known)
- text: The complaint as text

The complaints are reduced so that the posts before 2009 1 January are removed.

# Term Document Matrix
Term document matrix is a matrix showing relations between documents and words in them. It shows how much a word is appeared in document. Here, the documents are text columns in the csv data. It is extracted and following operations perfromed using `ntlk` library:

-  **Tokenization**: Tokenization is the process of breaking down text into individual words or tokens.

-  **Stopword Removal**: Stopwords are common words (like "the", "and", "is") that are often removed from text data to focus on the more meaningful words. 

-  **Digit Removal**: Tokens containing digits are often removed to clean the text data, especially if numbers are not relevant to the analysis.

- **Punctuation Removal**: Punctuation marks are removed to ensure that only alphanumeric tokens are kept.

- **Lemmatization**: Produces the base or dictionary form of a word. It is context-sensitive and considers the meaning and part of speech.

- **Stemming**: Reducing words to their root form by removing suffixes (e.g., "running" becomes "run").

After applying these operations a term-dcoument matrix constructed.

# Built SVD
I have built `numpy.SVD()` and `numpy.linalg.eig()` from scratch. Using power method the built SVD function can successfully split given term document matrix into SVD components. After That I have compared the approximated matrix A_k with A by calculated MSE of the matrix.

# Query Searching
From term document matrix one can also search words and retrieve which text of complaints that resembles most.

# How to Install and Run the Project

## Prerequisites

- `nltk==3.8.1`
- `numpy==1.26.4`
- `pandas==2.2.2`
- `scikit_learn==1.5.0`

## Installation

1. Clone the repository:

```
git clone
```

2. Install the dependencies:

```
pip install -r requirements.txt
```

3. Run a the file "LSI.ipynb"

