
# Ollama Setup Instructions Steps Explained

## Introduction
This repository contains the setup instructions for Llama3 and Gemma models. These instructions guide you through the process of running these models locally on your system.

## Prerequisites
- Ollama - Install here -> https://ollama.com/download
- For more reference -> https://github.com/ollama/ollama 
- Docker (if using Docker for setup)

## Setup Llama3
1. Clone the Ollama repository:
   ```bash
   git clone https://github.com/ollama/ollama.git
   cd ollama
   
2. Run llama3 model: Purpose: This command (ollama run llama3) initiates the Llama3 model using the ollama command-line interface (CLI). It starts the Llama3 model with its default configuration or parameters. By executing this command in your terminal or command prompt, you are instructing your local system to launch the Llama3 model. This assumes that ollama is installed and properly configured on your system. The run llama3 part specifies that you want to start the Llama3 model specifically.
   ```bash
   ollama run llama3

3. Use the following curl command to interact with the llama3 model/ Replace http://localhost:11434 with your specific setup details if using a different port or host.
Modify the prompt JSON object to interact with the models using different prompts. This curl command is used to interact with the Llama3 model after it has been started. It sends an HTTP POST request to the local server where Llama3 is running (http://localhost:11434/api/generate) with a JSON payload (-d '{"model": "llama3", "prompt": "What is the capital of France?"}') that specifies the model (Llama3) and a prompt ("What is the capital of France?"). When you execute this curl command, it sends a request to the Llama3 model server running on your local machine. The server processes the request, utilizes the specified model (llama3), generates a response based on the provided prompt (What is the capital of France?), and returns the result in the response body. This interaction demonstrates how you can programmatically communicate with the Llama3 model to obtain AI-generated responses for specific queries or prompts.
   ```bash
   curl -X POST -H "Content-Type: application/json" -d "{\"model\": \"llama3\", \"prompt\": \"What is the capital of France?\"}" http://localhost:11434/api/generate



## Setup Gemma Model
1. Run gemma model: This command (ollama run gemma:2b) initiates the Gemma model using the ollama command-line interface (CLI). It starts the Gemma model with a                         specific configuration (2b in this case, which likely denotes a specific version or configuration of the Gemma model).By running this command, you are                        instructing your local system to start the Gemma model. This step assumes that ollama (the command-line tool for managing LLMs) is installed and                              configured correctly on your system. The 2b version/configuration indicates which specific variant or setup of the Gemma model you want to run.
   ```bash
   ollama run gemma:2b

2. Use the following curl command to interact with the Gemma model. Replace http://localhost:11434 with your specific setup details if using a different port or host.
Modify the prompt JSON object to interact with the models using different prompts. This curl command is used to interact with the Gemma model after it has been started. It sends a HTTP POST request to the local server where Gemma is running (http://localhost:11434/api/generate) with a JSON payload (-d '{"model": "gemma:2b", "prompt": "What is the capital of France?"}') that specifies the model (Gemma with version 2b) and a prompt ("What is the capital of France?"). When you run this curl command, it sends a request to the Gemma model server running on your local machine. The server processes the request, uses the specified model (gemma:2b), generates a response based on the provided prompt (What is the capital of France?), and returns the result in the response body. This interaction demonstrates how you can programmatically communicate with the Gemma model to obtain AI-generated responses to specific queries or prompts.
   ```bash
   curl -X POST -H "Content-Type: application/json" -d '{"model": "gemma:2b", "prompt": "What is the capital of France?"}' http://localhost:11434/api/generate

3.  if i doesn't work try this
 ```bash
   curl -X POST -H "Content-Type: application/json" -d "{\"model\": \"gemma:2b\", \"prompt\": \"What is the capital of France?\"}" http://localhost:11434/api/generate



