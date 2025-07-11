# 🌐🧠 **Crypto & World News AI Assistant with LangGraph**

This project is an interactive AI assistant that can answer real-time questions about **cryptocurrency prices** and **world news** using tool-augmented language models and **LangGraph**. It integrates external APIs like **GNews** and **CoinDesk** to provide live data, powered by autonomous LLM agents.

---

## 📌 **Project Overview**

This AI assistant can:
- 📰 Fetch real-time **news headlines** for any country using the [GNews API](https://gnews.io/)
- 💰 Retrieve the current **Bitcoin price**
- 🤖 Respond to user questions using LLM + tools via **LangGraph's agent graph**

Built using:
- 🔁 **LangGraph** (for agent workflows)
- 🛠️ Tool integration (`getWorldNews`, `getBitcoinPrice`)
- 🧠 LLM (Groq, OpenAI, etc.)

---

## ⚙️ **Features**

- 🔗 LLM-agent connected to real APIs  
- 🌍 Country-specific news support (e.g., `in`, `us`, `jp`)  
- 🔁 Agent reasoning with tool use  
- 🧪 Notebook-based implementation for experimentation  
- 📤 Streaming responses using `graph.stream()`

---

## 🧠 **What is LangGraph?**

[LangGraph](https://github.com/langchain-ai/langgraph) is a library that allows you to build **stateful, multi-agent workflows** for language models using a graph structure. It extends LangChain by enabling:
- Branching decisions (like if/else logic)
- Tool-based action steps
- Message memory tracking
- Streaming outputs

LangGraph is ideal for orchestrating **tools + agents** in real-time, as seen in this project.

---

## 🔧 T**ools Used**

### `getWorldNews(country_code)`
Fetches latest headlines for a country using the [GNews API](https://gnews.io/). Example:

### `getBitcoinPrice()`
Retrieves real-time Bitcoin price using a crypto API.

## 📥 **Installation**

Install the required libraries:

```bash
pip install langchain-core==0.3.13
pip install langchain==0.2.16
pip install langchain-huggingface==0.1.1
pip install langgraph==0.2.68
pip uninstall -y numpy transformers
pip install numpy transformers
pip install -qU langchain-groq
```
## 🔑 **API Keys**

You’ll need:

* ✅ GNews API Key for news

* ✅ LLM Provider Key (e.g., Groq or OpenAI)

## ▶️ **How to Run**

* Define inputs:
```python

inputs = {
  "messages": [
    {"role": "user", "content": "You are good at cryptocurrency and world news"},
    {"role": "assistant", "content": "Ask me any question."},
    {"role": "user", "content": "What are the current situations in India?"}
  ]
}
```
* Run the agent with LangGraph:

```python

print_stream(graph.stream(inputs, stream_mode="values"))
```

## 🤝 **Contributing**

Pull requests and suggestions are welcome! Please open an issue first for major changes.
