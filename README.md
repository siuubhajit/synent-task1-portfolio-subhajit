# Portfolio Website(Internship project for Synent Technologies)

A one-page personal site built with plain HTML and CSS. It has a light theme and a dark theme. There is no framework and no build step. The only JavaScript is the small script that handles the theme toggle.

## Files

```
.
├──index.html   # page content and the theme toggle script
├──style.css    # layout, colors, and both themes
├──photo.png
└──README.md
```
## Page sections

- Hero: Name and profile photo.
- About Me: A short introduction.
- Skills: Cards for languages, web development, and core fundamentals.
- Contact: Email, GitHub, and LinkedIn links.

## How the theme toggle works

All colors in `style.css` are CSS variables. The light values are defined in `:root`, and the dark values are defined in `:root[data-theme="dark"]`. Switching the `data-theme` attribute on the `<html>` element changes every color on the page at once.

On the first visit, a script in the `<head>` reads the visitor's system setting (`prefers-color-scheme`) and picks dark or light before the page paints, so there is no flash of the wrong theme. The ◐ button in the nav switches themes and saves the choice in `localStorage`, so it is remembered on the next visit.

## Customizing

- Colors: edit the hex values in the two theme blocks at the top of `style.css`.
- Skills: copy an `<article class="skill">` block in `index.html` to add a card.
- Text size: the skill lines use `font-size` in the `.skill .meta` rule.
- Profile photo: put the image in the same folder as `index.html`, add an `<img class="profile-pic">` inside the hero section, and style it with the `.profile-pic` rule in `style.css`.

## Layout

The content column is capped at 900px and centered. Below 600px wide, the hero heading gets smaller so it fits on a phone.

## Author

Subhajit Majee
