# Quick Start Guide

## Setup (5 minutes)

### 1. Create GitHub Repository

**For username.github.io:**
```bash
# Repository name: username.github.io
# Example: johndoe.github.io
```

**For project site:**
```bash
# Repository name: my-blog
# Update _config.yml: baseurl: "/my-blog"
```

### 2. Upload These Files

Push all files to your new repository:

```bash
git init
git add .
git commit -m "Initial commit: Jekyll blog"
git branch -M main
git remote add origin https://github.com/username/repo-name.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to repository **Settings**
2. Click **Pages** in sidebar
3. Source: **Deploy from a branch**
4. Branch: **main**, folder: **/ (root)**
5. Click **Save**

Wait 2-3 minutes, then visit your site!

### 4. Personalize

Edit `_config.yml`:
- Change `title`, `description`, `author`, `email`
- Update `url` to your GitHub Pages URL
- Update social media usernames

### 5. Set Up Comments (Optional)

1. Enable Discussions in repo Settings → Features
2. Visit [giscus.app](https://giscus.app)
3. Enter your repo name and get config values
4. Update `_config.yml` with Giscus settings

## Writing Your First Post

### Create a new file: `_posts/2026-01-24-my-first-post.md`

```markdown
---
layout: post
title: "My First Post"
date: 2026-01-24 10:00:00 +0000
categories: [blog]
tags: [first-post, hello-world]
---

Hello world! This is my first blog post.

## A heading

Some content here...
```

### Commit and push:

```bash
git add _posts/2026-01-24-my-first-post.md
git commit -m "Add first blog post"
git push
```

Your post will appear in 2-3 minutes!

## Post Frontmatter Template

```markdown
---
layout: post
title: "Your Title Here"
date: YYYY-MM-DD HH:MM:SS +0000
categories: [category1, category2]
tags: [tag1, tag2, tag3]
author: Your Name
---
```

## Testing Locally (Optional)

```bash
# Install Ruby and Bundler first
bundle install
bundle exec jekyll serve

# Visit http://localhost:4000
```

## File Naming Convention

Posts MUST follow this format:
```
YYYY-MM-DD-title-with-dashes.md
```

Examples:
- ✅ `2026-01-24-hello-world.md`
- ✅ `2026-12-31-year-end-review.md`
- ❌ `hello-world.md` (missing date)
- ❌ `2026-1-24-hello.md` (month needs leading zero)

## Common Tasks

### Add a new page
Create `contact.md` in root:
```markdown
---
layout: page
title: Contact
permalink: /contact/
---

Your content...
```

### Change colors
Edit `assets/css/main.css` CSS variables:
```css
:root {
  --color-accent: #2563eb; /* Change this */
}
```

### Update navigation
Edit `_includes/header.html` nav links

## Troubleshooting

**Site not updating?**
- Check Actions tab for build errors
- Ensure post filename has correct date format
- Verify frontmatter is valid YAML (proper indentation)

**Comments not working?**
- Enable Discussions in repo settings
- Verify Giscus config in `_config.yml`
- Check that repo is public

## Support

- 📖 Full README: See `README.md`
- 🔧 Jekyll Docs: https://jekyllrb.com/docs/
- 🚀 GitHub Pages: https://docs.github.com/en/pages

Happy blogging!
