# LangChain Overview

## What is LangChain?

**LangChain** is a framework for building applications powered by **Large Language Models (LLMs)** such as GPT, Claude, etc.

It provides tools to combine:

* LLMs (language models)
* Prompt templates
* External tools (APIs, databases)
* Memory (conversation history)
* Execution logic (chains and agents)

> **Goal:** Build real-world AI applications, not just single prompt-response systems.

---

## Why LangChain?

Without LangChain:

```
User Input → LLM → Response
```

With LangChain:

```
User Input → Process → Tool/API → LLM → Output
```

LangChain helps you **structure and orchestrate AI workflows**.

---

## Core Concepts

### 1. LLM / Chat Models

* GPT, Claude, etc.
* Used for generating responses

---

### 2. Prompt Templates

* Dynamic prompts with variables
* Example:

```
"Translate {text} to {language}"
```

---

### 3. Chains

* Sequence of steps (fixed workflow)
* Example:

```
Input → LLM → Output
```

* Used when flow is predictable

---

### 4. Memory

* Stores conversation history
* Helps maintain context across interactions

---

### 5. Tools

* External integrations
* Examples:

  * APIs
  * Databases
  * Search engines
  * Calculators

---

### 6. Agents

* AI systems that can **decide actions dynamically**
* Combines:

  * LLM (reasoning)
  * Tools (execution)

---

## What is an Agent?

An **Agent** is an LLM-powered system that can:

1. Think
2. Decide
3. Act

### Example

```
User: "Get stock price of TCS"

Agent Flow:
1. Think → Need stock API
2. Act → Call API
3. Respond → Return result
```

---

## Is LangChain an Agentic Framework?

**Yes — but not only agentic.**

LangChain supports two styles:

---

### 1. Chains (Deterministic)

* Fixed flow
* Predictable behavior

```
Input → Step1 → Step2 → Output
```

---

### 2. Agents (Agentic)

* Dynamic decision-making
* Uses reasoning + tools

```
Input → Think → Choose Tool → Execute → Respond
```

---

## Chains vs Agents

| Feature        | Chains       | Agents        |
| -------------- | ------------ | ------------- |
| Flow           | Fixed        | Dynamic       |
| Control        | Developer    | AI Model      |
| Predictability | High         | Medium        |
| Use Case       | Simple flows | Complex tasks |

---

## Example (Real Use Case)

### Without Agent

```
User → LLM → Generate Splunk Query
```

---

### With Agent

```
User Query
   ↓
Agent:
   → Generate Query
   → Execute Splunk API
   → Summarize Results
   ↓
Final Response
```

> This is **Agentic AI**.

---

## Final Summary

* LangChain is a **framework for building LLM-powered applications**
* It supports:

  * **Chains** → Fixed workflows
  * **Agents** → Dynamic decision-making systems
* It is **not only agentic**, but includes agentic capabilities

---

## One-Line Definition

> **LangChain is a framework to build LLM-powered applications using structured workflows (chains) and intelligent decision-making systems (agents).**
