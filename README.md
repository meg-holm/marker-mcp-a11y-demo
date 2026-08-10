# Bramblewood Coffee Co. (a11y demo site)

A small fictional coffee shop website, built to demo Marker.io's MCP tool for
scanning and fixing accessibility issues.

## Pages

- `index.html` - home page
- `menu.html` - product listing
- `contact.html` - contact form

## Known accessibility issues (intentional)

These were added on purpose so there's something for the MCP tool to find and fix:

- Missing `lang` attribute on `<html>`
- Images with no `alt` text throughout
- Low-contrast text (`.muted-text`, `.price`, footer, nav links, button text)
- Heading levels skip from `h1` straight to `h3`/`h4`
- Clickable `<div>` elements used instead of `<button>`/`<a>` (nav links, add-to-cart,
  subscribe, submit, custom checkbox) - not keyboard accessible, no focus state
- `outline: none` globally, with no visible focus alternative
- Form inputs with placeholder text only, no associated `<label>`
- Duplicate `id="search"` on two different form elements (`menu.html`)
- Icon-only buttons/links with no accessible name (social icons, add-to-cart)
- Vague link text ("click here")
- A `<table>` with no header row or scope attributes

## Running locally

It's static HTML, so just open `index.html` in a browser, or serve it:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.
