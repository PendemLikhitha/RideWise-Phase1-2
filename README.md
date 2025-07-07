# 🚖 RideWise – Fare Comparison & Ride Booking App

RideWise is a **MERN-based prototype** that allows users to **compare ride fares** (Uber, Ola, Rapido) and **simulate ride booking**. This README covers:

- ✅ **Phase 1:** Route Map & ETA Visualization  
- ✅ **Phase 2:** Ride Booking Simulation  
- 🚧 **Coming Soon:** Phase 2.5 - Fare Comparison & Recommendation

---

## 🚀 Project Setup Instructions

### ✅ Prerequisites

- Node.js & npm installed
- Google Maps API key with the following APIs enabled:
  - **Maps JavaScript API**
  - **Directions API**
  - **Places API**

---

## 🧱 Installation & Setup

```bash
# 1. Clone the repo
git clone https://github.com/your-username/ridewise.git
cd ridewise

# 2. Install dependencies
npm install

# 3. Set up environment variable
# Create a `.env` file and add your API key:
echo "REACT_APP_GOOGLE_MAPS_API_KEY=YOUR_GOOGLE_MAPS_API_KEY" > .env

# 4. Start the development server
npm start
```

## 📦 Tech Stack

| Feature              | Library/Tool              |
|----------------------|---------------------------|
| Frontend             | React.js                  |
| Styling              | Tailwind CSS              |
| Maps & Directions    | @react-google-maps/api    |
| State Management     | React Hooks               |
| API Key Management   | `.env` file               |

---
## ✅ Phase 1: Route Map & ETA Visualization

### 🎯 Objective

- Show Google Map  
- Accept **pickup** and **drop** locations  
- Draw **polyline route**  
- Display **ETA** and **distance**

---

### ⚙️ Key Commands

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
npm install @react-google-maps/api
```

### Tailwind Setup
## tailwind.config.js
```bash
content: ['./src/**/*.{html,js,jsx,ts,tsx}'],
```

## postcss.config.js
```bash
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
};
```
## src/index.css
```bash
@tailwind base;
@tailwind components;
@tailwind utilities;
```
---
## ✅ Phase 2: Ride Booking Simulation
### 🎯 Objective
- Book a ride after route is shown
- Simulate ride status changes:
## "Requested" → "Driver Assigned" → "On Ride" → "Completed"

## ✅ Phase 2: Ride Booking Simulation

### 🎯 Objective

- Book a ride after the route is shown  
- Simulate ride status changes:  
  **"Requested" → "Driver Assigned" → "On Ride" → "Completed"**

---

### 🧠 Logic Used

- `useState()` to manage ride status  
- `setTimeout()` to simulate ride progress  
- Booking button is **disabled** after booking starts

---

### 🖱 Status Timeline

| Status           | Time After Click |
|------------------|------------------|
| Requested        | Immediately      |
| Driver Assigned  | +2 seconds       |
| On Ride          | +5 seconds       |
| Completed        | +10 seconds      |

---

## ✅ Coming Up: Phase 2.5 – Fare Comparison & Recommendation

### 🎯 Objective

- Compare ride providers (Uber, Ola, Rapido) using **mock fare data**  
- Display all available fare options  
- **Recommend** the best provider based on lowest price  
- Allow ride booking with the selected provider  
