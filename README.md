# Arlo's Chaos Hour 🧸

A tiny, self-contained browser game — no build step, no dependencies to install. Everything (HTML, CSS, JS) lives in one file: `index.html`.

## Play it locally
Just double-click `index.html`, or run a quick local server:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000

## Publish it on GitHub Pages (2 minutes)

1. Create a new repo on GitHub and push this folder to it:
   ```bash
   git init
   git add .
   git commit -m "Arlo's Chaos Hour"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
2. On GitHub, go to **Settings → Pages**.
3. Under "Build and deployment", set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. Save. Your game will be live at:
   ```
   https://<your-username>.github.io/<repo-name>/
   ```
   (GitHub Pages usually takes 30–60 seconds to go live after the first save.)

That's it — no build tools, no npm, no config files needed.

## What's in this version

- **Mobile-first**: canvas scales responsively (crisp on retina phones), redesigned d-pad + scream button, tuned for touch (no double-tap/zoom issues, no 300ms input delay).
- **More robust**: 90-second timed run with an end screen, high score saved locally, auto-pause when you switch tabs/apps, manual pause (P key or the ⏸ button), and defensive error handling around storage.
- **Steven the cat** 🐈: wanders the house, can be petted for a coin (mostly), occasionally hisses if you push your luck, and every so often knocks something off the table on his own.

## Ideas for taking it further

- **Sound**: a few short SFX (tiny Web Audio beeps need no asset files) for coins, yelps, and the scream.
- **Difficulty ramp**: have Mom and Dad speed up slightly as the timer runs down.
- **More rooms/characters**: a second floor, a baby sibling, a vacuum robot to dodge.
- **Combo scoring**: bonus coins for chaining interactions quickly.
- **Daily challenge seed**: fixed RNG seed per day so friends can compare scores.
- **Share button**: generate a shareable "I scored X coins" image or link.
- **Accessibility**: colorblind-safe palette check, `prefers-reduced-motion` support to tone down particle effects.
- **PWA**: add a manifest + service worker so it can be "installed" and played offline on a phone home screen.
