# langfuse/langfuse

**Open-source observability and analytics for LLM applications**

**Official Link:** [https://github.com/langfuse/langfuse](https://github.com/langfuse/langfuse)

---

## Overview

Langfuse is an open-source platform that provides observability, analytics, and monitoring for applications built with large language models (LLMs). It helps developers track, analyze, and optimize LLM usage and performance in production environments.

---

## Features
- **Tracing and Analytics:** End-to-end tracing of LLM calls, including prompt, response, latency, and cost.
- **Session and User Monitoring:** Track user sessions, activity, and errors for debugging and improvement.
- **Integrations:** Works with OpenAI, LangChain, LlamaIndex, and more.
- **SDKs:** Available for Python, Node.js, and other languages.
- **Self-hosted or Cloud:** Deploy on your own infrastructure or use Langfuse Cloud.
- **Advanced Querying:** Search, filter, and analyze traces and observations.
- **Error and Exception Tracking:** Identify and debug issues in LLM pipelines.
- **Caching and Performance:** Efficient caching and LRU management for large-scale applications.

---

## Installation

### Python SDK
```bash
pip install langfuse
```

- [Python SDK Docs](https://langfuse.com/docs/sdk/python)
- [Decorators](https://langfuse.com/docs/sdk/python/decorators)
- [Low-level SDK](https://langfuse.com/docs/sdk/python/low-level-sdk)
- [Langchain integration](https://langfuse.com/docs/integrations/langchain/tracing)

### Node.js SDK
```bash
npm i langfuse-node
# or
yarn add langfuse-node
# or
pnpm i langfuse-node
```
- [TypeScript SDK Docs](https://langfuse.com/docs/sdk/typescript)
- [Reference](https://js.reference.langfuse.com/modules/langfuse_node.html)

---

## Usage

### Python Example
```python
from langfuse import Langfuse

langfuse = Langfuse(public_key="YOUR_KEY", secret_key="YOUR_SECRET", host="https://cloud.langfuse.com")

@langfuse.observe()
def my_function():
    # Your LLM call here
    pass
```

### Node.js Example
```javascript
const { Langfuse } = require('langfuse-node');
const langfuse = new Langfuse({ publicKey: 'YOUR_KEY', secretKey: 'YOUR_SECRET', host: 'https://cloud.langfuse.com' });

// Use with your LLM pipeline
```

---

## Integrations
- **OpenAI SDK**
- **LangChain**
- **LlamaIndex**
- **Custom LLMs**

See [Integrations Documentation](https://langfuse.com/docs/integrations)

---

## Advanced
- **Session and Trace Management:** Fetch, filter, and analyze traces by user, session, or error type.
- **Exception and Error Tracking:** Find and debug exceptions in LLM pipelines.
- **Output Modes:** Compact, full JSON string, or file output for trace data.
- **Cache Management:** LRU cache with configurable size and automatic eviction.

---

## Deployment
- **Self-hosted:** Deploy using Docker, AWS, Azure, or other cloud providers.
- **Cloud:** Use [Langfuse Cloud](https://cloud.langfuse.com) for managed hosting.
- **Azure Deployment:** See [langfuse-azure](https://github.com/pamelafox/langfuse-azure)
- **AWS CDK Deployment:** See [langfuse-ecr-ecs-deployment-cdk](https://github.com/AI4Organization/langfuse-ecr-ecs-deployment-cdk)

---

## Documentation
- [Official Docs](https://langfuse.com/docs)
- [API Reference](https://js.reference.langfuse.com/)
- [Python SDK](https://langfuse.com/docs/sdk/python)
- [TypeScript SDK](https://langfuse.com/docs/sdk/typescript)

---

## License
MIT License

---

**Stars:** See GitHub for latest | **Watchers:** See GitHub for latest | **Forks:** See GitHub for latest 