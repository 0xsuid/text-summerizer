# Text Summerizer

Text Mining on CBC news article with Natural Language Processing(NLP) - Automatically summarize the given text using **spaCy** & **Python**.


# Requirements
1. [Spacy](https://spacy.io/usage)
2. [spaCy Model](https://spacy.io/usage/models)
    - ```python -m spacy download en_core_web_sm```

## Overview

1. Convert the input text to a list of sentences. Then, compute the
number of sentences in the given Text.
2. Calculate the frequency of words in each sentence: 
    - The output is a dictionary where each key is a sentence and the value is also a dictionary of word frequency.
3. Calculate Term frequency for each word in a sentence:  
```
TF(word) = (Number of times term “word” appears in a sentence) / (Total number of terms in the sentence)
```
4. Create a matrix termFrequency:  
    - The termFrequency matrix is a dictionary where each key is a sentence and the value is also a dictionary of word frequency.
5. For each word compute how many sentences contain that word.
6. Calculate IDF for each word in a sentence.
```
IDF(word) = log_e(Total number of sentences / number of sentences with term word in it)
```
7. Compute the TF-IDF for each word in each sentence.
8. Use the TF-IDF computed in (7) and give a weight for each sentence.
9. Threshold: compute the average sentence weight
10. Generate the summary : select a sentence for summarization if the weight of the sentence exceeds the threshold.


## References

- [COVID-19 Article - CBC news](https://www.cbc.ca/news/technology/droplet-transmission-1.5549547)
- [spaCy](https://spacy.io/usage/spacy-101)