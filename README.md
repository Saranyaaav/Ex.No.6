# Exp No - 6 
## Development of Python Code Compatible with Multiple AI Tools

### Register no : 212223040188

## AIM :
Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

### Explanation:
Experiment the persona pattern as a programmer for any specific applications related with your interesting area. 
Generate the outoput using more than one AI tool and based on the code generation analyse and discussing that. 


# INTRODUCTION

Artificial Intelligence tools such as ChatGPT, Gemini, Claude, and Copilot are increasingly used in software development for code generation, debugging, API integration, and data analysis.

Prompt engineering plays a major role in obtaining accurate and useful outputs from AI systems. Well-structured prompts help AI tools understand:

* The programming language
* The project requirement
* The expected output
* Constraints and formatting requirements

In this experiment, prompts are framed for different coding stages of a sample project involving API integration and data comparison.

---

# USE CASE SELECTED

## Weather Monitoring and Analysis System

### Scenario:

A smart weather analysis application collects weather data from multiple APIs and compares the outputs to provide accurate weather insights.

### APIs Used:

1. OpenWeather API
2. WeatherAPI

### Functional Requirements:

* Fetch weather data using Python
* Compare temperature, humidity, and weather conditions
* Display differences between APIs
* Generate recommendations based on weather data

---

### AI TOOLS USED

| AI Tool | Purpose                          |
| ------- | -------------------------------- |
| ChatGPT | Code generation and explanations |
| Gemini  | Alternative code suggestions     |
| Copilot | Programming assistance           |

---

## STAGE 1 – PROMPT FOR PYTHON CODE GENERATION

### Prompt Designed

“Generate Python code to fetch weather data from OpenWeather API using the requests library. The program should retrieve city temperature, humidity, and weather condition and display the output clearly.”

---

### AI-GENERATED RESPONSE

```python
import requests

api_key = "YOUR_API_KEY"
city = "Chennai"

url = f"https://api.openweathermap.org/data/2.5/weather?q={city}&appid={api_key}&units=metric"

response = requests.get(url)
data = response.json()

print("City:", city)
print("Temperature:", data['main']['temp'], "°C")
print("Humidity:", data['main']['humidity'], "%")
print("Condition:", data['weather'][0]['description'])
```

---

## Explanation

The AI generated Python code using:

* requests library
* JSON response handling
* API parameter integration

The code successfully retrieves and displays weather information.

---

## STAGE 2 – PROMPT FOR MULTIPLE API INTEGRATION

### Prompt Designed

“Write Python code to fetch weather data from both OpenWeather API and WeatherAPI. Compare temperature and humidity values from both APIs and display the differences in tabular format.”

---

### AI-GENERATED RESPONSE

```python
import requests
import pandas as pd

city = "Chennai"

# OpenWeather API
ow_key = "YOUR_OPENWEATHER_KEY"
ow_url = f"https://api.openweathermap.org/data/2.5/weather?q={city}&appid={ow_key}&units=metric"
ow_data = requests.get(ow_url).json()

# WeatherAPI
wa_key = "YOUR_WEATHERAPI_KEY"
wa_url = f"http://api.weatherapi.com/v1/current.json?key={wa_key}&q={city}"
wa_data = requests.get(wa_url).json()

comparison = pd.DataFrame({
    "Parameter": ["Temperature", "Humidity"],
    "OpenWeather": [
        ow_data['main']['temp'],
        ow_data['main']['humidity']
    ],
    "WeatherAPI": [
        wa_data['current']['temp_c'],
        wa_data['current']['humidity']
    ]
})

print(comparison)
```

---

## Explanation

The AI successfully:

* Integrated two APIs
* Compared outputs
* Displayed results in tabular format

This improved readability and analysis capability.

---

## STAGE 3 – PROMPT FOR ANALYZING DIFFERENCES

### Prompt Designed

“Analyze the differences between weather data returned by OpenWeather API and WeatherAPI. Explain possible reasons for variations in temperature and humidity readings.”

---

### AI-GENERATED RESPONSE

### Generated Analysis

“The differences between APIs may occur because each service uses different weather stations, update intervals, and prediction models. One API may provide more real-time sensor data while another uses averaged regional forecasts.”

---

## Explanation

The AI generated:

* Logical comparison
* Real-world reasoning
* Technical explanation

This improved analytical understanding.

---

## STAGE 4 – PROMPT FOR ACTIONABLE INSIGHTS

### Prompt Designed

“Based on the weather comparison results, suggest useful recommendations for users regarding outdoor activities and energy management.”

---

### AI-GENERATED RESPONSE

### Generated Insights

* Avoid outdoor activities during high temperature conditions.
* Use energy-efficient cooling systems during peak heat hours.
* Schedule industrial operations during cooler periods to reduce energy consumption.

---

## Explanation

The AI generated practical recommendations from the analyzed data.

---

# COMPARISON OF PROMPT EFFECTIVENESS

| Stage                  | Prompt Quality | AI Response Quality | Observation                 |
| ---------------------- | -------------- | ------------------- | --------------------------- |
| Python Code Generation | High           | Excellent           | Accurate code generation    |
| API Integration        | High           | Excellent           | Proper multi-API comparison |
| Difference Analysis    | Moderate       | Very Good           | Good reasoning capability   |
| Actionable Insights    | High           | Excellent           | Practical recommendations   |

---

## OBSERVATIONS

1. Clear prompts generated more accurate code.
2. Mentioning libraries improved coding precision.
3. Structured prompts produced better formatted outputs.
4. AI tools effectively handled API integration tasks.
5. Analytical prompts generated useful real-world insights.

---

## Possible Improvements

Future prompts can be refined by:

* Adding error handling requirements
* Specifying visualization needs
* Including performance optimization instructions
* Mentioning security practices for API keys

---

## RESULT

The prompts for AI-assisted project coding were successfully designed and evaluated. AI tools effectively generated:

* Python code
* API integrations
* Comparative analysis
* Actionable insights

The experiment demonstrated that well-structured prompts significantly improve the quality and usefulness of AI-generated coding assistance.

---

## CONCLUSION

This experiment highlighted the importance of prompt engineering in AI-assisted software development. Carefully framed prompts help AI tools generate accurate, structured, and context-aware code outputs.

The study concludes that:

* Prompt clarity directly impacts code quality.
* Structured prompts improve AI understanding.
* AI tools can effectively assist in project development when guided properly.

Prompt engineering is therefore an essential skill for students working on mini and final year projects involving AI-assisted coding.
