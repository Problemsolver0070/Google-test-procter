# Google-test-procter

A minimal proctored test wrapper for Google Forms. Single-page HTML.

Detects tab switches, app switches, window minimize, and fullscreen exit. Terminates the test immediately on any of those events.

## Usage

Open `index.html` in a browser. The wrapper embeds the Google Form in an iframe and listens for focus, visibility, and fullscreen events on the host page.

## States

- **Start screen** — instructions and a "Begin test" button. Requesting fullscreen happens on click.
- **Test active** — fullscreen iframe of the form. Any tab/window/fullscreen change terminates the test with no second chance.

## Notes

- iframe click loses focus from the host page, which is why the blur listener excludes iframe-focused state (handled in `index.html`).
- Renaming repo to `proctor` (correcting typo) is on the to-do list.
