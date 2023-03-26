<img align="right" src="https://visitor-badge.laobi.icu/badge?page_id=bictole.DeepNLP&right_color=red">

# DeepNLP [![Profile][title-img]][profile]

[title-img]:https://img.shields.io/badge/-SCIA--PRIME-red
[profile]:https://github.com/Pypearl

## Authors

[Victor Simonin](https://github.com/Bictole)\
[Alexandre Lemonnier](https://github.com/Alex-Leme)\
[Enguerrand De Gentile Duquesne](https://github.com/Engdomorphisme)

---

## Lab1

The Lab1 describes two functions used in natural language processing to generate **word embeddings**, which are vector representations of words in a corpus that capture their meaning and relationships to other words. The first function, "compute_co_occurrence_matrix", creates a co-occurrence matrix from a given corpus, where each row and column corresponds to a unique word and the value at position (i,j) represents the number of times word i co-occurs with word j within a specified window size. The second function, "reduce_to_k_dim", uses **truncated singular value decomposition** (SVD) to reduce the dimensionality of the co-occurrence matrix to generate k-dimensional word embeddings.

**Co-occurrence matrices** are commonly used in natural language processing to represent the distributional semantics of words, i.e., the idea that words that appear in similar contexts have similar meanings. Truncated SVD is a technique commonly used in dimensionality reduction tasks that involve large matrices, as it can efficiently identify the most informative dimensions while discarding less relevant ones. Together, these techniques can be used to generate high-quality **word embeddings** that can be used in a variety of NLP tasks, such as sentiment analysis, text classification, and machine translation.

## Lab2 

The Lab2 discusses the use of **attention mechanisms** in machine learning models. The focus is on a specific scenario where the input is a set of values and their corresponding key vectors, and the goal is to obtain an output that is a good approximation of the average of two of these values.

It explains that in this scenario, by setting the dot product of the query vector and the key vectors corresponding to the two values much larger than the dot product with any other key vectors, the output will be **heavily influenced** by these two values and will be a good approximation of their average. The query vector is defined as a linear combination of the means of the key vectors for the two values.

It also discusses a scenario where the **covariance matrix** for one of the items is different from the others and includes a non-negligible term. This affects the norm of the corresponding key vector, which in turn affects the attention scores and the output vector.

It further suggests a way to use **multi-headed attention** to achieve the desired output when the key vectors have unknown covariances. This involves using two query vectors designed to focus on the two values of interest, and averaging the outputs obtained from single-headed attention using these query vectors.
