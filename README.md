#  Information Retrieval<br>PAGE RANKING

<!-- #### Video Demo:  <URL HERE> -->
#### **Description:**
---
**PageRank** (PR) is an **algorithm** to **rank web pages** in **search engine results**.
PageRank is a *way of measuring the importance of website pages.*

Information Retrieval (IR) can be defined as a software program that deals
with the organization, storage, retrieval, and evaluation of information from
document repositories, particularly textual information.
Information Retrieval is the activity of obtaining material that can usually
be documented on an unstructured nature i.e. usually text which satisfies an
information need from within large collections which is stored on computers. For
example, Information Retrieval can be when a user enters a query into the
system. It can be classified in NLP science.

PageRank works by counting the number and quality of links to a page to determine a rough estimate of how important the website is. The underlying assumption is that more important websites are likely to receive more links from other websites.

It is not the only algorithm used by Google to order search engine results, but it is the first algorithm that was used by the company, and it is the best-known.

The PageRank algorithm outputs a probability distribution used to represent the likelihood that a person randomly clicking on links will arrive at any particular page. PageRank can be calculated for collections of documents of any size. It is assumed in several research papers that the distribution is evenly divided among all documents in the collection at the beginning of the computational process. The PageRank computations require several passes, called “iterations”, through the collection to adjust approximate PageRank values to more closely reflect the theoretical true value.

The above centrality measure is not implemented for multi-graphs.

in this case, Cranfield collection is used. [Full Cranfield dataset
](http://ir.dcs.gla.ac.uk/resources/test_collections/cran/cran.tar.gz)

    To implement a Page Ranking algorithm, preprocessing and making dataset ready is necessary.
    also gaining some information about it can be useful.
---
# PART 1:

The Cranfield collection is a standard IR text collection, consisting of 1400 documents from the aerodynamics field.
___
1. this program is preprocessing the collection.

       a. Function that tokenizes the text.characters that need special handling, as 
       discussed in the text (. , - etc.).
___
2. Determine the frequency of occurence for all the  words in this collection. 

        a. Vocabulary size (i.e. number of unique terms)

        b. Top 10 words in the ranking (i.e. the words with the highest frequencies)

        c. From these top 10 words, Finding "meaningful" (i.e. they are not stopwords),
        and eliminate "stopwords". 
    
        d. Minimum number of unique words accounting for half of 
        the total number of words in the collection.
___
3. Integrate the [Porter stemmer](https://tartarus.org/martin/PorterStemmer/) and  [Stopwords](https://www.ranks.nl/stopwords) eliminator into the code. 

        Answering again a-d from the previous point. 
___
4. the [Heaps law](https://nlp.stanford.edu/IR-book/html/htmledition/heaps-law-estimating-the-number-of-terms-1.html) 

        Use this function to predict what would be the vocabulary size
        if the corpus were to increase to 500,000 words or to 2,000,000 words for instance.
___

# PART 2
To complete this project, you need to use the pre-processing
tools implemented during previous part.
---
1. Implementing an indexing scheme based on the vectorial model. 
   For weighting:
   
        a. the TF/IDF weighting scheme
[TF/IDF](https://towardsdatascience.com/tf-idf-for-document-ranking-from-scratch-in-python-on-real-world-dataset-796d339a4089)
___
2. For each of the queries provided on the quries.txt, determine: 
   
        a. ranked list of documents, in descending order of their similarity with the query. 
        The output ofretrieval is a list of (query_id, document_id) pairs.




# Packages
**nltk**

[NLTK](https://www.nltk.org/index.html) is a leading platform for building Python programs to work with human language data.
   
   >[Installing NLTK](https://www.nltk.org/install.html)<font color='red'> (required)</font>
   
   >[Installing NLTK Data](https://www.nltk.org/data.html#installing-nltk-data)<font color='red'> (required)</font>
   
**regular expressions**

>[Installing regex](https://pypi.org/project/regex/)<font color='red'> (required)</font>