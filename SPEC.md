# APEX BRIEFING — Complete Build Specification
## For CC (repo setup/assets) and ChatGPT (HTML build)
## Date: March 29, 2026

---

## OVERVIEW

Build a cinematic technology briefing showcasing TFP's deployment of the Apex Box (by Secure Passage) for World Cup 2026 security at the Power & Light District. This is the companion piece to the TFP Capabilities Briefing — that one says "here's who we are," this one says "here's the technology we're deploying at your district."

**No voiceover.** Text on screen + video backgrounds + music. Same format as the TFP Briefing.

**Runtime:** ~68 seconds, synced to a trimmed version of "The Mountain" cinematic track.

**Audience:** Cordish Companies executive. Bo emails this as a follow-up alongside the TFP Capabilities Briefing.

**Deployment:** Hosted URL (Railway from GitHub), potentially at `apex.taskforceprotectiongov.com`

---

## REPO STRUCTURE

```
APEX-BRIEFING/
├── index.html              (HTML structure — built by ChatGPT)
├── style.css               (All styling — built by ChatGPT)
├── script.js               (Timeline logic — built by ChatGPT)
├── assets/
│   ├── audio/
│   │   └── music.mp3       ("The Mountain" trimmed to 68s, fade baked in)
│   ├── video/
│   │   ├── act1-bg.mp4     (World Cup / threat environment)
│   │   ├── act2-bg.mp4     (Tech / Apex reveal background)
│   │   ├── act3-v1.mp4     (Capability feature 1 background)
│   │   ├── act3-v2.mp4     (Capability feature 2 background)
│   │   ├── act3-v3.mp4     (Capability feature 3 background)
│   │   ├── act3-v4.mp4     (Capability feature 4 background)
│   │   ├── act3-v5.mp4     (Capability feature 5 background)
│   │   ├── act3-v6.mp4     (Capability feature 6 background)
│   │   ├── act4-bg.mp4     (Deployment / district context)
│   │   └── act5-bg.mp4     (Closing — dark atmospheric)
│   └── img/
│       ├── tfp-logo.png    (TFP Spartan helmet lockup)
│       ├── apex-connex.png (Orange Connex box photo — hero image)
│       ├── apex-pictogram.png (Isometric diagram with drone, cameras, satellite)
│       └── apex-logo.png   (Red "Ap" periodic table element badge)
└── package.json
```

**NOTE:** Video filenames above are placeholders. Brian will provide the actual asset list with final filenames. CC maps them accordingly.

---

## DESIGN SYSTEM

### Colors
```css
:root {
  --navy: #030d1a;
  --gold: #c9a84c;
  --red: #8b0000;
  --apex-red: #c0392b;    /* Secure Passage / Apex brand red */
  --white: #ffffff;
  --grey: #a0a8b0;
}
```

### Typography
- **Headlines:** `'Bebas Neue', sans-serif` — all caps, large
- **Body/Labels:** `'Barlow Condensed', sans-serif` — weights 400, 500, 600
- Google Fonts import: `Bebas+Neue` and `Barlow+Condensed:wght@400;500;600`

### Visual Treatment
- Same scanline + vignette overlays as TFP Briefing
- Video backgrounds at reduced opacity (0.2–0.3) with dark overlay
- Gold accent for TFP elements, Apex red (`--apex-red`) for Secure Passage elements
- All transitions smooth fades, subtle vertical slides
- Darker overall tone than TFP briefing — this is about technology and threat response

---

## RUNTIME & TIMING

Total runtime: **68 seconds** (music trimmed with fade baked in starting at ~60s)

### Start Screen (before timer begins)
- Black background
- Apex "Ap" periodic table logo centered, ~120px
- Text below: `APEX BY SECURE PASSAGE`
- Subtitle: `DEPLOYED BY TASK FORCE PROTECTION`
- Pulsing border play button: `▶ CLICK TO BEGIN`
- On click: start music, hide start screen, begin Act 1 at t=0

### Act Timing Breakdown

| Act | Time | Duration | Content |
|-----|------|----------|---------|
| **1 — The Threat** | 0:00–0:08 | 8s | World Cup context, why this matters |
| **2 — The Solution** | 0:08–0:20 | 12s | Apex Box reveal, hero image, tagline |
| **3 — Capabilities** | 0:20–0:42 | 22s | 6 tech features, ~3.5s each |
| **4 — The Deployment** | 0:42–0:55 | 13s | P&L District specific application |
| **5 — Close** | 0:55–0:68 | 13s | Logos, contact, fade to black |

---

## ACT-BY-ACT SPECIFICATION

---

### ACT 1 — THE THREAT (0:00–0:08)

**Purpose:** Establish urgency. World Cup 2026 is coming. Kansas City. Power & Light District. This is not a normal security environment.

**Background:** `act1-bg.mp4` — World Cup / large crowd / stadium context. Dark tones. Opacity 0.25.

