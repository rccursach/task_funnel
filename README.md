# Task Funnel

A single-page task funnel for when a new task makes you lose the thread of the one
you were on. Tasks pile up in the wide intake; heavier ones sink toward the narrow
throat. You pick up **one** task at a time, work it, and push it through.

- **Weight** = `important +1` + `urgent +3` + `delegable +5`, added up.
  Heavier sinks toward the throat; delegable tasks drift down so you clear/hand them off first.
- **Tie-break**: same weight → the task waiting longest sinks lower.
- **Throat**: exactly one active task. Finish it (*Done*) or *Put back* before picking another.
- **Decanted**: finished tasks, today's first; *See more* for earlier days.
- Colour is a calm hue ramp by weight (pale yellow → green → blue → purple). No red.

## Storage

Everything lives in your browser's `localStorage` (key `task-funnel/v1`). Nothing
leaves the page. Use **Export** for a JSON backup and **Import** to restore or move
between machines — clearing browser data wipes it otherwise.

## Run it

Just open `index.html`, or serve the folder:

```bash
python3 -m http.server 4173
```

## Deploy to GitHub Pages

1. Push this folder to a GitHub repo with `index.html` at the root.
2. Repo **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
   branch `main`, folder `/ (root)`.
3. Open the published URL.

Keyboard: `n` focuses the new-task field.
