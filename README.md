# 🚢 Container Ship Tracker

Real-time tracking application for container ships and cargo with live position updates, port history, and interactive route visualization on maps.

## Features

✨ **Live Position Tracking**
- Real-time GPS location updates
- Vessel speed and direction information
- Last update timestamp

🗺️ **Interactive Map**
- Current ship location on map
- Visited ports highlighted in green
- Upcoming ports marked in orange
- Route line connecting all ports
- Port details and arrival/departure times

📊 **Vessel & Container Information**
- Ship: MAJESTIC MAERSK (IMO 9619919)
- Container: TGBU6051037
- Origin and destination information
- Voyage status

📱 **Cross-Platform**
- React Native (iOS & Android)
- Works on iPhone via Expo Go
- Responsive design
- Offline support

🔄 **Real-Time Updates**
- WebSocket connection for live data
- Auto-refresh location every 30 seconds
- Push notifications for port arrivals

## Quick Start for iPhone

### Option 1: Expo Go (Easiest - No coding needed!)

1. Install **Expo Go** from App Store
2. Clone this repo: `git clone https://github.com/baranmustafa0905-cloud/container-ship-tracker.git`
3. Install Node.js from https://nodejs.org/
4. Run:
```bash
cd container-ship-tracker/mobile
npm install
npx expo start
```
5. Scan QR code with iPhone camera
6. Opens in Expo Go automatically

### Option 2: Full Native App

See `INSTALLATION.md` for complete setup guide.

## Tech Stack

**Frontend:**
- React Native + Expo
- React Navigation
- React Native Maps
- Redux for state management

**Backend:**
- Node.js + Express
- Socket.io for real-time updates
- Docker support

## Project Structure

```
container-ship-tracker/
├── mobile/                  # React Native app
│   ├── src/
│   │   ├── screens/        # Main screens
│   │   ├── components/     # Reusable components
│   │   ├── redux/          # State management
│   │   └── utils/          # Helper functions
│   ├── app.json            # Expo config
│   └── package.json
├── backend/                # Node.js backend
│   ├── src/
│   │   └── index.js        # Express + Socket.io server
│   └── package.json
├── docker-compose.yml      # Docker configuration
└── INSTALLATION.md         # Detailed setup guide
```

## Key Screens

### 1. 🗺️ Harita (Map)
- Interactive map with ship location
- All ports marked
- Route visualization
- Real-time position updates

### 2. 📍 Canlı Takip (Live Tracking)
- Current vessel status
- Real-time GPS coordinates
- Speed and heading
- Next port information

### 3. 📊 Detaylar (Details)
- Vessel specifications
- Container information
- Port history
- Upcoming ports schedule

### 4. ⚙️ Ayarlar (Settings)
- Enable/disable notifications
- Real-time tracking toggle
- API connection status
- Auto-refresh settings

## Vessel Information

**Ship:** MAJESTIC MAERSK
- IMO: 9619919
- Type: Container Ship
- Owner: Maersk Line Limited
- Flag: Denmark
- Length: 399 m
- Width: 59 m
- Gross Tonnage: 218,000 GT
- TEU Capacity: 18,000 TEU

**Container:** TGBU6051037
- Type: 20ft High Cube
- Origin: Shanghai, China
- Destination: Hamburg, Germany

## Port Route

**Route:** Shanghai → Singapore → Colombo → Suez → Rotterdam → Hamburg

### Visited Ports ✅
1. Shanghai Port, China (Aug 1-5, 2026)
2. Singapore Port, Singapore (Aug 15-18, 2026)
3. Colombo Port, Sri Lanka (Aug 28 - Sep 1, 2026)

### Upcoming Ports 📍
1. Port Said (Suez), Egypt (ETA: Sep 12, 2026)
2. Rotterdam Port, Netherlands (ETA: Sep 25, 2026)
3. Hamburg Port, Germany (ETA: Sep 28, 2026)

## API Endpoints

### REST API
```
GET /api/vessel           - Get vessel information
GET /api/location         - Get current location
GET /api/ports/visited    - Get visited ports
GET /api/ports/upcoming   - Get upcoming ports
GET /health               - Check server status
```

### WebSocket Events
```
vessel_data              - Initial vessel data
location_update          - Real-time location update (every 5 seconds)
request_location         - Request immediate location update
```

## Installation & Setup

See **INSTALLATION.md** for:
- ✅ Quick Start (Expo Go)
- ✅ Full Native Setup
- ✅ Docker Installation
- ✅ Troubleshooting
- ✅ Development Guide

## Environment Variables

Create `.env` in backend directory:
```
PORT=4000
MONGODB_URI=mongodb://localhost:27017/container-tracker
NODE_ENV=development
CORS_ORIGIN=*
```

## Running the App

### Mobile App
```bash
cd mobile
npm install
npx expo start          # For Expo Go
npm run ios            # For native iOS simulator
npm run android        # For Android emulator
```

### Backend Server
```bash
cd backend
npm install
npm run dev            # Starts on http://localhost:4000
```

### With Docker
```bash
docker-compose up      # Starts both backend and MongoDB
```

## Features Demo

- **Real-time Updates:** See ship location update every 30 seconds
- **Map Navigation:** Zoom and pan to explore the route
- **Port Details:** Tap any port for full information
- **Live Tracking:** Enable real-time GPS tracking
- **Notifications:** Get alerts when ship arrives at port
- **Offline Mode:** View last known location without internet

## License

MIT License - See LICENSE file for details

## Support

- 🐛 Report issues: GitHub Issues
- 💬 Discussions: GitHub Discussions

## Roadmap

- [ ] Multi-vessel tracking
- [ ] Multiple container tracking
- [ ] Weather integration
- [ ] Historical data analytics
- [ ] Notifications customization
- [ ] Dark mode
- [ ] Multilingual support

---

**Happy Tracking! 🚢⚓**
