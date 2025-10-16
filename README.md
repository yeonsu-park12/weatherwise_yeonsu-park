# 🌦️ WeatherWise: Intelligent Weather Analysis & Advisory System

## 🌟 Overview
**WeatherWise** is a Python application developed as a final project for the course **ISYS5002**.  
It integrates real-time weather data retrieval (via [wttr.in](https://wttr.in)), data visualization, and an intelligent conversational AI using the **hands-on-ai** framework with the **granite3.2** model.

The application follows **modular design principles**, allowing users to:
- Check current and forecast weather conditions
- View visual data trends
- Ask natural language questions to the AI weather advisor

---

## 🛠️ Setup and Installation

### ✅ Prerequisites
You need a **Google Colab** or **Jupyter Notebook** environment to run this project.

### 📦 Install Dependencies
Run the following commands in a notebook cell:

```bash
!pip install requests matplotlib pyinputplus
!pip install hands-on-ai

## 🔐 API & Server Configuration

This project uses:

- **[wttr.in](https://wttr.in)** for weather data (no API key required)  
- **hands-on-ai** for conversational AI

Set the following environment variables before running the app:

```python
import os

os.environ['HANDS_ON_AI_SERVER'] = 'https://ollama.serveur.au'
os.environ['HANDS_ON_AI_MODEL'] = 'granite3.2'

## ▶️ Running the Application

### 🧩 Open the Notebook
Open the `weatherwise_notebook.ipynb` file in your preferred environment (e.g., **Google Colab** or **Jupyter Notebook**).

### ⚙️ Execute Setup
Run the initial cells to install required packages and configure the environment variables.

### 🚀 Run the App
Execute the final cell containing:

```python
if __name__ == "__main__":
    run_app()

### 🕹️ Follow the Menu

Interact with the console-based menu to:

- View **temperature** or **precipitation** charts  
- Ask **natural language weather-related** questions to the AI advisor


---

## ✨ Core Features

### 🌐 Weather Data Retrieval
Fetches current and 3-day forecast data for user-specified cities via [wttr.in](https://wttr.in).

### 📊 Data Visualization
- **3-Day Temperature Chart:** Line plot showing average temperature trends.  
- **Precipitation Chart:** Dual-axis chart showing hourly precipitation (mm) and chance of rain (%).

### 🧠 Intelligent Advisory
Integrates the **granite3.2 large language model** hosted on the *hands-on-ai* server to analyze weather data and provide conversational, natural language insights.

### 🖥️ Intuitive UI
Console menu system implemented using the **pyinputplus** library for robust and user-friendly input handling.

---


## 🧱 Modular Design (Core Functions)

The application is built around the following core functions, demonstrating the **Single Responsibility Principle**:

| Function Name | Responsibility |
|----------------|----------------|
| `get_weather_data(location, forecast_days=5)` | Fetches raw weather JSON from wttr.in |
| `create_temperature_visualisation(weather_data, ...)` | Creates and displays the temperature line chart |
| `create_precipitation_visualisation(weather_data, ...)` | Creates and displays the precipitation dual-axis chart |
| `parse_weather_question(question)` | Stores the user question (simple stub for future NLP) |
| `generate_weather_response(parsed_question, weather_data)` | Summarizes data and calls the hands-on-ai LLM to generate the final response |

---


