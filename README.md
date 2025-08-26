Orienta – Orientation-Driven Utility Suite

Orienta is a responsive web app that turns your phone’s orientation into a smart switch for everyday tools—alarm, stopwatch, timer, and weather.

🚀 Overview

Orienta is a mobile-first, browser-based utility app where rotating your phone seamlessly unlocks different tools. With a lightweight architecture and clean design, Orienta transforms orientation into a natural interface for timekeeping and daily essentials.

Portrait (Upright) → ⏰ Alarm Clock

Landscape (Primary) → ⏱ Stopwatch

Portrait (Upside-Down) → ⏳ Timer

Landscape (Secondary) → ☀️ Weather of the Day

✨ Key Features

Mobile-first design → Responsive, touch-friendly, and accessible (WCAG 2.1 AA).

Orientation-aware switching → Uses Screen Orientation API with fallbacks (matchMedia + deviceorientation).

Time engine with precision → Drift-resistant stopwatch, alarm, and timer powered by Web Workers.

Weather integration → Fetches real-time data from Open-Meteo
 (free-tier, keyless).

Accessible UX → Clear typography, color-contrast compliant, ARIA live regions for announcements.

Light/Dark mode support → Honors system preference with a consistent accent palette.

🎨 Color Scheme Strategy

Neutral background for readability: Dark #121212 / Light #FAFAFA

Accent per feature:

Alarm → 🔴 Red #E63946

Stopwatch → 🔵 Blue #0077B6

Timer → 🟠 Amber #F4A261

Weather → 🟢 Teal #2A9D8F

High-contrast text (#FFFFFF / #0F172A) ensures accessibility (≥ 4.5:1 ratio).

Smooth mode-based color transitions for visual clarity.

📱 Demo & Preview

Simply open the app in a modern browser (Chrome, Safari, Edge).

No installation required.

Fully works on Android and iOS mobile browsers.

Can be deployed easily via GitHub Pages, Netlify, or Vercel.

⚙️ How It Works

Orientation Controller → Detects portrait/landscape with inversion, debounced to avoid flicker.

Time Engine (Web Worker) → Manages alarm, stopwatch, and timer with drift correction.

Weather Service → Uses geolocation (with timeout & fallback) or manual city input.

Offline Ready → Displays last known weather and lightweight caching.

🧩 Tech Stack

HTML5 + CSS3 (Tailwind tokens / custom styles)

Vanilla JavaScript (ES6 Modules)

Screen Orientation API + DeviceOrientation fallback

Web Workers for time management

Open-Meteo API (no key required)

🧪 Console Acceptance Tests

On load, Orienta runs lightweight self-tests in the browser console:

✅ Worker initialized

✅ Panels registered

✅ Time formatting works

✅ Orientation detection works
