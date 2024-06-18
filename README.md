
# Ollama Setup Instructions

## Introduction
This repository contains the setup instructions for Llama3 and Gemma models. These instructions guide you through the process of running these models locally on your system.

## Prerequisites
- Git
- Node.js (if applicable)
- Docker (if using Docker for setup)

## Setup Llama3
1. Clone the Ollama repository:
   ```bash
   git clone https://github.com/ollama/ollama.git
   cd ollama

## Run llama3 model
   ```bash
   ollama run llama3

## Use the following curl command to interact with the llama3 model
curl -X POST -H "Content-Type: application/json" -d '{"model": "llama3", "prompt": "What is the capital of France?"}' http://localhost:11434/api/generate

## Setup Gemma Model
ollama run gemma:2b

## Use the following curl command to interact with the Gemma model
curl -X POST -H "Content-Type: application/json" -d '{"model": "gemma:2b", "prompt": "What is the capital of France?"}' http://localhost:11434/api/generate



