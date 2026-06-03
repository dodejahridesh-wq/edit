---
name: huggingface-api
description: >
  Access and download pre-trained AI models, datasets, and pipelines.
---

# Hugging Face API

## Overview
Hugging Face is a platform and community hub for machine learning and AI models, providing tools to build, train, and deploy models, particularly transformers for Natural Language Processing (NLP), vision, and audio tasks.

## Programmatic Usage
```python
from transformers import pipeline

# Load a sentiment analysis pipeline
classifier = pipeline("sentiment-analysis")
result = classifier("I love using AI-powered OS skills!")
print(result)
```

## REST API Endpoints
Hugging Face Hub exposes REST APIs to fetch repository information and run serverless inference.
- **Inference API**: `POST https://api-inference.huggingface.co/models/{model_id}`
- **Fetch Model Info**: `GET https://huggingface.co/api/models/{model_id}`
