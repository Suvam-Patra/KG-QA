# Knowledge Graphs
A knowledge graph is a structured representation of knowledge in the form of a directed graph. In a knowledge graph, entities are represented as nodes, and relationships between entities are represented as directed edges connecting the nodes. This graph-like structure allows for efficient storage, retrieval, and reasoning about complex relationships and information.

Knowledge graphs are used to model and organize vast amounts of heterogeneous data from various sources, enabling powerful data integration and knowledge discovery. They are employed in a wide range of applications, including the semantic web, natural language processing, recommendation systems, question-answering systems, and more.
A knowledge graph is a powerful tool that can provide many benefits. Some of the key benefits of using a knowledge graph include:

**Data integration:** Knowledge graphs can help link and harmonize data from diverse sources, fostering data sharing and collaboration among organizations, and allowing for a more comprehensive view of the information.

**Enhanced understanding:** Knowledge graphs provide a richer context and understanding of information by representing relationships between entities in a visual and intuitive way.

**Combining siloed data sources:** Knowledge graphs help to combine disparate silos of data, giving you an overview of all of your knowledge – not only departmentally but also across departments and global organizations.

**Combining structured and unstructured data:** Knowledge graph technology means being able to connect different types of data in meaningful ways and supporting richer data services than most knowledge management systems.

**Informed decision making:** Using a knowledge graph means no more looking through piles of paper to find a particular document as knowledge graphs provide relevant facts and contextualized answers to your specific questions, rather than a broad search result with lots of irrelevant information.

For more information refer-

https://www.wisecube.ai/blog/8-benefits-of-building-a-knowledge-graph/

https://research.aimultiple.com/knowledge-graph/

# LLMs
Large Language Models (LLMs) are a type of artificial intelligence that can generate human-like text and perform a wide range of natural language processing tasks. These models are trained on vast amounts of text data and can generate coherent and contextually relevant responses to a wide range of prompts. LLMs have the ability to understand and generate text in multiple languages, making them a powerful tool for natural language processing tasks such as question answering, text generation, and language translation. LLMs are used in a variety of applications, including chatbots, virtual assistants, and content-generation tools.

# Llama_Index
Llama Index is a data framework for connecting custom data sources to large language models. It provides a simple and flexible way to ingest data from various sources and formats, structure the data into indices and graphs, and use the data with large language models to generate knowledge-augmented responses to queries. Llama Index provides a query interface that accepts any input prompt over your data and returns a response that is augmented with knowledge from your data sources. It is built on top of LangChain, which provides the fundamental building blocks for many different kinds of LLM applications.

![image](https://github.com/Suvam-Patra/KG-QA/assets/95912953/e2801812-48ad-477d-8458-1ffc1ff62d04)

For more information refer-

https://gpt-index.readthedocs.io/en/latest/

https://betterprogramming.pub/getting-started-with-llamaindex-169bbf475a94

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

# Code

https://github.com/Suvam-Patra/KG-QA/blob/main/KnowledgeGraphQA.ipynb

# Advantages
**Efficiency**: The code uses OpenAI’s GPT-3.5 model and the Llama Index library to efficiently generate a knowledge graph from a set of documents. This approach is faster and more scalable than traditional NLP techniques, which can require significant computational resources and time to process large amounts of data.

**Accuracy**: The use of large language models such as GPT-3.5 allows for more accurate generation of the knowledge graph and responses to queries. These models are trained on vast amounts of text data and can generate coherent and contextually relevant responses to a wide range of prompts.

**Flexibility**: The code is flexible and can be easily adapted to work with different data sources and formats. The Llama Index library provides a simple and flexible way to ingest data from various sources and structure it into indices and graphs.

**Ease of use**: The code is easy to use and does not require extensive knowledge of NLP techniques. Users can simply load their data into the specified directory, create instances of the required classes, and generate a knowledge graph and responses to queries with just a few lines of code.

# Disadvantages
**OpenAI API key requirement:** The code requires an OpenAI API key, which may not be accessible to all users.

**Cost of using OpenAI tokens:** Using the OpenAI API can be costly, as it consumes tokens each time a request is made. This could be a disadvantage for users with limited budgets or high usage requirements.

*You can use hugging face token in place of openai_api_key*

# References
https://github.com/jerryjliu/llama_index/tree/main


