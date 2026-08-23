# Vistora — website

Marketing site for [Vistora](https://vistora.thestreamic.in), a free, local-first video editor for Windows. Published by [The Streamic](https://thestreamic.in).

Static HTML, no build step. `serve.cjs` runs a local server for development.

## Pages

| File | Purpose |
|---|---|
| `index.html` | Home |
| `features.html` | Full feature list |
| `download.html` | Windows installer download (pulls from GitHub Releases) |
| `whats-new.html` | Release notes, latest release first |
| `docs.html` | Documentation |
| `contact.html` | Contact |
| `vistora-privacy-policy.html`, `flowdeck-privacy-policy.html` | Privacy policies |

## Releasing a new version

The download links on this site point at GitHub Releases on the app repo, e.g.:

```
https://github.com/Thestreamic/vistora/releases/download/v<version>/Vistora-Setup-<version>.exe
```

When a new Vistora build ships:

1. Publish the installer as a GitHub Release tagged `v<version>` (e.g. `v1.4.0`) with `Vistora-Setup-<version>.exe` attached.
2. Update every `1.x.x` version string and download link across `index.html`, `features.html`, `contact.html`, `docs.html`, and `download.html` to match.
3. Add a new release-note entry at the top of `whats-new.html` — new features, then fixes — matching the existing card layout.
4. Commit and push to `main`. The site is served from this branch.

## Local development

```bash
node serve.cjs
```

## Current release

**v1.4.0** — screen/window picker, system audio + microphone recorded together, auto-minimise on Record, Screen & voice mode, Add Audio Layer.
