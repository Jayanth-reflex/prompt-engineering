# BoundaryML/baml

**The AI framework that adds the engineering to prompt engineering (Python/TS/Ruby/Java/C#/Rust/Go compatible)**

**Official Link:** [https://github.com/BoundaryML/baml](https://github.com/BoundaryML/baml)

---

## BAML: Basically a Made-up Language

BAML is a simple prompting language for building reliable **AI workflows and agents**. It makes prompt engineering easy by turning it into _schema engineering_—where you mostly focus on the models of your prompt to get more reliable outputs. You don't need to write your whole app in BAML, only the prompts! You can wire-up your LLM Functions in any language of your choice. See quickstarts for Python, TypeScript, Ruby, Go, and more.

BAML comes with all batteries included—full typesafety, streaming, retries, wide model support, even when they don't support native tool-calling APIs.

**Try BAML:** [Prompt Fiddle](https://promptfiddle.com) • [Interactive App Examples](https://baml-examples.vercel.app)

---

## The core BAML principle: LLM Prompts are functions

The fundamental building block in BAML is a function. Every prompt is a function that takes in parameters and returns a type.

```baml
function ChatAgent(message: Message[], tone: "happy" | "sad") -> string
```

Every function additionally defines which models it uses and what its prompt is.

```baml
function ChatAgent(message: Message[], tone: "happy" | "sad") -> StopTool | ReplyTool {
    client "openai/gpt-4o-mini"

    prompt #"
        Be a {{ tone }} bot.

        {{ ctx.output_format }}

        {% for m in message %}
        {{ _.role(m.role) }}
        {{ m.content }}
        {% endfor %}
    "#
}

class Message {
    role string
    content string
}

class ReplyTool {
  response string
}

class StopTool {
  action "stop" @description(#"
    when it might be a good time to end the conversation
  "#)
}
```

---

## BAML Functions can be called from any language

Below we call the ChatAgent function we defined in BAML through Python. BAML's Rust compiler generates a "baml_client" to access and call them.

```python
from baml_client import b
from baml_client.types import Message, StopTool

messages = [Message(role="assistant", content="How can I help?")]

while True:
  print(messages[-1].content)
  user_reply = input()
  messages.append(Message(role="user", content=user_reply))
  tool = b.ChatAgent(messages, "happy")
  if isinstance(tool, StopTool):
    print("Goodbye!")
    break
  else:
    messages.append(Message(role="assistant", content=tool.response))
```

You can write any kind of agent or workflow using chained BAML functions. An agent is a while loop that calls a Chat BAML Function with some state.

And if you need to stream, add a couple more lines:

```python
stream = b.stream.ChatAgent(messages, "happy")
# partial is a Partial type with all Optional fields
for tool in stream:
    if isinstance(tool, StopTool):
      ...
    
final = stream.get_final_response()
```

And get fully type-safe outputs for each chunk in the stream.

---

## Test prompts 10x faster, right in your IDE

BAML comes with native tooling for VSCode (jetbrains + neovim coming soon).

- Visualize full prompt (including any multi-modal assets), and the API request.
- BAML gives you full transparency and control of the prompt.
- Using AI is all about iteration speed. If testing your pipeline takes 2 minutes, you can only test 10 ideas in 20 minutes. If you reduce it to 5 seconds, you can test 240 ideas in the same amount of time.
- The playground also allows you to run tests in parallel—for even faster iteration speeds 🚀.
- No need to login to websites, and no need to manually define json schemas.

---

## Enable reliable tool-calling with any model

BAML works even when the models don't support native tool-calling APIs. We created the SAP (schema-aligned parsing) algorithm to support the flexible outputs LLMs can provide, like markdown within a JSON blob or chain-of-thought prior to answering. Read more about SAP.

With BAML, your structured outputs work in Day-1 of a model release. No need to figure out whether a model supports parallel tool calls, or whether it supports recursive schemas, or `anyOf` or `oneOf` etc.

See it in action with: **Deepseek-R1** and OpenAI O1.

---

## Switch from 100s of models in a couple lines

```baml
function Extract() -> Resume {
+  client openai/o3-mini
  prompt #"
    ....
  "#
}
```

Retry policies • fallbacks • model rotations. All statically defined. Want to do pick models at runtime? Check out the Client Registry.

We support: OpenAI • Anthropic • Gemini • Vertex • Bedrock • Azure OpenAI • Anything OpenAI Compatible (Ollama, OpenRouter, VLLM, LMStudio, TogetherAI, and more)

---

## Build beautiful streaming UIs

BAML generates a ton of utilities for NextJS, Python (and any language) to make streaming UIs easy.

BAML's streaming interfaces are fully type-safe. Check out the Streaming Docs, and our React hooks.

---

## Fully Open-Source, and offline

- 100% open-source (Apache 2)
- 100% private. AGI will not require an internet connection, neither will BAML
   - No network requests beyond model calls you explicitly set
   - Not stored or used for any training data
- BAML files can be saved locally on your machine and checked into Github for easy diffs.
- Built in Rust. So fast, you can't even tell it's there.

---

## BAML's Design Philosophy

Everything is fair game when making new syntax. If you can code it, it can be yours. This is our design philosophy to help restrict ideas:

1. Avoid invention when possible
   - Yes, prompts need versioning — we have a great versioning tool: git
   - Yes, you need to save prompts — we have a great storage tool: filesystems
2. Any file editor and any terminal should be enough to use it
3. Be fast
4. A first year university student should be able to understand it

---

## Why a new programming language

We used to write websites like this:

```python
def home():
    return "<button onclick=\"() => alert(\\\"hello!\\\")\">Click</button>"
```

And now we do this:

```jsx
function Home() {
  return <button onClick={() => setCount(prev => prev + 1)}>
          {count} clicks!
         </button>
}
```

New syntax can be incredible at expressing new ideas. Plus the idea of maintaining hundreds of f-strings for prompts kind of disgusts us 🤮. Strings are bad for maintainable codebases. We prefer structured strings.

The goal of BAML is to give you the expressiveness of English, but the structure of code.

---

## FAQ

| Do I need to write my whole app in BAML? | Nope, only the prompts! BAML translates definitions into the language of your choice! [Python](https://docs.boundaryml.com/guide/installation-language/python), [TypeScript](https://docs.boundaryml.com/guide/installation-language/typescript), [Ruby](https://docs.boundaryml.com/guide/installation-language/ruby) and [more](https://docs.boundaryml.com/guide/installation-language/rest-api-other-languages). |
| ---------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Is BAML stable?                          | Yes, many companies use it in production! We ship updates weekly!                                                                                                                                                                                                                                                                                                                                                    |
| Why a new language?                      | [Jump to section](#why-a-new-programming-language)                                                                                                                                                                                                                                                                                                                                                                   |

---

## Contributing

Checkout our guide on getting started

---

## Citation

You can cite the BAML repo as follows:

```bibtex
@software{baml,
  author = {Vaibhav Gupta, Aaron Villalpando and Boundary ML team},
  title = {BAML},
  url = {https://github.com/boundaryml/baml},
  year = {2024}
}
```

---

Made with ❤️ by Boundary

HQ in Seattle, WA

P.S. We're hiring for software engineers that love rust. Email us or reach out on discord!

---

**Stars:** 4.7k | **Forks:** 202 | **Watchers:** 21
