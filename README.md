
# Ollama Setup Instructions

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
   
2. Run llama3 model
   ```bash
   ollama run llama3

3. Use the following curl command to interact with the llama3 model
   ```bash
   curl -X POST -H "Content-Type: application/json" -d '{"model": "llama3", "prompt": "What is the capital of France?"}'  http://localhost:11434/api/generate

## Setup Gemma Model
1. Run llama3 model
   ```bash
   ollama run gemma:2b

2. Use the following curl command to interact with the Gemma model
   ```bash
   curl -X POST -H "Content-Type: application/json" -d '{"model": "gemma:2b", "prompt": "What is the capital of France?"}' http://localhost:11434/api/generate



