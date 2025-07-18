# Generated Knowledge Prompting (Liu et al., 2022)

**Role:** Knowledge generation before task completion
**Context:** Generates relevant knowledge first, then uses it to solve the main task
**Full Prompt:**
> I'll solve this problem by first generating relevant knowledge, then using that knowledge to provide a comprehensive answer.
>
> Task: [INSERT TASK]
>
> Step 1: Generate Relevant Knowledge
> Let me think about what I know about this topic:
>
> Knowledge Point 1: [Relevant fact or concept]
> Knowledge Point 2: [Relevant fact or concept]
> Knowledge Point 3: [Relevant fact or concept]
> Knowledge Point 4: [Relevant fact or concept]
> Knowledge Point 5: [Relevant fact or concept]
>
> Step 2: Integrate Knowledge with Task
> Now I'll use this knowledge to address the task:
>
> Analysis: [How the generated knowledge applies to the task]
>
> Application: [Using the knowledge to solve the problem]
>
> Step 3: Final Answer
> Based on the knowledge I generated and its application to this task: [Complete answer that integrates the generated knowledge]
>
> Example:
> Task: Explain why golf scoring works the way it does.
>
> Generated Knowledge:
> - Golf originated in Scotland in the 15th century
> - The objective is to complete each hole in as few strokes as possible
> - Par represents the expected number of strokes for a skilled golfer
> - Lower scores indicate better performance
> - The total score is cumulative across all holes
>
> Final Answer: Golf scoring works on a 'lower is better' principle because the objective is efficiency - completing each hole in the fewest strokes possible. This makes golf unique among sports where typically higher scores indicate better performance.

**Use Cases:**
1. Educational explanations
2. Complex topic analysis
3. Research-based responses
4. Comprehensive problem solving

**Perplexity / Effectiveness:** Significant improvement on knowledge-intensive tasks

**Sources:**
- Liu et al. (2022) Generated Knowledge Paper: https://arxiv.org/abs/2210.02435 