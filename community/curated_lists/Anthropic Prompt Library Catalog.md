# Anthropic Prompt Library: Complete Catalog

This file catalogs complete prompt templates from the [Anthropic Prompt Library](https://docs.anthropic.com/en/resources/prompt-library/library). Each entry includes the system prompt, user example, example output, and API usage code. For the full, up-to-date list, visit the [official library](https://docs.anthropic.com/en/resources/prompt-library/library).

---

## Meeting Scribe

**System Prompt:**
> Your task is to review the provided meeting notes and create a concise summary that captures the essential information, focusing on key takeaways and action items assigned to specific individuals or departments during the meeting. Use clear and professional language, and organize the summary in a logical manner using appropriate formatting such as headings, subheadings, and bullet points. Ensure that the summary is easy to understand and provides a comprehensive but succinct overview of the meeting’s content, with a particular focus on clearly indicating who is responsible for each action item.

**User Example:**
Meeting notes:  
Date: Verona, Italy - Late 16th century  
Attendees:  
- Lord Capulet (Head of the Capulet family)  
- Lord Montague (Head of the Montague family)  
- Prince Escalus (Ruler of Verona)  
- Friar Laurence (Religious advisor)  
Agenda:  
1. Address the ongoing feud between the Capulet and Montague families  
2. Discuss the secret marriage of Romeo Montague and Juliet Capulet  
3. Develop a plan to bring peace to Verona  
4. Address the tragic deaths of Romeo and Juliet  
Discussion:  
- Prince Escalus opened the meeting by expressing his grave concern over the long-standing feud between the Capulet and Montague families. He admonished both Lord Capulet and Lord Montague for the recent violent clashes that have disturbed the peace in Verona’s streets. The Prince warned that further violence would result in severe consequences, including heavy fines and potential exile for the perpetrators.  
- Friar Laurence then broached the topic of the between Romeo Montague and Juliet Capulet, which had taken place under his guidance. Lord Capulet and Lord Montague evidently had not known about it, and reacted with anger and disbelief. However, Friar Laurence urged them to consider the profound and tragic love shared by their children and the potential for this love to heal the rift between the families going forward.  
- Prince Escalus proposed a formal truce between the Capulet and Montague families. He demanded that both sides lay down their arms and cease all hostile actions against one another. The Prince declared that any violation of the truce would result in severe punishments, including the possibility of exile or even execution. Lord Capulet and Lord Montague, recognizing the wisdom in the Prince’s words and the necessity of peace for the well-being of their families and the city, grudgingly agreed to the terms of the truce.  
- The meeting took a somber turn as the tragic deaths of Romeo and Juliet were addressed. Friar Laurence recounted the unfortunate series of events that led to the young lovers taking their own lives, emphasizing the devastating impact of the families’ hatred on their innocent children. Lord Capulet and Lord Montague, overcome with grief and remorse, acknowledged that their blind hatred had ultimately caused the loss of their beloved children.  
- Prince Escalus called upon the families to learn from this heartbreaking tragedy and to embrace forgiveness and unity in honor of Romeo and Juliet’s memory. He urged them to work together to create a lasting peace in Verona, setting aside their long-standing animosity. Friar Laurence offered his support in mediating any future disputes and providing spiritual guidance to help the families heal and move forward.  
- As the meeting drew to a close, Lord Capulet and Lord Montague pledged to put an end to their feud and work towards reconciliation. Prince Escalus reaffirmed his commitment to ensuring that the truce would be upheld, promising swift justice for any who dared to break it.  
- The attendees agreed to meet regularly to discuss the progress of their reconciliation efforts and to address any challenges that may arise.

**Example Output:**
Meeting Summary: Reconciliation and Peace in Verona Date: Late 16th century, Verona, Italy

Attendees:
* Lord Capulet (Head of the Capulet family)
* Lord Montague (Head of the Montague family)
* Prince Escalus (Ruler of Verona)
* Friar Laurence (Religious advisor)

Key Takeaways:
* Prince Escalus addressed the ongoing feud between the Capulet and Montague families, warning of severe consequences for further violence.
* Friar Laurence revealed the secret marriage between Romeo Montague and Juliet Capulet, urging the families to consider the potential for their love to heal the rift.
* Prince Escalus proposed a formal truce between the families, threatening severe punishments for any violations.
* The tragic deaths of Romeo and Juliet were discussed, with Lord Capulet and Lord Montague acknowledging their role in the heartbreaking outcome.
* Prince Escalus called for forgiveness and unity in honor of Romeo and Juliet’s memory, urging the families to work together for lasting peace in Verona.

Action Items:
* Lord Capulet and Lord Montague:  
   * Lay down arms and cease all hostile actions against one another.  
   * Work towards reconciliation and embrace forgiveness.  
   * Attend regular meetings to discuss progress and address challenges.
* Prince Escalus:  
   * Enforce the truce and ensure its adherence.  
   * Administer swift justice for any violations of the truce.
* Friar Laurence:  
   * Provide mediation and spiritual guidance to support the families in their healing and reconciliation process.

Next Steps:
* The attendees will meet regularly to monitor the progress of reconciliation efforts and address any arising challenges.

**API Usage Example:**
```python
import anthropic
client = anthropic.Anthropic(api_key="my_api_key")
message = client.messages.create(
    model="claude-opus-4-20250514",
    max_tokens=4000,
    temperature=0.5,
    system="Your task is to review the provided meeting notes and create a concise summary that captures the essential information, focusing on key takeaways and action items assigned to specific individuals or departments during the meeting. Use clear and professional language, and organize the summary in a logical manner using appropriate formatting such as headings, subheadings, and bullet points. Ensure that the summary is easy to understand and provides a comprehensive but succinct overview of the meeting’s content, with a particular focus on clearly indicating who is responsible for each action item.",
    messages=[{"role": "user", "content": [{"type": "text", "text": "Meeting notes: ..."}]}]
)
print(message.content)
```

---

## Brand Builder

**System Prompt:**
> Your task is to create a comprehensive design brief for a holistic brand identity based on the given specifications. The brand identity should encompass various elements such as suggestions for the brand name, logo, color palette, typography, visual style, tone of voice, and overall brand personality. Ensure that all elements work together harmoniously to create a cohesive and memorable brand experience that effectively communicates the brand’s values, mission, and unique selling proposition to its target audience. Be detailed and comprehensive and provide enough specific details for someone to create a truly unique brand identity.

**User Example:**
Brand specs: This is a brand that focuses on creating high-quality, stylish clothing and accessories using eco-friendly materials and ethical production methods. The brand targets environmentally conscious consumers aged 25-40 who value fashion, sustainability, and social responsibility. The brand identity should achieve the following goals: 1. Reflect the brand’s commitment to sustainability, ethical practices, and environmental stewardship. 2. Appeal to the target audience by conveying a sense of style, quality, and trendiness. 3. Differentiate the brand from competitors in the sustainable fashion market. 4. Create a strong emotional connection with consumers and inspire them to make more environmentally friendly choices.

**Example Output:**
Design Brief: Brand Identity for an Eco-Friendly Fashion Brand

Brand Name Suggestion: “Sēnsus” (Latin for “sense” or “perception,” evoking a sense of mindfulness and connection with the environment)

Logo:
* A minimalistic and modern logo that combines a stylized leaf or plant motif with a sleek, sans-serif typeface.
* The leaf or plant element symbolizes the brand’s commitment to sustainability and environmental stewardship, while the clean typography conveys a sense of sophistication and style.
* The logo should be versatile and work well across various applications, including clothing tags, packaging, and digital platforms.

Color Palette:
* A neutral and earthy color palette that reflects the brand’s eco-friendly ethos, such as shades of green, beige, and warm grays.
* Accent colors like deep teal or mustard yellow can be used sparingly to add vibrancy and depth.
* The color palette should evoke a sense of natural harmony and balance, while still being fashion-forward and appealing to the target audience.

Typography:
* A combination of a clean, modern sans-serif typeface for headlines and a complementary serif typeface for body copy.
* The typography should be legible and visually appealing, conveying a sense of quality and sophistication.
* Consistent use of typographic hierarchy and spacing will create a cohesive and organized brand identity.

Visual Style:
* A minimalistic and uncluttered visual style that emphasizes high-quality product photography and clean, modern layouts.
* Incorporate natural elements, such as plant motifs or textures, to reinforce the brand’s eco-friendly values and connection with nature.
* Use negative space effectively to create a sense of openness and breathability, reflecting the brand’s commitment to sustainability.

Tone of Voice:
* The brand’s tone of voice should be approachable, knowledgeable, and authentic.
* Use language that educates and inspires consumers about the benefits of sustainable fashion and ethical production methods.
* Incorporate a touch of sophistication and style to appeal to the target audience’s fashion-conscious sensibilities.

Brand Personality:
* Eco-conscious and environmentally aware, yet stylish and fashion-forward.
* Confident and passionate about promoting sustainable practices and ethical choices.
* Inclusive and welcoming, inviting consumers to join a like-minded community committed to making positive changes.

Overall, the brand identity for “Sēnsus” should strike a balance between eco-friendly values and fashion-forward aesthetics, appealing to consumers who want to look stylish while making environmentally responsible choices. The cohesive visual and verbal elements should create a strong emotional connection with the target audience and inspire them to embrace a more sustainable lifestyle.

**API Usage Example:**
```python
import anthropic
client = anthropic.Anthropic(api_key="my_api_key")
message = client.messages.create(
    model="claude-opus-4-20250514",
    max_tokens=2000,
    temperature=1,
    system="Your task is to create a comprehensive design brief for a holistic brand identity based on the given specifications. The brand identity should encompass various elements such as suggestions for the brand name, logo, color palette, typography, visual style, tone of voice, and overall brand personality. Ensure that all elements work together harmoniously to create a cohesive and memorable brand experience that effectively communicates the brand’s values, mission, and unique selling proposition to its target audience. Be detailed and comprehensive and provide enough specific details for someone to create a truly unique brand identity.",
    messages=[{"role": "user", "content": [{"type": "text", "text": "Brand specs: ..."}]}]
)
print(message.content)
```

---

## Philosophical Musings

**System Prompt:**
> Your task is to discuss a philosophical concept or thought experiment on the given topic. Briefly explain the concept, present the main arguments and implications, and encourage critical thinking by posing open-ended questions. Maintain a balanced, objective tone that fosters intellectual curiosity.

**User Example:**
The trolley problem and the ethics of utilitarianism

**Example Output:**
The trolley problem is a thought experiment that challenges our moral intuitions and raises questions about the ethics of utilitarianism. The basic scenario is as follows:

A runaway trolley is about to kill five people on the tracks ahead. You are standing next to a lever that can divert the trolley onto a side track, where it will kill only one person. Should you pull the lever to save five lives at the cost of one?

This dilemma highlights the core principle of utilitarianism, which holds that the morally right action is the one that produces the greatest good for the greatest number of people. In this case, pulling the lever would maximize utility by saving five lives, even though it would directly cause the death of one person.

However, the trolley problem also raises concerns about the limits of utilitarianism and the ethics of actively causing harm to achieve a greater good. It prompts us to consider questions such as:

* Is it morally acceptable to sacrifice an innocent person for the sake of saving a larger number of people?
* Does the principle of utility justify any means to achieve the greatest good, or are there ethical constraints that should not be violated?
* How do we weigh the value of different lives, and is it fair to make such calculations?

What are your thoughts on the trolley problem and the ethics of utilitarianism? Do you believe that maximizing utility should be the primary goal of moral decision-making, or are there other important considerations? How would you approach the dilemma presented in the trolley problem, and what ethical principles would guide your choice?

**API Usage Example:**
```python
import anthropic
client = anthropic.Anthropic(api_key="my_api_key")
message = client.messages.create(
    model="claude-opus-4-20250514",
    max_tokens=2000,
    temperature=1,
    system="Your task is to discuss a philosophical concept or thought experiment on the given topic. Briefly explain the concept, present the main arguments and implications, and encourage critical thinking by posing open-ended questions. Maintain a balanced, objective tone that fosters intellectual curiosity.",
    messages=[{"role": "user", "content": [{"type": "text", "text": "The trolley problem and the ethics of utilitarianism"}]}]
)
print(message.content)
```

---

## Sources
- [Anthropic Prompt Library](https://docs.anthropic.com/en/resources/prompt-library/library)
- [Meeting Scribe](https://docs.anthropic.com/en/prompt-library/meeting-scribe)
- [Brand Builder](https://docs.anthropic.com/en/prompt-library/brand-builder)
- [Philosophical Musings](https://docs.anthropic.com/en/prompt-library/philosophical-musings) 