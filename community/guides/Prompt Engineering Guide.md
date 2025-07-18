# brexhq/prompt-engineering

**Tips and tricks for working with Large Language Models like OpenAI's GPT-4.**

**Official Link:** [https://github.com/brexhq/prompt-engineering](https://github.com/brexhq/prompt-engineering)

---

## Brex's Prompt Engineering Guide

This guide was created by Brex for internal purposes. It's based on lessons learned from researching and creating Large Language Model (LLM) prompts for production use cases. It covers the history around LLMs as well as strategies, guidelines, and safety recommendations for working with and building programmatic systems on top of large language models, like OpenAI's GPT-4.

The examples in this document were generated with a non-deterministic language model and the same examples may give you different results.

This is a living document. The state-of-the-art best practices and strategies around LLMs are evolving rapidly every day. Discussion and suggestions for improvements are encouraged.

---

## Table of Contents
- What is a Large Language Model?
  - A Brief, Incomplete, and Somewhat Incorrect History of Language Models
- What is a prompt?
  - Hidden Prompts
  - Tokens
  - Token Limits
  - Prompt Hacking
    - Jailbreaks
    - Leaks
- Why do we need prompt engineering?
  - Give a Bot a Fish
    - Semantic Search
  - Teach a Bot to Fish
    - Command Grammars
    - ReAct
    - GPT-4 vs GPT-3.5
- Strategies
  - Embedding Data
    - Simple Lists
    - Markdown Tables
    - JSON
    - Freeform Text
    - Nested Data
  - Citations
  - Programmatic Consumption
  - Chain of Thought
    - Averaging
    - Interpreting Code
    - Delimiters
  - Fine Tuning
    - Downsides
- Additional Resources

---

## What is a Large Language Model (LLM)?
A large language model is a prediction engine that takes a sequence of words and tries to predict the most likely sequence to come after that sequence. It does this by assigning a probability to likely next sequences and then samples from those to choose one. The process repeats until some stopping criteria is met.

Large language models learn these probabilities by training on large corpuses of text. As language models become more accurate at predicting sequences, many surprising abilities emerge.

### A Brief, Incomplete, and Somewhat Incorrect History of Language Models
- **Pre-2000’s:** N-gram models, limited by state space and sparsity.
- **Mid-2000’s:** Deep neural networks, continuous representations.
- **Early-2010’s:** LSTM networks, improved sequence modeling.
- **Late-2010’s:** Transformers ("Attention Is All You Need"), parallelizable, context window.
- **2020’s:** Generative Pre-Trained models (GPT), few-shot learning, RLHF, ChatGPT, rapid progress.

---

## What is a prompt?
A prompt, sometimes referred to as context, is the text provided to a model before it begins generating output. It guides the model to explore a particular area of what it has learned so that the output is relevant to your goals.

### Hidden Prompts
Hidden prompts are portions of the prompt not intended to be seen by the user, often used to set tone, constraints, and goals. Always assume any content in a hidden prompt can be seen by the user.

### Tokens and Token Limits
Tokens are the atomic unit of consumption for a language model. Token limits are model dependent (e.g., 4,096 for GPT-3, 8,192 or 32,768 for GPT-4). Prompts tend to be append-only, and you must truncate context to allow room for the response.

### Prompt Hacking
- **Jailbreaks:** Bypassing guidelines via clever input.
- **Leaks:** Hidden prompt data can be exposed to the user.

---

## Why do we need prompt engineering?
Prompt engineering is the art of writing prompts to get the language model to do what we want it to do. There are two broad buckets:

### Give a Bot a Fish
Embed all the information the bot needs in the hidden context. Use semantic search to find relevant documents and include them in the prompt.

### Teach a Bot to Fish
Give the bot a list of commands and let it compose programs. Use command grammars, ReAct (reasoning and acting), and provide examples. GPT-4 is more reliable for these scenarios than GPT-3.5.

---

## Strategies
- **Embedding Data:** Use lists, Markdown tables, JSON, freeform text, or nested data as appropriate.
- **Citations:** Ask the model to cite sources, use unique IDs.
- **Programmatic Consumption:** Ask for output in JSON or YAML for easier parsing.
- **Chain of Thought:** Ask the model to show its work for more reliable results. Use delimiters to separate reasoning from the final answer.
- **Fine Tuning:** Use as a last resort; has downsides like cost, overhead, and risk of data leakage.

---

## Additional Resources
- OpenAI Cookbook
- Prompt Hacking
- Dair.ai Prompt Engineering Guide

---

## License
MIT License

---

**Stars:** 9.2k | **Forks:** 480 | **Watchers:** 90 