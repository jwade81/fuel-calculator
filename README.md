# Fuel Trip Cost Calculator

A Matrix-themed fuel trip cost calculator that estimates driving costs between your home and any destination using the Google Maps Distance Matrix API.

## Features

- **Two vehicle profiles** with saved MPG values
- **Google Maps Distance Matrix API** for accurate route distances
- **One-way and round-trip cost calculations**
- **Matrix-inspired UI** — neon green on black, digital rain, monospace fonts
- **Mobile-first responsive design**
- **All settings saved to localStorage** — persists between sessions

## Live Demo

Visit: `https://YOUR_USERNAME.github.io/fuel-calculator/`

## Setup — Google Maps API Key

The app requires a Google Maps Distance Matrix API key to calculate distances.

### Get a Free API Key

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project (or select an existing one)
3. Navigate to **APIs & Services → Library**
4. Search for and enable **Distance Matrix API**
5. Go to **APIs & Services → Credentials**
6. Click **Create Credentials → API Key**
7. Copy your new API key

### Add the Key to the App

Open `index.html` and find this line near the top of the `<script>` section:

```js
const GOOGLE_MAPS_API_KEY = 'YOUR_API_KEY_HERE';
```

Replace `YOUR_API_KEY_HERE` with your actual API key.

### Restrict the Key (Recommended)

1. In Google Cloud Console, go to **Credentials**
2. Click on your API key
3. Under **Application restrictions**, select **HTTP referrers**
4. Add your GitHub Pages URL: `https://YOUR_USERNAME.github.io/fuel-calculator/*`
5. Under **API restrictions**, select **Restrict key** and choose **Distance Matrix API**
6. Click **Save**

### API Billing

Google provides a $200/month free credit for Maps Platform APIs. The Distance Matrix API costs $5 per 1,000 requests, so the free tier covers approximately 40,000 calculations per month — more than enough for personal use.

## Default Vehicles

| Vehicle | MPG |
|---|---|
| 2007 Chevy Tahoe | 15 MPG |
| 2017 Ford Explorer AWD Sport | 20 MPG |

Both vehicles and their MPG values can be customized in the Settings panel.

## Tech Stack

- Single `index.html` file — no build tools, no frameworks
- Vanilla HTML, CSS, and JavaScript
- Google Fonts (Share Tech Mono)
- Google Maps Distance Matrix API
- localStorage for persistence
