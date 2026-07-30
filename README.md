# AIPrototypes

A portfolio of small HTML game prototypes, each paired with a design log
explaining the intent behind it — the question being explored, the
constraints, and what changed through iteration.

Live site: `https://glencmcknight.github.io/AIPrototypes/` (after enabling
GitHub Pages — see below).

## Structure

```
/index.html                    → landing page, grid of all prototypes
/shared/style.css              → shared design system (used by every page)
/games/<project-name>/index.html     → the playable prototype
/games/<project-name>/writeup.html   → design intent / build log for that prototype
```

## Adding a new prototype

1. Duplicate `/games/_template/` into `/games/your-game-name/`.
2. Build the prototype in `index.html`. Link back to `../../shared/style.css`
   and `../../index.html` (nav is already wired up in the template).
3. Write the design log in `writeup.html`. It doesn't need to follow a
   numbered timeline unless the build genuinely happened in phases — use
   whatever structure tells the real story.
4. Add a new card to the grid in the root `/index.html`, replacing one of
   the "Next prototype slot" placeholders:

```html
<div class="panel card">
  <div>
    <div class="status">Active build</div>
    <h2>Your Game Name</h2>
    <p class="tagline">One-line description of what it explores.</p>
  </div>
  <div class="links">
    <a class="btn" href="games/your-game-name/index.html">Play</a>
    <a class="btn ghost" href="games/your-game-name/writeup.html">Design Log</a>
  </div>
</div>
```

5. Commit and push. GitHub Pages redeploys automatically.

## Enabling GitHub Pages (one-time setup)

1. Go to the repo on GitHub → **Settings** → **Pages**.
2. Under "Build and deployment", set **Source** to `Deploy from a branch`.
3. Set **Branch** to `main` and folder to `/ (root)`. Save.
4. The site will be live in a minute or two at
   `https://glencmcknight.github.io/AIPrototypes/`.
