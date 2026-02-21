# Latency Tester

Measure audio and visual latency in headphones, speakers, Bluetooth devices, and VR.

**[Try it live](https://domsleee.github.io/latency-tester/)**

## How it works

A beat plays at a configurable BPM. You tap when you hear (or see) it. The time between the beat firing and your tap is your device's latency.

After 4 warm-up beats to lock into the rhythm, measurement begins. The displayed value is a rolling average of your last 10 taps.

## Features

- **Audio + Visual modes** — test with sound, screen flash, or both simultaneously
- **Precise timing** — beats scheduled on the Web Audio clock (sample-accurate), tap matching uses pure math against the beat grid with zero drift
- **Offset calibration** — dial in your headphone offset until latency reads ~0ms, then use that value in your DAW/game
- **Signed history graph** — see early (below the beat line) vs late (above) with hover tooltips
- **Configurable tap keys** — default Enter/z/x, bind any key
- **BPM range 20–1200** — changeable mid-session
- **All settings persist** in localStorage (BPM, offset, keys, audio/visual)
- **Zero dependencies** — single HTML file, vanilla JS, Web Audio API
- **Mobile-friendly** — works great on phones for testing Bluetooth headphones

## Offset calibration workflow

1. Run a test with offset = 0 to measure raw latency (e.g. ~45ms)
2. Click **Avg** to set the offset from your current average
3. Re-test — measured latency should now read ~0ms
4. Use that offset value in your application's audio settings

## Inspired by

[NullVoxPopuli/latency-tester](https://github.com/NullVoxPopuli/latency-tester) — this is a ground-up rewrite addressing the open issues from that project.
