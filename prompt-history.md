# Prompt History – AI Weather Automation

## 1. Weather Summary Prompt

### Prompt

> Generate a concise weather summary from the provided weather data. Mention the temperature, weather condition, humidity and wind speed in a user-friendly format.

### Purpose

Used to convert the raw weather information received from the weather API into an easy-to-understand natural-language summary.

---

## 2. Gemini Output Formatting

### Prompt

> Return the weather information in a structured format containing the temperature, weather condition, humidity, wind speed and a concise weather summary.

### Purpose

Used to make the Gemini response easier to process and store in Google Sheets.

---

## 3. Debugging Gemini Output

### Problem

The Gemini response was returned as a nested response containing `content`, `parts`, and `text` fields instead of directly returning the generated text.

### Debugging Approach

The response structure was inspected to identify the location of the generated text.

### Solution

The n8n expression was adjusted to access the generated text from the appropriate nested field.

---

## 4. Google Sheets Integration

### Problem

The Google Sheet was created but initially was not appearing correctly while configuring the Google Sheets node in n8n.

### Debugging Approach

The Google account connection, spreadsheet name and sheet configuration were checked.

### Solution

The Google Sheets node was configured with the correct spreadsheet and worksheet, allowing the workflow output to be stored successfully.

---

## 5. Final Workflow

The final workflow connects:

```text
OpenWeatherMap API
        ↓
      n8n
        ↓
     Gemini
        ↓
 Google Sheets
```

The workflow successfully retrieves weather information, generates an AI-powered summary, and stores the resulting weather record in Google Sheets.

---

## Key Learning

During development, AI assistance was used for understanding n8n expressions, formatting Gemini output, debugging API responses, and configuring the workflow integrations.
