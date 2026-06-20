# Changelog

Notable changes to **SkyLocation** across iOS and Android. Format based on [Keep a Changelog](https://keepachangelog.com/). Dates are release dates; older entries summarize the highlights of earlier releases.

Get the latest: **[App Store](https://apps.apple.com/app/skylocation/id6751451868)** · **[Google Play](https://play.google.com/store/apps/details?id=com.skylocation.android)**

---

## [Android 1.5.2] - 2026-06-20

### Fixed
- Wrong country shown for some **coastal cities** (point now resolves to the correct country via a nearest-city fallback).
- Redundant / inaccurate **Nearest City** row when it duplicated the exact place.
- **Map preview** now loads for everyone, corrected the Maps key to trust the production signing certificate.

### Changed
- Release hardening: added the `VIBRATE` permission so the locating-radar haptics work, guarded the location callback against a rare crash, and excluded entitlement state from cloud/device backup.

## [iOS 4.1] - 2026-06-16

### Fixed
- **Light-mode** text that could render invisible on some screens.
- Wrong country for **coastal cities**, and a redundant **Nearest City** line.

## [iOS 4.0] - 2026-06-10

### Added
- **Exact Place**: pinpoint precision down to the village or suburb, as a Pro feature.

### Changed
- Accuracy stays **free for everyone**: nearest city + country from the offline database are not gated. Location card reordered to *Coordinates → Likely At → Nearest City → Country*.

## [iOS 3.5] - 2026-05

### Added
- New **160,000-place offline database**: smaller on disk and far more accurate, ending "wrong/far city" results.
- **"Likely At"** (exact place) and an accurate **"Nearest City"** for orientation.

## [iOS 3.3] - 2026-04

### Added
- **Horizon**: sunrise, sunset, golden hour, civil twilight, and moon phase, plus a live compass that points to your saved beacons. Fully offline.

---

<sub>Looking for what is next? The roadmap is the [issue tracker](https://github.com/onekapisch/skylocation/issues). 👍 the features you want.</sub>
