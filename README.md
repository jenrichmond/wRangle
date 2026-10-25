# Data Wrangling Tool (Quarto book)

A step-by-step guide to cleaning messy psychology survey data in R, using the
tidyverse (dplyr, tidyr, readr, lubridate), janitor, naniar, and here.

Work through it from raw import to an analysis-ready dataset, or jump straight
to whichever task matches what you're stuck on.

Built by [Reveal Research](https://www.revealresearch.org).

## Editing

Each step lives in its own chapter file, written in plain Markdown:

| File | Chapter |
|---|---|
| `index.qmd` | Welcome, how to use this, "Jump to a task" grid |
| `01-setup.qmd` | Set up your project |
| `02-import.qmd` | Import your data (CSV, Excel, SPSS, Qualtrics) |
| `03-overview.qmd` | Get an overview & spot problems |
| `04-names.qmd` | Clean & rename columns |
| `05-types.qmd` | Variable types |
| `06-missing.qmd` | Missing data |
| `07-dates.qmd` | Dates & durations |
| `08-recode.qmd` | Recoding & scale scores |
| `09-reshape.qmd` | Reshape wide & long |
| `10-filter.qmd` | Inclusion & exclusion |
| `11-duplicates.qmd` | Duplicates |
| `12-combine.qmd` | Combine files |
| `13-validate.qmd` | Check your data is clean |
| `14-export.qmd` | Save your clean data |

Chapter order and the part groupings ("Getting started", "Cleaning", …) are
set in `_quarto.yml`. Colours live in `styles.scss`; the code colours match
RStudio's Cobalt theme and live in `cobalt.theme`.

### Building blocks used in the chapters

- `## Heading {#sec-some-id}` — each step; the `{#sec-...}` id is what links point to.
- `::: {.question}` — the "which of these is you?" box at the top of a chapter.
- `::: {.pkgs}` — the "Packages:" line under each step heading.
- `::: {.callout-tip}` — the tip box.
- `::: {.callout-note collapse="true"}` — a collapsible box (used for the problem checklist).
- `::: {.next-steps}` — the "Where to next" links.
- Links between steps: `[link text](06-missing.qmd#sec-missing-recode)`.

Code is in plain ` ```r ` blocks, so the book renders without running any R.

## Building the site

In RStudio, open the folder as a project and click **Render Book** (Build
pane), or from a terminal run:

```
quarto render
```

The site is written to `docs/`. To publish with GitHub Pages, commit `docs/`
and set Settings → Pages → Source to the `main` branch, `/docs` folder. Use
`quarto preview` for a live preview that refreshes as you edit.

## Suggesting changes

Found something confusing, missing, or wrong? Open an
[issue](https://github.com/jenrichmond/wRangle/issues/new), or use the
"Edit this page" link on any page of the book.

## License

Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) —
share and adapt freely, with credit. Code is illustrative; adapt variable and
file names to your own dataset.
