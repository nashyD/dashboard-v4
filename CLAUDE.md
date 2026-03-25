This is a PWA supplement tracking dashboard called PROTOCOL. Here's the full context:
Structure:

index.html — The entire app. Vanilla JS, no frameworks. Single-file PWA with inline CSS and JS.
api/chat.js — Vercel serverless function that proxies Anthropic API calls (keeps the API key server-side via ANTHROPIC_API_KEY env var).
sw.js — Service worker for offline caching.
manifest.json — PWA manifest for home screen install.

What the app does:

Supplement stack manager with daily check-off tracking, streak counting, and adherence logging
Command center dashboard with radial gauges, 7-day adherence bars, sparkline charts, monthly cost analytics, and low-stock alerts
Timing engine that groups supplements into dosing windows (Fasted AM, With Meal, Pre-workout, Post-workout, Evening) with fasting-safe flags
Biomarker tracking (sleep, energy, mood, focus, gym performance) on a 1-10 scale with 7-day trend sparklines
Built-in Claude AI chat that sends the user's full stack, adherence history, and biomarker data as context
Each supplement card has SVG molecular structure icons, molecular formulas, mechanism-of-action tags, cost per serving, and servings remaining
Onboarding flow for new users: name entry → choose from 5 starter templates (Foundational, Nootropic Focus, Athletic Performance, Longevity, Start Blank) in a responsive grid
All data persists in localStorage. Each user gets their own data on their device.

Tech details:

Hosted on Vercel, deployed from GitHub (nashyD/sup-dashboard-v3)
Animated particle background with neural-network-style connections (canvas)
Glass morphism cards, IBM Plex Mono + Outfit typography
Chat hits /api/chat which proxies to Anthropic's API with the user's stack as system context

Design aesthetic: Luxury biotech × supercar HUD. Dark obsidian (#08080c) with bioluminescent accents (red #ff2d55, purple #bf5af2, teal #30d5c8, green #32d74b, yellow #ffd60a). Glass cards, radial gauges, staggered fade-in animations.
Run /init to create a CLAUDE.md file with this context so you always have it.
