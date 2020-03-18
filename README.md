TF-IDF-variants-MAP-REDUCE-On-Java
===================================

Stage-1
--------
- TFIDF for all terms in each document, sorted alphabetically by words’ letters, and formatted for easy readability.
- List of top fifteen words from each document having the highest TFIDF value.

Stage-2
--------


Observations on the variation between Stage 1 and Stage 2:
-------------------------------------------------------------

- We observe the words with more relevance across the corpus appear in the top 15 .
- The effect of the words that just appear once in a word and once in a document or very few
documents is high on the TF IDF value on the whole as the denominator depends on it.
- Ignoring such words effects the value as follows:
