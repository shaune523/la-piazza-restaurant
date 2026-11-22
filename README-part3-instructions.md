# La Piazza: Part 3 installation instructions

These are additions to the existing four HTML files in your GitHub repository. **Keep all your existing HTML and images.** Colors/fonts below are a provisional restaurant-themed palette; compare with the Part 1 style guide and adjust CSS variables and font choices as needed.

## 1. Upload two new files to the repository root
- `styles.css`
- `script.js`

## 2. Make the following edits to EACH of the four HTML pages

Inside `<head>`, before `</head>`, add:

```html
<link rel="stylesheet" href="styles.css">
<script src="script.js" defer></script>
```

Change `<header>` to `<header class="site-header">`.

Immediately before the opening `<nav aria-label="Main navigation">` tag, insert:

```html
<button class="menu-toggle" type="button" aria-label="Open navigation menu"
        aria-expanded="false" aria-controls="main-navigation">
  <span></span><span></span><span></span>
</button>
```

Change `<nav aria-label="Main navigation">` to:

```html
<nav id="main-navigation" class="site-nav" aria-label="Main navigation">
```

Change `<footer>` to `<footer class="site-footer">`.

On each page, add `aria-current="page"` to its current navigation link. For example, on menu.html use:

```html
<a href="menu.html" aria-current="page">Menu</a>
```

For order and menu CTA links, apply `class="button"` or `class="button-secondary"` to the opening anchor tag. Examples:

```html
<a class="button" href="https://www.lapiazzarest.com">Order Now</a>
<a class="button-secondary" href="menu.html">View Our Menu</a>
```

## 3. Optional README replacement

```markdown
# La Piazza Restaurant Website

GD107 Final Project — Shaun Eggleston

## Pages
- Home (`index.html`)
- About (`about.html`)
- Menu (`menu.html`)
- Contact (`contact.html`)

## Part 3 progress
- Responsive custom CSS with mobile, tablet, and desktop layouts
- Restaurant-themed colors, typography, spacing, buttons, and image styling
- JavaScript hamburger menu with animated icon, keyboard accessibility, and working links
- External `styles.css` and `script.js` shared by all four HTML pages

## Technologies
HTML5, CSS3 (Flexbox and Grid), vanilla JavaScript

## Running locally
Open `index.html` in a web browser. All four HTML files, `styles.css`, `script.js`, and the `images` folder must be in the repository.

## Testing
Test at 375px mobile, 800px tablet, and 1280px desktop. On mobile, open/close the menu and verify every link. Check images and the map on the Contact page.
```

## 4. Test, then push
- At 375px, the navigation button should show and the links should open when tapped.
- At 800px, show full navigation and 2-column cards.
- At 1280px, show full navigation and 3-column cards.
- Check all links and image files, and validate CSS at https://jigsaw.w3.org/css-validator/.
- Commit with message: `Add responsive Part 3 styles and mobile navigation`.
- Confirm the public repository contains both new files and the updated README before submitting its URL.
