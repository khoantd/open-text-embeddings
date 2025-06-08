# Open Text Embeddings Project Structure

## Overview
This project appears to be a text embeddings service that provides embedding functionality through various interfaces (server, AWS, Modal).

## Directory Structure

```
open-text-embeddings/
├── open/
│   └── text/
│       └── embeddings/
│           ├── server/           # Server implementation
│           │   ├── app.py        # Main FastAPI application
│           │   ├── aws.py        # AWS-specific functionality
│           │   ├── gzip.py       # Compression utilities
│           │   ├── modal.py      # Modal cloud integration
│           │   └── __main__.py   # Server entry point
│           └── openai.py         # OpenAI embeddings implementation
├── server-requirements.txt       # Server dependencies
├── test-requirements.txt         # Testing dependencies
├── setup.py                      # Package setup configuration
├── Dockerfile                    # Container configuration
└── serverless.yml               # Serverless deployment config
```

## Key Components

### Server Implementation (`open/text/embeddings/server/`)
- `app.py`: Main FastAPI application that handles embedding requests
- `aws.py`: AWS-specific functionality for cloud deployment
- `gzip.py`: Compression utilities for handling large text data
- `modal.py`: Integration with Modal cloud platform
- `__main__.py`: Entry point for running the server

### Embeddings Implementation
- `openai.py`: Implementation of OpenAI embeddings functionality

### Configuration Files
- `server-requirements.txt`: Core dependencies for the server
  - fastapi
  - mangum
  - sentence_transformers==2.2.2
  - langchain==0.1.6
  - InstructorEmbedding==1.0.1
  - uvicorn

- `test-requirements.txt`: Dependencies for testing

### Deployment
- `Dockerfile`: Container configuration for deployment
- `serverless.yml`: Serverless deployment configuration

## Dependencies
The project relies on several key packages:
- FastAPI for the web server
- sentence_transformers for text embeddings
- langchain for AI/ML functionality
- InstructorEmbedding for embedding models
- uvicorn as the ASGI server

## Note
There was a recent issue with dependency versions, specifically around huggingface_hub and sentence_transformers compatibility. This should be considered when updating dependencies. 