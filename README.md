# Knkowledge Graphs
A knowledge graph is a structured representation of knowledge in the form of a directed graph. In a knowledge graph, entities are represented as nodes, and relationships between entities are represented as directed edges connecting the nodes. This graph-like structure allows for efficient storage, retrieval, and reasoning about complex relationships and information.

Knowledge graphs are used to model and organize vast amounts of heterogeneous data from various sources, enabling powerful data integration and knowledge discovery. They are employed in a wide range of applications, including semantic web, natural language processing, recommendation systems, question-answering systems, and more.

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

