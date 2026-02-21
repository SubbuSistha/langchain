# Roles in LLM (Chat Models)

## What are Roles?

**Roles** define **who is speaking in a conversation** when interacting with a chat-based LLM.

Instead of plain text, chat models use **structured messages with roles**.

> **Role = identity of the message sender (system, user/human, assistant/ai)**

---

## Why Roles are Needed

* Provide **structure** to conversation
* Help model understand **context**
* Allow control over **behavior and tone**
* Enable **multi-turn conversations**

---

## Main Roles

### 1. system (Most Important)

Controls how the model behaves.

* Sets instructions
* Defines personality
* Controls tone and style

#### Example

```python
("system", "You are a helpful teacher")
```

---

### 2. human / user

Represents input from the user.

#### Example

```python
("human", "What is AI?")
```

---

### 3. ai / assistant

Represents the model’s previous responses.

#### Example

```python
("ai", "AI is machines simulating human intelligence")
```

---

## Complete Example

```python
messages = [
    ("system", "You are a helpful teacher"),
    ("human", "What is Java?"),
    ("ai", "Java is a programming language"),
    ("human", "Give example")
]
```

The model uses the full conversation to generate the next response.

---

## How LLM Uses Roles

```
system → sets rules
human → asks question
ai → gives response
```

The model considers all messages to produce the next output.

---

## Without Roles (Less Effective)

```python
"Explain AI like a teacher"
```

* Less structured
* Less control

---

## With Roles (Better)

```python
("system", "You are a teacher"),
("human", "Explain AI")
```

* Clear instructions
* Better response quality

---

## LangChain Example

```python
from langchain_google_genai import ChatGoogleGenerativeAI

llm = ChatGoogleGenerativeAI(model="gemini-1.5-flash-latest")

messages = [
    ("system", "You are a helpful assistant"),
    ("human", "Explain LangChain")
]

response = llm.invoke(messages)

print(response.content)
```

---

## Naming Differences Across APIs

| Concept | LangChain | OpenAI    |
| ------- | --------- | --------- |
| User    | human     | user      |
| AI      | ai        | assistant |
| System  | system    | system    |

---

## Real-World Analogy

| Role   | Example          |
| ------ | ---------------- |
| system | Teacher rules    |
| human  | Student question |
| ai     | Teacher answer   |

---

## Best Practices

* Always include a **system role** for better control
* Keep conversation history for context
* Use clear instructions in system message

---

## Final Summary

* Roles define **who is speaking**
* Main roles:

  * **system** → instructions
  * **human** → user input
  * **ai** → model response

> **Roles enable structured, context-aware conversations in LLMs**

---
