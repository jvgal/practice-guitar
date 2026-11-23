# practice-guitar

Free, open-source guitar practice app. Runs in the browser, nothing to install, works offline.

**Live:** https://jvgal.github.io/practice-guitar/ · [Leia em português](README.pt-BR.md)

## Exercises

- **Metronome** with the 7 core rhythmic cells (eighths, shuffle, triplets, sixteenths, gallops, syncopation), live notation and adjustable BPM.
- **Interactive fretboard** — scale + chord in the 5 CAGED shapes, with an optional **cycle of 4ths** mode that changes the shape along with the key (G→C→F… / E→D→C…).
- **Scales note by note** — hear each note, see its name and degree on the fretboard. Major, natural minor, harmonic minor, minor/major pentatonic and blues.
- **Connecting the shapes** — climb the scale across all 5 positions, up the whole neck.
- **Build the scale** — fill in the degrees, submit for grading and get a score.
- **Chromatic warm-up** — 1-2-3-4 and finger permutations.

## Pages

| File | What it is |
|---|---|
| `index.html` | Main page: metronome, CAGED shapes, scales, cycle of 4ths |
| `scale-builder.html` | Build-the-scale quiz |
| `warmup.html` | Chromatic warm-up |

`montar-escala.html` and `psicomotor.html` are redirect stubs kept so old links don't break.

## Running

Just open `index.html` in a browser. No build step, no dependencies — plain HTML + vanilla JS, Web Audio API and SVG.

For local development with a server:

```bash
python3 -m http.server 8000
```

## Contributing

PRs welcome — see [CONTRIBUTING.md](CONTRIBUTING.md). You don't need to code to help: feedback on music notation, theory and exercise design is just as valuable.

## License

MIT — use it, copy it, make it better.

Made in Serra da Mantiqueira, Brazil. 🎸
