# Manoj Gali | Portfolio

Personal portfolio for **Manoj Gali**, Senior SAP CPI Integration Consultant.

**Live site:** https://manojgali.com (also at https://manoj-iflowdev.github.io)

## About

A single-page, terminal-inspired portfolio in a monochrome neo-brutalist style. It covers experience across ConocoPhillips, JPMorgan Chase, Bal Pharma and Nike, plus skills, projects, education and a contact section. There is also an interactive terminal: press `Ctrl + K`.

## Tech stack

- Plain HTML, CSS and vanilla JavaScript, with no build step and no dependencies
- Content-driven: every section is rendered from JSON files in `data/`
- Fonts: Inter and JetBrains Mono (Google Fonts)
- Hosted on GitHub Pages

## Project structure

```
.
├── index.html            # Page shell; sections are filled in by JS
├── CNAME                 # Custom domain for GitHub Pages
├── assets/
│   ├── css/style.css     # All styling
│   ├── js/main.js        # Loads data/*.json and renders each section
│   ├── img/              # Profile photo, project images, logos/
│   └── files/resume.pdf  # Downloadable resume
└── data/                 # Site content
    ├── hero.json  about.json  experience.json  skills.json
    ├── projects.json  education.json  contact.json
    └── navigation.json  footer.json  site-config.json
```

## Editing content

Edit the JSON files in `data/`, not the HTML.

| To change | Edit | Field |
| --- | --- | --- |
| Profile photo | `data/about.json` | `avatarUrl` |
| Company logo | `data/experience.json` | `logo` (per position) |
| Project cover image | `data/projects.json` | `image` (per project) |
| Work history, skills, links | the matching JSON file | |

Put images in `assets/img/` and reference them by relative path, for example `assets/img/logos/nike.svg`.

## Run locally

`main.js` loads the JSON with `fetch`, so open the site through a local server rather than `file://`:

```bash
python -m http.server 8000
# then open http://localhost:8000
```

## Deployment

Pushing to `main` publishes the site through GitHub Pages. The custom domain is set by the `CNAME` file and these DNS records at the domain registrar:

| Type | Host | Value |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `manoj-iflowdev.github.io` |

## Contact

- Email: manoj.gali695@gmail.com
- GitHub: [@manoj-iflowdev](https://github.com/manoj-iflowdev)

Company names and logos are trademarks of their respective owners and are shown to describe work history only.
