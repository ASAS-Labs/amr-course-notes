# Course Notes - Static Site

A minimal, hand-crafted website for organizing academic materials.

## Quick Start

Open `index.html` in your browser. That's it.

No build step. No server. No dependencies.

---

## Structure

```
course-site/
├── index.html              ← Home page
├── template.html           ← Copy this to create new pages
├── css/
│   └── style.css           ← All styling
├── notes/
│   ├── index.html          ← Notes section index
│   └── example.html        ← Example with math/code
├── hws/
│   └── index.html          ← Homework section index
├── projects/
│   └── index.html          ← Projects section index
└── appendix/
    └── index.html          ← Appendix section index
```

---

## Adding a New Page

1. Copy `template.html` to the appropriate folder
2. Rename it (e.g., `notes/lecture-01.html`)
3. Edit the content:
   - Update `<title>`
   - Update breadcrumb
   - Update `class="active"` on nav link
   - Fix relative paths if needed (see below)
   - Add your content
4. Add a link in the section's `index.html`

### Path Reference

From files in `notes/`, `hws/`, `projects/`, or `appendix/`:
- CSS: `../css/style.css`
- Home: `../index.html`
- Other sections: `../notes/index.html`, etc.

From subdirectories (e.g., `notes/chapter1/page.html`):
- CSS: `../../css/style.css`
- Home: `../../index.html`

---

## LaTeX Math

Write math using standard LaTeX syntax:

- Inline: `$x^2$` renders as x²
- Display: `$$\int_0^1 x dx$$` renders centered

Powered by KaTeX (loaded from CDN).

---

## Code Blocks

Wrap code in `<pre><code>`:

```html
<pre><code>def example():
    return "hello"</code></pre>
```

No syntax highlighting by default (keeps it simple). Add highlight.js if you want it.

---

## Offline Use

The site works offline except for math rendering (KaTeX is loaded from CDN).

For true offline math:

1. Download KaTeX: https://github.com/KaTeX/KaTeX/releases
2. Extract to `js/katex/`
3. Update all HTML files to reference local paths:
   - `js/katex/katex.min.css`
   - `js/katex/katex.min.js`
   - `js/katex/contrib/auto-render.min.js`

---

## Customization

### Colors

Edit CSS variables in `css/style.css`:

```css
:root {
  --text: #1a1a1a;
  --accent: #2c5282;  /* Change this for different link color */
  ...
}
```

### Site Title

Search and replace "Course Notes" across all HTML files.

### Typography

The site uses system fonts. To use custom fonts, add them to CSS.

---

## Hosting Online

Upload all files to any static host:
- GitHub Pages (free)
- Netlify (free)
- Any web server (just copy the files)

No server-side processing needed.
