# TASK FORCE PROTECTION -- APEX BRIEFING — Complete Build Specification

## Date: March 29, 2026

---

## OVERVIEW

Build a cinematic technology briefing showcasing TFP's deployment of the Apex Box (by Secure Passage) for World Cup 2026 security at the Power & Light District. This is a html presentation that will be sent to executives in charge of the Power and Light district to thank them for awarding the bid and saying "here's who we are," this one says "here's the technology we're deploying at your district."

**No voiceover.** Text on screen + video backgrounds + music. Same format as the TFP Briefing.

**Runtime:** 50-60 seconds, synced to a trimmed version of "The Mountain" cinematic track.

**Audience:** Cordish Companies executive. Bo emails a link to this, which will be hosted online as a follow-up to the bid meeting.
**Deployment:** Hosted URL (Railway from GitHub), potentially at `briefing.taskforceprotectiongov.com`

---

## REPO STRUCTURE

```
APEX-BRIEFING/
├── index.html              (HTML structure — built by ChatGPT)
├── style.css               (All styling — built by ChatGPT)
├── script.js               (Timeline logic — built by ChatGPT)
├── assets/
│   ├── video/
│   │   ├── scene1-intro.mp4          (5s)
│   │   ├── scene2-challenge.mp4      (5s)
│   │   ├── scene3-solution.mp4       (5s)
│   │   ├── scene4-drone.mp4          (6s)
│   │   ├── scene5-command.mp4        (5s)
│   │   ├── scene6-coverage.mp4       (5s)
│   │   ├── scene7-detection.mp4      (5s)
│   │   ├── scene8-scalable.mp4       (5s)
│   │   └── scene9-closing.mp4        (7s)
│   ├── audio/
│   │   └── music.mp3                 (~50-60s, trimmed with fade baked in)
│   └── img/
│       ├── tfp-logo.png              (TFP Spartan helmet lockup)
│       ├── apex-connex.png           (Orange Connex box photo — hero image)
│       └── apex-logo.png             (Red "Ap" periodic table element badge)
└── package.json
```

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

Total runtime: **48 seconds of content + fade to black = ~52 seconds**

### Start Screen (before timer begins)
- Black background
- TFP Logo centered
- Text below: `TASK FORCE PROTECTION`
- Subtitle: `DEPLOYING APEX TECHNOLOGY`
- Pulsing border play button: `▶ CLICK TO BEGIN`
- On click: start music, hide start screen, begin Scene 1 at t=0

### Scene Timing Breakdown

| Scene | Time | Duration | Video File | Title |
|-------|------|----------|------------|-------|
| 1 | 0:00–0:05 | 5s | scene1-intro.mp4 | APEX AT THE WORLD CUP |
| 2 | 0:05–0:10 | 5s | scene2-challenge.mp4 | THE CHALLENGE |
| 3 | 0:10–0:15 | 5s | scene3-solution.mp4 | OUR SOLUTION |
| 4 | 0:15–0:21 | 6s | scene4-drone.mp4 | REAL-TIME DRONE NETWORK |
| 5 | 0:21–0:26 | 5s | scene5-command.mp4 | CENTRALIZED COMMAND |
| 6 | 0:26–0:31 | 5s | scene6-coverage.mp4 | INTELLIGENT COVERAGE |
| 7 | 0:31–0:36 | 5s | scene7-detection.mp4 | ADVANCED DETECTION |
| 8 | 0:36–0:41 | 5s | scene8-scalable.mp4 | SCALABLE & RELIABLE |
| 9 | 0:41–0:48 | 7s | scene9-closing.mp4 | SECURING THE FUTURE |
| — | 0:48–0:52 | 4s | — | Fade to black, music ends |

---

## SCENE-BY-SCENE CONTENT

### Scene 1 — APEX AT THE WORLD CUP (0:00–0:05)
**Video:** scene1-intro.mp4
**Title:** `APEX AT THE WORLD CUP` — Bebas Neue, large, white
**Content:** Task Force Protection secures the Power & Light District with advanced Apex drone technology for the 2026 FIFA World Cup.

### Scene 2 — THE CHALLENGE (0:05–0:10)
**Video:** scene2-challenge.mp4
**Title:** `THE CHALLENGE` — Bebas Neue, large, white
**Content:** Large-scale events create dynamic, high-density environments that demand real-time situational awareness beyond traditional methods.

### Scene 3 — OUR SOLUTION (0:10–0:15)
**Video:** scene3-solution.mp4
**Title:** `OUR SOLUTION` — Bebas Neue, large, white
**Content:** Apex delivers a mobile, rapidly deployable command platform integrated with intelligent drone networks for comprehensive coverage.
**Optional:** Show `apex-connex.png` as hero image if layout allows.

