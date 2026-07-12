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
├── main.pdf
├── README.md
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/akankshaparashar45/AI-Research-Agent.git
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

## Tool Output
 
- Agent: Expert Research Analyst
- Task: User Query: 'what is the temperature in kaiserslautern (Germany) today?'.
- Task Description: Analyze this query carefully. Determine if current information from the web is needed. If the query contains words such as today, current, latest, recent, weather, news, temperature, forecast, price, stock, or live information, you MUST call search_tool before answering. Do not answer from your own knowledge before calling search_tool for such queries.
When calling search_tool, pass ONLY a dictionary with exactly one key: 'query'.
Correct example:
{"query": "current temperature in Kaiserslautern Germany today"}
Do not pass an empty string.
Do not pass a list.
Do not pass search results.
Do not pass URLs.
After receiving the search_tool output, synthesize the gathered information with your internal knowledge to provide a clear, accurate, and comprehensive answer directly addressing the user's query.
- Result: 
Climograph, Kaiserslautern

Throughout June, Kaiserslautern reaches its highest average temperature on 29.06, hitting 23.1°C | 73.6°F.
The coldest day is 01.06, with a minimum of 11°C | 51.9°F.
Early in the month, average highs and lows are 20.8°C | 69.4°F and 12.1°C | 53.8°F, respectively.
Mid-month temperatures reach highs of 21.2°C | 70.2°F, with lows at 12.6°C | 54.7°F.
At month’s end, values settle around 22.3°C | 72.1°F for highs and 13.4°C | 56.1°F for lows.
The hottest 10-day period is 21-30, with highs averaging 18°C | 64.4°F.
The coldest is 1-10, with lows down to 16.6°C | 61.9°F. [...] ## 

## 


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
