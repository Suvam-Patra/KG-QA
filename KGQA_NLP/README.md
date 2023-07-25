## Knowledge Graph Generation and Question Answering using NLP Techniques
This project demonstrates how to generate a knowledge graph from a text using natural language processing (NLP) techniques and use the resulting knowledge graph to answer questions. The project uses several NLP libraries and tools, including spaCy, Stanford CoreNLP, OpenIE and BERT.

![image](https://github.com/Suvam-Patra/KG-QA/assets/95912953/620f7d98-d15e-403c-b8e3-bfa622a97d34)

# Usage
**Named Entity Recognition (NER):** Named Entity Recognition (NER) is the process of identifying and classifying named entities in text. Named entities are real-world objects such as people, locations, organizations, and dates that are represented by proper nouns. NER involves identifying the boundaries of named entities in the text and classifying them into predefined categories. In the code you provided, NER is performed using the spacy_ner() function, which uses the spaCy library to extract named entities from the input text.

**Coreference Resolution:** Coreference resolution is the process of identifying and resolving references to the same entity within a text. This involves identifying pronouns and other referring expressions that refer to the same entity and linking them together. Coreference resolution is important for understanding the meaning of a text, as it allows us to determine which entities are being referred to by different expressions. In the code you provided, coreference resolution is performed using the coreference() function, which uses the AllenNLP library to resolve coreferences in the input text.

**Relation Extraction:** Relation extraction is the process of identifying and extracting relations between named entities in text. This involves identifying pairs of named entities that are related to each other and extracting information about the nature of their relationship. Relation extraction can be used to generate structured representations of information from unstructured text data. In the code you provided, relation extraction is performed using the extract_relations() function, which uses spaCy and the Stanford CoreNLP server to extract relations from the input text.

# Code

https://github.com/Suvam-Patra/KG-QA/blob/main/KGQA_NLP.ipynb

# Advantages
**Integration of multiple NLP techniques:** The code integrates multiple NLP techniques, including named entity recognition, coreference resolution, and relation extraction, to generate a comprehensive knowledge graph from the input text.

**Use of pre-trained models:** The code makes use of pre-trained models, such as spaCy’s NER model and BERT for question answering, which can save time and effort compared to training models from scratch.

# Disadvantages
**Data quality:** The quality of the generated knowledge graph and the accuracy of the answers to the questions depend on the quality of the input data. If the input data is incomplete, inaccurate, or inconsistent, this can affect the performance of the code and the accuracy of the answers.

**Generate noisy or irrelevant relation:** One potential disadvantage of using OpenIE for relation extraction is that it may generate noisy or irrelevant relations. OpenIE is designed to extract open-domain relation triples from text, representing a subject, a relation, and the object of the relation. However, not all relations extracted by OpenIE may be relevant or useful for a particular application.

**Complexity of questions:** Another potential disadvantage of the code for question answering is that it may not be able to handle complex or multi-faceted questions. The code uses a pre-trained BERT model to generate answers to questions based on the extracted relations, but this approach may not be able to handle questions that require reasoning or inference across multiple relations or that involve complex logical or temporal relationships. Additionally, the code may not be able to handle questions that require information that is not present in the extracted relations or that require additional context or background knowledge.

# References

chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://dl.acm.org/doi/pdf/10.1145/3594778.3594877

chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://arxiv.org/pdf/1909.07606.pdf
