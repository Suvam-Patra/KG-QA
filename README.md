# Knkowledge Graphs
A knowledge graph is a structured representation of knowledge in the form of a directed graph. In a knowledge graph, entities are represented as nodes, and relationships between entities are represented as directed edges connecting the nodes. This graph-like structure allows for efficient storage, retrieval, and reasoning about complex relationships and information.

Knowledge graphs are used to model and organize vast amounts of heterogeneous data from various sources, enabling powerful data integration and knowledge discovery. They are employed in a wide range of applications, including the semantic web, natural language processing, recommendation systems, question-answering systems, and more.
# LLMs
LLMs are a phenomenal piece of technology for knowledge generation and are pre-trained on large amounts of publicly available data.

# Llama_Index
Llama Index is a data framework for connecting custom data sources to large language models. It provides a simple and flexible way to ingest data from various sources and formats, structure the data into indices and graphs, and use the data with large language models to generate knowledge-augmented responses to queries. Llama Index provides a query interface that accepts any input prompt over your data and returns a response that is augmented with knowledge from your data sources. It is built on top of LangChain, which provides the fundamental building blocks for many different kinds of LLM applications.

![image](https://github.com/Suvam-Patra/KG-QA/assets/95912953/e2801812-48ad-477d-8458-1ffc1ff62d04)

For more information refer-

https://gpt-index.readthedocs.io/en/latest/

https://betterprogramming.pub/getting-started-with-llamaindex-169bbf475a94


## Building and Utilizing Knowledge Graphs with Large Language Models for Question Answering
This project demonstrates how to generate a knowledge graph from a set of documents using OpenAI’s GPT-3 model and the Llama Index library. The resulting knowledge graph is visualized using the NetworkX and Matplotlib libraries, and queries can be answered using a query engine created from the knowledge graph index and large language models.

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

# Installation
To install this project, clone the repository to your local machine and navigate to the project directory. Then, install the required libraries using the following command:

pip install -r requirements.txt

# Usage
To use this project, first load your data into a directory and specify the path to that directory when creating an instance of the SimpleDirectoryReader class. Then, create instances of the LLMPredictor, ServiceContext, and StorageContext classes as shown in the code.

Next, create an instance of the GPTKnowledgeGraphIndex class using the .from_documents() method and specify the appropriate parameters. You can then visualize the knowledge graph using the NetworkX and Matplotlib libraries as shown in the code.

Finally, create an instance of a query engine using the .as_query_engine() method of the knowledge graph index. You can use this query engine to generate responses to queries about the content of your documents using large language models.

#
