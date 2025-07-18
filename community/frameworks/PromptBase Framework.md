# microsoft/promptbase

**All things prompt engineering**

**Official Link:** [https://github.com/microsoft/promptbase](https://github.com/microsoft/promptbase)

---

## Overview
`promptbase` is an evolving collection of resources, best practices, and example scripts for eliciting the best performance from foundation models like GPT-4. It currently hosts scripts demonstrating the Medprompt methodology, including examples of how these prompting techniques ("Medprompt+") extend into non-medical domains.

---

## Features
- Medprompt methodology for high-performance prompting
- Dynamic few-shot selection
- Self-generated chain of thought (CoT)
- Majority vote ensembling and choice-shuffle ensembling
- Case studies and structured interviews on prompt engineering
- Specialized deep dives into prompt engineering tooling
- Example scripts for benchmarks: MMLU, GSM8K, MATH, HumanEval, BIG-Bench-Hard, DROP

---

## Medprompt and The Power of Prompting
Medprompt composes three distinct strategies:
- **Dynamic Few Shots:** Selects k training examples most similar to the test input using embedding-based k-NN.
- **Self-Generated Chain of Thought (CoT):** Uses LLMs to generate reasoning steps for training examples, improving complex reasoning.
- **Majority Vote Ensembling:** Combines outputs from multiple prompts or varied temperature runs, using choice-shuffling for robustness.

This approach led to breakthrough performance in medical and general benchmarks, often matching or exceeding specialist-tuned models.

---

## Medprompt+ | Extending the Power of Prompting
Medprompt+ extends the Medprompt framework to general knowledge and reasoning benchmarks (e.g., MMLU). It uses a portfolio approach, dynamically selecting between chain-of-thought and direct few-shot prompts based on the question type, further boosting performance.

---

## Running Scripts
1. Clone the repo and install the promptbase package:
   ```bash
   cd src
   pip install -e .
   ```
2. Download datasets (see repo for links) and place them in `src/promptbase/datasets`.
3. Run a test, e.g.:
   ```bash
   python -m promptbase gsm8k
   ```

---

## Dataset Links
- MMLU: https://github.com/hendrycks/test
- HumanEval: https://huggingface.co/datasets/openai_humaneval
- DROP: https://allenai.org/data/drop
- GSM8K: https://github.com/openai/grade-school-math
- MATH: https://huggingface.co/datasets/hendrycks/competition_math
- Big-Bench-Hard: https://github.com/suzgunmirac/BIG-Bench-Hard

---

## Other Resources
- [Medprompt Blog](https://www.microsoft.com/en-us/research/blog/the-power-of-prompting/)
- [Medprompt Research Paper](https://arxiv.org/abs/2311.16452)
- [Medprompt+ Blog](https://www.microsoft.com/en-us/research/blog/steering-at-the-frontier-extending-the-power-of-prompting/)
- [Microsoft Introduction to Prompt Engineering](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/prompt-engineering)
- [Microsoft Advanced Prompt Engineering Guide](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/advanced-prompt-engineering?pivots=programming-language-chat-completions)

---

## License
MIT License

---

**Stars:** 5.6k | **Forks:** 318 | **Watchers:** 58 