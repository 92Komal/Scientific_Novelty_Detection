# Scientific Novelty Detection
**Phrase Extraction :** 
The BERT-based model is efficient for contextual representations of the sentences. 
We use BERT-CRF model to extract the phrases from the contribution sentences. 
We train model two extra datasets SciClaim and SciERC. The Sciclaim 12,738 annotations on 901 sentences from expert-identified claims in SBS
papers, recognized causal language in PubMed papers, and claims and causal language heuristically discovered from CORD-19 abstracts and 
the SciERC dataset includes annotations for scientific entities, their relations, and coreference clusters. This dataset is annotated for 500 scientific abstracts. For contextual representations of sentences, the BERT-based model is effective. The CRF layer is used to identify scientific phrases in contribution sentences. CRF takes advantage of the surrounding context while labeling tokens in a sequence.


**Triplet Extraction :** 
We have to organize these phrases into triplets: subject, predicate, and object. The information unit is set according to the base (NCG) dataset. We classify contribution sentences of the NCG dataset into one of the twelve Information Units, namely ablation analysis, approach, baselines, experiments, experimental setup, research problem, hyperparameters, model, results, task, dataset, and code. We label the contribution sentences with the Information Units. The predicate is unique in triplets. We create a BERT-based binary classifier to classify the predicate. In this  classifier, 1 indicates a predicate, while 0 indicates a non-predicate. We input the article's sentence with a phrase marker into the binary classifier. The phrases have to be formed as a triplet. We split them into a few categories based on their composition to a deeper understanding of triplets properties. To learn in deep of the triplet's characteristics, we categorized triplets into five categories _A, B, C, D, E_. For the type  _A, B, C, D_ . We use four BERT-based classifiers to validate triplets and extract type E triplets using a rule-based approach. We use the _Neo4j_ platform for the visualization of the knowledge graph. Neo4j is a graph database optimized for storing graph nodes, attributes, and edges. 

