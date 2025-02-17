# Ollama Function Calling Example

## Requirements & Install

- Python 3.7+
- Ollama installed and running on your system
- Internet connection for API access

Install the required packages:
   ```
   # create & open virtual environments
   python3 -m venv venv
   source venv/bin/activate
   # close
   # deactivate

   pip install -r requirements.txt
   ```

Ensure Ollama is installed and running on your system. For installation instructions, please refer to the [Ollama documentation](https://github.com/jmorganca/ollama).

## Usage

1. Start the bot:
   ```
   chainlit run function_call.py
   ```

2. Open your web browser and navigate to `http://localhost:8000`.

3. Interact with the bot through the chat interface. You can ask for weather information, request jokes, or try other queries to test the AI's understanding.

## Examples

Here are some sample queries you can try:

- "What's the current weather in New York?"
- "Tell me a joke"
- "How's the temperature in Tokyo right now?"

Feel free to experiment with different phrasings and requests to explore the AI's capabilities.

## How It Works

1. **User Input**: The user sends a message through the Chainlit interface.
2. **AI Processing**: The Ollama model, utilizing Langchain's OllamaFunction, processes the input to understand the user's intent.
3. **Function Calling**: Based on the understood intent, the appropriate function (weather or joke) is called.
4. **API Interaction**: The chosen function interacts with the respective API (Open-Meteo for weather, Official Joke API for jokes).
5. **Response Generation**: The AI generates a human-readable response based on the API data.
6. **Output**: The response is displayed to the user through the Chainlit interface.

## APIs Used

- **Weather Data**: [Open-Meteo API](https://open-meteo.com/)
- **Jokes**: [Official Joke API](https://official-joke-api.appspot.com/)
