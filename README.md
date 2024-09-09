# LangChain Chatbot Demo

This repository contains a chatbot built using Python and the LangChain library. The chatbot is designed to manage chat history, support personalized conversations, and stream responses, making it both engaging and highly interactive.

## Key Features
- **In-Memory Chat History**: The chatbot stores chat history for each session using unique session IDs, allowing it to recall previous interactions and maintain context over multiple exchanges.
- **Personalized Conversations**: The bot remembers user names, previous queries (like math problems), and provides personalized replies, creating a more natural interaction.
- **Streaming Responses**: Responses are streamed, providing a dynamic experience where the chatbot can send parts of its reply as they are generated.
- **Multi-Session Support**: Each session is managed by a unique session ID, enabling multiple users to interact with the bot simultaneously with independent histories.
- **Message Handling Pipeline**: The bot uses message templates and token counters to manage conversation flows efficiently.

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/langchain-chatbot-demo.git
```

### 2. Install Dependencies
Navigate to the project directory and install the necessary Python packages:
```bash
pip install -r requirements.txt
```

### 3. Run the Notebook
Open and run `Chatbot.ipynb` using Jupyter or Google Colab.

## How it Works

1. **Model and API Integration**: The chatbot utilizes the `llama3-8b-8192` model from `langchain_groq`, with API keys provided for authentication.
2. **Session-Based Chat**: The bot stores chat history in memory per session, allowing it to maintain user context. Use the `get_session_history()` function to access or initialize session histories.
3. **Streaming and Trimming**: The bot streams its responses for a conversational flow. Token counting and trimming are used to optimize message handling.
4. **Multi-Message Conversations**: The bot can handle multiple sequential messages and recall prior information, such as names or past questions.
   
## Future Enhancements
- **Persistent Storage**: Implement a database to store chat history across runtime sessions.
- **Improved NLP**: Integrate advanced NLP techniques to enhance the chatbot’s ability to understand and respond to more complex queries.
- **User Authentication**: Implement user authentication for personalized sessions that span multiple devices or sessions.

## Dependencies
- Python 3.8 or higher
- LangChain and related libraries
- Jupyter Notebook

## Summary
This project demonstrates how to build an interactive, intelligent chatbot with personalized responses using the LangChain framework. With features like session-based memory, streaming responses, and efficient message processing, the chatbot offers a dynamic and scalable foundation for further development. The flexibility of LangChain allows for easy extension, whether it's adding persistent memory, improving natural language understanding, or integrating authentication.
