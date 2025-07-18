# Tree of Thoughts Prompting (Yao et al., 2023)

**Role:** Tree-structured reasoning with evaluation and backtracking
**Context:** Explores multiple reasoning branches with systematic evaluation
**Full Prompt:**
> I need to solve this problem using a tree of thoughts approach. I'll explore multiple reasoning paths, evaluate each branch, and backtrack when necessary.
>
> Problem: [INSERT PROBLEM]
>
> Step 1: Generate Initial Thoughts (Branches)
> Thought A: [First possible approach]
> Thought B: [Second possible approach]
> Thought C: [Third possible approach]
>
> Step 2: Evaluate Each Thought
> Evaluation of Thought A:
> - Strengths: [What makes this approach promising]
> - Weaknesses: [Potential issues or limitations]
> - Likelihood of success: [High/Medium/Low]
>
> Evaluation of Thought B:
> - Strengths: [What makes this approach promising]
> - Weaknesses: [Potential issues or limitations]
> - Likelihood of success: [High/Medium/Low]
>
> Evaluation of Thought C:
> - Strengths: [What makes this approach promising]
> - Weaknesses: [Potential issues or limitations]
> - Likelihood of success: [High/Medium/Low]
>
> Step 3: Select Best Path and Expand
> Based on evaluation, I'll pursue [Selected thought] because [reasoning].
>
> Expanding on [Selected thought]:
> Sub-step 3.1: [Detailed next step]
> Sub-step 3.2: [Detailed next step]
> Sub-step 3.3: [Detailed next step]
>
> Step 4: Evaluate Progress and Backtrack if Needed
> [Assessment of current path and decision to continue or backtrack]
>
> Step 5: Final Solution
> [Complete solution with reasoning]

**Use Cases:**
1. Complex planning problems
2. Creative writing
3. Game strategy
4. Multi-step decision making

**Perplexity / Effectiveness:** Superior performance on tasks requiring exploration and strategic lookahead

**Sources:**
- Yao et al. (2023) Tree of Thoughts Paper: https://arxiv.org/abs/2305.10601
- https://dev.to/zerotomastery/beginners-guide-to-tree-of-thoughts-prompting-with-examples-4op6 