# ReAct Prompting (Yao et al., 2022)

**Role:** Reasoning + Action prompting
**Context:** Combines reasoning with concrete actions for problem-solving
**Full Prompt:**
> I'll solve this problem using ReAct (Reasoning + Action) approach, where I think through each step and then take concrete actions.
>
> Question: [INSERT QUESTION]
>
> Thought 1: I need to understand what information is required to answer this question and what actions I can take.
> Action 1: [Specific action I will take - e.g., search for information, analyze data, calculate something]
> Observation 1: [What I learned from taking this action]
>
> Thought 2: Based on my observation, I now understand [insight]. My next step should be [reasoning for next action].
> Action 2: [Next specific action]
> Observation 2: [What I learned from this action]
>
> Thought 3: Now I have [summarize what I know]. I need to [reasoning for next step].
> Action 3: [Next action]
> Observation 3: [Result of this action]
>
> Thought 4: I can now [reasoning] because [evidence from observations].
> Action 4: [Final action - formulate answer]
> Observation 4: [Final result]
>
> Final Answer: Based on my reasoning and actions, the answer is [complete answer with justification].

**Use Cases:**
1. Information retrieval tasks
2. Multi-step problem solving
3. Research questions
4. Agent-based reasoning

**Perplexity / Effectiveness:** Reduces hallucinations and improves accuracy on knowledge-intensive tasks

**Sources:**
- Yao et al. (2022) ReAct Paper: https://arxiv.org/abs/2210.03629
- https://www.promptingguide.ai/techniques/react 