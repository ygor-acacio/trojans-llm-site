# Logic Trojans in LLM-Generated Financial Code — project site

Static website for an undergraduate capstone project (Escola Politécnica, University of
São Paulo): can a multi-agent defense detect **logic trojans** that large language models
insert into financial code, and does the way the agents are combined matter?

**Live site:** https://YOUR-USER.github.io/YOUR-REPO/  ← update after enabling Pages

## What this repository is

Just the website — plain HTML/CSS/JS, no build step, no backend, no trackers.

```
index.html      the whole site (Overview · The problem · Approach · Results · Demonstration · About)
styles.css      styling (light + dark, follows the viewer's system theme)
app.js          tab navigation + the offline demo logic
config.js       one flag to show/hide the interactive demo
data/           the pre-recorded samples the demo replays
assets/         figures
```

## Publish with GitHub Pages

1. Push this repository to GitHub.
2. **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*,
   Branch = `main`, Folder = `/ (root)`. Save.
3. The site goes live at `https://YOUR-USER.github.io/YOUR-REPO/` after a minute.
   (A `.nojekyll` file is included so GitHub serves the files as-is.)

## The interactive demo

The **Demonstration** tab is **off by default**. To turn it on, open `config.js` and set
`demoEnabled: true`, then commit and push. Set it back to `false` to hide it again.

The demo is fully offline: it never calls any AI model and never runs any code in the
browser. It only replays samples and reviewer verdicts that were recorded during the
experiment (`data/demo_data.json`), so there is no usage cost — the flag only controls when
the demo is publicly visible.

## Credits

Ygor Acacio Maria, advised by Prof. Dr. Victor Takashi Hayashi and Prof. Dr. Marcos Antonio
Simplicio Junior. Department of Computer Engineering and Digital Systems (PCS), Escola
Politécnica, USP. Partial results were presented at the AISec Dev workshop (CBSoft 2026).
