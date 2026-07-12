# mjayjoh.github.io

Personal website of **Minjae Joh** — live at **[mjayjoh.github.io](https://mjayjoh.github.io)**.

Built with [Jekyll](https://jekyllrb.com) on the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template and hosted for free on GitHub Pages. Content is written in Markdown; each push to `master` rebuilds and republishes the site automatically.

## Navigating the site

The site is organized into tabs shown in the top navigation bar. Here's what each tab is and which file to edit to change it:

| Tab | URL | Edit this file |
| --- | --- | --- |
| **About me** (home) | `/` | [`_pages/about.md`](_pages/about.md) |
| **Education** | `/education/` | [`_pages/education.md`](_pages/education.md) |
| **Experience** | `/experience/` | [`_pages/experience.md`](_pages/experience.md) |
| **Leadership** | `/leadership/` | [`_pages/leadership.md`](_pages/leadership.md) |
| **Publications** | `/publications/` | one Markdown file per paper in [`_publications/`](_publications/) |
| **CV** | `/cv/` | [`_pages/cv.md`](_pages/cv.md) (skills, languages) + PDF at [`files/minjae-joh-resume.pdf`](files/minjae-joh-resume.pdf) |

The **sidebar** on the left (name, photo, location, email, GitHub) and site-wide settings live in [`_config.yml`](_config.yml). The left-hand photo is [`images/profile.png`](images/profile.png).

### Common edits

- **Which tabs appear in the header:** [`_data/navigation.yml`](_data/navigation.yml). Removing (or commenting out) an entry hides the tab without deleting its page; reordering the entries reorders the tabs. Some tabs from the template (Talks, Teaching, Portfolio, Blog) are commented out there.
- **Add a publication:** create a new file in [`_publications/`](_publications/) (copy an existing one as a starting point) — the Publications page and the CV's publication list update automatically.
- **Swap the resume:** save the new PDF over [`files/minjae-joh-resume.pdf`](files/minjae-joh-resume.pdf) (keep the filename) — the "Download as PDF" button keeps working.
- **Replace the profile photo:** overwrite [`images/profile.png`](images/profile.png). Use an upright, roughly square image.
- **Fonts:** headers and nav tabs use Libre Baskerville, loaded in [`_includes/head/custom.html`](_includes/head/custom.html) and wired up in [`_sass/_themes.scss`](_sass/_themes.scss).

## Running locally

Local previews use the provided Docker setup (no need to install Ruby/Jekyll). With [Docker](https://www.docker.com/) running:

```bash
docker compose up -d      # build + serve at http://localhost:4000
docker compose logs -f    # watch build output / errors
docker compose down       # stop
```

The site live-reloads when you edit Markdown or HTML. **Changes to `_config.yml`, `_data/`, or `_sass/` require a restart** (`docker compose restart`).

## Publishing changes

```bash
git add -A
git commit -m "describe your change"
git push origin master
```

GitHub Pages rebuilds within a minute or two; the update then appears at [mjayjoh.github.io](https://mjayjoh.github.io). A hard refresh (Cmd/Ctrl+Shift+R) clears cached CSS/images.

---

Template: [Academic Pages](https://github.com/academicpages/academicpages.github.io), a fork of [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) by Michael Rose. Template documentation lives at [academicpages.github.io](https://academicpages.github.io/).
