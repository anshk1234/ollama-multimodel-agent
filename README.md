# Ollama Multimodal Agent

A Streamlit based web interface for interacting with multimodal AI models running locally through Ollama.

This project allows users to run powerful AI models on their own machine and interact with them through a simple web interface. The Streamlit app acts as the frontend UI while Ollama handles the local model inference.

## Features
        
* Local AI model execution using Ollama
* Clean web interface built with Streamlit
* Multimodal support (text and file inputs)
* No external API keys required
* Fully local and privacy friendly

## Architecture

User Interface: Streamlit
Model Runtime: Ollama (running locally)

Flow:

User Input → Streamlit UI → Local Ollama Model → Response → Streamlit Output

The application sends prompts from the Streamlit frontend to the Ollama server running locally on the user's machine.

## Installation

### 1. Clone the repository

git clone https://github.com/anshk1234/ollama-multimodel-agent.git

cd ollama-multimodel-agent

### 2. Install Python dependencies

pip install -r requirements.txt

### 3. Install Ollama

Download and install Ollama from:

https://ollama.com

### 4. Pull a model

Example:

ollama pull llama3

or

ollama pull llava

## Running the Application

Start the Streamlit app:

streamlit run main.py

Make sure the Ollama server is running locally before starting the app.

## Example Workflow

1. Start Ollama on your system
2. Run the Streamlit application
3. Open the provided local URL
4. Enter prompts or upload inputs
5. The app sends the request to Ollama
6. The model response is displayed in the UI

## Project Structure

ollama-multimodel-agent

.streamlit/
main.py
requirements.txt
neural.json
LICENSE

## Tech Stack

Python
Streamlit
Ollama

## Future Improvements

* Better multimodal file handling
* Model selection inside UI
* Chat history memory
* Deployment options

## Try the web app:

[ollama multimodel agent](https://ollama-multimodel-agent.streamlit.app/) powered by streamlit

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://ollama-multimodel-agent.streamlit.app/)

## License

MIT License

## Author

Ansh Kunwar
