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

## Environment Variables

Create a `.env` file (or configure secrets in Google Colab) and add the following:

```text
OPENAI_API_KEY=your_api_key
TAVILY_API_KEY=your_api_key
```

---

## Output
 
--- Kicking off Crew ---
╭──────────────────────────────────────────── Crew Execution Started ─────────────────────────────────────────────╮
│                                                                                                                 │
│  Crew Execution Started                                                                                         │
│  Name: crew                                                                                                     │
│  ID: a9f2e6a3-827e-4b65-9d93-c067ea850b55                                                                       │
│                                                                                                                 │
│                                                                                                                 │
╰─────────────────────────────────────────────────────────────────────────────────────────────────────────────────╯


🚀 Crew: crew
└── 📋 Task: 53c3d624-2fde-4abe-9035-66ed537bc75e
       Status: Executing Task...


🚀 Crew: crew
└── 📋 Task: 53c3d624-2fde-4abe-9035-66ed537bc75e
       Status: Executing Task...
    └── 🤖 Agent: Expert Research Analyst
            Status: In Progress


# Agent: Expert Research Analyst
## Task: User Query: 'what is the temperature in kaiserslautern (Germany) today?'.
---
Analyze this query carefully. Determine if current information from the web is needed.
If the query contains words such as today, current, latest, recent, weather, news, temperature, forecast, price, stock, or live information, you MUST call search_tool before answering.
Do not answer from your own knowledge before calling search_tool for such queries.

When calling search_tool, pass ONLY a dictionary with exactly one key: 'query'.
Correct example:
{"query": "current temperature in Kaiserslautern Germany today"}
Do not pass an empty string.
Do not pass a list.
Do not pass search results.
Do not pass URLs.

After receiving the search_tool output, synthesize the gathered information with your internal knowledge to provide a clear, accurate, and comprehensive answer directly addressing the user's query.
🤖 Agent: Expert Research Analyst
    Status: In Progress


search tool is called


# Agent: Expert Research Analyst
## Thought: Action: search_tool
## Using tool: search_tool
## Tool Input: 
"{\"query\": \"current temperature in Kaiserslautern Germany today\"}"
## Tool Output: 
Climograph, Kaiserslautern

Throughout June, Kaiserslautern reaches its highest average temperature on 29.06, hitting 23.1°C | 73.6°F.
The coldest day is 01.06, with a minimum of 11°C | 51.9°F.
Early in the month, average highs and lows are 20.8°C | 69.4°F and 12.1°C | 53.8°F, respectively.
Mid-month temperatures reach highs of 21.2°C | 70.2°F, with lows at 12.6°C | 54.7°F.
At month’s end, values settle around 22.3°C | 72.1°F for highs and 13.4°C | 56.1°F for lows.
The hottest 10-day period is 21-30, with highs averaging 18°C | 64.4°F.
The coldest is 1-10, with lows down to 16.6°C | 61.9°F. [...] ## 

## 

# Kaiserslautern Weather in June

Are you planning a holiday with hopefully nice weather in Kaiserslautern in June 2026? Here you can find all information about the weather in Kaiserslautern in June:

## Kaiserslautern weather in June

|  |  |  |  |  |  |
 ---  ---  --- |
|  | Temperature June | 17.2°C | 63°F |  | Precipitation / Rainfall June | 74mm | 2.9 inches |
|  | Temperature June max. | 21.4°C | 70.5°F |
|  | Temperature June min. | 12.6°C | 54.6°F |

|  |  |  |
 --- 
|  | Temperature June | 17.2°C | 63°F |
|  | Temperature June max. | 21.4°C | 70.5°F ||  | Temperature June min. | 12.6°C | 54.6°F |
|  | Precipitation / Rainfall June | 74mm | 2.9 inches |

Hotel Room with Beach View

## Climate for Kaiserslautern in June

Climograph, Kaiserslautern [...] 1.2 °C

(34.1) °F

1.8 °C

(35.3) °F

5.2 °C

(41.4) °F

9.6 °C

(49.2) °F

13.6 °C

(56.5) °F

17.2 °C

(63) °F

19 °C

(66.2) °F

18.6 °C

(65.5) °F

14.8 °C

(58.6) °F

10.4 °C

(50.8) °F

5.5 °C

(41.9) °F

2.3 °C

(36.1) °F

-1.1 °C

(30) °F

-1.1 °C

(30) °F

1.4 °C

(34.4) °F

4.9 °C

(40.8) °F

9.1 °C

(48.4) °F

12.6 °C

(54.6) °F

14.6 °C

(58.3) °F

14.3 °C

(57.7) °F

10.9 °C

(51.7) °F

7.3 °C

(45.1) °F

3.1 °C

(37.6) °F

0.1 °C

(32.2) °F

3.5 °C

(38.4) °F

4.9 °C

(40.8) °F

9.2 °C

(48.5) °F

13.9 °C

(57.1) °F

17.7 °C

(63.9) °F

21.4 °C

(70.5) °F

23.2 °C

(73.8) °F

22.8 °C

(73.1) °F

