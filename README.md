# Translation and Vector Search with LangChain and Elasticsearch
This example translates dataset columns from one language to another using LangChain after it uses Elastic's vector database capabilities to learn more about the translated documents.

### Configure an environment variable for your OpenAI API Key
First, you want to configure an environment variable for your OpenAI API Key, which you can find on the [API keys page in OpenAI's developer portal](https://platform.openai.com/api-keys). More infomation on getting started for the first can also be found in the [LangChain quick start guide](https://python.langchain.com/v0.1/docs/get_started/quickstart/).

```bash
export OPENAI_API_KEY="your_api_key"
```

### Set up Elasticsearch
This demo uses Elasticsearch version 8.12; if you are new, check out our Quick Start on [Elasticsearch](https://www.elastic.co/guide/en/elasticsearch/reference/current/getting-started.html) and the [documentation on the integration between LangChain and Elasticsearch](https://python.langchain.com/v0.2/docs/integrations/vectorstores/elasticsearch/).

### Install the required packages
You will use [Jupyter Notebooks](https://jupyter.org/) to work with a dataset interactively. You will want to use asynchronous execution by installing [nest_asyncio](https://pypi.org/project/nest-asyncio/). For data manipulation when working with structured data, you must have [pandas](https://pandas.pydata.org/) installed.

To enhance your language model applications, particularly in integrating natural language processing capabilities, you will use the [LangChain](https://langchain.com/) library. To work with Elasticsearch, you will use [Elasticsearch Python Client](https://www.elastic.co/guide/en/elasticsearch/client/python-api/current/getting-started-python.html) to connect to Elasticsearch. The `langchain-elasticsearch` package allows for interaction between LangChain and Elasticsearch.

Since this example leverages OpenAI's language models, the `langchain-openai` package provides the needed support for easily integrating these models. For tasks involving text tokenization, which is crucial for preprocessing in many NLP tasks, you will use  [tiktoken](https://pypi.org/project/tiktoken/) package will be required to break text into manageable pieces for further processing efficiently.

```bash
pip install jupyter pandas langchain nest_asyncio langchain-elasticsearch langchain-openai tiktoken elasticsearch datasets
```

### Load a Jupyter Notebook
You will want to load a Jupyter Notebook to work with your data interactively. To do so, you can run the following in your terminal.

```bash
jupyter notebook
```

In the right-hand corner, you can select where it says “New” to create a new Jupyter Notebook.

## Blog post
You can find a write-up of this solution on [Elastic's Search Labs blog](https://www.elastic.co/search-labs/blog/unlocking-multilingual-insights).

## Next steps
- You can check out our [blog post](https://www.elastic.co/search-labs/blog/elasticsearch-knn-and-num-candidates-strategies) on the subject for more information on `num_candidates`, which could be a natural next step here. 
- If you are looking to tune this example a bit more, you may want to check out [our documentation on tuning an approximate KNN search](https://www.elastic.co/guide/en/elasticsearch/reference/current/tune-knn-search.html).
- Additionally you can find another tutorial on working with [multilingual datasets](https://github.com/elastic/elasticsearch-labs/blob/main/notebooks/search/04-multilingual.ipynb) on Search Labs as well as this post which walks you through [how to build multilingual RAG with Elastic and Mistral.](https://www.elastic.co/search-labs/blog/building-multilingual-rag-with-elastic-and-mistral)

## Additional resources
- [LangChain and Elastic collaborate to add vector database and semantic reranking for RAG](https://www.elastic.co/search-labs/blog/langchain-collaboration)
- [Elastic LangChain Integration](https://www.elastic.co/search-labs/integrations/langchain)

## Related webinars
- [Semantic search basics](https://www.elastic.co/virtual-events/getting-started-semantic-search-excellence)
- [Semantic search advanced](https://www.elastic.co/virtual-events/advanced-semantic-search-excellence)
- [Beyond RAG basics with Cohere](https://www.elastic.co/virtual-events/beyond-rag-basics)
