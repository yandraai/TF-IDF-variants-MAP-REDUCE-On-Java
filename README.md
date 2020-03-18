TF-IDF-variants-MAP-REDUCE-On-Java
===================================

Stage-1
--------
- TFIDF for all terms in each document, sorted alphabetically by words’ letters, and formatted for easy readability.
- List of top fifteen words from each document having the highest TFIDF value.

Stage-2
--------
- Modified the programs to remove from consideration all those words that occur only once in each document. Repeated the tasks of Stage-1 above

Observations on the variation between Stage 1 and Stage 2:
-------------------------------------------------------------
- We observe the words with more relevance across the corpus appear in the top 15 .
- The effect of the words that just appear once in a word and once in a document or very few
documents is high on the TF IDF value on the whole as the denominator depends on it.
- Ignoring such words effects the value as follows:

|Word Frequency|Document Frequency|Number of Documents that word appears in| TF -VALUE | IDF - VALUE|
|--------------|------------------|----------------------------------------|-----------|-------------|
|Only with frequency greater than 1.|Considers only those words that occur more than once. So,decreased|Considers those documents that has this word more than once. So, decreased.| Increases as the denominator decreases as we are eliminating the words that are not very frequent in the document| Increases as the denominator decreases because we are considering only the documents that have the word more than once.|

***For Instance***:
 Observe the word “Lorem” in document 0001. Though it appeared 4 times in the document
and 8 documents have the word more than once, the TF IDF value in the first program is only 0.0038 and
s not in the top 15 words of the document BUT after ignoring the less frequent words , we observe that
the TF IDF value shoots up to 0.043 which now give the actual picture regarding the relevance of the
word in the corpus and it now appears in the top15.

Stage-3
-------
- Now considering a “Term” to mean a 2-gram (two words occurring sequentially) in a document. Comparision on which one of these till now (2 and Stage 3) better charaterizes the document better.
**Stage-2**: Unigram after removing the words that appear just once in each document.
**Stage-3**: Bigram for all the words in each document.
*In general, bigrams or ngrams give a better context about the document than a unigram tf-idf gives.
Reason being bigrams portray more information than a unigram does. For example, Injected Humour is
one such word that makes more sense together when characterizing the document than the individual
words do. Choosing bigram signature makes more sense in this context which speaks better about the
document
However, when the corpus is sparse, ie.,the occurrence of the bigrams together is less frequent then
they might turn up having very less tf-idf value leading to be less useful than unigrams.*
