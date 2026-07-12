# AI-Research-Agent
Using CrewAI orchestration, LangChain, OpenAI LLMs, RAG, memory, and web search APIs
# AI Agent with CrewAI and LangChain

An intelligent AI Research Assistant built using **CrewAI**, **LangChain**, and **OpenAI LLMs**. The agent can understand user queries, decide when external information is required, search the web, utilize memory, and generate accurate, context-aware responses.

This project was developed to explore the architecture and implementation of modern AI Agents, including agent reasoning, tool usage, memory, and Retrieval-Augmented Generation (RAG).

---

## Features

- AI-powered Research Agent
- Intelligent tool selection
- Web Search Integration (Tavily)
- Context-aware conversations
- Short-Term Memory
- Entity Memory
- Retrieval-Augmented Generation (RAG)
- Prompt Engineering
- Modular Agent Architecture
- Extensible design for additional tools and agents

---

## Project Workflow

```
                User Query
                     │
                     ▼
              CrewAI Research Agent
                     │
          Understand the user query
                     │
      Decide whether external information
              is required or not
                     │
         ┌───────────┴───────────┐
         │                       │
         ▼                       ▼
   Use Internal Knowledge    Call Search Tool
                                  │
                                  ▼
                          Tavily Search API
                                  │
                                  ▼
                         Search Results
                                  │
                                  ▼
      Combine Search Results + Memory + User Query
                                  │
                                  ▼
                           OpenAI LLM
                                  │
                                  ▼
                          Final Response
```

---

## Technologies Used

| Category | Tools |
|----------|------|
| Programming Language | Python |
| Agent Framework | CrewAI |
| LLM Framework | LangChain |
| Language Model | OpenAI GPT-4o Mini |
| Memory | CrewAI Memory |
| Vector Storage | RAGStorage |
| Embeddings | OpenAI text-embedding-3-small |
| Web Search | Tavily Search API |
| Development Environment | Google Colab |

---

## Project Structure

```
AI-Agent/
│
├── main.ipynb
├── requirements.txt
├── README.md
├── short-term-memory/
├── entity-memory/
└── images/
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/<username>/AI-Agent-with-CrewAI-and-LangChain.git
```

Move into the project directory

```bash
cd AI-Agent-with-CrewAI-and-LangChain
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Environment Variables

Create a `.env` file (or configure secrets in Google Colab) and add the following:

```text
OPENAI_API_KEY=your_api_key
TAVILY_API_KEY=your_api_key
```

---

## Example Query

```
What is the current temperature in Berlin?
```

The agent automatically:

- Determines that live information is needed.
- Calls the Tavily Search tool.
- Retrieves relevant information.
- Combines search results with memory.
- Generates an accurate response.

---

## Skills Demonstrated

- AI Agent Development
- CrewAI
- LangChain
- Retrieval-Augmented Generation (RAG)
- Prompt Engineering
- Agent Memory
- Tool Calling
- OpenAI API Integration
- Tavily Search API
- Python

---

## Future Improvements

- Multi-agent collaboration
- PDF document retrieval
- Local vector database support
- Streamlit web interface
- LangGraph workflow implementation
- Additional external tools

---

## Learning Objectives

This project demonstrates practical implementation of:

- AI Agent Architecture
- Tool-based reasoning
- Memory management
- RAG pipelines
- Prompt engineering
- LLM orchestration
- Autonomous decision-making

---

## License

This project is intended for learning and demonstration purposes.
