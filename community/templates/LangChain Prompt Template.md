# LangChain Prompt Template

**Role:** Framework-based prompt management  
**Context:** Structured prompt construction with variable management

---

## Full Prompt
> ```python
> from langchain.prompts import PromptTemplate
>
> # Define the template with variables
> template = '''
> You are a {role} with expertise in {domain}. Your task is to {task_description}.
>
> Context: {context}
>
> Specific requirements:
> - {requirement_1}
> - {requirement_2}
> - {requirement_3}
>
> Input data: {input_data}
>
> Please provide a comprehensive response that addresses all requirements and demonstrates your expertise in {domain}.
>
> Format your response as follows:
> 1. Analysis: [Your analysis of the input]
> 2. Recommendations: [Your specific recommendations]
> 3. Implementation: [How to implement your recommendations]
> 4. Considerations: [Important considerations or caveats]
> '''
>
> # Create the prompt template
> prompt = PromptTemplate(
>     input_variables=['role', 'domain', 'task_description', 'context', 'requirement_1', 'requirement_2', 'requirement_3', 'input_data'],
>     template=template
> )
>
> # Example usage
> formatted_prompt = prompt.format(
>     role='senior data scientist',
>     domain='machine learning',
>     task_description='analyze the provided dataset and recommend the best ML approach',
>     context='This is a classification problem with imbalanced data from a financial services company',
>     requirement_1='Handle class imbalance appropriately',
>     requirement_2='Ensure model interpretability for regulatory compliance',
>     requirement_3='Optimize for both precision and recall',
>     input_data='Customer transaction dataset with 50,000 records, 25 features, 3% positive class'
> )
> ```
>
> Alternative Template for Content Generation:
>
> ```python
> content_template = '''
> You are an expert content creator specializing in {content_type} for {target_audience}.
>
> Topic: {topic}
> Goal: {goal}
> Tone: {tone}
> Length: {length}
>
> Key points to cover:
> {key_points}
>
> Additional context:
> {additional_context}
>
> Please create compelling content that:
> - Engages the {target_audience} audience
> - Maintains a {tone} tone throughout
> - Incorporates all key points naturally
> - Achieves the specified goal: {goal}
> - Meets the length requirement: {length}
>
> Content:
> '''
> ```

---

## Use Cases
- Dynamic prompt generation
- Template-based workflows
- Variable prompt management
- Scalable prompt engineering

---

**Effectiveness:** Enables systematic and scalable prompt engineering practices  
**Source:** LangChain Documentation [25][26] 