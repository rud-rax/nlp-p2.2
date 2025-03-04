It is essential to represent text data in numerical form for NLP task. For this we plan to implement below models : 

---

## BoW

The **Bag of Words (BoW)** model is a simple and widely used technique in natural language processing (NLP) for representing text data. It converts text into numerical feature vectors, making it suitable for machine learning algorithms. 


### **Key Concepts of the Bag of Words Model**
1. **Tokenization**:
   - The text is split into individual words or tokens.
   - Example: "I love NLP" → ["I", "love", "NLP"].

2. **Vocabulary Creation**:
   - A vocabulary is created from all unique words in the dataset.
   - Example: For the sentences "I love NLP" and "NLP is fun," the vocabulary is ["I", "love", "NLP", "is", "fun"].

3. **Vectorization**:
   - Each sentence is represented as a vector based on the frequency of words in the vocabulary.
   - Example:
     - "I love NLP" → [1, 1, 1, 0, 0]
     - "NLP is fun" → [0, 0, 1, 1, 1]



### **Steps to Implement Bag of Words**
1. **Preprocessing**:
   - Convert text to lowercase.
   - Remove punctuation, stopwords, and perform stemming/lemmatization if needed.

2. **Build Vocabulary**:
   - Create a dictionary of unique words from the entire corpus.

3. **Create Feature Vectors**:
   - For each document, count the occurrences of each word in the vocabulary.



### **Example**
#### Input:
- Document 1: "I love NLP"
- Document 2: "NLP is fun"

#### Vocabulary:
["I", "love", "NLP", "is", "fun"]

#### Feature Vectors:
- Document 1: [1, 1, 1, 0, 0]
- Document 2: [0, 0, 1, 1, 1]



### **Advantages**
- Simple and easy to implement.
- Works well for small datasets and basic tasks like text classification.



### **Disadvantages**
- Ignores word order and context (e.g., "I love NLP" and "NLP love I" are treated the same).
- Sparse representation (most entries in the vector are zeros).
- Does not capture semantic meaning or relationships between words.

---


### **Variations**
1. **Binary BoW**: Represents presence (1) or absence (0) of words instead of frequency.
2. **TF-IDF**: Weights words based on their importance in the document and corpus.
3. **N-grams**: Extends BoW to include word pairs or sequences (e.g., "I love", "love NLP").


---

# Binary BoW



---
# TF-IDF

**TF-IDF (Term Frequency-Inverse Document Frequency)** is a statistical measure used to evaluate the importance of a word in a document relative to a corpus. It combines two metrics:

1. **Term Frequency (TF)**: How often a word appears in a document.
    
2. **Inverse Document Frequency (IDF)**: How rare or common a word is across the entire corpus.
    

The TF-IDF value increases with the number of times a word appears in a document but is offset by the frequency of the word in the corpus. This helps to highlight words that are more meaningful to a specific document.