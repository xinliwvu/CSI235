# CSI-235 · Artificial Intelligence for All

Course companion site for CSI-235 (Fall 2026), University at Albany, SUNY.
Brightspace remains the system of record for assignments, grades and the current syllabus.

## Publishing this to GitHub Pages

1. Create a repository (e.g. `csi235`) and push the contents of this folder to `main`.
2. **Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)`**.
3. The site appears at `https://<your-username>.github.io/csi235/` within a minute or two.

Everything here is static HTML, CSS and JavaScript. There is no build step and no
server-side code, which is exactly what GitHub Pages serves.

## Editing the schedule

Open `index.html` and find the `WEEKS` array near the bottom. Each entry is one row:

```js
{n:4, topic:'AI and Linguistics / Lost Knowledge',
 anchor:'A sealed Herculaneum scroll read cover to cover, June 2026',
 mats:['lostknowledge']},
```

- `mats` lists keys from the `MATERIALS` object above it. Add a new deck by adding
  one entry to `MATERIALS` and naming its key in the right week.
- `badge:'...'` puts a small label on a week (Week 7 uses it for the midterm).

## Turning on "this week"

At the top of the script, set:

```js
const FIRST_MONDAY = '2026-08-24';   // the Monday of Week 1
```

That highlights the current week in the schedule and shows a "next meeting" notice
in the header. Left empty, both features stay off and nothing else changes.

## Notes

- `.nojekyll` stops GitHub from hiding files and folders that begin with an underscore.
  Do not delete it.
- Filenames are lowercase with hyphens on purpose: GitHub Pages is case-sensitive
  even though Windows is not.
- The lecture decks work fully here except live phone voting, which needs the Claude
  runtime. The show-of-hands buttons in each poll work everywhere.
- The Lost Knowledge deck embeds images credited to the Vesuvius Challenge (CC BY-NC 4.0)
  and Wikimedia Commons (CC BY-SA 3.0 / public domain); credit lines are on the slides.
  Confirm those licences suit a public site before publishing.
