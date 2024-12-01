# Multi-Agent Collaboration System

A system demonstrating collaboration between specialized AI agents using LangGraph and LangChain. Implementation is derived from the following sources:

- [[Multi-agent network](https://langchain-ai.github.io/langgraph/tutorials/multi_agent/multi-agent-collaboration/)]
- [[AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation](https://arxiv.org/abs/2308.08155)]

## Overview

This project implements a workflow where multiple AI agents collaborate to complete complex tasks. The current implementation features two specialized agents:

- A Research Agent that can search for information
- A Chart Generator Agent that can create data visualizations

## Features

- **Multi-Agent Workflow**: Uses LangGraph to coordinate between agents
- **Specialized Agents**: Each agent has specific capabilities and tools
- **State Management**: Maintains conversation state between agents
- **Conditional Routing**: Smart routing between agents based on task completion

## Requirements

- Python 3.9+
- Required packages:
  - langchain
  - langchain-anthropic
  - langgraph
  - matplotlib
  - jupyter
  - IPython

## API Keys Required

The following API keys need to be set as environment variables:

- `ANTHROPIC_API_KEY` - for Claude 3.5 Sonnet
- `TAVILY_API_KEY` - for web search capabilities

## Usage

1. Open the Jupyter notebook:

```bash
jupyter notebook multi-agent-collaboration.ipynb
```

2. Run all cells in order

3. The system will:
   - Initialize the agents and tools
   - Set up the workflow graph
   - Execute the specified task
   - Display results with proper formatting

## Example Task

The notebook includes an example task where the agents:

1. Research UK's GDP data for the past 5 years
2. Create a line chart visualization of the data

## Architecture

The system consists of:

- **Research Node**: Handles data gathering using Tavily search
- **Chart Node**: Creates visualizations using matplotlib
- **Router**: Manages workflow between agents
- **State Graph**: Coordinates the overall agent collaboration

## Output

The system provides:

- Detailed state tracking of agent interactions
- Visual output (charts/graphs) when generated
- Structured conversation history
- Clear indication of task completion
