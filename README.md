# WeatherWise: Intelligent Weather Analysis & Advisory System

## 🌟 Overview

**WeatherWise** is a Python application developed as a final project for the course. It integrates real-time weather data retrieval (via `wttr.in`), data visualization, and an intelligent conversational AI (using the `hands-on-ai` framework with the `granite3.2` model).

The application is structured using modular design principles, allowing users to check current and forecast conditions, view visual data trends, and ask natural language questions to the AI advisor.

## 🛠️ Setup and Installation

### Prerequisites

You need a Google Colab or Jupyter environment to run this notebook.

1. **Install Dependencies**
   The application requires the following Python libraries:
   ```bash
   pip install requests matplotlib pyinputplus
The AI components rely on the hands-on-ai package:Bashpip install hands-on-ai
API Key and Server ConfigurationThis application uses the provided hands-on-ai server for conversational AI and the wttr.in service for weather data (no API key required for wttr.in).The following environment variables must be set in the notebook (or your environment) for the AI to function:Python# These are configured within the notebook's setup section
os.environ['HANDS_ON_AI_SERVER'] = '[https://ollama.serveur.au](https://ollama.serveur.au)'
os.environ['HANDS_ON_AI_MODEL'] = 'granite3.2'
# If required by the server, an API key input prompt is included in the notebook.
Running the ApplicationOpen the Notebook: Open the weatherwise_notebook.ipynb file in your preferred environment (e.g., Google Colab).Execute Setup: Run the initial cell to install packages and configure environment variables.Run run_app(): Execute the final cell containing the if __name__ == "__main__": run_app() call.Follow the Menu: Interact with the console-based menu to view charts or ask the AI advisor questions.✨ Core FeaturesWeather Data Retrieval: Fetches current and 3-day forecast data for user-specified cities.Data Visualization:3-Day Temperature Chart: Line plot showing average temperature trends.Precipitation Chart: Dual-axis chart showing hourly precipitation (mm) and chance of rain (%).Intelligent Advisory: Uses the granite3.2 LLM to analyze weather data and provide natural language advice based on user queries.Intuitive UI: Console menu system implemented using the pyinputplus library for robust input handling.🧱 Modular Design (Core Functions)The application is built around the following required core functions, demonstrating the single responsibility principle:Function NameResponsibilityget_weather_data(location, forecast_days=5)Fetches raw weather JSON from wttr.in.create_temperature_visualisation(weather_data, ...)Creates and displays the temperature line chart.create_precipitation_visualisation(weather_data, ...)Creates and displays the precipitation dual-axis chart.parse_weather_question(question)Stores the user question for the AI model.generate_weather_response(parsed_question, weather_data)Summarizes data and calls the hands-on-ai LLM to generate the final response.
