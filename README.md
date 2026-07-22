# Pillgrid

**LED matrix video filter — a KD tool.**

Pillgrid reconstructs any video, image, or live camera feed as a wall of LED dots in real time, in the browser. One WebGL fragment shader, one HTML file, no build step, no dependencies.

## Use it

Open `index.html` in a browser — that's it. Drop a video or image anywhere on the stage, or use the source buttons:

- **Demo** — built-in animated test signal
- **File** — any video or image file (also drag & drop)
- **Camera** — live webcam (requires serving over `localhost` or `https`; browsers block camera on `file://` pages)

To serve locally:

```bash
python3 -m http.server 8000
```

## Controls

- **Presets** — Reference, Billboard, OLED, Broadcast, Ghost, Brutal — plus **Shuffle** for a random look that still reads well, and **Reset**
- **Source extras** — **Mirror** (flip horizontally, handy for camera), **Contain** (fit the whole frame instead of filling; out-of-frame dots go dark)
- **Matrix** — dot shape (pill / round / square), axis, pitch, length, size response, stagger, jitter
- **Signal** — contrast, gamma, exposure, black point, softness, bloom, vignette
- **Motion** — per-dot flicker (amount + speed), scanning wave (speed sign sets direction), glitch, grain
- **Color** — tint / duotone / true-RGB modes, saturation, six tint presets, custom dim + bright colors
- **Playback** — click the stage (or press space) to pause/resume a loaded video; fullscreen button on the stage

### Keyboard

`Space` play/pause · `R` record · `S` snapshot · `F` fullscreen

## Export & share

- **Record clip** captures the filtered canvas at 60 fps — MP4 where the browser supports it (Safari), WebM elsewhere. Load your clip, hit record, play it through, stop.
- **Snapshot** saves the current frame as a PNG at full canvas resolution.
- **Copy settings link** puts your exact look into the URL, so a filter recipe can be shared or bookmarked.

---

Built with the KD design system — Instrument Sans, `#0339F8`.
