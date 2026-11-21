# Time-Travel Planner for NecroMerger

A free, mobile-first web tool for the mobile game **NecroMerger**. Plan your Time Shard spending, work out how many shards a run will give you, and share your setup with a short code.

**Live site:** `https://YOUR-USERNAME.github.io/YOUR-REPO/` (replace after you publish)

> Unofficial fan project. Not affiliated with or endorsed by the NecroMerger developers.

## Features

- **Planner**: pick experiments and see the total Time Shard cost and which inventions it unlocks.
- **Time Machine calculator**: Devourer max level × Feats × Legendaries × Other, with a full breakdown, the amount needed to advance, and a collection screen for all 12 legendaries (per-copy, group set and completion bonuses).
- **Rune costs**: runes needed for your legendaries, an "Effective costs" mode that accounts for free stations, and a Tare button to count only what you add.
- **Spender**: enter your shards (or follow the calculator live) and buy experiments level by level, without going over budget.
- **Share and save**: one short save string covers everything. Export a PNG dashboard that carries your save inside it, and load it back later from the image.
- **Drallieiv Helper links**: paste a link from the community helper to load its selection, or open the helper with your current planner selection.
- **Spoiler safe**: Level 100+ content stays hidden until you turn it on.
- Works offline and can be added to your home screen.

## Run locally

It is a single static page, so there is no build step.

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

Opening `index.html` directly also works, but the offline support only activates over http(s).

## Publish on GitHub Pages

1. Create a new GitHub repository (public).
2. Upload everything in this folder to the repository root (keep `.nojekyll`).
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select **main** and **/ (root)**, then **Save**.
5. After a minute your site is live at `https://YOUR-USERNAME.github.io/YOUR-REPO/`.
6. In `index.html`, change `<meta property="og:image" content="og-image.png">` to the full URL of `og-image.png` on your site. Link previews on Discord and other apps need the full address.

To update the site later, edit `index.html` and commit. The service worker tries the network first, so visitors get the new version when they are online.

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
- [Drallieiv Helper](https://drallieiv.github.io/NecroMerger-Inventor/): link format compatibility, and a reference for experiment data.
- UncleMumble's Time Shard calculator spreadsheet: reference for the Time Machine formulas and rune costs.
- Fonts: Pixelify Sans and Jersey 10 (SIL Open Font License 1.1).

See `THIRD_PARTY_NOTICES.md` for details.
