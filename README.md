# Personal website — Mohammad Shoaib Babar

A static personal and academic homepage. No build step, no framework, no
dependencies: three files do the work and a browser can open them directly.

## What is here

```
index.html            the whole page — all content lives in this file
assets/css/style.css  layout, typography, light and dark themes, print styles
assets/js/main.js     nav highlighting, theme toggle, footer year
assets/favicon.svg    monogram used as the browser tab icon
.nojekyll             tells GitHub Pages to serve the files as-is
robots.txt            allows search engines to index the site
```

## Viewing it locally

Double-clicking `index.html` works. To see it exactly as a web server would
serve it, run a local server from this folder:

```bash
python -m http.server 8000
```

Then open <http://localhost:8000>.

## Editing the content

All text sits in `index.html`, in plain sections you can read top to bottom:
`about`, `research`, `education`, `publications`, `experience`, `projects`,
`skills`, `awards`, `contact`. To add a job or a degree, copy an existing
`<article class="entry">` block and change the date and the text inside it.
To add a project, copy an `<article class="card">` block.

Two places repeat information and need updating together if details change:

- the email address and LinkedIn link appear in the masthead, in the contact
  section at the bottom, and in the structured-data block near the end of the file
- the page title and description appear in `<title>`, in the `description`
  meta tag, and in the Open Graph tags

## Themes

The page follows the operating system's light or dark setting by default. The
small round button in the navigation bar overrides that, and the choice is
remembered in the browser. Clearing site data resets it to the system setting.

## Printing

A print stylesheet reformats the page into a clean single-column CV: the
navigation, the theme button and the collapsible thesis abstract are dropped,
colours flatten to black on white, and entries are kept from splitting across
pages. Print to PDF from the browser to get a shareable copy.

## Deployment

The site is published with GitHub Pages from the `main` branch and is live at
<https://mshoaibb9010.github.io>. Pushing to `main` republishes it; the change
is usually live within a minute or two.
