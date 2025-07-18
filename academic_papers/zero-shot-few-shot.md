# Zero-Shot and Few-Shot Prompting

## Zero-Shot Template

**Role:** Zero-shot task completion
**Context:** Performs tasks without examples, relying on pre-trained knowledge
**Full Prompt:**
> I need to complete this task based on my training and understanding, without any specific examples to guide me.
>
> Task: [INSERT TASK]
>
> Instructions: [Specific instructions for the task]
>
> My approach:
> 1. I'll analyze what the task is asking for
> 2. I'll draw on my relevant knowledge and training
> 3. I'll structure my response appropriately
> 4. I'll provide a complete and accurate answer
>
> Response: [Complete response to the task]
>
> Example:
> Task: Classify the sentiment of this text: 'I think the vacation was okay.'
>
> My approach:
> 1. This is a sentiment classification task
> 2. I need to determine if the sentiment is positive, negative, or neutral
> 3. The word 'okay' suggests a lukewarm, neither positive nor negative sentiment
> 4. I'll classify this as neutral
>
> Response: Neutral

**Use Cases:**
1. Simple classification tasks
2. Straightforward questions
3. Basic reasoning
4. General knowledge queries

**Perplexity / Effectiveness:** Effective for simple tasks, limited performance on complex reasoning

**Sources:**
- Radford et al. (2019) GPT Research: https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf

---

## Few-Shot Template

**Role:** Few-shot learning with examples
**Context:** Uses examples to guide model behavior and establish patterns
**Full Prompt:**
> I'll complete this task by learning from the examples provided and applying the same pattern to the new input.
>
> Task: [INSERT TASK TYPE]
>
> Here are examples of how to complete this task:
>
> Example 1:
> Input: [Example input 1]
> Output: [Example output 1]
>
> Example 2:
> Input: [Example input 2]
> Output: [Example output 2]
>
> Example 3:
> Input: [Example input 3]
> Output: [Example output 3]
>
> Pattern Analysis:
> Based on these examples, I can see that [description of the pattern or rule].
>
> Now I'll apply this pattern to the new input:
>
> New Input: [INSERT NEW INPUT]
> My Analysis: [How I'm applying the learned pattern]
> Output: [New output following the established pattern]
>
> Specific Example for Sentiment Analysis:
>
> Example 1:
> Input: 'This movie was fantastic!'
> Output: Positive
>
> Example 2:
> Input: 'I was disappointed with the service.'
> Output: Negative
>
> Example 3:
> Input: 'The hotel was decent.'
> Output: Neutral
>
> Pattern: I'm classifying emotional expressions - positive words indicate positive sentiment, negative words indicate negative sentiment, and lukewarm words indicate neutral sentiment.
>
> New Input: 'The food was amazing!'
> Output: Positive

**Use Cases:**
1. Pattern recognition tasks
2. Classification problems
3. Structured output generation
4. Domain-specific applications

**Perplexity / Effectiveness:** Significant improvement over zero-shot for structured tasks

**Sources:**
- Brown et al. (2020) Few-Shot Learning Paper: https://arxiv.org/abs/2005.14165 