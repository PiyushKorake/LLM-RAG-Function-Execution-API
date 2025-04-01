# LLM + RAG-Based Function Execution API

## Overview

This Python-based API service dynamically retrieves and executes automation functions using **LLM (Large Language Models)** combined with **RAG (Retrieval-Augmented Generation)**. The system processes user prompts, maps them to predefined automation functions, and generates executable Python code to invoke those functions.

### Features:
- Execute common automation tasks such as opening applications (e.g., Chrome, Calculator) or retrieving system information (e.g., CPU, RAM usage).
- Use Hugging Face or spaCy models to convert user queries into embeddings.
- Retrieve matching functions dynamically based on the user's input.
- Generate and return executable Python code for the matched function.
- Expose the functionality via a FastAPI service.

## Prerequisites

Before running the application, ensure that you have Python 3.x installed.

### Dependencies:
- **fastapi**: Web framework for building the API.
- **uvicorn**: ASGI server to run the FastAPI app.
- **transformers**: Hugging Face transformers for embedding generation.
- **spacy**: For generating text embeddings using spaCy.
- **sentence-transformers**: For using pre-trained SentenceTransformer models.
- **faiss-cpu**: Vector database for storing and retrieving function embeddings.

To install the required dependencies, create a virtual environment and run the following:
```bash
pip install -r requirements.txt

## Setup Instructions

### Step 1: Clone the repository
Clone the repository from GitHub:
```bash
git clone https://github.com/your-repository.git
cd your-repository

Setup Instructions
Step 1: Clone the repository
Clone the repository from GitHub:

bash
Copy
git clone https://github.com/your-repository.git
cd your-repository
Step 2: Install the dependencies
Ensure all necessary dependencies are installed:

bash
Copy
pip install -r requirements.txt
Step 3: Download the spaCy model
If you haven't already, download the spaCy model used for embedding:

bash
Copy
python -m spacy download en_core_web_md
Step 4: Run the FastAPI server
Start the FastAPI server with uvicorn:

bash
Copy
uvicorn api_service:app --reload
The server will start running at http://localhost:8000.

API Usage
Endpoint: /execute
This endpoint accepts a user prompt and returns the corresponding function and generated code.

Method:
POST

Request Body:
json
Copy
{
  "prompt": "Open calculator"
}
Example Response:
json
Copy
{
  "function": "open_calculator",
  "code": "open_calculator()"
}
Endpoint: /add_function
This endpoint allows users to dynamically add new functions to the registry.

Method:
POST

Request Body:
json
Copy
{
  "function_name": "open_paint",
  "function_code": "def open_paint():\n    os.system('mspaint')"
}
Example Response:
json
Copy
{
  "message": "Function open_paint added successfully."
}
Testing the API
Testing with Postman:
Create a new POST request to http://localhost:8000/execute.

In the Body tab, select raw and JSON.

Add the following JSON to the body:

json
Copy
{
  "prompt": "Open calculator"
}
Click Send and check the response for the generated code.

Testing with cURL:
You can also test the API with the following cURL command:

bash
Copy
curl -X 'POST' \
  'http://localhost:8000/execute' \
  -H 'Content-Type: application/json' \
  -d '{"prompt": "Open calculator"}'
Optional Enhancements
Logging
The application logs function execution and errors. You can check the console logs to see function status and error details.

Custom Functions
The /add_function endpoint allows you to add custom user-defined functions to the function registry dynamically. For example, adding a function to open Paint:

Request Example:


{
  "function_name": "open_paint",
  "function_code": "def open_paint():\n    os.system('mspaint')"
}



---
```

### Summary of the Sections in the README:

1. **Overview**: Provides a summary of the project’s purpose and features.
2. **Prerequisites**: Lists the dependencies needed to run the project.
3. **Setup Instructions**: Details the steps to clone the repo, install dependencies, and run the server.
4. **API Usage**: Describes how to use the `/execute` and `/add_function` API endpoints.
5. **Testing the API**: Guides you on how to test the API using Postman and cURL.
6. **Optional Enhancements**: Talks about logging and adding custom user-defined functions.
7. **License**: Provides the license type (MIT).

### Instructions for GitHub:
1. Create a new file named **`README.md`** in your repository.
2. Copy and paste the provided content.
3. Commit and push the file to your GitHub repository.

This should now provide a full, well-documented guide for setting up, running, and using the project. Let me know if you'd like any further modifications or need help with other parts of the project!

