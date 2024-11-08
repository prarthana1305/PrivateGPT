# 📚 PrivateGPT: Offline Chat Application with Advanced Document Search

**PrivateGPT** is an offline chat application designed to deliver secure, private, and customizable natural language interactions. This project allows users to search through document contents and query files on their local machine, without requiring internet connectivity.

At its core, the application uses **Ollama Mistral 7b** as the Large Language Model (LLM), integrated with **Nomic-embed-text** embeddings for efficient text search. By leveraging **Qdrant** as the vector store and **Gradio** for a user-friendly interface, this application provides a powerful and intuitive offline search experience.

## 🌟 Key Features
- **Offline Functionality**: Operates completely offline, ensuring privacy and security.
- **Advanced Natural Language Processing**: Uses the **Ollama Mistral 7b** model for understanding and responding to complex queries.
- **Efficient Document Search**: Utilizes **Nomic-embed-text** embeddings to convert text into numerical vectors, enabling quick search results.
- **User-Friendly Interface**: Built using **Gradio** for easy interaction.
- **Customizable**: Supports integration with additional models from **Hugging Face** and flexible configurations.

## 🚀 Getting Started

### 📦 Installation
Make sure you have **Python 3.8+**, **Poetry**, and **Ollama** installed on your system.

#### Step 1: Clone the Repository
git clone https://github.com/zylon-ai/private-gpt.git
cd private-gpt



#### Step 2 :  Install Poetry (if not already installed)
Poetry is a Python dependency management tool that simplifies managing libraries
and ensures compatibility. It creates isolated environments and manages dependencies,
so you don't have to worry about conflicting package versions.
curl -sSL https://install.python-poetry.org | python3 -



#### Step 3: Install Dependencies
PrivateGPT uses Poetry to manage its dependencies. You can install all the necessary
packages based on your preferred setup. To install everything needed for a local setup
with UI, Qdrant as the vector store, and Ollama as the LLM and embeddings provider, run:
poetry install --extras "ui vector-stores-qdrant llms-ollama embeddings-ollama"



#### Step 4: Set Up Configuration
PrivateGPT uses YAML configuration files. You can customize settings by editing files like
settings.yaml and settings-ollama.yaml. To use the Ollama Mistral 7b model, update your
configuration in settings-ollama.yaml.



#### Step 5: Run the Application
Make sure Ollama is installed and running on your local system:
ollama serve

# To start the PrivateGPT server, run:
PGPT_PROFILES=ollama make run
This will load configurations from both settings.yaml and settings-ollama.yaml,and open the application on http://localhost:8001.


# 🌐 Available Setups
PrivateGPT is highly flexible, allowing different setups for LLM, embeddings, and vector stores.

# Here are some examples:
1. Local Setup with Qdrant:
poetry install --extras "vector-stores-qdrant llms-ollama embeddings-ollama"

2. Remote Setup with Hugging Face Models:
poetry install --extras "llms-huggingface embeddings-huggingface"

3. With Gradio UI:
poetry install --extras "ui"


![Application Demo](C:\Users\Prarthana\Downloads)

# 🛠️ Main Concepts
#### 1. Ollama Mistral 7b (LLM)
The Ollama Mistral 7b model is a powerful LLM designed for natural language processing tasks.
It's optimized for understanding user queries and providing meaningful responses even in offline mode.


#### 2. Nomic-Embed-Text (Embeddings)
Embeddings convert text into numerical vectors, allowing efficient document search.
By leveraging Nomic-embed-text, PrivateGPT can quickly sift through large volumes of data to find relevant information.


#### 3. Qdrant (Vector Store)
Qdrant is a high-performance vector store that indexes embeddings for fast retrieval.
It allows PrivateGPT to handle large datasets with low latency.


#### 4. Poetry (Dependency Management)
Poetry simplifies the process of managing Python dependencies by using a single file (pyproject.toml) for defining all project requirements. It ensures that your dependencies are isolated, compatible,and up-to-date.


#### 5. Gradio (User Interface)
Gradio allows you to create a web-based user interface for your machine learning applicationwith minimal effort. It makes it easy to test and interact with PrivateGPT.


# 🖥️ Usage 
Once the server is up and running, open your browser and go to: http://localhost:8001



