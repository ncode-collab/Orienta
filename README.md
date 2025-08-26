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

📓 Example Structured Prompt (used for Orienta)

Role:
You are a senior front-end engineer and UX specialist building a mobile-first, browser-only web application.

Task:
Develop a one-page web app that detects device orientation and displays different features:
- Portrait (upright) → Alarm Clock
- Landscape (right-side up) → Stopwatch
- Portrait (upside down) → Timer
- Landscape (right-side up, alternate view) → Weather of the Day (from a free weather API)

Constraints:
- Must run entirely in the browser (no native apps, no server-side code).
- Mobile-first design: responsive, touch-friendly, accessible (WCAG 2.1 AA).
- Use Screen Orientation API with fallbacks (matchMedia, deviceorientation).
- Smooth transitions (<200ms), no flicker.
- Use vanilla JavaScript, CSS (Tailwind CDN or plain CSS), and HTML only.
- Use Web Workers for time-based functions (stopwatch, timer, alarm).
- Weather API must be free-tier and keyless (e.g., Open-Meteo).
- Code should be modular, efficient, and commented.

Color Scheme Strategy:
- Use a neutral dark background (#121212) for consistency across modes.
- Define one accent color per feature:
  - Alarm → Warm Red (#E63946)
  - Stopwatch → Bright Blue (#0077B6)
  - Timer → Amber/Orange (#F4A261)
  - Weather → Teal/Green (#2A9D8F)
- Text color: high-contrast white (#FFFFFF) or off-white (#E0E0E0).
- Secondary text: soft gray (#9E9E9E).
- Buttons: filled with feature accent color; hover/active = darker shade.
- Ensure contrast ratio ≥ 4.5:1 for accessibility.
- Respect prefers-color-scheme: auto-switch to light theme (light background + same accent system).

Inputs:
- Device orientation events (portrait/landscape, including upside-down).
- API response from weather service.

Outputs:
1. A single self-contained index.html file including:
   - <style> section with color tokens and responsive design
   - <script type="module"> with orientation controller, time engine, weather service
   - UI panels for Alarm, Stopwatch, Timer, Weather
2. Inline comments explaining logic and color usage.
3. Console-based test harness that verifies:
   - Orientation correctly switches to each feature
   - Stopwatch precision (ms level)
   - Timer and Alarm accuracy across tab switches
   - Weather loads with offline fallback
   - Each mode applies its feature-specific accent color
4. Explanation (short text) of how orientation detection, fallback logic, and color strategy are implemented.

Format:
- Section 1: Full Code (index.html)
- Section 2: Console Test Cases
- Section 3: Explanation of Approach
- Section 4: Color Scheme & Accessibility Notes
