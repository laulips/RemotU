# RemotU Mobile — neurological rehabilitation prototype

An open, interactive mobile prototype for home-based neurorehabilitation (stroke, traumatic brain injury, post-neurosurgery). Use it as a base for your own work.

> **Not a medical device.** All exercises, doses, scores and patients are invented sample content and have not been clinically validated. Do not use for patient care. Software that guides treatment may be regulated as a medical device (EU MDR, FDA) — that is the builder's responsibility.

## What's inside
- **Patient:** onboarding, today's session, 3-question check-in, motor exercise player, visual-memory game, completion, progress, plan, messaging.
- **Therapist:** patient list with adherence, patient detail with pain flags, visual motor library (anatomical / functional filters), cognitive library review across six domains, messaging.
- **Patient exercise guide:** tap any motor exercise in the plan, or “How to?” in the player, for video + steps.
- **Bilingual:** Italian / English (header toggle).
- **Design constraints:** minimal text, one task per screen, short sessions, ≥44px targets — for aphasia, fatigue and cognitive load.

## Variants (props on the root component)
- `playerStyle`: `focus` · `coach` · `ritmo`
- `adherence`: `streak` · `orto` (weekly garden) · `nessuno`
- `theme`: `calmo` · `contrasto` · `notte`
- `textSize`: `normale` · `grande`
- `lang`: `it` · `en`

## Files
- `RemotU Mobile.dc.html` — the prototype: template markup + one logic class. Open it in a browser.
- `support.js` — runtime that renders the component. Keep it next to the HTML.
- `ios-frame.jsx` — generic phone bezel (not Apple artwork).
- `Accessibility Guide.dc.html` — design rules for aphasia, fatigue and cognitive load, colour contrast table, and a checklist of what is built and what still needs building.

## Modifying
- **Copy / translations:** the `S.it` and `S.en` objects in the logic class.
- **Motor exercises:** the `MOT` array (segments, family, dose, IT/EN text and steps).
- **Cognitive exercises:** the `COG` array.
- **Colours:** `themeVars()` defines each theme's CSS variables.
- **Imagery:** striped blocks are placeholders. Replace them with your own exercise videos or illustrations.

Serve the folder from any static host (GitHub Pages, Netlify, etc.). Some browsers block local file loading, so use a local server (`npx serve`) if opening the file directly fails.

## Licence
MIT — free to use, copy, modify and redistribute, with attribution and no warranty. Fonts: Fraunces, DM Sans, DM Mono (SIL Open Font License, via Google Fonts).
