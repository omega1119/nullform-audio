# Nullform Audio

Website for [nullform.audio](https://nullform.audio)

## Structure

```
nullform-audio/
├── CNAME                    # Domain configuration
├── README.md
├── index.html               # Redirect shell (language detection) into en/
├── favicon.svg
├── assets/
│   ├── css/
│   │   └── styles.css       # Main stylesheet
│   ├── fonts/               # Self-hosted Inter
│   ├── images/              # Product screenshots
│   └── js/
│       ├── main.js          # Theme toggle, nav, footer, cookie consent
│       └── redirect.js      # Language redirect logic
└── en/                      # English locale
    ├── index.html           # Landing page
    ├── privacy.html         # Privacy policy
    ├── terms.html           # Terms of service
    ├── links/index.html     # Social links page (not localised)
    └── products/
        ├── pentagraph.html  # PentaGraph 5-band graphic EQ
        └── decaychain.html  # DecayChain bit-crusher and wavetable distortion
```

The site files live at the repository root, not in a `docs/` folder.

## Localization

The site is English only today. To add a language, copy `en/` to a new locale folder
(e.g. `de/`), translate it, update the `data-languages` JSON on every page, and add a
`data-redirect-<lang>` attribute for it to the root `index.html` script tag.

## Local Development

See [LOCAL_DEV.md](LOCAL_DEV.md). Quick start:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080/en/`

## Deployment

The site is deployed via GitHub Pages from the root of the `main` branch. A push to
`main` publishes live, so open a pull request for changes.