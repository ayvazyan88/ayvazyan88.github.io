---
layout: post
title: "Getting Started with Jekyll for GitHub Pages"
date: 2026-01-15 14:30:00 +0000
categories: [tutorial]
tags: [jekyll, github-pages, tutorial, static-site]
author: Your Name
---

Jekyll is a fantastic static site generator that's perfect for blogs, documentation sites, and personal portfolios. In this post, I'll share what I've learned about using Jekyll with GitHub Pages.

## Why Jekyll?

Jekyll has several advantages that make it ideal for blogging:

- **Simplicity**: Write in Markdown, no database required
- **Speed**: Static HTML means lightning-fast page loads
- **Free Hosting**: GitHub Pages provides free, reliable hosting
- **Version Control**: All content is tracked with Git
- **Flexibility**: Highly customizable with Liquid templates

## Basic Workflow

The workflow is beautifully simple:

1. Write your post in Markdown
2. Add proper frontmatter
3. Commit and push to GitHub
4. Your site updates automatically

### Example Post Structure

Here's what a typical post looks like:

```markdown
---
layout: post
title: "My Post Title"
date: 2026-01-15
categories: [tutorial]
tags: [jekyll, guide]
---

Your content here...
```

## Key Features

### Markdown Support

Jekyll uses [Kramdown](https://kramdown.gettalong.org/), which supports:

- **Bold** and *italic* text
- [Links](https://jekyllrb.com)
- Lists (ordered and unordered)
- Code blocks with syntax highlighting
- Tables, blockquotes, and more

### Liquid Templating

Jekyll uses Liquid for templating. Here's a simple example:

```liquid
{% raw %}
{% for post in site.posts limit:5 %}
  <h2>{{ post.title }}</h2>
  <p>{{ post.excerpt }}</p>
{% endfor %}
{% endraw %}
```

### Collections & Data Files

You can organize content beyond just posts:

- **Pages**: Static pages like About, Contact
- **Collections**: Custom content types
- **Data Files**: YAML, JSON, or CSV data

## Tips for Success

1. **Use Descriptive Filenames**: `2026-01-15-descriptive-title.md`
2. **Leverage Frontmatter**: Add metadata for better organization
3. **Test Locally**: Use `bundle exec jekyll serve` before pushing
4. **Keep it Simple**: Don't over-complicate your theme
5. **Use Git Branches**: Test major changes in separate branches

## Common Pitfalls

### 1. Incorrect Date Format

Always use `YYYY-MM-DD` in filenames and frontmatter:

```markdown
# Good
date: 2026-01-15

# Bad
date: 01/15/2026
```

### 2. Missing Frontmatter

Every post needs valid frontmatter:

```markdown
---
layout: post
title: "Title"
date: 2026-01-15
---
```

### 3. Forgetting to Update _config.yml

Remember to restart your local server after changing `_config.yml`:

```bash
# Stop the server (Ctrl+C)
# Restart it
bundle exec jekyll serve
```

## Useful Resources

Here are some helpful links I've bookmarked:

- [Jekyll Documentation](https://jekyllrb.com/docs/) - Official docs
- [GitHub Pages Docs](https://docs.github.com/en/pages) - Hosting guide
- [Kramdown Syntax](https://kramdown.gettalong.org/syntax.html) - Markdown reference
- [Liquid Docs](https://shopify.github.io/liquid/) - Templating language

## Conclusion

Jekyll makes blogging simple and enjoyable. The combination of Markdown, Git, and free hosting on GitHub Pages is hard to beat. Whether you're documenting your learning journey or sharing expertise, Jekyll provides a solid foundation.

Give it a try, and you might never want to go back to traditional CMS platforms!

---

*Have questions about Jekyll? Leave a comment below!*
