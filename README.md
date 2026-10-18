# Pseudo.NET website

Static site (plain HTML + CSS, no build step), deliberately kept **outside** the compiler solution
(`../PseudoNet`). Intended to be its own Git repository, served by GitHub Pages.

```
index.html        English home page
fr/index.html     French home page
style.css         shared styles (light/dark)
assets/           demo-tetris.gif goes here (see ../PseudoNet/docs/RECORDING.md)
.nojekyll         tells GitHub Pages to serve files as-is
```

## Before publishing
- Replace the remaining placeholder: `YOUR-PAYPAL-HANDLE` (`grep -r "YOUR-" .`).

## Publishing on GitHub Pages
Repository: `pseudonet-lang/pseudonet-lang.github.io` (the `<org>.github.io` name makes the site live at the root),
public, push this folder, then *Settings → Pages → Deploy from branch → main / root*. The site appears at
`https://pseudonet-lang.github.io/` (French: `/fr/`).

## Preview locally
```bash
python -m http.server 8080
```
then open <http://localhost:8080/>.

## Adding a language
Copy `fr/index.html` to `<lang>/index.html`, translate, and add a link in the nav of the other pages.