18.8 °C

(65.8) °F

13.8 °C

(56.9) °F

8 °C

(46.5) °F

4.4 °C

(40) °F

64

(2)

57

(2)

62

(2)

60

(2)

79

(3)

74

(2)

78

(3)

70

(2)

66

(2)

67

(2)

68

(2)

78

(3)# Ventusky

Fire

# Kaiserslautern

49°26'N / 7°46'E / Altitude 239 m / 16:34 2026/06/11, Europe/Berlin (UTC+2)

|  |  |
 --- |
| partly cloudy | 17 °C |
|  |
| Wind speed  20 km/h |

partly cloudy

|  |  |
 --- |
| Humidity | 59 % |
| Air pressure | 1022 hPa |
| Clouds | 50 % |
| Cloud base | 5486 m |

Calculated from nearby stations (15:55 2026/06/11)

Open Radar Map

## Weather for the next 24 hours [...] | 40 |
| 35 |
| 30 |
| 25 |
| 20 |
| 15 |
| 10 |
| 5 |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |
 ---  ---  ---  ---  ---  ---  --- |
| Thu 11 overcast | Fri 12 overcast with rain | Sat 13 partly cloudy | Sun 14 partly cloudy | Mon 15 clear sky with few clouds | Tue 16 overcast | Wed 17 overcast | Thu 18 clear sky with few clouds | Fri 19 clear sky with few clouds | Sat 20 mixed with rain showers | Sun 21 clear sky with few clouds | Mon 22 clear sky with few clouds | Tue 23 partly cloudy | Wed 24 mixed with rain showers |

overcast
overcast with rain
partly cloudy
partly cloudy
clear sky with few clouds
overcast
overcast
clear sky with few clouds
clear sky with few clouds
mixed with rain showers
clear sky with few clouds
clear sky with few clouds
partly cloudy
mixed with rain showers [...] | 02:00 | 05:00 | 08:00 | 11:00 | 14:00 | 17:00 | 20:00 | 23:00 |
 ---  ---  ---  --- |
| overcast with light rain 11 °C 0.3 mm 90 %  SW  10 km/h | overcast with rain 11 °C 0.6 mm 90 %  SW  13 km/h | overcast with rain 12 °C 0.7 mm 80 %  SW  12 km/h | overcast 14 °C 0 mm 40 %  SW  12 km/h | overcast 16 °C 0 mm 30 %  W  13 km/h | overcast 16 °C 0 mm 20 %  SW  12 km/h | mostly cloudy 17 °C 0 mm 10 %  SW  13 km/h | partly cloudy 16 °C 0 mm 10 %  SW  10 km/h |

overcast with light rain
overcast with rain
overcast with rain
overcast
overcast
overcast
mostly cloudy
partly cloudy

## Meteogram

|  |

| 40 |
| 35 |
| 30 |
| 25 |
| 20 |
| 15 |
| 10 |
| 5 |weather25.com
Search
weather in Germany
Remove from your favorite locations
Add to my locations
Share
weather in Germany

# Kaiserslautern weather in June 2026

Patchy rain possible
Light drizzle
Patchy rain possible
Partly cloudy
Cloudy
Partly cloudy
Partly cloudy
Sunny
Sunny
Thundery outbreaks possible
Sunny
Thundery outbreaks possible
Partly cloudy
Partly cloudy

## The average weather in Kaiserslautern in June

The temperatures in Kaiserslautern in June are comfortable with low of 11°C and and high up to 22°C.

You can expect about 3 to 8 days of rain in Kaiserslautern during the month of June. It’s a good idea to bring along your umbrella so that you don’t get caught in poor weather. [...] | Month | Temperatures | Rainy Days | Dry Days | Snowy Days | Rainfall | Weather | More details |
 ---  ---  ---  --- |
| January | 4° / -1° | 10 | 8 | 14 | 103 mm | Awful | Kaiserslautern in January |
| February | 5° / -1° | 9 | 9 | 11 | 96 mm | Awful | Kaiserslautern in February |
| March | 10° / 2° | 8 | 17 | 7 | 72 mm | Awful | Kaiserslautern in March |
| April | 15° / 5° | 5 | 23 | 2 | 66 mm | Ok | Kaiserslautern in April |
| May | 18° / 7° | 9 | 22 | 0 | 139 mm | Ok | Kaiserslautern in May |
| June | 22° / 11° | 7 | 23 | 0 | 119 mm | Ok | Kaiserslautern in June |
| July | 24° / 13° | 7 | 24 | 0 | 133 mm | Good | Kaiserslautern in July |
| August | 24° / 13° | 6 | 25 | 0 | 99 mm | Perfect | Kaiserslautern in August | [...] | September | 20° / 10° | 4 | 26 | 0 | 80 mm | Good | Kaiserslautern in September |
| October | 14° / 6° | 6 | 25 | 0 | 79 mm | Good | Kaiserslautern in October |
| November | 9° / 3° | 8 | 17 | 4 | 92 mm | Awful | Kaiserslautern in November |
| December | 5° / 1° | 11 | 10 | 11 | 128 mm | Awful | Kaiserslautern in December |Home