**Animation sequence:**
- **0:00–0:01:** Black. Music begins. Video background fades in.
- **0:01–0:03:** Text appears, centered:
  - `FIFA WORLD CUP 2026` — Bebas Neue, clamp(40px, 6vw, 64px), white
  - Gold line expands below
  - `KANSAS CITY` — Bebas Neue, 28px, gold
- **0:03–0:06:** Second text block fades in below:
  - `Power & Light District — 9 blocks, 2 residential towers, 1 major venue` — Barlow Condensed 400, 15px, grey
  - `An open-access entertainment zone in the center of it all.` — Barlow Condensed 400, 14px, grey
- **0:06–0:08:** Final line fades in:
  - `THIS REQUIRES MORE THAN STANDARD SECURITY.` — Barlow Condensed 600, 16px, white, letter-spacing 0.2em
- **0:08:** Fade out to Act 2.

---

### ACT 2 — THE SOLUTION (0:08–0:20)

**Purpose:** Introduce Apex. The orange Connex box is the hero. This is what "more than standard security" looks like.

**Background:** `act2-bg.mp4` — dark, tech-oriented footage. Opacity 0.2. The Connex photo is the visual star, not the background video.

**Animation sequence:**
- **0:08–0:10:** Apex "Ap" logo badge fades in top-center (~80px). Below it:
  - `INTEGRATED TECHNOLOGY` — Barlow Condensed 600, 13px, gold, letter-spacing 0.5em
  - `APEX` — Bebas Neue, clamp(60px, 9vw, 100px), white
  - Gold line expands
- **0:10–0:14:** Orange Connex box photo (`apex-connex.png`) fades in. Centered, ~450px wide. This is the money shot.
- **0:14–0:16:** Below the photo:
  - `DEPLOY ANYWHERE. DEFEND EVERYWHERE.` — Barlow Condensed 500, 15px, gold, letter-spacing 0.25em
- **0:16–0:20:** Below tagline, a brief description fades in:
  - `Deployable security infrastructure by Secure Passage — real-time monitoring, intelligent sensors, autonomous drone surveillance, and integrated command capability in a single hardened unit.` — Barlow Condensed 400, 13px, grey, max-width 600px, centered
- **0:20:** Fade to Act 3.

---

### ACT 3 — CAPABILITIES (0:20–0:42)

**Purpose:** The tech specs. Six features, each with its own background video. Fast, punchy, technical. Same rhythm as the capability cards in the TFP Briefing.

**Structure:** 6 features, ~3.5 seconds each. Full-screen takeover per feature with unique video background. Crossfade transitions.

**Layout for each:** Centered text, same card structure as TFP Briefing (number label, title, gold line, description).

#### Feature 1 — Gunshot Detection (0:20–0:23.5)
- **Video:** `act3-v1.mp4`
- **Label:** `01`
- **Title:** `GUNSHOT DETECTION & BEHAVIOR ANALYSIS`
- **Description:** `Intelligent sensor technology with aggressive behavior tracking and spoken word analysis`

#### Feature 2 — Thermal & Night Vision (0:23.5–0:27)
- **Video:** `act3-v2.mp4`
- **Label:** `02`
- **Title:** `THERMAL & NIGHT VISION SURVEILLANCE`
- **Description:** `Advanced video with movement tracking, perimeter monitoring, and panoramic coverage`

#### Feature 3 — License Plate Recognition (0:27–0:30.5)
- **Video:** `act3-v3.mp4`
- **Label:** `03`
- **Title:** `LICENSE PLATE RECOGNITION & CROWD INTELLIGENCE`
- **Description:** `Pedestrian and traffic tracking, crowd movement analysis for dynamic response`

#### Feature 4 — Autonomous Drones (0:30.5–0:34)
- **Video:** `act3-v4.mp4`
- **Label:** `04`
- **Title:** `AUTONOMOUS DRONE SURVEILLANCE`
- **Description:** `Integrated launch pad for automated aerial monitoring — uninterrupted overhead coverage`

#### Feature 5 — Truman PDR Integration (0:34–0:37.5)
- **Video:** `act3-v5.mp4`
- **Label:** `05`
- **Title:** `TRUMAN PDR — PHYSICAL DETECTION & RESPONSE`
- **Description:** `Proactive risk management platform by Secure Passage — real-time alerts and automated reporting`

#### Feature 6 — Haystax OIC (0:37.5–0:42)
- **Video:** `act3-v6.mp4`
- **Label:** `06`
- **Title:** `HAYSTAX OIC — OPERATIONAL INTELLIGENCE CENTER`
- **Description:** `Organizational and community safety platform — seamless remote monitoring and threat modeling`

---

### ACT 4 — THE DEPLOYMENT (0:42–0:55)

**Purpose:** Make it specific to Cordish. This isn't theoretical — here's how Apex deploys at Power & Light for World Cup.

**Background:** `act4-bg.mp4` — urban/district context, dark tones. Opacity 0.25.

