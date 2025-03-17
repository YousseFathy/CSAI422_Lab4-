# CSAI422_Lab4-
CSAI 422: Lab 4 - Conversational Agent

Overview
This project builds a conversational agent that uses external tools (e.g., WeatherAPI) and reasoning techniques like **Chain of Thought (CoT)** and **ReAct** to solve problems.

Features
Basic Tool Calling: Get current weather and forecasts.
Chain of Thought (CoT): Break down complex queries into steps.
ReAct Reasoning**: Solve problems iteratively using Thought → Action → Observation
Setup
1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
2.	Install dependencies:
bash
Copy
pip install openai python-dotenv requests
3.	Create a .env file:
Copy
OPENAI_API_KEY=your_openai_api_key
WEATHER_API_KEY=your_weatherapi_key
4.	Run the script:
bash
Copy
python conversational_agent.py
________________________________________

Example Conversations
Basic Agent
Copy
User: What's the weather in Paris?
Agent: The current weather in Paris is 15°C with clear skies.
CoT Agent
Copy
User: What's the temperature difference between New York and London?
Agent: New York: 20°C, London: 15°C. Difference: 5°C.
ReAct Agent
Copy
User: Compare weather in Tokyo and Sydney.
Agent:
1. Thought: Get weather for Tokyo and Sydney.
2. Action: [Calls get_current_weather for Tokyo]
3. Observation: Tokyo is 18°C with rain.
4. Action: [Calls get_current_weather for Sydney]
5. Observation: Sydney is 25°C with sun.
6. Final Answer: Tokyo is cooler (18°C) and rainy, Sydney is warmer (25°C) and sunny.
________________________________________
Challenges
1.	API Key Management: Used .env to securely load keys.
2.	Error Handling: Added user-friendly error messages for API failures.
3.	ReAct Implementation: Debugged Thought → Action → Observation steps.
________________________________________
References
•	OpenAI API Docs
•	WeatherAPI Docs

