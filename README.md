# ✈️ AI Trip Planner (n8n Workflow)

An AI-powered travel planning system that automatically generates **personalized itineraries**, **budget-friendly hotel recommendations**, and **destination insights**, all delivered via email.

---

## 🚀 Features

* 🧠 **AI-Generated Itinerary**
  
  * Day-wise travel plan based on budget and trip duration
* 💰 **Budget Optimization**

  * Ensures total trip cost (stay + activities) stays within user-defined budget
* 🏨 **Hotel Recommendations**

  * Fetches real-time hotel data and returns **Top 5 options** within budget
* 🌍 **Travel Research**

  * Provides local insights:

    * Best areas to stay
    * Food & culture
    * Transport options
    * Hidden gems
* 🌦️ **Live Data Integration**

  * Weather details
  * Country info (currency, language, timezone)
* 📧 **Automated Email Delivery**

  * Sends a structured HTML travel plan to the user

---

## 🧩 Workflow Overview

1. **User Input (Form Trigger)**

   * Destination
   * Travel dates
   * Budget
   * Number of travelers
   * Email

2. **Data Collection**

   * OpenWeather API → Weather + Geo coordinates
   * RestCountries API → Country details
   * SerpAPI → Hotel listings

3. **Processing**

   * Filter hotels within budget
   * Sort by ratings
   * Calculate trip duration
   * Merge all data streams

4. **AI Processing**

   * Research Agent → Destination insights
   * Itinerary Generator → Budget-based daily plan

5. **Output**

   * HTML email with:

     * Travel itinerary
     * Research summary
     * Hotel recommendations

---

## ⚙️ Tech Stack

* **Automation:** n8n
* **AI/LLM:** Groq (LLaMA 3.1)
* **APIs:** OpenWeather, SerpAPI, RestCountries
* **Language:** JavaScript (n8n Code Node)
* **Email Service:** Gmail API

---

## 📂 Project Setup

### 1. Import Workflow

* Open n8n
* Import the provided JSON file

### 2. Configure API Keys

Create a `.env` file:

```
OPENWEATHER_API_KEY=your_key_here
SERPAPI_API_KEY=your_key_here
GROQ_API_KEY=your_key_here
```

Replace placeholders in the workflow accordingly.

---

### 3. Add Credentials in n8n

* Groq API
* Gmail OAuth2

---

### 4. Run the Workflow

* Activate workflow
* Submit form
* Receive travel plan via email 🎉

---

## 🔒 Security

* API keys are **not stored in the repository**
* Use environment variables for all sensitive data
* Mask credentials before sharing workflows

---

## 📌 Future Improvements

* Flight booking integration
* Multi-city trip planning
* Frontend dashboard
* WhatsApp/Telegram notifications

---

## 👨‍💻 Author

AI Automation Project built using n8n and LLMs.
