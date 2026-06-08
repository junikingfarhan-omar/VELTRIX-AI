# VELTRIX-AI - Weather Dashboard

A modern, responsive weather dashboard built with React and Node.js that fetches real-time weather data from public APIs.

## Features

✅ **Real-time Weather Data** - Fetches current weather conditions  
✅ **5-Day Forecast** - Extended weather predictions  
✅ **Multiple Cities** - Search and compare weather across different locations  
✅ **Responsive Design** - Works seamlessly on desktop, tablet, and mobile  
✅ **Detailed Metrics** - Temperature, humidity, wind speed, UV index, and more  
✅ **Beautiful UI** - Modern interface with smooth animations  
✅ **Weather Alerts** - Notifications for severe weather conditions  

## Tech Stack

### Frontend
- **React 18+** - UI library
- **Vite** - Build tool and dev server
- **Tailwind CSS** - Styling
- **Axios** - HTTP client
- **React Query** - Server state management

### Backend
- **Node.js** - Runtime
- **Express.js** - Web framework
- **OpenWeatherMap API** - Weather data provider
- **Dotenv** - Environment variable management
- **Cors** - Cross-origin resource sharing

## Project Structure

```
VELTRIX-AI/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/    # Reusable React components
│   │   ├── pages/         # Page components
│   │   ├── hooks/         # Custom React hooks
│   │   ├── services/      # API service calls
│   │   ├── styles/        # CSS/Tailwind styles
│   │   ├── utils/         # Utility functions
│   │   ├── App.tsx
│   │   └── main.tsx
│   ├── package.json
│   └── vite.config.ts
├── server/                # Express backend
│   ├── src/
│   │   ├── routes/        # API routes
│   │   ├── controllers/   # Request handlers
│   │   ├── services/      # Business logic
│   │   ├── middleware/    # Express middleware
│   │   ├── types/         # TypeScript types
│   │   └── index.ts
│   ├── package.json
│   └── tsconfig.json
├── package.json
├── .gitignore
└── README.md
```

## Getting Started

### Prerequisites
- Node.js 16+ and npm/yarn
- OpenWeatherMap API key (free tier available)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/junikingfarhan-omar/VELTRIX-AI.git
   cd VELTRIX-AI
   ```

2. **Install dependencies**
   ```bash
   npm install
   cd client && npm install
   cd ../server && npm install
   cd ..
   ```

3. **Set up environment variables**
   
   Create `.env` file in the root:
   ```
   VITE_API_URL=http://localhost:5000/api
   ```

   Create `server/.env` file:
   ```
   PORT=5000
   OPENWEATHER_API_KEY=your_api_key_here
   NODE_ENV=development
   CORS_ORIGIN=http://localhost:5173
   ```

4. **Start development servers**
   ```bash
   npm run dev
   ```

   - Frontend: http://localhost:5173
   - Backend: http://localhost:5000

## API Endpoints

### Weather Routes
- `GET /api/weather/current?city=London` - Get current weather
- `GET /api/weather/forecast?city=London` - Get 5-day forecast
- `GET /api/weather/coordinates?lat=51.5&lon=-0.1` - Get weather by coordinates
- `GET /api/weather/search?query=Lond` - Search city suggestions

## Usage

1. Enter a city name in the search bar
2. View current weather conditions and metrics
3. Check the 5-day forecast
4. Add multiple cities to compare weather
5. Toggle between Celsius and Fahrenheit

## Environment Variables

### Frontend (`.env`)
```
VITE_API_URL=http://localhost:5000/api
```

### Backend (`server/.env`)
```
PORT=5000
NODE_ENV=development
OPENWEATHER_API_KEY=your_key_here
CORS_ORIGIN=http://localhost:5173
```

## Building for Production

```bash
npm run build
npm start
```

## Deployment

### Vercel (Frontend)
```bash
vercel deploy
```

### Heroku or Railway (Backend)
```bash
git push heroku main
```

## API Documentation

### Current Weather
```
GET /api/weather/current?city=London

Response:
{
  "city": "London",
  "temperature": 15,
  "description": "Partly cloudy",
  "humidity": 65,
  "windSpeed": 12,
  "uvIndex": 3,
  "feelsLike": 13,
  "pressure": 1013
}
```

### Forecast
```
GET /api/weather/forecast?city=London

Response:
{
  "city": "London",
  "forecast": [
    {
      "date": "2024-01-15",
      "tempMax": 18,
      "tempMin": 12,
      "description": "Sunny",
      "icon": "01d"
    },
    ...
  ]
}
```

## Contributing

1. Create a feature branch (`git checkout -b feature/amazing-feature`)
2. Commit your changes (`git commit -m 'Add amazing feature'`)
3. Push to the branch (`git push origin feature/amazing-feature`)
4. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For support, email support@veltrix-ai.com or open an issue on GitHub.

## Roadmap

- [ ] User accounts and saved cities
- [ ] Weather alerts and notifications
- [ ] Historical weather data
- [ ] Air quality index integration
- [ ] Multiple language support
- [ ] Dark mode toggle
- [ ] Progressive Web App (PWA)
- [ ] Mobile app with React Native

---

**Live Demo:** [https://veltrix-ai-rho.vercel.app](https://veltrix-ai-rho.vercel.app)