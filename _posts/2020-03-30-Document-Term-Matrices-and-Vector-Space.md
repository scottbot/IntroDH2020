---
layout: post
title: "Document Term Matricies and Vector Space"
author: "Gayathri Manchella"
---

**Global weight** is the weight of an index term across a collection of documents using probability arguments, and you take the frequency of that term over all words in the book. **Local weight** is just in a certain index you chose. Thus, weight of an index term: w = local weight  * global weight. For large sets, we take log values, which implies independence when adding terms, which can lead to negative values, so we invert the document formula from d/D to D/d which leads to **IDF**, which is: **inverse document frequency**.

The IDF model assumes that terms occur independently, but oftentimes, that's not the case, because terms relevant to a given topic tend to co-occur (for example, laundry and detergent, or pajamas and bedtime). IDF measures of the specificity or level of detail at which a given concept is represented, and because of the inversion terms that occur a lot (a, is, and, in, of, the) are all low- IDF terms. This makes sense because they don’t add to our understanding of the topic. On the other hand, brand names, technical terms, and scientific nomenclature words tend to be more discriminatory, thus, high-IDF terms.
Now things get a little more technical: if you want to compare two documents, first get the vectors for each, and take the dot product, or do the **cosine similarity**, a formula to find the angle between the two vectors. A cosine similarity makes use of normalizing data set.

---

Some vocab words:

**Polysemy**: same terms can be used in different contexts 
Example: [driving cars] vs. [driving results] Thus, irrelevant documents can be retrieved because they may share some words from the query. This affects precision. 

**Synonymity**: different terms can be used in the same contexts 
Example: [car insurance] vs. [auto insurance] So relevant documents might not be retrieved. This affects recall.  

**Ordering**: different terms can be used in different positions in different contexts 
Example: [junior college] vs. [college junior] This can affect precision and recall.
However, some digital humanists don’t agree with the IDF model. They argue for (1) conceptual history and (2) vector semantics. 

**Conceptual history**: articulates how ideas function as historical objects and to explain how they emerge and transform over time. Concepts are not words, each word is unique because it has a separate connotation. The technical term in linguistics is onomasiology which names the study of how multiple words express a single concept.

**Vector semantics**: subfield of computational linguistics devoted to the quantitative study of word meaning.
This works well because concepts are best understood as structural patterns that recur among words. They want to use the **vector-space model**: creates statistical profiles for every word, and each of those profiles can be broken up into any number of clusters. However, this is not good for describing broad themes, but can dissect how the word has been used which is everything the above failed to do. Why does conceptual history matter so much? Well because the history of concepts is meant to narrate change over time; *freedom* was not a concept till *slaver*. Furthermore, *rights* are associated with *parliament* and *church*, but now *rights* are associated with *man* and *sacred*. 

---

So what are some ways humanists use these tools to make pretty graphs? 

**(1) To visualize single texts**: this means they want to visualize textual patterns that are open to direct inspection, like frequency charts. 

**(2) Choose features to represent texts**, like scatterplots and Ngrams. 

**(3) Identify distinctive vocabulary**, like word clouds,

**(4) Find or organize work**, like keyword searching in library catalogs and full-text databases, but a big limitation in this is that works of poetry or fiction published before 1960, for instance, are often not tagged as “poetry” or “fiction. 

**(5) Model literary forms**, which means you first identify a concept that you’re trying to understand, and then try to model it, or 

**(6) model social boundaries**, which means you use text to mark social transactions, political or legal history, and lastly, and the most interesting is 

**(7) unsupervised modeling**, which means modeling without having a hypothesis for the result. The models we have have a supervised goal (ex. Model Harry Potter, we know Harry is most common), but in modeling, we don’t know what kind of pattern will emerge.

---

5 Hypothesis to Know:

**Statistical semantics hypothesis**: Statistical patterns of human word usage can be used to figure out what people mean

**Bag of words hypothesis**: if there are two similar matrices, the work they correspond to also has similar meanings 

**Distributional hypothesis**: Words that occur in similar contexts tend to have similar meaning

**Extended distributional hypothesis**: Patterns that co-occur with similar pairs tend to have similar meaning in expressing semantic relations

**Latent relation hypothesis**: Pairs  of  words  that  co-occur  in  similar patterns  tend to have similar semantic relations
 
 ---

A **document-term matrix** or **term-document matrix** is a mathematical matrix that describes the frequency of terms that occur in a collection of documents. It is used in natural language processing, and adding collocation as terms improves the quality of the vectors, especially when computing similarities between documents
