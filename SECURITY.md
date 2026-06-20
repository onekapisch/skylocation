# Security & Privacy

SkyLocation is **offline-first and on-device by design**. This document explains exactly what the app does with your data, what (if anything) leaves your device, and how to report a security issue. Plain language, no hedging.

## TL;DR

- The apps have **no accounts, no analytics, no tracking, and no third-party tracking SDKs**.
- Your **coordinates and location history are computed and stored on your device** and are never uploaded by us.
- The only network traffic the app can generate is **optional** (map tiles you choose to view, and purchase verification). Core GPS, nearest-city, and country resolution work fully offline.

## What stays on your device

- GPS coordinates, altitude, speed, heading, and accuracy.
- The resolved city/country and "Exact Place" (computed locally from the bundled 160,000-place database).
- Your entire **Location History** and favorites (stored in the app's local database).
- Horizon data (sun, moon, beacons) — calculated on-device with standard astronomical formulas.

We have **no server** that receives any of this. There is nothing to log in to.

## What can leave your device, and only then

| Action | What is sent | To whom | Notes |
|---|---|---|---|
| Viewing the **interactive map / map preview** | The map region being displayed | Apple Maps / Google Maps SDK | Only when you open a map. The location *pin* is accurate offline; map *tiles* are what need a connection. Governed by Apple/Google map policies. |
| Buying / restoring **Pro** | Purchase receipt + an anonymous app-user identifier | Apple App Store / Google Play + RevenueCat | Standard in-app-purchase verification. **No location data** is involved. |
| Tapping **Share / SOS / Open in Maps** | The text or image *you* choose to share | The app/recipient *you* pick | User-initiated, via the system share sheet. |

That is the complete list. The app makes no background network calls and sends no telemetry.

## Permissions

- **Location** (While Using) — the entire point of the app; used on-device only.
- **Android** also declares `INTERNET` (optional map tiles + purchase verification) and `VIBRATE` (haptic feedback). No background location, no storage, no contacts.

## Honest note about the website

The apps are tracker-free. The marketing site at **skylocation.app** uses **privacy-respecting, aggregate web analytics** (Vercel Analytics — no cookies, no cross-site tracking, no sale of data) to count visits. If you want zero analytics, use the app: it has none. We call this out here rather than claim the website is analytics-free.

## Reporting a vulnerability

If you find a security or privacy issue, please report it privately first:

- 📧 **kapisch@icloud.com** — subject line `SECURITY: SkyLocation`.

Please include the platform + version, a description, and reproduction steps. We aim to acknowledge within **72 hours** and to fix verified issues in the next reasonable release. Please do not open a public issue for security reports, and please do not test against other users' data. Responsible disclosure is appreciated and credited if you wish.

For non-security bugs, use the public [issue tracker](https://github.com/onekapisch/skylocation/issues/new/choose).
