

---

## The Golden RAGtriever - Community Edition 

Welcome to Verba: The Golden RAGtriever, an community-driven open-source application designed to offer an end-to-end, streamlined, and user-friendly interface for Retrieval-Augmented Generation (RAG) out of the box. In just a few easy steps, explore your datasets and extract insights with ease, either locally with Ollama and Huggingface or through LLM providers such as Anthrophic, Cohere, and OpenAI. This project is built with and for the community, please be aware that it might not be maintained with the same urgency as other Weaviate production applications. Feel free to contribute to the project and help us make Verba even better! <3



## What Is Verba?

Verba is a fully-customizable personal assistant utilizing [Retrieval Augmented Generation (RAG)] for querying and interacting with your data, **either locally or deployed via cloud**. Resolve questions around your documents, cross-reference multiple data points or gain insights from existing knowledge bases. Verba combines state-of-the-art RAG techniques with Weaviate's context-aware database. Choose between different RAG frameworks, data types, chunking & retrieving techniques, and LLM providers based on your individual use-case.

## Feature Lists

|  Model Support                  | Implemented | Description                                             |
| --------------------------------- | ----------- | ------------------------------------------------------- |
| Ollama (e.g. Llama3)              |           | Local Embedding and Generation Models powered by Ollama |
| HuggingFace (e.g. MiniLMEmbedder) |           | Local Embedding Models powered by HuggingFace           |
| Cohere (e.g. Command R+)          |           | Embedding and Generation Models by Cohere               |
| Anthrophic (e.g. Claude Sonnet)   |           | Embedding and Generation Models by Anthrophic           |
| OpenAI (e.g. GPT4)                |           | Embedding and Generation Models by OpenAI               |
| Groq (e.g. Llama3)                |           | Generation Models by Groq (LPU inference)               |
| Novita AI (e.g. Llama3.3)         |           | Generation Models by Novita AI                          |
| Upstage (e.g. Solar)              |           | Embedding and Generation Models by Upstage              |

|  Embedding Support | Implemented | Description                              |
| -------------------- | ----------- | ---------------------------------------- |
| Weaviate             |           | Embedding Models powered by Weaviate     |
| Ollama               |           | Local Embedding Models powered by Ollama |
| SentenceTransformers |           | Embedding Models powered by HuggingFace  |
| Cohere               |           | Embedding Models by Cohere               |
| VoyageAI             |           | Embedding Models by VoyageAI             |
| OpenAI               |           | Embedding Models by OpenAI               |
| Upstage              |           | Embedding Models by Upstage              |