### Scene 4 — REAL-TIME DRONE NETWORK (0:15–0:21)
**Video:** scene4-drone.mp4
**Title:** `REAL-TIME DRONE NETWORK` — Bebas Neue, large, white
**Content:** Autonomous Apex drones provide persistent aerial oversight with precision gimbal imaging and seamless live feeds.

### Scene 5 — CENTRALIZED COMMAND (0:21–0:26)
**Video:** scene5-command.mp4
**Title:** `CENTRALIZED COMMAND` — Bebas Neue, large, white
**Content:** Unified operations center fuses drone telemetry, sensor data, and ground assets into actionable intelligence.

### Scene 6 — INTELLIGENT COVERAGE (0:26–0:31)
**Video:** scene6-coverage.mp4
**Title:** `INTELLIGENT COVERAGE` — Bebas Neue, large, white
**Content:** Multi-layered sensing delivers clear visibility across crowded urban zones, day or night.

### Scene 7 — ADVANCED DETECTION (0:31–0:36)
**Video:** scene7-detection.mp4
**Title:** `ADVANCED DETECTION` — Bebas Neue, large, white
**Content:** High-precision PTZ and AI-assisted systems identify and track potential risks with speed and accuracy.

### Scene 8 — SCALABLE & RELIABLE (0:36–0:41)
**Video:** scene8-scalable.mp4
**Title:** `SCALABLE & RELIABLE` — Bebas Neue, large, white
**Content:** Proven drone fleet architecture scales effortlessly while maintaining continuous, organized patrol patterns.

### Scene 9 — SECURING THE FUTURE (0:41–0:48)
**Video:** scene9-closing.mp4
**Title:** `SECURING THE FUTURE` — Bebas Neue, large, white
**Content:** Task Force Protection + Apex technology ensures safe, world-class experiences in the Power & Light District during the 2026 World Cup.
**Additional elements:**
- TFP logo (~200px)
- Apex "Ap" logo badge (~50px)
- `Technology Partner: Secure Passage` — Barlow Condensed 400, 12px, grey
- `(660) 227-9063` — Barlow Condensed 400, 15px, grey
- `taskforceprotectiongov.com` — Barlow Condensed 400, 15px, gold

### After Scene 9 (0:48–0:52)
Fade to black. Music ends. No loop. Done.

---

## JAVASCRIPT TIMELINE

```javascript
const timeline = [
  { start: 0,  end: 5,  scene: 'scene1' },
  { start: 5,  end: 10, scene: 'scene2' },
  { start: 10, end: 15, scene: 'scene3' },
  { start: 15, end: 21, scene: 'scene4' },
  { start: 21, end: 26, scene: 'scene5' },
  { start: 26, end: 31, scene: 'scene6' },
  { start: 31, end: 36, scene: 'scene7' },
  { start: 36, end: 41, scene: 'scene8' },
  { start: 41, end: 48, scene: 'scene9' },
];
```

Music volume: 0.15. No JS volume fade needed — fade is baked into the audio file.

---

## ASSET PREPARATION

### Already in repo:
- `music.mp3` — needs to be re-trimmed to ~52s to match new runtime
- `tfp-logo.png` — TFP Spartan helmet
- `apex-connex.png` — Orange Connex box photo
- `apex-logo.png` — Red "Ap" periodic table element

### Video compression standard:
```bash
ffmpeg -i INPUT.mp4 -vf "scale=960:-2" -c:v libx264 -crf 28 -preset slow -an -pix_fmt yuv420p OUTPUT.mp4
```

---

## CC EXECUTION ORDER

1. ~~Create GitHub repo `APEX-BRIEFING`~~ (done)
2. ~~Create folder structure~~ (done)
3. ~~Copy shared assets~~ (done)
4. ~~Add video assets~~ (Brian uploading)
5. Update `SPEC.md` with this document
6. Brian directs ChatGPT to the repo to build the HTML presentation

---

## WHAT SUCCESS LOOKS LIKE

A Cordish executive watches the TFP Capabilities Briefing and thinks "these guys are serious." Then they open this link and see the specific technology TFP is bringing to their district for World Cup. Autonomous drones. Gunshot detection. Thermal surveillance. A hardened command hub that drops on-site and turns nine city blocks into a sensor-rich monitored environment. They forward both links to their operations team and say "get these guys on the phone."

---

*This spec is the planning document. ChatGPT builds the presentation. CC manages the repo. Any changes go through Brian.*
