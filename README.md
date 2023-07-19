# Knkowledge Graphs
A knowledge graph is a structured representation of knowledge in the form of a directed graph. In a knowledge graph, entities are represented as nodes, and relationships between entities are represented as directed edges connecting the nodes. This graph-like structure allows for efficient storage, retrieval, and reasoning about complex relationships and information.

Knowledge graphs are used to model and organize vast amounts of heterogeneous data from various sources, enabling powerful data integration and knowledge discovery. They are employed in a wide range of applications, including the semantic web, natural language processing, recommendation systems, question-answering systems, and more.

# LLMs
Large Language Models (LLMs) are a type of artificial intelligence that can generate human-like text and perform a wide range of natural language processing tasks. These models are trained on vast amounts of text data and can generate coherent and contextually relevant responses to a wide range of prompts. LLMs have the ability to understand and generate text in multiple languages, making them a powerful tool for natural language processing tasks such as question answering, text generation, and language translation. LLMs are used in a variety of applications, including chatbots, virtual assistants, and content-generation tools.

## Knowledge Graph Generation and Question Answering using NLP Techniques
This project demonstrates how to generate a knowledge graph from a text using natural language processing (NLP) techniques and use the resulting knowledge graph to answer questions. The project uses several NLP libraries and tools, including spaCy, Stanford CoreNLP, and BERT.

# Requirements
To run this project, you will need to have the following libraries and tools installed:

spacy

stanfordnlp

stanza

torch

transformers

You will also need to have access to a running instance of the Stanford CoreNLP server.

![image](https://github.com/Suvam-Patra/KG-QA/assets/95912953/620f7d98-d15e-403c-b8e3-bfa622a97d34)

# Usage
**Named Entity Recognition (NER):** Named Entity Recognition (NER) is the process of identifying and classifying named entities in text. Named entities are real-world objects such as people, locations, organizations, and dates that are represented by proper nouns. NER involves identifying the boundaries of named entities in the text and classifying them into predefined categories. In the code you provided, NER is performed using the spacy_ner() function, which uses the spaCy library to extract named entities from the input text.

**Coreference Resolution:** Coreference resolution is the process of identifying and resolving references to the same entity within a text. This involves identifying pronouns and other referring expressions that refer to the same entity and linking them together. Coreference resolution is important for understanding the meaning of a text, as it allows us to determine which entities are being referred to by different expressions. In the code you provided, coreference resolution is performed using the coreference() function, which uses the AllenNLP library to resolve coreferences in the input text.

**Relation Extraction:** Relation extraction is the process of identifying and extracting relations between named entities in text. This involves identifying pairs of named entities that are related to each other and extracting information about the nature of their relationship. Relation extraction can be used to generate structured representations of information from unstructured text data. In the code you provided, relation extraction is performed using the extract_relations() function, which uses spaCy and the Stanford CoreNLP server to extract relations from the input text.

# Advantages
**Integration of multiple NLP techniques:** The code integrates multiple NLP techniques, including named entity recognition, coreference resolution, and relation extraction, to generate a comprehensive knowledge graph from the input text.
**Use of pre-trained models:** The code makes use of pre-trained models, such as spaCy’s NER model and BERT for question answering, which can save time and effort compared to training models from scratch.
**Modularity:** The code is modular, with separate functions for each step of the process, making it easy to understand and modify.

# Disadvantages
**Data quality:** The quality of the generated knowledge graph and the accuracy of the answers to the questions depend on the quality of the input data. If the input data is incomplete, inaccurate, or inconsistent, this can affect the performance of the code and the accuracy of the answers.
**generate noisy or irrelevant relation:** One potential disadvantage of using OpenIE for relation extraction is that it may generate noisy or irrelevant relations. OpenIE is designed to extract open-domain relation triples from text, representing a subject, a relation, and the object of the relation. However, not all relations extracted by OpenIE may be relevant or useful for a particular application.


# Llama_Index
Llama Index is a data framework for connecting custom data sources to large language models. It provides a simple and flexible way to ingest data from various sources and formats, structure the data into indices and graphs, and use the data with large language models to generate knowledge-augmented responses to queries. Llama Index provides a query interface that accepts any input prompt over your data and returns a response that is augmented with knowledge from your data sources. It is built on top of LangChain, which provides the fundamental building blocks for many different kinds of LLM applications.

![image](https://github.com/Suvam-Patra/KG-QA/assets/95912953/e2801812-48ad-477d-8458-1ffc1ff62d04)

For more information refer-

https://gpt-index.readthedocs.io/en/latest/

https://betterprogramming.pub/getting-started-with-llamaindex-169bbf475a94

# Advantages
**Efficiency**: The code uses OpenAI’s GPT-3.5 model and the Llama Index library to efficiently generate a knowledge graph from a set of documents. This approach is faster and more scalable than traditional NLP techniques, which can require significant computational resources and time to process large amounts of data.

**Accuracy**: The use of large language models such as GPT-3.5 allows for more accurate generation of the knowledge graph and responses to queries. These models are trained on vast amounts of text data and can generate coherent and contextually relevant responses to a wide range of prompts.

**Flexibility**: The code is flexible and can be easily adapted to work with different data sources and formats. The Llama Index library provides a simple and flexible way to ingest data from various sources and structure it into indices and graphs.

**Ease of use**: The code is easy to use and does not require extensive knowledge of NLP techniques. Users can simply load their data into the specified directory, create instances of the required classes, and generate a knowledge graph and responses to queries with just a few lines of code.

## Building and Utilizing Knowledge Graphs with Large Language Models for Question Answering
This project demonstrates how to generate a knowledge graph from a set of documents using OpenAI’s GPT-3.5 model and the Llama Index library. The resulting knowledge graph is visualized using the NetworkX and Matplotlib libraries, and queries can be answered using a query engine created from the knowledge graph index and large language models.

# Requirements
To run this project, you will need to have the following libraries installed:

openai

logging

sys

llama_index

networkx

matplotlib

IPython

You will also need to have an OpenAI API key and set it as an environment variable using the os.environ method.

# System Architecture
The system's architecture comprises several key components:

Language Model: The core of the system is based on a fine-tuned ChatOpenAI language model (e.g., GPT-3.5) that is capable of processing conversational inputs.

LLMPredictor: This component wraps the language model and provides prediction capabilities, handling the communication with the model's API.

ServiceContext: Responsible for managing the language model's prediction service and chunking long documents for efficient processing.

StorageContext: Manages the storage of the generated knowledge graph using a SimpleGraphStore.

GPTKnowledgeGraphIndex: The knowledge graph index is constructed using this class, and it supports embeddings to measure similarity between queries and graph entries.

# Usage
To use this project, first load your data into a directory and specify the path to that directory when creating an instance of the SimpleDirectoryReader class. Then, create instances of the LLMPredictor, ServiceContext, and StorageContext classes as shown in the code.

Next, create an instance of the GPTKnowledgeGraphIndex class using the .from_documents() method and specify the appropriate parameters. You can then visualize the knowledge graph using the NetworkX and Matplotlib libraries as shown in the code.

Finally, create an instance of a query engine using the .as_query_engine() method of the knowledge graph index. You can use this query engine to generate responses to queries about the content of your documents using large language models.



