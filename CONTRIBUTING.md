# Contributing

Thanks for helping. This repo is the static site behind [tools.panoskokmotos.com](https://tools.panoskokmotos.com): free AI tools for social impact and the Impact Compass app (`compass/`).

## Good places to start

Issues labelled [`good first issue`](https://github.com/panoskokmotos/social-impact-tools/labels/good%20first%20issue) are small and self-contained. Comment on the issue before you start so two people don't take the same one.

## Setup

No install step. It is plain HTML, CSS and JS, plus a few Python and Node build scripts.

- Python 3 and Node 20 or newer.
- Open the HTML files directly, or serve the folder: `python3 -m http.server`.

## Before you open a pull request

If you changed `compass/data.js` or `compass/data.el.js`:

1. `python3 compass/build-pages.py` (English pages and sitemap)
2. `python3 compass/build-el.py` (Greek pages)
3. `node compass/build-og.mjs` (share images)
4. `node compass/test-data.mjs` must pass
5. Bump `CACHE_NAME` in `compass/sw.js`

If you edited a file in `partials/`, run `python build.py` and commit the result.

## Content rules for the Problem Atlas

The full rules are in the header of `compass/data.js`. In short: figures are approximate and phrased that way, every problem names its sources, each intervention has an evidence rating (`strong`, `promising` or `debated`), and no real charity is named.

## Pull requests

- One change per pull request, with a short description of what and why.
- Pull requests merged during Hacktoberfest get the `hacktoberfest-accepted` label.
