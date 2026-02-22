# 🌍 AI Trip Planner Agent
An intelligent agent designed to streamline your travel planning by leveraging a multi-tool architecture to handle complex queries, from itinerary generation to real-time expense and weather information.

## 🚀 Overview
The AI Trip Planner Agent acts as a central hub for all travel planning needs. At its core, it uses a FastAPI backend to expose an API that can be consumed by a front-end, such as a Streamlit UI. The system's intelligence is powered by an Agentic Workflow that orchestrates various specialized tools to provide accurate and comprehensive responses.
 
## 📐 Architecture
The agent's architecture is modular and scalable, built around a central Agentic Workflow.
 
<img width="1892" height="632" alt="AI Trip D" src="https://github.com/user-attachments/assets/17377a02-b251-4dd3-87da-b6dc28f244dc" />

## Core Components
Streamlit UI: The user-facing application for interacting with the agent. It sends HTTP requests and form inputs to the backend.

FastAPI Backend: The main entry point for all requests. It receives user inputs, invokes the handle_requests() method to initiate the workflow, and returns the aggregated response. 
 
Config & Cross-Cutting: This layer handles essential services for the entire application, including:

config.yaml: Configuration settings.

Config Loader: Loads and manages the application configuration.

Logger: Logs system events and errors.

Exception Handler: Manages and gracefully handles errors.

Document Save Utility: A utility for saving documents and other data.

## Agentic Workflow & Tools
The heart of the system is the Agentic Workflow, which dynamically selects and executes the appropriate tools to fulfill the user's request. This workflow interacts with a suite of specialized tools, each designed for a specific task.

Model Loader & Prompt Library: The agent's intelligence is driven by a Large Language Model (LLM). The Model Loader fetches the required LLM, and the Prompt Library provides pre-defined templates to guide the model's responses and ensure accuracy.

Tools Suite: A collection of specialized tools that the agent can call upon. Each tool is built with a clear purpose and can make external API calls as needed.

Expense Calculator Tool: Uses an Arithmetic Operations Tool and Expense Utility to calculate and manage travel expenses. It can also make calls to the Currency Rates API.

Currency Conversion Tool: Uses a Currency Utility to handle currency conversions, relying on a REST API call to the Currency Rates API.

Place Search Tool: Utilizes a Place Utility to search for locations of interest. It connects to the Maps/Place API to get data.

Weather Tool: Fetches real-time weather information using a Weather Utility, which calls an external Weather API.

## 🛠️ Features
Intelligent Itinerary Generation: Generates detailed travel plans based on user preferences.

Real-time Information: Provides up-to-date weather forecasts, currency exchange rates, and location details.

Expense Management: Calculates and manages trip costs, including currency conversion.

Scalable Architecture: The modular design allows for easy integration of new tools and functionalities.

LLM Integration: Leverages the power of LLMs for natural language understanding and generation.

## 📥 Getting Started
Prerequisites
Python 3.x

(Additional dependencies will be listed here, e.g., FastAPI, Streamlit, etc.)

## Installation
Clone the repository:

    git clone https://github.com/your-username/ai-trip-planner-agent.git
    cd ai-trip-planner-agent

## Install dependencies:

    pip install -r requirements.txt

## Running the Application
    Set up your environment variables, including any API keys for the external services.

## Start the FastAPI backend:

    uvicorn main:app --reload

## In a new terminal, run the Streamlit UI:

    streamlit run app.py

The application should now be accessible in your web browser.

🤝 Contribution
Contributions are welcome! Please feel free to open a pull request or submit an issue on the GitHub repository.


