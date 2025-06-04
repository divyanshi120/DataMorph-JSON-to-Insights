# DataMorph-JSON-to-Insights
DataMorph is a tool designed to seamlessly transform structured JSON data into a memory-driven visual insights platform . The project's core objective is to enable intuitive and dynamic interpretation of large-scale, memory-stored JSON data through meaningful visualizations and insights.
DataMorph is a powerful Flask-based web application that transforms JSON-formatted weather data into meaningful visual insights. The tool utilizes real-time data from the OpenWeatherMap API, processes it, and generates instant visual summaries—giving users a clear and actionable understanding of current weather conditions in any city. Additionally, it logs all data into an Excel file for long-term analysis.

This project demonstrates how structured JSON data retrieved from memory (via an API) can be converted into human-readable insights and stored systematically for further use.

⚙️ Functionality & Workflow
User Input:

Users submit a city name through a simple HTML form.

JSON Data Fetching:

The application queries the OpenWeatherMap API to fetch the city's weather details in JSON format.

Insight Extraction:

From the JSON data, it extracts key weather metrics:

Temperature (°C)

Humidity (%)

Pressure (hPa)

Wind Speed (m/s)

Weather Description

Insight Visualization:

A bar chart is dynamically created using Matplotlib to show Temperature and Humidity.

The plot is converted to a base64-encoded PNG so it can be embedded directly into the webpage without saving it to disk.

Insight Storage:

The weather data is logged in an Excel file (weather_data.xlsx) using pandas and openpyxl.

The application checks whether the file already exists and appends new data without overwriting previous entries.

Error Feedback:

If the user enters an invalid city name, a helpful error message is displayed.

Frontend Display:

The user sees:

The generated bar graph

Detailed weather metrics

Error messages (if any)

💻 Tech Stack Used
Layer	Technology
Backend	Python + Flask
API Integration	OpenWeatherMap API
Data Format	JSON
Visualization	Matplotlib
Data Storage	Pandas + Openpyxl (Excel)
Frontend Templating	HTML + Jinja2 (Flask)

✅ Key Features
✅ Real-time JSON-to-Insight transformation

✅ Dynamic plotting using in-memory image encoding

✅ Persistent Excel logging of weather data

✅ User-friendly error handling

✅ Clean and extensible architecture

📁 Core Files
app.py: Main application script with routes, logic, and integration

templates/index.html: Frontend template for input and output

weather_data.xlsx: Output file storing historical weather logs

