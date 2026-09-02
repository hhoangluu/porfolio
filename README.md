# Breach Games — portfolio

One static page. No build step, no dependencies, no backend.

    index.html      the page
    assets/         images and the gameplay clip
    play/           Mahjong Zen, the full production build
    .nojekyll       GitHub Pages serves the files as-is

Served at https://hhoangluu.github.io/porfolio/

## Two things to know before editing

**The game under `play/` is a built artefact.** It comes from the Mahjong Zen
repo (`npm run build`, then copy `dist/` here). Editing it here is pointless —
the next build overwrites it.

**It only runs on hostnames the build allows.** Mahjong Zen ships a sitelock
that refuses to run anywhere it was not published, so `hhoangluu.github.io` is
named explicitly in `src/platform/sitelock.ts` in the game repo. A custom domain
needs adding there and a rebuild, or the page renders a "wrong site" panel
instead of the game.

This copy is built with analytics disabled, so portfolio traffic never reports
into the live game's project and no keys are published here.
