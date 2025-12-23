# Jekyll Site Setup Guide

## What I've Created

Your site is now configured with **Just the Docs** theme. Here's the structure:

```
AMR_WEBSITE/
├── _config.yml          # Jekyll configuration
├── Gemfile              # Ruby dependencies
├── .gitignore           # Git ignore rules
├── index.md             # Homepage
├── notes/
│   ├── index.md         # Notes section
│   └── example-lyapunov.md  # Example note
├── assignments/
│   └── index.md         # Assignments section
├── projects/
│   └── index.md         # Projects section
├── appendix/
│   └── index.md         # Appendix section
└── course-site/         # Old HTML version (ignored by git)
```

---

## Option 1: Let GitHub Pages Build It (Easiest)

You don't need to install anything locally. Just push to GitHub:

```bash
cd /home/vivek/Desktop/AMR_WEBSITE
git add .
git commit -m "Migrate to Jekyll with Just the Docs theme"
git push
```

Then enable GitHub Pages:
1. Go to https://github.com/vivekmattam02/amr-notes/settings/pages
2. Under "Source", select: **Deploy from a branch**
3. Branch: **main**, Folder: **/ (root)**
4. Click **Save**

Your site will be live at: `https://vivekmattam02.github.io/amr-notes/`

---

## Option 2: Preview Locally (Optional)

If you want to preview changes before pushing:

### Install Ruby and Jekyll

```bash
# Install Ruby (if not already installed)
sudo apt-get update
sudo apt-get install ruby-full build-essential zlib1g-dev

# Install bundler
gem install bundler

# Install dependencies
cd /home/vivek/Desktop/AMR_WEBSITE
bundle install

# Serve the site locally
bundle exec jekyll serve
```

Then open: `http://localhost:4000/amr-notes/`

---

## Adding New Content

### Add a New Note

1. Create a file: `notes/your-topic.md`
2. Add front matter:

```yaml
---
layout: default
title: Your Topic Title
parent: Notes
nav_order: 2
---
```

3. Write your content in Markdown
4. Commit and push (or preview locally first)

### Add Math

- Inline: `$x^2 + y^2 = r^2$`
- Display: `$$\int_0^\infty e^{-x^2} dx$$`

### Add Code

```python
def example():
    return "Hello"
```

---

## Next Steps

1. **Push to GitHub** (see Option 1 above)
2. **Enable GitHub Pages** in repository settings
3. **Wait 1-2 minutes** for the site to build
4. **Visit your live site**: https://vivekmattam02.github.io/amr-notes/

The old `course-site/` folder is now ignored by git (in `.gitignore`). You can delete it if you want, or keep it as a backup.
