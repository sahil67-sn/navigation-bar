# Navigation Bar Website

A small multi-page HTML/CSS project that demonstrates a reusable navigation bar. Five pages share one stylesheet and link to each other, and each page has its own gradient background.

## Files

| File | Page | Background gradient (45deg) |
|------|------|-----------------------------|
| `index.html` | Home (landing page) | Olive to orange |
| `aboutus.html` | About Us | Blue to orange |
| `gallery.html` | Gallery | Aqua to orange |
| `achivment.html` | Achievements | Brown to orange |
| `contactus.html` | Contact Us | Grey to orange |
| `style.css` | Shared styles for the navigation bar | n/a |

## Features

- Rounded, semi-transparent white navigation bar centered on the page
- Five links: **Home**, **About Us**, **Gallery**, **Achivements**, **Contact Us**
- Links are evenly spaced with flexbox
- Hover effect: each menu item zooms to 1.5x
- A different gradient background on every page, defined in that page's own `<style>` block
- Shared navigation styles in a single `style.css`

## Project Structure

```
.
├── index.html
├── aboutus.html
├── gallery.html
├── achivment.html
├── contactus.html
├── style.css
└── README.md
```

Keep all files in the same folder so the links and the stylesheet resolve.

## Getting Started

No installation or build step is needed.

1. Download or clone the project and keep all files in one folder.
2. Open `index.html` in any modern web browser.
3. Use the navigation bar to move between pages.

## How It Works

- Each page links to `style.css`, which styles the navigation bar (`.box`), the menu list (`ul`), the items (`li`) and the links (`a`).
- Each page sets only its own full-height container (`.con`) and background gradient inline in the page.
- `.con` is a flex container, which centers the navigation bar both vertically and horizontally.
- The navigation HTML is the same on all five pages.

## Tech Stack

- HTML5
- CSS3 (flexbox, `linear-gradient`, `rgba` colors, `:hover` with `transform`)

## Known Issues

- **Invalid HTML structure:** `<a>` tags wrap `<li>` items directly inside `<ul>`. Browsers display it, but valid HTML expects `<li><a>...</a></li>`.
- **Spelling:** "Achivements" and the file name `achivment.html` should be "Achievements" / `achievements.html`.
- **No active-page indicator:** the current page is not highlighted in the menu.
- **Placeholder content:** each page only shows the heading "Navigation Bar" and the menu, with no real page content.
- **Not responsive:** large text (`xx-large`), fixed percentages and `100vh` mean the menu can look crowded or overflow on small screens.
- **Repeated code:** the navigation markup is copied into all five files, so any change has to be made five times.
- All pages share the default title "Document".

## Possible Improvements

- Fix the `<ul>` / `<li>` / `<a>` structure
- Correct the "Achievements" spelling and rename the file
- Highlight the active page
- Add a unique `<title>` and real content for each page
- Add media queries or a hamburger menu for mobile screens
- Use a `<nav>` element and a `position: sticky` bar
- Move the shared gradient and layout CSS into `style.css` with a per-page class
