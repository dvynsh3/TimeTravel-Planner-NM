# Time-Travel Planner for NecroMerger

A mobile-first web tool for the mobile game **NecroMerger**. Plan your Time Shard spending for the Inventor, work out how many shards a run will give you, how many legendaries you need to make and how many runes they will cost you. Share your setup with a link or an exported png.

**Live site:** `https://dvynsh3.github.io/TimeTravel-Planner-NM/` 

> Unofficial fan project. Not affiliated with or endorsed by the NecroMerger developers.

## Features

- **Planner**: pick experiments and see the total Time Shard cost and which inventions it unlocks.
- **Time Shard calculator**: Devourer max level × Feats × Legendaries × Other, with a full breakdown, the amount needed to advance, and a collection screen for all 12 legendaries (per-copy, group set and completion bonuses).
- **Rune costs**: runes needed for your legendaries, an "Effective costs" mode that accounts for free stations, and a Tare button to count runes for the legendaries you will make next.
- **Spender**: enter your shards (or follow the amount from calculator) and buy experiments level by level, without going over budget.
- **Share and save**: your whole setup lives in a short link (copy it from the export menu or the address bar). Paste a link to load it, or export a PNG dashboard that carries your save inside it and load it back later from the image, or just drag and drop the PNG anywhere on the page.
- **Drallieiv Helper**: paste a link from the [Drallieiv Helper Tool](https://drallieiv.github.io/NecroMerger-Inventor/) to load its selection, or open the helper with your current planner selection. Compatible both ways.
- **Rune stock**: tell it which runes and max level stations you already have, and the rune counts shrink to what you still need (with Effective costs on).
- **Level 100+ options**: the legendary group hack, tracked in the calculator and hidden until you turn spoilers on.
- **Spoiler safe**: Level 100+ content stays hidden until you turn it on.
- **Desktop layout**: on wide screens the calculator stays on the left while the planner or spender fills the right.
- Works offline and can be added to your home screen.

## Run locally

It is a single static page, so there is no build step.

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

Opening `index.html` directly also works, but the offline support only activates over http(s).

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole app (code, data, fonts and images in one file) |
| `manifest.webmanifest`, `icon-*.png`, `apple-touch-icon.png` | Home-screen install support |
| `sw.js` | Offline support |
| `og-image.png` | Link preview image |
| `.nojekyll` | Tells GitHub Pages to serve files as they are |
| `LICENSE`, `THIRD_PARTY_NOTICES.md` | Licences and credits |

## Credits

- Game data and art: the [NecroMerger Wiki](https://necromerger.wiki.gg/) and the game itself.
- [Drallieiv Helper](https://drallieiv.github.io/NecroMerger-Inventor/): initial inspiration, link format compatibility, and a reference for experiment data.
- [UncleMumble's Time Shard calculator spreadsheet](https://docs.google.com/spreadsheets/d/1Ug5sJjNoo6mfVeCaRA4wmGCiYNOfYy8OiheXtA-aV3E/edit?usp=sharing): reference for the Time Machine formulas and rune costs.
- Fonts: Pixelify Sans and Jersey 10 (SIL Open Font License 1.1).

See `THIRD_PARTY_NOTICES.md` for details.
