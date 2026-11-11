# Gridset Cell Changer

A browser-based tool for adding commands to matching cells in Grid 3 `.gridset`
and `.grid3user` files. Files are processed locally in your browser and are not
uploaded.

Open [`index.html`](./index.html) from a local static web server. For example:

```powershell
python -m http.server 8000
```

Then visit `http://localhost:8000`. The app uses JSZip and AACProcessors from
their public CDNs, so an internet connection is required to load the app and
its validation support.

## Features

- Filter cells by commands, auto-content type, inserted text, caption and grid
  name.
- Preview matching cells before adding commands.
- Avoid duplicate commands and choose where new commands are inserted.
- Save, load and combine reusable JSON change schemas.
- Process standalone gridsets or selected gridsets in a `.grid3user` archive.
- Undo changes and download a verified result.

Always test edited gridsets in Grid 3 before distributing them.

## Tests

Serve this directory over HTTP as above, then open
[`tests/cell-changer.html`](./tests/cell-changer.html). The regression tests run
in the browser and report their results on the page.

## Deploying with GitHub Pages

The app is a static site. In the repository settings, enable GitHub Pages from
the default branch and select the repository root as the source. The root
[`index.html`](./index.html) is the app entry point.

The cell changer was extracted from
[`simonjudge/gridset-style-changer`](https://github.com/simonjudge/gridset-style-changer).
