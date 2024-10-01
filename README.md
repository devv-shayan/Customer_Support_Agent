# AI-Powered Customer Support Agent

This project implements an AI-powered customer support agent using Python. The agent categorizes customer queries, analyzes sentiment, and generates appropriate responses based on the query's category and sentiment. It leverages Google's Generative AI (gemini-1.5-flash model) through the `langchain-google-genai` integration and uses `LangGraph` and `LangChain` to manage the workflow.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Setup](#setup)
- [Usage](#usage)
- [Workflow Explanation](#workflow-explanation)
- [Example](#example)
- [Dependencies](#dependencies)
- [Notes](#notes)

## Features

- **Query Categorization**: Classifies customer queries into predefined categories:
  - Technical
  - Billing
  - General
  - Sales
  - Returns
  - Shipping
  - Account Management
- **Sentiment Analysis**: Analyzes the sentiment of the query as Positive, Neutral, or Negative.
- **Dynamic Routing**: Routes the query to the appropriate response function based on category and sentiment.
- **Automated Responses**: Generates tailored responses for each category using AI.
- **Escalation Mechanism**: Automatically escalates queries with negative sentiment to a human agent.
- **Workflow Visualization**: Displays the workflow graph using Mermaid diagrams.

## Installation

Before running the agent, you need to install the required Python packages. You can install them using pip:

```bash
pip install langgraph
pip install langchain
pip install langchain-google-genai
pip install python-dotenv

