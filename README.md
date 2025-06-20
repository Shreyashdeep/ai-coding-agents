# AI Coding Agents

This repository contains a helpful AI Assistant specialized in frontend development, capable of generating HTML, CSS, JavaScript, and React code. The assistant operates in a cyclical mode of "start, plan, analyze, observe," enabling it to understand user queries, plan step-by-step execution, select relevant tools, perform actions, and learn from observations.

## Features

- **Frontend Development Focus**: Specialized in generating code for HTML, CSS, JavaScript, and React applications.
- **Intelligent Planning**: Plans execution steps based on user queries and available tools.
- **Tool Integration**: Utilizes a `run_command` tool to execute shell commands, enabling it to create directories, files, and manage project dependencies.
- **Code Generation**: Can "writeCode" to generate and modify files with specified content.
- **Observational Learning**: Adjusts its actions based on the output of executed commands and generated code.
- **Vite Integration**: Prioritizes Vite for creating React applications for a modern and efficient development setup.

## How it Works

The AI Assistant follows a structured workflow:

1.  **User Query**: The user provides a natural language query describing the desired frontend application or modification.
2.  **Planning**: The assistant analyzes the query and formulates a step-by-step plan to achieve the goal.
3.  **Action Selection**: Based on the plan, the assistant selects the most appropriate tool from its `available_tools`.
4.  **Tool Execution**: The selected tool is executed with the necessary input (e.g., a shell command or code to write).
5.  **Observation**: The assistant observes the output or result of the tool's execution.
6.  **Iteration**: Based on the observation, the assistant continues planning, selecting, and executing actions until the user's query is resolved.

### Available Tools

-   `run_command`: Executes a given shell command string and returns the output. This is used for tasks like creating directories, navigating, and running package manager commands (e.g., `npm install`).
-   `writeCode`: (Implicitly used in examples, but not explicitly defined as a function in the provided `main.py`'s `available_tools` dictionary. It's crucial for the agent's functionality to write code into files. This would typically take `file` and `code` as input.)

## Getting Started

### Prerequisites

-   Python 3.x
-   `google-generativeai` library
-   `python-dotenv` library
-   An active Google API Key

### Installation

1.  **Clone the repository (or copy `main.py`):**

    ```bash
    git clone [https://github.com/Shreyashdeep/ai-coding-agents.git](https://github.com/Shreyashdeep/ai-coding-agents.git)
    cd ai-coding-agents
    ```

2.  **Install dependencies:**

    ```bash
    pip install -r requirements.txt # Assuming a requirements.txt with google-generativeai and python-dotenv
    ```
    If you don't have a `requirements.txt`, you can install them manually:
    ```bash
    pip install google-generativeai python-dotenv
    ```

3.  **Set up your Google API Key:**

    Create a `.env` file in the root directory of the project and add your Google API Key:

    ```
    GOOGLE_API_KEY=YOUR_API_KEY_HERE
    ```

    Replace `YOUR_API_KEY_HERE` with your actual Google API Key.

### Running the Assistant

Execute the `main.py` script
