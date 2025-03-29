# LLM + RAG-Based Function Execution API

This project is a Python-based API service that dynamically retrieves and executes automation functions using **LLM (Large Language Models)** and **RAG (Retrieval-Augmented Generation)**. The system processes user prompts, maps them to predefined automation functions, and generates executable Python code for function invocation.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Setup Instructions](#setup-instructions)
3. [Usage Instructions](#usage-instructions)
4. [Testing the API](#testing-the-api)
5. [Bonus Enhancements](#bonus-enhancements)
6. [Contributing](#contributing)
7. [License](#license)

## Project Overview

This project provides an API that can dynamically execute automation functions based on user queries. The API uses a **vector-based retrieval system (RAG)** that matches user input to the appropriate function and generates executable Python code for it. The functionalities supported include application control, system monitoring, and command execution.

### Key Features:
- **Function Registry**: A collection of automation functions like opening applications and monitoring system metrics.
- **LLM + RAG for Function Retrieval**: Use of pre-trained models to convert user queries into vector embeddings and retrieve the most relevant function.
- **Dynamic Code Generation**: Automatically generate Python code to execute the retrieved function.
- **API Service**: Built with **FastAPI**, exposing a REST API to interact with the system.
- **Logging & Monitoring**: Logs execution results and allows for monitoring function usage.

## Setup Instructions

To get this project up and running on your local machine, follow these steps:

### 1. Clone the repository:
First, clone the repository from GitHub to get a local copy of the project:
```bash
git clone https://github.com/PiyushKorake/LLM-RAG-Function-Execution-API.git
cd LLM-RAG-Function-Execution-API