Forecast

Radar

Explore

More

Sign in

# Daily ForecastLocationKaiserslautern, Rhineland-Palatinate 67663, Germany · as of 2:34 PM UTC

## Trending Now

## Severe weather threat rises for Plains, Midwest Thursday with strong tornadoes possible

## Thousands lose power as storms hit Upper Midwest and Central Plains

## Atlantic hurricane season outlook update

## Lake Powell about 158 feet away from “dead pool”

## Severe weather threat rises for Plains, Midwest Thursday with strong tornadoes possible

## Thousands lose power as storms hit Upper Midwest and Central Plains

## Atlantic hurricane season outlook update

## Lake Powell about 158 feet away from “dead pool”

## Home & Garden

## Gardens endure hot, dry summers better if you choose these plants [...] ## Where in the world is ... the 'Cave of Melody'?

## Spring Is Here

## 8 underrated summer getaways with great weather

## How to keep your dog safe at the beach

## 3 Things You Need To Know About The 2026 Hurricane Season

## 2026 Hurricane Season's Start: Where Atlantic Storms Form In June

## 8 underrated summer getaways with great weather

## How to keep your dog safe at the beach

## 3 Things You Need To Know About The 2026 Hurricane Season

## 2026 Hurricane Season's Start: Where Atlantic Storms Form In June

## We Love Critters

Arena-Pethelpful

## Bison calves battle Yellowstone River current to reunite with their mama

Arena-Pethelpful

## Golden Retriever is too scared of waves to retrieve his own ball

Arena-Pethelpful [...] Arena-Pethelpful

## Gray Wolf Spotted in Sequoia National Park for the First Time in Over 100 Years

Arena-Pethelpful

## North Carolina Has Elk? When and Where to Spot Them

Arena-Pethelpful

## Bison calves battle Yellowstone River current to reunite with their mama

Arena-Pethelpful

## Golden Retriever is too scared of waves to retrieve his own ball

Arena-Pethelpful

## Gray Wolf Spotted in Sequoia National Park for the First Time in Over 100 Years

Arena-Pethelpful

## North Carolina Has Elk? When and Where to Spot Them

## Heat wave poses extra risk for GLP-1 users

Popular for weight loss, drugs like Ozempic and Wegovy can suppress thirst when you need water the most. Here’s how doctors say to stay safe when temperatures soar.

## Sun & Moon## Accessibility links

## Search for a location

# Kaiserslautern - Weather warnings issued

## Forecast - Kaiserslautern

### Day by day forecast

### Environmental Summary

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Hour by hour forecast

### Environmental Summary

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset [...] ### Sunrise Sunset

### Sunrise Sunset

### Sunrise Sunset

## Outlook forecast map

## Forecast for Europe

### Latest forecast for Europe

## To play this video you need to enable JavaScript in your browser.

This video can not be played

## Observations for KaiserslauternObservations

## Settings

## More Weather

### UK

### About BBC Weather

### Elsewhere

BBC Weather in association with MeteoGroup, external

All times are Central European Summer Time (Europe/Berlin, GMT+2) unless otherwise stated.

## Explore the BBC
🤖 Agent: Expert Research Analyst
    Status: In Progress
└── 🧠 Thinking...


🤖 Agent: Expert Research Analyst
    Status: In Progress




# Agent: Expert Research Analyst
## Final Answer: 
The current temperature in Kaiserslautern, Germany today is about 17°C, which is roughly 63°F. The latest available reading shows partly cloudy conditions, with wind around 20 km/h and humidity near 59%.


🚀 Crew: crew
└── 📋 Task: 53c3d624-2fde-4abe-9035-66ed537bc75e
       Status: Executing Task...
    └── 🤖 Agent: Expert Research Analyst
            Status: ✅ Completed


🚀 Crew: crew
└── 📋 Task: 53c3d624-2fde-4abe-9035-66ed537bc75e
       Assigned to: Expert Research Analyst
       Status: ✅ Completed
    └── 🤖 Agent: Expert Research Analyst
            Status: ✅ Completed

╭──────────────────────────────────────────────── Task Completion ────────────────────────────────────────────────╮
│                                                                                                                 │
│  Task Completed                                                                                                 │
│  Name: 53c3d624-2fde-4abe-9035-66ed537bc75e                                                                     │
│  Agent: Expert Research Analyst                                                                                 │
│                                                                                                                 │
│                                                                                                                 │
╰─────────────────────────────────────────────────────────────────────────────────────────────────────────────────╯


╭──────────────────────────────────────────────── Crew Completion ────────────────────────────────────────────────╮
│                                                                                                                 │
│  Crew Execution Completed                                                                                       │
│  Name: crew                                                                                                     │
│  ID: a9f2e6a3-827e-4b65-9d93-c067ea850b55                                                                       │
│                                                                                                                 │
│                                                                                                                 │
╰─────────────────────────────────────────────────────────────────────────────────────────────────────────────────╯



--- Crew Execution Complete ---


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
