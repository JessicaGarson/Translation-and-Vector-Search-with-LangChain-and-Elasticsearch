# Translation and Vector Search with LangChain and Elasticsearch

This is an example that translates a column from Chinese to English using Doctran and uses vector search in Elasticsearch to learn more about the translated documents. The dataset used is a set of press clippings from my band's recent run of shows in the Shanghai area.

## Getting started

First, you want to configure an environment variable for your OpenAI API Key, which you can find on the [API keys page in OpenAI's developer portal](https://platform.openai.com/api-keys). More infomation on getting started for the first can also be found in the [LangChain quick start guide](https://python.langchain.com/v0.1/docs/get_started/quickstart/).

```bash
export OPENAI_API_KEY="your_api_key"
```

This demo uses Elasticsearch version 8.13; if you are new, check out our Quick Start on [Elasticsearch](https://www.elastic.co/guide/en/elasticsearch/reference/current/getting-started.html) and the [documentation on the integration between LangChain and Elasticsearch](https://python.langchain.com/v0.2/docs/integrations/vectorstores/elasticsearch/).

You will want to load a Jupyter Notebook to work with your data interactively. To do so, you can run the following in your terminal.

    ```
    jupyter notebook
    ```

In the right-hand corner, you can select where it says “New” to create a new Jupyter Notebook.

## Additional resources
