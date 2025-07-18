# Self-Consistency Prompting (Wang et al., 2022)

**Role:** Multiple reasoning paths with consistency checking
**Context:** Generates multiple solutions and selects the most consistent answer
**Full Prompt:**
> I'm going to solve this problem multiple ways to ensure I get the correct answer. I'll show different reasoning paths and then identify the most consistent solution.
>
> Problem: When I was 6 my sister was half my age. Now I'm 70, how old is my sister?
>
> Solution Path 1:
> - When I was 6, my sister was half my age, so she was 3 years old
> - The age difference between us is 6 - 3 = 3 years
> - This age difference never changes
> - Now I'm 70, so my sister is 70 - 3 = 67 years old
>
> Solution Path 2:
> - When I was 6, my sister was 3 (half my age)
> - My sister is 3 years younger than me
> - If I'm currently 70, then my sister is 70 - 3 = 67 years old
>
> Solution Path 3:
> - At age 6, the age gap was 6 - 3 = 3 years
> - Age gaps remain constant throughout life
> - Current age of sister = 70 - 3 = 67 years old
>
> All paths lead to the same answer: 67 years old.
>
> Now solve this problem using multiple reasoning paths: [INSERT PROBLEM]

**Use Cases:**
1. Complex arithmetic problems
2. Logic puzzles
3. Mathematical verification
4. Critical reasoning tasks

**Perplexity / Effectiveness:** +17.9% improvement on GSM8K, +11.0% on SVAMP, +12.2% on AQuA

**Sources:**
- Wang et al. (2022) Self-Consistency Paper: https://arxiv.org/abs/2203.11171
- https://www.geeksforgeeks.org/self-consistency-prompting/ 