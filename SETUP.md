# Setup Notes

This profile only renders correctly if the repo is named exactly like your
GitHub username — e.g. `github.com/anshumanpanda156/anshumanpanda156`.
Create that repo if it doesn't exist yet, then drop these files at its root.

## 1. Replace the username
`README.md` uses `anshumanpanda156` as a placeholder in every widget URL
(stats, top languages, streak, snake, connect links). If that isn't your
real GitHub username, find-and-replace it throughout the file.

## 2. Enable the snake workflow
`.github/workflows/snake.yml` builds the contribution graph and pushes it
to an `output` branch.

- **Settings → Actions → General → Workflow permissions** — set to
  **Read and write permissions**.
- Run it once manually (**Actions tab → Generate Snake Animation →
  Run workflow**) so the `output` branch exists immediately, rather than
  waiting for the first scheduled run.

## 3. A note on the streak widget
This uses `streak-stats.demolab.com` rather than the old
`github-readme-streak-stats.herokuapp.com` URL you'll see in a lot of older
READMEs — Heroku discontinued free dynos, so the herokuapp.com host is no
longer reliable. `demolab.com` is the project's current maintained endpoint.

## 4. Fill in your projects
The "Projects" section ships with three realistic placeholder entries
(AI Chat Application, Document Workspace, Language Learning Platform) so it
never reads as an empty template. For each one, replace:

- The `<h4>` title → your actual project name
- The description → one real line on what it does
- The two `#` links → your repo and live URL (delete the "Live" link
  entirely if there isn't one — including the `·` separator before it)

Nothing else in the card needs to change. To add a fourth project, copy one
full block (from `<h4>` down through its links line) along with the
preceding divider-dots line, and paste it before the closing divider.

## 5. Fonts and rendering
Banner, dividers, and footer are plain SVG using system fonts — no external
font loading, so they render identically in light and dark mode without
flicker or fallback issues.

## 6. Optional: visitor counter
This version intentionally leaves out a visitor-count badge to keep the
footer quiet. If you want one back, add this line above the footer image:

```html
<p align="center"><sub><img src="https://komarev.com/ghpvc/?username=anshumanpanda156&style=flat-square&color=8b5cf6&label=Profile+Views" alt="Visitor count" /></sub></p>
```