**This is a single screen with the isometric pictogram as the visual anchor.**

**Animation sequence:**
- **0:42–0:44:** Apex pictogram (`apex-pictogram.png`) fades in, centered, ~350px wide. The isometric diagram showing the full ecosystem — container, drone, cameras, satellite, weather station.
- **0:44–0:46:** Title above or below pictogram:
  - `DEPLOYMENT: POWER & LIGHT DISTRICT` — Bebas Neue, clamp(28px, 4vw, 40px), white
  - Gold line
- **0:46–0:55:** Deployment details appear as a grid or stacked list, fading in staggered:
  - `KC LIVE! VENUE — Perimeter surveillance, event crowd monitoring`
  - `ONE LIGHT & TWO LIGHT TOWERS — 24/7 residential coverage`
  - `9-BLOCK ENTERTAINMENT DISTRICT — Roving drone patrols, sensor coverage`
  - `WORLD CUP MATCH DAYS — Elevated posture, federal agency coordination`
  - Each line: Barlow Condensed 400, 13px, white. Location name in gold or bold.

---

### ACT 5 — CLOSE (0:55–0:68)

**Purpose:** Partnership branding. TFP + Secure Passage. Contact. Done.

**Background:** `act5-bg.mp4` — dark atmospheric. Opacity 0.2.

**Animation sequence:**
- **0:55–0:57:** Black pause. Then TFP logo fades in, centered, ~200px wide.
- **0:57–0:59:** Below TFP logo:
  - `TASK FORCE PROTECTION LLC` — Bebas Neue, 22px, white
  - Gold line (100px)
- **0:59–0:61:** Apex "Ap" badge appears below the gold line (~50px), with:
  - `Technology Partner: Secure Passage` — Barlow Condensed 400, 12px, grey
- **0:61–0:63:** Contact info fades in:
  - `(660) 227-9063` — Barlow Condensed 400, 15px, grey
  - `taskforceprotectiongov.com` — Barlow Condensed 400, 15px, gold
- **0:63–0:68:** Hold. Music fading (fade baked into audio). Everything fades to black.

- **After 0:68:** Black screen. No loop. Done.

---

## JAVASCRIPT ARCHITECTURE

Same as TFP Briefing — single timer driven by `music.currentTime`, simple timeline array, `requestAnimationFrame` loop. Scene activation by time. Sub-animations by time thresholds.

```javascript
const timeline = [
  { start: 0,    end: 8,    scene: 'act1' },
  { start: 8,    end: 20,   scene: 'act2' },
  { start: 20,   end: 23.5, scene: 'feat1' },
  { start: 23.5, end: 27,   scene: 'feat2' },
  { start: 27,   end: 30.5, scene: 'feat3' },
  { start: 30.5, end: 34,   scene: 'feat4' },
  { start: 34,   end: 37.5, scene: 'feat5' },
  { start: 37.5, end: 42,   scene: 'feat6' },
  { start: 42,   end: 55,   scene: 'act4' },
  { start: 55,   end: 68,   scene: 'act5' },
];
```

Music volume: 0.15. No JS volume fade needed — fade is baked into the audio file.

---

## ASSET PREPARATION

### Already available (copy from TFP-BRIEFING repo):
- `music.mp3` — trimmed 68s version of "The Mountain" (already exists)
- `tfp-logo.png` — TFP Spartan helmet
- `apex-connex.png` — Orange Connex box photo
- `apex-pictogram.png` — Isometric diagram
- `apex-logo.png` — Red "Ap" periodic table element

### Needed from Brian:
- Video assets for each act/feature — Brian will provide the list
- All videos should be compressed before adding:
```bash
ffmpeg -i INPUT.mp4 -vf "scale=960:-2" -c:v libx264 -crf 28 -preset slow -an -pix_fmt yuv420p OUTPUT.mp4
```

---

## CC EXECUTION ORDER

1. Create GitHub repo `APEX-BRIEFING`
2. Create folder structure: `assets/audio/`, `assets/video/`, `assets/img/`
3. Copy shared assets from TFP-BRIEFING (music, logos, Apex images)
4. Add video assets as Brian provides them
5. Add this spec as `SPEC.md`
6. Add `package.json` for Railway static serving
7. Commit and push: `"Initial setup: folder structure, assets, spec"`
8. Brian directs ChatGPT to the repo to build the HTML presentation

---

## WHAT SUCCESS LOOKS LIKE

A Cordish executive watches the TFP Capabilities Briefing and thinks "these guys are serious." Then they open this link and see the specific technology TFP is bringing to their district for World Cup. Autonomous drones. Gunshot detection. Thermal surveillance. A hardened command hub that drops on-site and turns nine city blocks into a sensor-rich monitored environment. They forward both links to their operations team and say "get these guys on the phone."

---

*This spec is the planning document. ChatGPT builds the presentation. CC manages the repo. Any changes go through Brian.*