|  Data Support                                          | Implemented | Description                                    |
| -------------------------------------------------------- | ----------- | ---------------------------------------------- |
| [UnstructuredIO](https://docs.unstructured.io/welcome)   |           | Import Data through Unstructured               |
| [Firecrawl](https://www.firecrawl.dev/)                  |           | Scrape and Crawl URL through Firecrawl         |
| [UpstageDocumentParse](https://upstage.ai/)              |           | Parse Documents through Upstage Document AI    |
| PDF Ingestion                                            |           | Import PDF into Verba                          |
| GitHub & GitLab                                          |           | Import Files from Github and GitLab            |
| CSV/XLSX Ingestion                                       |           | Import Table Data into Verba                   |
| .DOCX                                                    |           | Import .docx files                             |
| Multi-Modal (using [AssemblyAI](https://assemblyai.com)) |           | Import and Transcribe Audio through AssemblyAI |

|  RAG Features         | Implemented     | Description                                                               |
| ----------------------- | --------------- | ------------------------------------------------------------------------- |
| Hybrid Search           |               | Semantic Search combined with Keyword Search                              |
| Autocomplete Suggestion |               | Verba suggests autocompletion                                             |
| Filtering               |               | Apply Filters (e.g. documents, document types etc.) before performing RAG |
| Customizable Metadata   |               | Free control over Metadata                                                |
| Async Ingestion         |               | Ingest data asynchronously to speed up the process                        |
| Advanced Querying       | planned       | Task Delegation Based on LLM Evaluation                                   |
| Reranking               | planned       | Rerank results based on context for improved results                      |
| RAG Evaluation          | planned       | Interface for Evaluating RAG pipelines                                    |
| Agentic RAG             | out of scope  | Agentic RAG pipelines                                                     |
| Graph RAG               | out of scope  | Graph-based RAG pipelines                                                 |

| Chunking Techniques | Implemented | Description                                             |
| ---------------------- | ----------- | ------------------------------------------------------- |
| Token                  |           | Chunk by Token powered by [spaCy](https://spacy.io/)    |
| Sentence               |           | Chunk by Sentence powered by [spaCy](https://spacy.io/) |
| Semantic               |           | Chunk and group by semantic sentence similarity         |
| Recursive              |           | Recursively chunk data based on rules                   |
| HTML                   |           | Chunk HTML files                                        |
| Markdown               |           | Chunk Markdown files                                    |
| Code                   |           | Chunk Code files                                        |
| JSON                   |           | Chunk JSON files                                        |

|  Cool Bonus            | Implemented     | Description                                             |
| ------------------------ | --------------- | ------------------------------------------------------- |
| Docker Support           |               | Verba is deployable via Docker                          |
| Customizable Frontend    |               | Verba's frontend is fully-customizable via the frontend |
| Vector Viewer            |               | Visualize your data in 3D                               |
| Multi-User Collaboration | out of scope  | Multi-User Collaboration in Verba                       |

|  RAG Libraries | Implemented | Description                        |
| ---------------- | ----------- | ---------------------------------- |
| LangChain        |           | Implement LangChain RAG pipelines  |
| Haystack         | planned   | Implement Haystack RAG pipelines   |
| LlamaIndex       | planned   | Implement LlamaIndex RAG pipelines |



---

# Getting Started with Verba

You have three deployment options for Verba:

- Install via pip

```
pip install goldenverba
```

- Build from Source

```
git clone https://github.com/Atheer-Alshahrani/Verba.git

pip install -e .
```

- Use Docker for Deployment

**Prerequisites**: If you're not using Docker, ensure that you have `Python >=3.10.0,<3.13.0` installed on your system.

```
git clone https://github.com/weaviate/Verba

docker compose --env-file <your-env-file> up -d --build
```

If you're unfamiliar with Python and Virtual Environments, please read the [python tutorial guidelines](./PYTHON_TUTORIAL.md).

# API Keys and Environment Variables

You can set all API keys in the Verba frontend, but to make your life easier, we can also prepare a `.env` file in which Verba will automatically look for the keys. Create a `.env` in the same directory you want to start Verba in. You can find an `.env.example` file in the [goldenverba](./goldenverba/.env.example) directory.

> Make sure to only set environment variables you intend to use, environment variables with missing or incorrect values may lead to errors.

Below is a comprehensive list of the API keys and variables you may require:

| Environment Variable   | Value                                                                                  | Description                                                                                                                   |
| ---------------------- | -------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| WEAVIATE_URL_VERBA     | URL to your hosted Weaviate Cluster                                                    | Connect to your [WCS](https://console.weaviate.cloud/) Cluster                                                                |
| WEAVIATE_API_KEY_VERBA | API Credentials to your hosted Weaviate Cluster                                        | Connect to your [WCS](https://console.weaviate.cloud/) Cluster                                                                |
| ANTHROPIC_API_KEY      | Your Anthropic API Key                                                                 | Get Access to [Anthropic](https://www.anthropic.com/) Models                                                                  |
| OPENAI_API_KEY         | Your OpenAI Key                                                                        | Get Access to [OpenAI](https://openai.com/) Models                                                                            |
| OPENAI_EMBED_API_KEY   | Your OpenAI Key                                                                        | Use a different endpoint for embeddings                                                                                       |
| OPENAI_BASE_URL        | URL to OpenAI instance                                                                 | Models                                                                                                                        |
| OPENAI_EMBED_BASE_URL  | URL to OpenAI instance                                                                 | Use a different endpoint for embeddings                                                                                       |
| OPENAI_MODEL           | The name of the model to be used when selecting OpenAI as a Generator                  | Default: the first model in the list returned by the endpoint                                                                 |
| OPENAI_EMBED_MODEL     | The name of the OpenAI embedding model to be used when selecting OpenAI as an Embedder | Default: `text-embedding-3-small`                                                                                             |
| OPENAI_CUSTOM_EMBED    | `true` \| `false`                                                                      | Allow Verba to recognize custom embedding model names (not only OpenAI ones)                                                  |
| COHERE_API_KEY         | Your API Key                                                                           | Get Access to [Cohere](https://cohere.com/) Models                                                                            |
| GROQ_API_KEY           | Your Groq API Key                                                                      | Get Access to [Groq](https://groq.com/) Models                                                                                |
| NOVITA_API_KEY         | Your Novita API Key                                                                    | Get Access to [Novita AI](https://novita.ai?utm_source=github_verba&utm_medium=github_readme&utm_campaign=github_link) Models |
| OLLAMA_URL             | URL to your Ollama instance (e.g. http://localhost:11434 )                             | Get Access to [Ollama](https://ollama.com/) Models                                                                            |
| UNSTRUCTURED_API_KEY   | Your API Key                                                                           | Get Access to [Unstructured](https://docs.unstructured.io/welcome) Data Ingestion                                             |
| UNSTRUCTURED_API_URL   | URL to Unstructured Instance                                                           | Get Access to [Unstructured](https://docs.unstructured.io/welcome) Data Ingestion                                             |
| ASSEMBLYAI_API_KEY     | Your API Key                                                                           | Get Access to [AssemblyAI](https://assemblyai.com) Data Ingestion                                                             |
| GITHUB_TOKEN           | Your GitHub Token                                                                      | Get Access to Data Ingestion via GitHub                                                                                       |
| GITLAB_TOKEN           | Your GitLab Token                                                                      | Get Access to Data Ingestion via GitLab                                                                                       |
| FIRECRAWL_API_KEY      | Your Firecrawl API Key                                                                 | Get Access to Data Ingestion via Firecrawl                                                                                    |
| VOYAGE_API_KEY         | Your VoyageAI API Key                                                                  | Get Access to Embedding Models via VoyageAI                                                                                   |
| EMBEDDING_SERVICE_URL  | URL to your Embedding Service Instance                                                 | Get Access to Embedding Models via [Weaviate Embedding Service](https://weaviate.io/developers/wcs/embeddings)                |
| EMBEDDING_SERVICE_KEY  | Your Embedding Service Key                                                             | Get Access to Embedding Models via [Weaviate Embedding Service](https://weaviate.io/developers/wcs/embeddings)                |
| UPSTAGE_API_KEY        | Your Upstage API Key                                                                   | Get Access to [Upstage](https://upstage.ai/) Models                                                                           |
| UPSTAGE_BASE_URL       | URL to Upstage instance                                                                | Models                                                                                                                        |
| DEFAULT_DEPLOYMENT     | Local, Weaviate, Custom, Docker                                                        | Set the default deployment mode                                                                                               |
| SYSYEM_MESSAGE_PROMPT  | Prompt text value                                                                      | Default value starts with: "You are Verba, a chatbot for..."                                                                  |
| OLLAMA_MODEL           | Your Ollama Model                                                                      | Set the default Ollama model to use                                                                                           |
| OLLAMA_EMBED_MODEL     | Your Ollama Embedding Model                                                            | Set the default Ollama embedding model to use                                                                                 |


## Weaviate

Verba provides flexibility in connecting to Weaviate instances based on your needs. You have three options:

1. **Local Deployment**: Use Weaviate Embedded which runs locally on your device (except Windows, choose the Docker/Cloud Deployment)
2. **Docker Deployment**: Choose this option when you're running Verba's Dockerfile.
3. **Cloud Deployment**: Use an existing Weaviate instance hosted on WCD to run Verba

**💻 Weaviate Embedded**
Embedded Weaviate is a deployment model that runs a Weaviate instance from your application code rather than from a stand-alone Weaviate server installation. When you run Verba in `Local Deployment`, it will setup and manage Embedded Weaviate in the background. Please note that Weaviate Embedded is not supported on Windows and is in Experimental Mode which can bring unexpected errors.

** Weaviate Cloud Deployment (WCD)**

If you prefer a cloud-based solution, Weaviate Cloud (WCD) offers a scalable, managed environment. Learn how to set up a cloud cluster and get the API keys by following the [Weaviate Cluster Setup Guide](https://weaviate.io/developers/wcs/guides/create-instance).

** Docker Deployment**
Another local alternative is deploying Weaviate using Docker. For more details, follow the [How to install Verba with Docker](#how-to-install-verba-with-docker) section.

![Deployment in Verba](https://github.com/weaviate/Verba/blob/2.0.0/img/verba_deployment.png)

** Custom Weaviate Deployment**

If you're hosting Weaviate yourself, you can use the `Custom` deployment option in Verba. This will allow you to specify the URL, PORT, and API key of your Weaviate instance.

## Ollama

Verba supports Ollama models. Download and Install Ollama on your device (https://ollama.com/download). Make sure to install your preferred LLM using `ollama run <model>`.

Tested with `llama3`, `llama3:70b` and `mistral`. The bigger models generally perform better, but need more computational power.

> Make sure Ollama Server runs in the background and that you don't ingest documents with different ollama models since their vector dimension can vary that will lead to errors

You can verify that by running the following command

```
ollama run llama3
```

## Unstructured

Verba supports importing documents through Unstructured IO (e.g plain text, .pdf, .csv, and more). To use them you need the `UNSTRUCTURED_API_KEY` and `UNSTRUCTURED_API_URL` environment variable. You can get it from [Unstructured](https://unstructured.io/)

> UNSTRUCTURED_API_URL is set to `https://api.unstructuredapp.io/general/v0/general` by default

## AssemblyAI

Verba supports importing documents through AssemblyAI (audio files or audio from video files). To use them you need the `ASSEMBLYAI_API_KEY` environment variable. You can get it from [AssemblyAI](https://assemblyai.com)

## OpenAI

Verba supports OpenAI Models such as Ada, GPT3, and GPT4. To use them, you need to specify the `OPENAI_API_KEY` environment variable. You can get it from [OpenAI](https://openai.com/)

You can also add a `OPENAI_BASE_URL` to use proxies such as LiteLLM (https://github.com/BerriAI/litellm)

```
OPENAI_BASE_URL=YOUR-OPENAI_BASE_URL
```

### OpenAI Embeddings

To specify a different endpoint for your embeddings, set the `OPENAI_EMBED_API_KEY` and `OPENAI_EMBED_BASE_URL` environment variables.

If you are using a custom OpenAI Server for embeddings, ensure you set `OPENAI_CUSTOM_EMBED=true`. This will allow Verba to recognize custom embedding model names instead of the default OpenAI embedding model names.

## HuggingFace

If you want to use the HuggingFace Features, make sure to install the correct Verba package. It will install required packages to use the local embedding models.
Please note that on startup, Verba will automatically download and install embedding models when used.

```bash
pip install goldenverba[huggingface]

or

pip install `.[huggingface]`
```

> If you're using Docker, modify the `Dockerfile` accordingly. It's not possible to install a custom Verba installation if you pull the Docker Image from the Docker Hub, as of now, you'd need to install the Docker deployment from the source code and modify the `Dockerfile` beforehand.

## Groq

To use Groq LPUs as generation engine, you need to get an API key from [Groq](https://console.groq.com/keys).

> Although you can provide it in the graphical interface when Verba is up, it is recommended to specify it as `GROQ_API_KEY` environment variable before you launch the application.  
> It will allow you to choose the generation model in an up-to-date available models list.

## Novita

To use Novita AI as generation engine, you need to get an API key from [Novita AI](https://novita.ai/settings/key-management?utm_source=github_verba&utm_medium=github_readme&utm_campaign=github_link).

# How to deploy with pip

`Python >=3.10.0`

1. (Very Important) **Initialize a new Python Environment**

```
python3 -m virtualenv venv
source venv/bin/activate
```

2. **Install Verba**

```
pip install goldenverba
```

3. **Launch Verba**

```
verba start
```

> You can specify the --port and --host via flags

4. **Access Verba**

```
Visit localhost:8000
```

5. (Optional)**Create .env file and add environment variables**

# How to build from Source

1. **Clone the Verba repos**

```
git clone https://github.com/Atheer-Alshahrani/Verba.git
```

2. **Initialize a new Python Environment**

```
python3 -m virtualenv venv
source venv/bin/activate
```

3. **Install Verba**

```
pip install -e .
```

4. **Launch Verba**

```
verba start
```

> You can specify the --port and --host via flags

5. **Access Verba**

```
Visit localhost:8000
```

6. (Optional) **Create .env file and add environment variables**


## Verba Walkthrough

### Select your Deployment

The first screen you'll see is the deployment screen. Here you can select between `Local`, `Docker`, `Weaviate Cloud`, or `Custom` deployment. The `Local` deployment is using Weaviate Embedded under the hood, which initializes a Weaviate instance behind the scenes. The `Docker` deployment is using a separate Weaviate instance that is running inside the same Docker network. The `Weaviate Cloud` deployment is using a Weaviate instance that is hosted on Weaviate Cloud Services (WCS). The `Custom` deployment allows you to specify your own Weaviate instance URL, PORT, and API key.

You can skip this part by setting the `DEFAULT_DEPLOYMENT` environment variable to `Local`, `Docker`, `Weaviate`, or `Custom`.

### Import Your Data

First thing you need to do is to add your data. You can do this by clicking on `Import Data` and selecting either `Add Files`, `Add Directory`, or `Add URL` tab. Here you can add all your files that you want to ingest.
You can then configure every file individually by selecting the file and clicking on `Overview` or `Configure` tab.


### Query Your Data

With Data imported, you can use the `Chat` page to ask any related questions. You will receive relevant chunks that are semantically relevant to your question and an answer generated by your choosen model. You can configure the RAG pipeline under the `Config` tab.


## Open Source Contribution

Your contributions are always welcome! Feel free to contribute ideas, feedback, or create issues and bug reports if you find any! Before contributing, \

### Project Architecture

You can learn more about Verba's architecture and implementation in its [technical documentation](./TECHNICAL.md) and [frontend documentation](./FRONTEND.md). It's recommended to have a look at them before making any contributions.

## Known Issues

- **Weaviate Embeeded** currently not working on Windows yet
  - Will be fixed in future versions, until then please use the Docker or WCS Deployment

