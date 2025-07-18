# Chain-of-Thought Prompting (Wei et al., 2022)

**Role:** Chain-of-thought reasoning
**Context:** Enables step-by-step reasoning for complex mathematical and logical problems
**Full Prompt:**
> I want you to solve this problem step by step, showing your reasoning at each stage. Think through the problem methodically and explain your thought process.
>
> Example 1:
> Q: Roger has 5 tennis balls. He buys 2 more cans of tennis balls. Each can has 3 tennis balls. How many tennis balls does he have now?
> A: Let me think through this step by step.
> - Roger started with 5 tennis balls
> - He bought 2 cans of tennis balls
> - Each can contains 3 tennis balls
> - So he got 2 × 3 = 6 additional tennis balls
> - Total tennis balls = 5 + 6 = 11
> The answer is 11.
>
> Example 2:
> Q: The cafeteria had 23 apples. If they used 20 to make lunch and bought 6 more, how many apples do they have?
> A: Let me work through this step by step.
> - The cafeteria started with 23 apples
> - They used 20 apples to make lunch
> - After making lunch, they had 23 - 20 = 3 apples left
> - They bought 6 more apples
> - Total apples now = 3 + 6 = 9
> The answer is 9.
>
> Now solve this problem: [INSERT PROBLEM]

**Use Cases:**
1. Mathematical problem solving
2. Logical reasoning tasks
3. Complex analysis
4. Educational explanations

**Perplexity / Effectiveness:** Significant improvement on GSM8K benchmark, outperforming fine-tuned models

**Sources:**
- Wei et al. (2022) Chain-of-Thought Paper: https://arxiv.org/abs/2201.11903
- https://www.geeksforgeeks.org/artificial-intelligence/tree-of-thought-tot-prompting/ 