# Frikk Jarl — Digital Business Card

A single-file, black-and-white digital business card. The name and title sit
quietly to the left; a procedural ASCII tornado owns the rest of the screen —
a real-time storm with parallax cloud decks, statistically-timed lightning, and
a "create lightning" button.

No build step, no dependencies, no external requests. Just open `index.html`.

## Run it

```bash
open index.html          # macOS — or double-click the file
```

To serve it (nicer for phones on the same network):

```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```

## What's inside

- **Procedural tornado** — one density function (funnel silhouette × rising
  corkscrew noise) drawn through an ASCII density ramp on a `<canvas>`.
- **Parallax sky** — eight cloud decks, nearer ones bigger/faster/brighter; the
  two closest pass *in front of* the funnel.
- **Lightning** — a 1/f "storm clock" plus Hawkes self-excitation give surges
  and lulls that feel real rather than metronomic; strikes are born from visible
  cloud, flash the whole deck (graded by proximity), and fire realistic
  multi-stroke flicker. Press **create lightning** for a big one.
- **Light + dark** — dark is the full storm; light is a clean ink-on-paper
  vortex (no clouds, no lightning). Toggle top-right; follows OS theme too.
- **Responsive** — the funnel bends around the name; on phones it becomes a
  full-screen storm with the card floating over it.

Everything is inline in `index.html` (~30 KB). Runs at ~30 fps for a fraction of
one CPU core.
