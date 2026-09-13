# IGCSE Threshold & Paper Analyzer

A single-page, no-build web app for Cambridge IGCSE students. Select your subjects, enter Mock 1 and Mock 2 marks for every paper/component you sit, and get a paper-by-paper improvement plan with grade estimates.

**Not affiliated with Cambridge International.** This is an independent student tool.

## Features

- Subject selection for 0607, 0610, 0620, 0625, 0417, 0510, 0500 and 3226
- Paper-combination/option selection where Cambridge uses more than one component combination for a subject
- Entry for every paper's Mock 1 and Mock 2 marks, plus optional weak-topic notes per paper
- Mark validation (no negative marks, marks capped at each paper's maximum, blank fields treated as "not entered" rather than zero)
- Overall percentage, grade estimate, and Mock 1 → Mock 2 trend per subject
- Where verified Cambridge grade-threshold data is available for the selected option, it is shown as a clearly labelled **historical threshold estimate** (never presented as an official prediction); where no verified data exists, the app says so instead of guessing
- Paper-by-paper priority ranking (high / medium / low) with weak-topic notes shown alongside the paper that needs them
- A/A* planning targets with a small buffer, clearly labelled as planning targets, not official Cambridge requirements
- Results dashboard summarising how many selected subjects sit in each grade band
- Save/clear inputs to your browser's local storage — nothing is sent to a server
- Print-friendly report view
- Responsive layout from 320px mobile up to desktop, with visible keyboard focus states and no reliance on colour alone

## How to use

1. Open `index.html` (locally or via GitHub Pages).
2. Tick every subject you take.
3. For each subject, choose the paper combination/option you actually sit.
4. Enter Mock 1 and/or Mock 2 marks for each paper. Leave a box blank if you haven't sat that mock — it will not be treated as zero.
5. Optionally add weak-topic notes under any paper.
6. Click **Analyze results** to see your dashboard and per-subject reports.
7. Use **Save locally** to keep your inputs in this browser for next time, **Print report** for a clean printout, or **Reset** to start over.

## Run locally

No build step or dependencies are required.

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
# then just open index.html in a browser, e.g.:
open index.html      # macOS
xdg-open index.html  # Linux
start index.html      # Windows
```

## Deploy with GitHub Pages

1. Push this repository to GitHub with `index.html` at the repository root.
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch", choose your default branch and the `/ (root)` folder.
4. Save. GitHub will publish the site at `https://<your-username>.github.io/<your-repo>/`.

No `package.json`, build process, API keys, or backend are needed — it's a static HTML file.

## Data and threshold disclaimer

Cambridge publishes official grade thresholds after each examination series, and they vary by series because thresholds are set according to paper difficulty in that series. This app stores a small set of **verified historical threshold figures** (converted to a percentage of each option's published overall maximum mark) for the sessions and options that could be sourced. Where a subject/option has no verified threshold data on record, the app states this explicitly rather than inventing a number. Component maximum marks shown during entry are approximate where the exact figure could not be verified against an official source — check your own exam paper/timetable for the precise figure if it matters to you.

Nothing produced by this app is an **official Cambridge threshold**. Anything derived from historical data is labelled a **historical threshold estimate**, and A/A* targets are labelled **planning targets**. Treat every grade estimate as a planning aid, not a guarantee.

## Privacy / no backend

- All calculations run entirely in your browser.
- No marks, notes, or any other data are uploaded to a server.
- No accounts, analytics, or tracking of any kind.
- "Save locally" only writes to this browser's `localStorage`, and "Clear saved data" removes it. Nothing leaves your device either way.

## Independence notice

This project is an independent, community-built student tool. It is **not produced, endorsed, or affiliated with Cambridge International** (Cambridge Assessment International Education) in any way. Always confirm your actual grades and thresholds against official Cambridge sources.
