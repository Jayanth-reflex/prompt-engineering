# Hugging Face Prompt Template Framework

**Role:** Systematic prompt construction framework  
**Context:** Structured approach to prompt engineering with consistent formatting

---

## Full Prompt
> Template Structure:
>
> ## Context
> [Provide background information and context for the task]
>
> ## Instruction
> [Clear, specific instruction for what needs to be accomplished]
>
> ## Input
> [The specific input data or content to be processed]
>
> ## Format Requirements
> [Specific formatting requirements for the output]
>
> ## Examples
> [Provide 2-3 relevant examples if this is a few-shot prompt]
>
> ## Additional Guidelines
> [Any additional constraints, preferences, or requirements]
>
> ## Output
> [Space for the model's response]
>
> Complete Example:
>
> ## Context
> You are a technical documentation expert helping to create clear, comprehensive API documentation for developers.
>
> ## Instruction
> Transform the provided API endpoint information into well-structured documentation that includes description, parameters, example requests, and response formats.
>
> ## Input
> Endpoint: POST /api/users
> Creates a new user account
> Parameters: name (string, required), email (string, required), role (string, optional, default: 'user')
> Returns: user object with id, created timestamp
>
> ## Format Requirements
> - Use markdown formatting
> - Include code blocks for examples
> - Organize with clear headers
> - Include both successful and error response examples
>
> ## Examples
> [Include similar API documentation examples]
>
> ## Additional Guidelines
> - Use clear, concise language
> - Include security considerations
> - Provide realistic example values
> - Follow REST API documentation best practices
>
> ## Output
> [Generated documentation]

---

## Use Cases
- Systematic prompt design
- Template reuse and consistency
- Complex task structuring
- Documentation generation

---

**Effectiveness:** Improved consistency and quality across prompt applications  
**Source:** Hugging Face Transformers Documentation [23][25] 