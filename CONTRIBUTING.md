# Contributing

Thanks for wanting to help! This project is deliberately small and simple — please keep it that way.

## Ground rules

- **No dependencies, no build step.** Each page is a single self-contained HTML file with vanilla JS, Web Audio API and inline SVG. It must keep working offline from a `file://` URL.
- **Keep the visual style**: dark background `#111`, accent red `#ec3013`, Archivo font.
- UI text is in English.

## How to test

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then click through: metronome (play/stop, count-in, cells), the three automated exercises ("PLAY WITH METRONOME" buttons — they are mutually exclusive), and both secondary pages.

## Non-code contributions

You don't need to write code to contribute. Especially welcome:

- **Music notation review** — the rhythmic cells are drawn by hand in SVG (beams, stems, triplet brackets); corrections from people who read music are gold.
- **Theory / exercise design** — better degree labels, scale choices, fingering advice.
- Open an issue describing the problem (a screenshot + what it should look like is enough).

## Architecture notes (index.html)

- One **lookahead scheduler**: `schedule()` runs on a 25 ms `setInterval` and books audio events ~0.12 s ahead on the Web Audio clock.
- A **master gain** node cuts all sound instantly on stop.
- Visual highlights are `setTimeout`s guarded by the playing state.
- The three automated exercises (scale walk, shape connecting, cycle of 4ths) share the scheduler and are mutually exclusive.

## Pull requests

1. Fork, branch, make the change.
2. Test in at least one desktop and one mobile browser if the change touches layout or audio.
3. Keep PRs small and focused — one fix or feature per PR.
