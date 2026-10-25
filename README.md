# 🌦️ Weather API

A simple weather API built with Python. I made this project while following a tutorial to learn how to build and consume APIs.

## ✨ Features

- Get current weather conditions for any city
- Returns clean JSON responses
- Handles invalid city names and API errors gracefully
- Easy to run locally

## 🛠️ Tech Stack

- **Language:** Python 3
- **Framework:** Flask / FastAPI *(replace with the one you used)*
- **Data source:** OpenWeatherMap API *(replace if you used a different one)*
- **Libraries:** `requests`, `python-dotenv`

## 📁 Project Structure

```
weather-api/
├── main.py             # App entry point
├── requirements.txt    # Python dependencies
├── .env                # API key (not committed)
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- An API key from your weather data provider

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/weather-api.git
   cd weather-api
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate      # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Add your API key**

   Create a `.env` file in the project root:
   ```
   API_KEY=your_api_key_here
   ```

5. **Run the app**
   ```bash
   python main.py
   ```

   The API will be available at `http://localhost:5000` *(or `8000` for FastAPI)*.

## 📡 Usage

### Get weather by city

```
GET /weather?city=Kathmandu
```

**Example response:**

```json
{
  "city": "Kathmandu",
  "temperature": 22.5,
  "description": "clear sky",
  "humidity": 54,
  "wind_speed": 3.1
}
```

**Error response:**

```json
{
  "error": "City not found"
}
```

## 🔒 Security Note

Never commit your `.env` file or API key. Make sure `.env` is listed in your `.gitignore`.

## 🗺️ Future Improvements

- [ ] Add 5-day forecast endpoint
- [ ] Add caching to reduce API calls
- [ ] Support temperature unit conversion (°C / °F)
- [ ] Add tests
- [ ] Deploy online

## 🙏 Credits

Built by following a tutorial: **[Tutorial Name](https://link-to-tutorial)** by *Author Name*.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
