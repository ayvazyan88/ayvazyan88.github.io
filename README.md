# Personal Blog

A minimalist static blog built with Jekyll and hosted on GitHub Pages. Simply add a Markdown file, commit it, and your new blog post appears automatically.

## Features

- **Minimalist Design**: Clean, focused on content with generous whitespace
- **Tags & Categories**: Organize your posts and help readers discover related content
- **Comments System**: Powered by Giscus (GitHub Discussions)
- **Syntax Highlighting**: Beautiful code blocks via Rouge
- **Responsive Design**: Works perfectly on all devices
- **SEO Optimized**: Built-in SEO tags and sitemap generation
- **RSS Feed**: Automatic feed generation for subscribers
- **Fast & Secure**: Static site = lightning fast and inherently secure

## Quick Start

### 1. Fork or Clone This Repository

**For a User/Organization Site** (recommended):
- Create a new repository named `username.github.io` (replace `username` with your GitHub username)
- Your site will be available at `https://username.github.io`

**For a Project Site**:
- Create a repository with any name (e.g., `my-blog`)
- Your site will be available at `https://username.github.io/my-blog`
- Update `baseurl: "/my-blog"` in `_config.yml`

### 2. Configure Your Site

Edit `_config.yml` to personalize your blog:

```yaml
title: My Personal Blog
description: Your blog description here
author: Your Name
email: your.email@example.com
url: "https://username.github.io"
baseurl: "" # Leave empty for user site

# Update social links
social:
  github: your-github-username
  twitter: your-twitter-handle
  linkedin: your-linkedin-username
```

### 3. Set Up Comments (Optional)

To enable comments via Giscus:

1. Visit [giscus.app](https://giscus.app)
2. Enter your repository name (must be public with Discussions enabled)
3. Enable GitHub Discussions in your repo: Settings → Features → Discussions
4. Copy the configuration values and update `_config.yml`:

```yaml
comments:
  enabled: true
  giscus:
    repo: "username/repo-name"
    repo_id: "YOUR_REPO_ID"
    category: "General"
    category_id: "YOUR_CATEGORY_ID"
```

### 4. Enable GitHub Pages

1. Go to your repository Settings
2. Navigate to Pages (in the sidebar)
3. Under "Build and deployment":
   - Source: Deploy from a branch
   - Branch: `main` (or `master`), folder: `/ (root)`
4. Click Save

GitHub will automatically build and deploy your site within a few minutes.

## Writing Posts

### Create a New Post

1. Create a new file in the `_posts` directory
2. Name it using the format: `YYYY-MM-DD-title.md`
3. Add frontmatter and content:

```markdown
---
layout: post
title: "Your Post Title"
date: 2026-01-24 10:00:00 +0000
categories: [blog, tutorial]
tags: [jekyll, web-development]
author: Your Name
---

Your content goes here...
```

### Frontmatter Options

- `layout`: Use `post` for blog posts
- `title`: Post title (required)
- `date`: Publication date (required)
- `categories`: Array of categories (optional)
- `tags`: Array of tags (optional)
- `author`: Author name (optional, defaults to site.author)
- `comments`: Set to `false` to disable comments on a specific post

### Example Workflow

```bash
# 1. Create a new post
touch _posts/2026-01-24-my-awesome-post.md

# 2. Edit the file and add your content

# 3. Commit and push
git add _posts/2026-01-24-my-awesome-post.md
git commit -m "Add new blog post: My Awesome Post"
git push origin main

# 4. Wait 2-3 minutes for GitHub Pages to rebuild
# Your post is now live!
```

## Local Development

To test your blog locally before pushing:

### Prerequisites

- Ruby (version 2.7 or higher)
- Bundler gem

### Setup

```bash
# Install dependencies
bundle install

# Run local server
bundle exec jekyll serve

# Your site will be available at http://localhost:4000
```

### Tips

- Use `--livereload` flag for automatic browser refresh: `bundle exec jekyll serve --livereload`
- Use `--drafts` flag to preview draft posts: `bundle exec jekyll serve --drafts`
- Draft posts go in the `_drafts` folder (without date in filename)

## Project Structure

```
.
├── _config.yml          # Site configuration
├── _posts/              # Blog posts (YYYY-MM-DD-title.md)
├── _layouts/            # Page templates
│   ├── default.html     # Base template
│   ├── post.html        # Blog post template
│   └── page.html        # Static page template
├── _includes/           # Reusable components
│   ├── head.html        # HTML head section
│   ├── header.html      # Site header
│   ├── footer.html      # Site footer
│   └── comments.html    # Comments section
├── assets/
│   ├── css/
│   │   └── main.css     # Main stylesheet
│   └── js/              # JavaScript files
├── index.html           # Homepage
├── about.md             # About page
├── archive.html         # Archive page (all posts)
├── tags.html            # Tags page
├── Gemfile              # Ruby dependencies
└── README.md            # This file
```

## Customization

### Colors & Styling

Edit `/assets/css/main.css` and modify the CSS variables at the top:

```css
:root {
  --color-text: #1a1a1a;
  --color-accent: #2563eb;
  --font-sans: -apple-system, BlinkMacSystemFont, 'Segoe UI', ...;
  --max-width: 720px;
}
```

### Adding Pages

Create a new `.md` file in the root directory:

```markdown
---
layout: page
title: My New Page
permalink: /my-page/
---

Page content here...
```

Then add a link in `_includes/header.html`.

### Changing Navigation

Edit `_includes/header.html` to add/remove navigation links.

## Troubleshooting

### Site Not Building

1. Check the Actions tab in your GitHub repository for build errors
2. Ensure all required fields in `_config.yml` are filled
3. Verify post filenames follow the `YYYY-MM-DD-title.md` format
4. Check that frontmatter is valid YAML

### Comments Not Showing

1. Verify GitHub Discussions is enabled in your repository
2. Double-check Giscus configuration in `_config.yml`
3. Ensure the repository is public
4. Check browser console for JavaScript errors

### Local Build Fails

```bash
# Update dependencies
bundle update

# Clear cache and rebuild
bundle exec jekyll clean
bundle exec jekyll build
```

## GitHub Pages Limitations

- Sites are limited to 1GB
- Soft bandwidth limit of 100GB per month
- Maximum 10 builds per hour
- Some Jekyll plugins are not supported (this theme uses only supported plugins)

## Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Giscus Documentation](https://giscus.app)
- [Markdown Guide](https://www.markdownguide.org/)

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

If you encounter issues or have questions:

1. Check existing [GitHub Issues](https://github.com/username/repo/issues)
2. Open a new issue with detailed information
3. Refer to Jekyll and GitHub Pages documentation

---

**Happy blogging!** Start writing and share your thoughts with the world.
