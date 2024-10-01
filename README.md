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
```

## Setup
This section outlines how to configure the API key and import necessary libraries for the customer support agent.

### API Key Configuration:
- Obtain the `GEMINI_API_KEY` from Google to access the gemini-1.5-flash model.
- Configure the API key using the `google.generativeai` library.

### Import Necessary Libraries:
- Ensure all the required libraries are installed and imported for the workflow.

## Usage
Instructions on how to implement functions for each step of the customer support agent:
1. Define the state class.
2. Implement the functions for query categorization, sentiment analysis, response generation, escalation, and routing logic.
3. Build and compile the workflow graph using `StateGraph`.
4. Run the agent by processing queries through the `run_customer_support` function.

## Workflow Explanation
An overview of how the AI-powered customer support agent processes queries:
1. **Categorization**: Determines the category of the query.
2. **Sentiment Analysis**: Assesses the sentiment as Positive, Neutral, or Negative.
3. **Routing**: Routes queries based on category and sentiment.
   - Escalates queries with Negative sentiment to human agents.
   - Provides an AI-generated response for other queries.
4. **Response Generation**: Produces a tailored response using the AI model.
5. **Output**: Returns the final result with category, sentiment, and response.

## Example
Example of how the agent processes a customer query:
- **Input Query**: "The phone I bought isn't working; can I get a refund?"
- **Expected Output**:
  - Category: Returns
  - Sentiment: Negative
  - Response: This query has been escalated to a human agent due to its negative sentiment.

## Dependencies
A list of Python libraries and external tools required to run the customer support agent:
- **Python Libraries**:
  - `langgraph`
  - `langchain`
  - `langchain-google-genai`
  - `python-dotenv`
  - `typing`
  - `IPython.display`
  - `os`
- **Google Generative AI**:
  - Access to the gemini-1.5-flash model via API key.
- **Environment**:
  - The agent is designed to run in a Google Colab notebook or any environment that supports IPython display.

## Notes
Additional information on security, error handling, and extensibility:
- **API Key Security**: Ensure the `GEMINI_API_KEY` is securely stored and not exposed.
- **Error Handling**: Implement error handling for potential API failures in production environments.
- **Customization**:
  - Modify categories in the `categories_query` function.
  - Enhance sentiment analysis with additional categories or a scoring system.
- **Extensibility**: Extend the workflow to include more complex logic or integrations.
- **Visualization**: The workflow graph helps in debugging and visually representing the agent's logic.



