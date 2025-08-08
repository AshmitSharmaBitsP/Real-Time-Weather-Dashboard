# Vue 3 + Vite

# 🌤️ Weather Dashboard

A beautiful, responsive weather dashboard built with **Vue.js** and **Tailwind CSS** that dynamically changes its theme based on current weather conditions.

## ✨ Features

### 🎨 **Dynamic Weather Themes**

- **☀️ Sunny**: Warm yellowish-orange gradients
- **☁️ Cloudy**: Soft blue-purple gradients
- **🌧️ Rainy**: Deep blue-grey gradients
- **⛈️ Storm**: Dark dramatic gradients
- **❄️ Snow**: Light grey-white gradients
- **🌫️ Mist/Fog**: Cool blue-grey gradients
- **🌙 Night**: Dark blue-black gradients (auto-detects night time)

### 📱 **Core Functionality**

- Real-time weather data for any city worldwide
- 5-day weather forecast with detailed information
- Today's hourly forecast breakdown
- Search functionality with popular cities quick-select
- Responsive design for all devices
- Smooth animations and transitions
- Glass morphism UI effects

### 📊 **Weather Metrics**

- Current temperature with "feels like" temperature
- High/Low temperatures
- Wind speed and direction
- Humidity percentage
- Visibility distance
- Atmospheric pressure
- Sunrise and sunset times

## 🚀 Quick Start

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/vue-weather-dashboard.git
cd vue-weather-dashboard
```

### 2. Install dependencies
```bash
npm install
```

### 3. Add your OpenWeatherMap API key
- Copy the `.env.example` file to `.env`:
  ```bash
  cp .env.example .env
  ```
- Open `.env` and set your API key:
  ```env
  VITE_OPENWEATHER_API_KEY=07ffcb7657b6e6c455318c9d6765dd70
  ```
  *(Replace with your own key if you have one!)*

### 4. Start the development server
```bash
npm run dev
```
- Open the URL shown in your terminal (e.g., http://localhost:3000 or http://localhost:3001)

### 5. Build for production
```bash
npm run build
```

## 🔧 Configuration

### Setting up OpenWeatherMap API

1. Sign up at [OpenWeatherMap](https://openweathermap.org/api) if you need your own API key
2. Copy your API key
3. Add it to the `.env` file as shown above
4. **Restart the dev server** after changing the `.env` file

> **Note:**
> - If the API key is missing or invalid, the app will use mock data for demo purposes.
> - With a valid API key, you get real, live weather data for all features.

## 📁 Project Structure

```
vue-weather-dashboard/
├── public/
├── src/
│   ├── components/
│   │   ├── SearchBar.vue          # Search functionality
│   │   ├── CurrentWeather.vue     # Current weather display
│   │   ├── WeatherCard.vue        # Reusable weather info cards
│   │   └── ForecastWeather.vue    # 5-day forecast component
│   ├── Services/
│   │   └── weatherService.js      # API service (uses .env for API key)
│   ├── App.vue                    # Main application component
│   ├── main.js                    # Vue app entry point
│   └── style.css                  # Global styles and Tailwind
├── index.html                     # Standalone version (StackBlitz ready)
├── package.json
├── vite.config.js
├── tailwind.config.js
├── .env.example                   # Example environment file
└── README.md
```

## 🎯 Component Architecture

### **App.vue**

- Main application state management
- Dynamic theme switching logic
- API data fetching and error handling

### **SearchBar.vue**

- City search functionality
- Popular cities quick selection
- Loading states and form validation

### **CurrentWeather.vue**

- Current weather conditions display
- Temperature, humidity, wind speed, etc.
- Weather icons and descriptions

### **WeatherCard.vue**

- Reusable component for weather metrics
- Consistent styling and hover effects
- Icon and data display

### **ForecastWeather.vue**

- 5-day weather forecast
- Hourly breakdown for today
- Interactive forecast cards

## 🎨 Theming System

The app automatically detects weather conditions and applies appropriate themes:

```javascript
const getWeatherTheme = (weatherMain, weatherIcon) => {
  const hour = new Date().getHours();
  const isNight = hour < 6 || hour > 20;

  if (isNight) return 'weather-night';

  switch (weatherMain.toLowerCase()) {
    case 'clear': return 'weather-sunny';
    case 'clouds': return 'weather-clouds';
    case 'rain': return 'weather-rain';
    // ... more themes
  }
};
```

## 📱 Responsive Design

- **Desktop**: Full-width layout with side-by-side components
- **Tablet**: Stacked layout with optimized spacing
- **Mobile**: Single-column layout with touch-friendly buttons

## 🌐 Browser Support

- ✅ Chrome (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ⚠️ Internet Explorer (limited support)

## 🛠️ Technologies Used

- **Vue.js 3** - Progressive JavaScript framework
- **Tailwind CSS** - Utility-first CSS framework
- **Vite** - Fast build tool and dev server
- **OpenWeatherMap API** - Weather data source
- **Poppins Font** - Modern, friendly typography

## 📈 Performance Features

- **Lazy loading** of weather icons
- **Debounced search** to reduce API calls
- **Optimized bundling** with Vite
- **CDN delivery** for fonts and assets
- **Efficient state management** with Vue 3 Composition API

## 🎓 Learning Outcomes

This project demonstrates:

- ✅ **Vue.js 3** with Composition API
- ✅ **Component-based architecture**
- ✅ **API integration** and error handling
- ✅ **Responsive design** with Tailwind CSS
- ✅ **State management** and reactivity
- ✅ **Modern JavaScript** (ES6+)
- ✅ **CSS animations** and transitions
- ✅ **User experience** design principles

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 🙏 Acknowledgments

- [OpenWeatherMap](https://openweathermap.org/) for weather data API
- [Tailwind CSS](https://tailwindcss.com/) for the utility-first CSS framework
- [Vue.js](https://vuejs.org/) for the amazing reactive framework
- [Poppins Font](https://fonts.google.com/specimen/Poppins) for beautiful typography

## 📞 Contact

**Your Name** - your.email@example.com

Project Link: [https://github.com/yourusername/vue-weather-dashboard](https://github.com/yourusername/vue-weather-dashboard)

---

⭐ **Star this repository if you found it helpful!**

![Made with ❤️](https://img.shields.io/badge/Made%20with-%E2%9D%A4%EF%B8%8F-red)
![Built for Learning](https://img.shields.io/badge/Built%20for-Learning-brightgreen)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
