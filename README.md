##  Groq With Gradio

This repository contains code for a Gradio chat interface powered by Groq's Large Language Model (LLM) completions API.

###  Description

This project allows users to interact with a helpful assistant through a chat interface. The assistant is built using Groq's LLM, specifically the `llama3-70b-8192` model, and provides short and informative responses to user queries.

###  Getting Started

1. Prerequisites:
    * Python 3.6 or later
    * `groq` library ([https://console.groq.com/docs/libraries](https://console.groq.com/docs/libraries))
    * `gradio` library ([https://gradio.app/](https://gradio.app/))
2. Installation:
    * Clone this repository.
    * Install the required libraries:
        ```bash
        pip install groq gradio
        ```
3. Environment Variables:
    * Create a `.env` file in the project root directory.
    * Add the following line to the `.env` file, replacing `<YOUR_GROQ_API_KEY>` with your actual Groq API key:

        ```
        GROQ_API_KEY=<YOUR_GROQ_API_KEY>
        ```

4. Run the application:
    * Open a terminal in the project directory and run:

        ```bash
        python main.py
        ```

    * This will launch the Gradio chat interface in your web browser.

###  How it Works

The code defines an async function `chat_groq` that handles user interactions. Here's a breakdown of the functionality:

* Groq Client: It initializes a Groq client using your API key stored in the environment variable.
* System Prompt: It defines a system prompt message for the assistant, indicating its helpful and concise nature.
* Message History: It constructs the message history by combining system prompts, user messages, and assistant responses.
* Chat Completion Request: It sends a chat completion request to the Groq LLM API using the constructed message history. 
* Response Generation: It iterates through the response stream and retrieves the generated content from the LLM.
* Gradio Chat Interface: Finally, it utilizes Gradio's `ChatInterface` component to display the chat interface and facilitate user interaction.

###  Additional Notes

* This is a basic example showcasing Gradio and Groq integration for a chat interface.
* The code utilizes environment variables for secure storage of the API key.
* Feel free to customize the system prompt and explore different Groq LLM models for varied assistant behavior.
