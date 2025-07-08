**Project Description:**

Our aim is to build a content-based recommender system that helps researchers quickly find relevant PubMed articles for a given GEO dataset(genome dataset) by identifying and recommending similar literature.
This project was inspired by paper: "Recommender system of scholarly papers using public datasets", PMCID: PMC8378599

We scraped data using NCBI Entrez API to get genome metadata(geo series) and pubmed article data, we also made sure to download the relevant pubmed article that was linked with the geo series(using the mentioned pmid in the geo series)

Dataset: Pubmed data that contains data about pubmed articles including pubmed id (pmid) and Geo dataset which is a meta data of geo expression. We extracted 3500 Geo series data and 5000 pubmed data

As our recommender system is completely content based we aim to explore different vectorization techniques followed by cosine similarity to rank and evaluate their performance in recommending relevant papers and later combine two best performing to build a hybrid recommender system

For evaluation: 
Our two dataset both have PMIDs column which links the geo and pubmed data together. (pmid is unique identiciation article number so when researchers upload their geo metadata they also submit a pmid that they wrote which related to research paper that was written based on the data. so during eval we check where this matching pmid is recommended in the top 10 or not to evaluate performance.

-------------------------------------------------------------------------------------------
This is the first notebook that contains:
- Data Cleaning and exploration process
Vectorization techniques:
- TF-IDF
- Weighted TF-IDF
- Word2Vec
- BioWord2Vec

**Requirements:**
- pandas = 2.2.2
- numpy = 1.26.4
- nltk = 3.9.1
- spacy = 3.8.7
- matplotlib = 3.10.0
- seaborn = 0.13.2
- scikit-learn = 1.6.1
- scipy = 1.13.1
- gensim = 4.3.3
- wordcloud = 1.9.4
- Bio-word2vec pre trained embedding (BioWordVec_PubMed_MIMICIII_d200.vec.bin) file included among the files. can be found in !wget https://ftp.ncbi.nlm.nih.gov/pub/lu/Suppl/BioSentVec/BioWordVec_PubMed_MIMICIII_d200.vec.bin

Dataset used: geo_final_5000.csv, pubmed_final_5000.csv

-----------------------------------------------------------------------------------------------------------------------------------------------
Next : Please refer to other notebooks for different vectorization techniques
