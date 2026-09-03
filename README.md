# AI-Powered Weather Automation using n8n

## 📌 Project Overview

This project is an automated weather information workflow built using **n8n**. It retrieves weather data from the **OpenWeatherMap API**, sends the information to **Google Gemini** to generate a human-readable weather summary, and stores the processed weather records in **Google Sheets**.

The workflow demonstrates API integration, AI-powered text processing, workflow automation, and data storage.

---

## 🏗️ Architecture

```text
OpenWeatherMap API
        ↓
       n8n
        ↓
   Google Gemini
        ↓
  Google Sheets
```

### Workflow Components

1. **OpenWeatherMap API**

   * Retrieves current weather information.
   * Provides data such as temperature, weather condition, humidity, and wind speed.

2. **n8n**

   * Acts as the workflow automation platform.
   * Connects the weather API, Gemini, and Google Sheets.
   * Processes and passes data between the different services.

3. **Google Gemini**

   * Processes the raw weather information.
   * Generates a concise, user-friendly weather summary.

4. **Google Sheets**

   * Stores the generated weather records.
   * Provides a simple way to view and track workflow results.

---

## ✨ Features

* Automated weather data retrieval
* OpenWeatherMap API integration
* Google Gemini AI-powered weather summaries
* Google Sheets data storage
* End-to-end workflow automation using n8n
* Structured weather records
* Easy-to-understand weather output

---

## 🛠️ Technologies Used

* **n8n** – Workflow automation
* **OpenWeatherMap API** – Weather data
* **Google Gemini** – AI-generated weather summaries
* **Google Sheets** – Data storage
* **Google APIs** – Google Sheets integration

---

## 🔄 Workflow

The workflow follows these steps:

### Step 1: Get Weather Data

The OpenWeatherMap API is called to retrieve current weather information for the selected location.

### Step 2: Process Weather Data

The weather information is passed through n8n and prepared for AI processing.

### Step 3: Generate AI Summary

Google Gemini receives the weather information and generates a concise natural-language summary.

### Step 4: Store Results

The generated weather information and summary are written to Google Sheets for persistent storage.

---

## 🤖 AI Prompt

Gemini is instructed to analyze the weather information and generate a concise, user-friendly summary containing the important weather details.

Example:

```text
Generate a concise weather summary from the provided weather data.
Mention the temperature, weather condition, humidity and wind speed
in a user-friendly format.
```

---

## 📊 Output

The workflow stores weather records in Google Sheets.

Example information includes:

* Weather condition
* Temperature
* Humidity
* Wind speed
* AI-generated weather summary

---

## 📁 Repository Contents

```text
weather-automation-n8n/
│
├── README.md
├── weather-workflow.json
└── prompt-history.md
```

The `weather-workflow.json` file contains the exported n8n workflow.

The `prompt-history.md` file documents the major AI prompts and debugging steps used during development.

---

## ⚙️ Setup Instructions

### 1. Import the Workflow

Import `weather-workflow.json` into an n8n instance.

### 2. Configure OpenWeatherMap

Add your OpenWeatherMap API credentials to the relevant n8n node.

### 3. Configure Google Gemini

Add your Gemini API credentials to the Gemini node.

### 4. Configure Google Sheets

Connect the Google account and select the spreadsheet used for storing weather records.

### 5. Execute the Workflow

Run the workflow and verify that:

* Weather data is retrieved successfully.
* Gemini generates the weather summary.
* The result is added to Google Sheets.

---

## 🔐 Security

API keys and credentials are **not included in this repository**.

Credentials should be configured securely inside n8n.

---

## 🎯 Learning Outcomes

This project demonstrates:

* REST API integration
* AI/LLM integration
* Workflow automation
* Data transformation
* Google Sheets integration
* Debugging n8n expressions and AI outputs
* Using AI to generate structured, human-readable information

---

## 👩‍💻 Author

**Bhavana H P**

GitHub: https://github.com/BHAVANA-HP
