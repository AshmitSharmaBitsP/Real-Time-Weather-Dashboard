# 🌤️ OpenWeatherMap API Setup Guide

## Getting Your API Key

### Step 1: Sign Up for OpenWeatherMap
1. Visit [OpenWeatherMap API](https://openweathermap.org/api)
2. Click "Sign Up" and create a free account
3. Verify your email address

### Step 2: Get Your API Key
1. Log in to your OpenWeatherMap account
2. Go to your [API Keys page](https://home.openweathermap.org/api_keys)
3. Copy your API key (it will look like: `1234567890abcdef1234567890abcdef`)

### Step 3: Configure Your Application
1. Open the `.env` file in your project root
2. Replace `your_openweathermap_api_key_here` with your actual API key:

```env
VITE_OPENWEATHER_API_KEY=1234567890abcdef1234567890abcdef
```

### Step 4: Restart Your Development Server
```bash
npm run dev
```

## ⚠️ Important Notes

- **API Key Activation**: New API keys take up to 2 hours to activate
- **Free Tier Limits**: 60 calls/minute, 1,000,000 calls/month
- **Environment Variables**: The API key is stored in `.env` file (not committed to git)
- **Fallback**: If no API key is provided, the app will use mock data

## 🔧 Testing Your Setup

1. Start the development server: `npm run dev`
2. Open http://localhost:3000
3. Search for a city (e.g., "London", "Tokyo", "New York")
4. If you see real weather data, your API key is working!

## 🚨 Troubleshooting

### "Invalid API key" error?
- Make sure your API key is correct
- Wait 2 hours after creating the key
- Check that you've updated the `.env` file

### "City not found" error?
- Check the city spelling
- Try using the city name in English
- Some cities might need country codes (e.g., "London,UK")

### Still seeing mock data?
- Restart the development server after updating `.env`
- Check that the API key is properly set in the `.env` file
- Verify the API key is active in your OpenWeatherMap account

## 📊 API Features Available

With a real API key, you'll get:
- ✅ Real-time current weather
- ✅ 5-day weather forecast
- ✅ Accurate temperature, humidity, wind data
- ✅ Weather conditions and icons
- ✅ Sunrise/sunset times
- ✅ Air pressure and visibility data 