# Local-Autogpt-LLm
This is a custom python script that works like AutoGPT. It can use any local llm model, such as the quantized Llama 4b, and leverage the available tools to accomplish your goal through langchain. It is still a work in progress and I am constantly improving it.

## Features

- Use any local llm model
- Leverage tools such as google-search, requests_all, wikipedia, and human
- Initialize an agent with zero-shot-react-description
- Execute the agent with a goal

## Installation

To use this script, you need to have Python 3.6 or higher installed on your machine. You also need to install the following dependencies:

- langchain
- LlamaCpp
- google-api-python-client
- requests

You can install them using pip:
pip install langchain LlamaCpp google-api-python-client requests


You also need to download a llm model and place it in your desired path. You can use the quantized Llama 4b model from here.

**note you can use other models too, just change the import from llama.cpp to gpt4all etc andthen change everything else accordingly
 
You also need to set some environment variables for the script to work properly:

- MODEL_PATH: The path to your llm model file
- TEMP: The temperature for the llm model (default: 0.8)
- NCTX: The number of context tokens for the llm model (default: 8196)
- GOOGLE_API_KEY: Your Google API key for using google-search tool
- GOOGLE_CSE_ID: Your Google Custom Search Engine ID for using google-search tool
- AI_GOAL: The goal you want the agent to achieve

## Usage

To run the script, simply execute it with python:

python local_auto_llm.py

The script will print out the goal, the agent initialization, and the agent execution with the response.

For example, if you set the goal as “Where is Germany Located”, the script will output something like this:

Goal: Where is Germany Located
Initializing agent...
Agent initialized.
Executing agent with goal...
Response: Germany is a country in Central and Western Europe. It borders Denmark to the north, Poland and the Czech Republic to the east, Austria and Switzerland to the south, France and Luxembourg to the southwest, and Belgium and the Netherlands to the west. Germany covers an area of about 357,022 square kilometers and has a population of about 83 million people.
Execution time in seconds: 12.34

## To do
- Fix {tools} is not a valid tool issue
- Try different models

## Contributing

This project is open for contributions. If you have any suggestions, feedback, or issues, please feel free to open an issue or a pull request on GitHub.




