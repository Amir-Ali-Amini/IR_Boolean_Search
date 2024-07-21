# Developing an Information Retrieval System with Advanced Boolean Search

This repository contains the implementation of an advanced Information Retrieval System developed as a part of my university project. The project demonstrates an efficient approach to Boolean search queries, utilizing advanced data structures for optimal performance.

## Project Details

**Author:** AmirAli Amini  
**Student ID:** 610399102  
**Project:** HW1  

## Project Overview

The primary objective of this project was to design an efficient Information Retrieval System that supports Boolean search queries. The project addresses several challenges, including efficient data storage and fast query execution, by employing advanced data structures and search algorithms.

### Key Challenges

The main challenge was designing a posting list structure to store document indices efficiently, including the word indices within each document. This required an innovative approach to ensure quick data retrieval while maintaining the necessary information for query operations.

### Solutions Implemented

1. **Efficient Data Structure:** A custom data structure was developed that outperforms traditional linked lists, enabling faster data access.

2. **Binary Search:** To enhance search speed, a binary search method was implemented to quickly locate data within our structures.

3. **Two-Dimensional Arrays:** While using two-dimensional arrays for dictionary storage can reduce code readability, it did not impact the code's execution speed.

## Libraries Used

### 1. NLTK (Natural Language Toolkit)

- **`word_tokenize`:** Used for tokenizing input text, ensuring faster data processing.
- **`stopwords`:** Utilized to remove common stopwords from English texts.

### 2. Python Standard Libraries

- **`string`:** Employed to handle English language punctuation.
- **`numpy`:** Used for efficient numerical computations and array manipulations.
- **`copy`:** Facilitated deep copying of arrays to ensure data integrity.

## Code Explanation

The code implements a custom Information Retrieval System using a sophisticated posting list data structure. The list stores each word alongside the documents it appears in and its specific indices within those documents. This structure is crucial for executing complex queries, including proximity (near) queries.

### Posting List Structure

The posting list is structured as follows:

```python
[
    {"word": "<word>", "docs": [{"doc": <document_number>, "indexes": [<index_list>]}]}
]
```

# Usage example

```
# Create an instance of the search engine
engine = searchEngine()

# Input documents
engine.input(['text1.txt', 'test.txt'])

# Execute queries
result1 = engine.find("amirali and aa")
result2 = engine.find("hasani n/3 amini")

print(result1)  # Output: [1, 2]
print(result2)  # Output: [1]
```
