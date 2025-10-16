# WeatherWise: Intelligent Weather Analysis & Advisory System

## Subtitle: Harnessing Python and AI to Create Intuitive Weather Applications

| Author | Yeonsu Park |
| :--- | :--- |
| Student ID | 23319734 |
| Course | ISYS5002 Introduction to Programming |
| Date | October 19, 2025 |

---
## 💡 Project Overview

WeatherWise is a comprehensive Python application developed for this programming assignment. It successfully integrates real-time weather data retrieval (using the **wttr.in API**), two distinct **data visualizations** using Matplotlib, and a **natural language processing (NLP) interface** for activity advisory.

This project's core purpose is to demonstrate **modular design**, robust technical implementation, and the effective use of **intentional prompting techniques** when collaborating with AI tools throughout the development process.

---
## ✨ Core Application Features (Required)

1.  **Weather Data Component (Standard Option):** * Utilizes the raw `wttr.in` JSON API (`?format=j1`) for data retrieval, meeting the Standard Option requirement.
    * Provides current conditions and a **3-day forecast** for user-specified locations.
    * Includes robust error handling for API connection failures and invalid location inputs.
2.  **Data Visualisation (2 Required):**
    * **Temperature Trend Chart:** A line plot displaying the average daily temperature (in °C) over the forecast period.
    * **Precipitation Risk Plot:** A dual-axis plot comparing hourly precipitation (mm) and the chance of rain (%) for a selected day.
3.  **Natural Language Interface:** * The `parse_weather_question` function uses regex to interpret user queries (e.g., "Is it a good day for running tomorrow?").
    * The `suggest_activity` function generates natural, weather-aware advice based on calculated average temperature and current weather conditions.
4.  **User Interface:** Implemented as an intuitive console-based menu system.

---
## 🛠️ Setup and Installation

### Prerequisites

Ensure **Python 3.8+** is installed on your system.

### Dependencies

Install all necessary libraries, including the required UI package:

```bash
pip install requests matplotlib pyinputplus
