# Autocorrect-Feature
Developed an Autocorrect Feature using NLP, processing a dataset of 17,647 unique words from "Moby Dick" to suggest corrections based on similarity and word probability. This project demonstrated core autocorrect principles, leveraging frequency analysis and Jaccard distance algorithms.


This project implements an Autocorrect Feature using Natural Language Processing (NLP) techniques. The goal is to replicate the autocorrect functionality found in smartphones but using a smaller dataset from a book. The project utilizes the text from "Moby Dick" to create a vocabulary of 17,647 unique words. This dataset serves as the foundation for the autocorrect system, which calculates word frequencies and probabilities to suggest corrections.

Key Features

Vocabulary Building: Extracts all words from the text data, converts them to lowercase, and removes duplicates to form a base vocabulary.

Frequency Analysis: Calculates the frequency of each word and computes a probability distribution. For example, the word "the" appeared with a probability of 0.066 (6.6% occurrence rate).

Similarity Measurement: Employs the Jaccard distance algorithm with q-grams (q=2) to compare letter pairs between words. This allows the system to rank potential corrections based on both similarity and word probability.

Autocorrect Functionality: Checks if a typed word exists in the vocabulary. If not, it generates a list of similar words, sorted by their similarity score and probability.

Example Outputs

Input: "qusetion"
Top Suggestions: "question," "section"

Input: "teers"
Top Suggestions: "steers," "terse"

Input: "hl"
Top Suggestions: "highly," "earthly"

Code Structure

The project is structured as follows:

Data Loading: Loads the text data from "Moby Dick" and preprocesses it.

Vocabulary Creation: Creates a set of unique words from the preprocessed text.

Frequency Calculation: Computes the frequency and probability of each word.

Autocorrect Function: Defines a function that takes an input word, checks if it exists in the vocabulary, and suggests corrections based on similarity and probability.
