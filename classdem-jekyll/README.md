# ClassDem Website

**Class Struggle in Ancient Greek Democracy**  
UKRI/ERC Frontier Research Grant 2024–2029

A Jekyll-based website for GitHub Pages with blogging capability.

---

## Quick Start

### Option 1: Deploy to GitHub Pages (Recommended)

1. **Create a GitHub repository**
   - Go to github.com and create a new repository called `classdem` (or your preferred name)
   - Make it public

2. **Upload these files**
   - Upload all files from this folder to the repository
   - Or use Git: `git init`, `git add .`, `git commit -m "Initial commit"`, `git push`

3. **Enable GitHub Pages**
   - Go to repository Settings → Pages
   - Source: "Deploy from a branch"
   - Branch: `main` (or `master`)
   - Click Save

4. **Your site will be live at:**
   - `https://yourusername.github.io/classdem/`
   - Or configure a custom domain (e.g., `classdem.ed.ac.uk`)

### Option 2: Local Development

```bash
# Install Ruby and Bundler first, then:
bundle install
bundle exec jekyll serve

# Site will be at http://localhost:4000
```

---

## Managing Content with Claude Code

This site is designed to be easily managed with Claude Code. Here are common tasks:

### Adding a News Post / Blog Entry

Ask Claude Code:
> "Add a news post about [event/announcement]. The date is [date]."

Posts go in `_posts/` with filename format: `YYYY-MM-DD-title-slug.md`

```markdown
---
title: "Your Post Title"
date: 2025-01-15
category: News  # or: Event, Publication, Announcement
author: ClassDem Team
---

Your content here in Markdown.
```

### Updating Team Members

Ask Claude Code:
> "Add [Name] as a new postdoctoral fellow working on [topic]."

Team data is in `_data/team.yml`. Add entries under the appropriate section.

### Adding a Publication

Ask Claude Code:
> "Add a new publication: [title] by [authors] in [venue]."

Edit `_pages/publications.md` directly.

### Updating the Project Description

Ask Claude Code:
> "Update the project page to include [new information]."

Edit `_pages/project.md`.

---

## File Structure

```
classdem-jekyll/
├── _config.yml          # Site configuration
├── _data/
│   └── team.yml         # Team member data
├── _includes/
│   ├── header.html      # Navigation
│   └── footer.html      # Footer
├── _layouts/
│   ├── default.html     # Base template
│   ├── home.html        # Homepage
│   ├── page.html        # Standard pages
│   ├── post.html        # Blog posts
│   └── research.html    # Research strand pages
├── _pages/
│   ├── project.md       # Project description
│   ├── team.md          # Team page
│   ├── publications.md  # Publications
│   └── blog.md          # News listing
├── _posts/              # Blog posts (news, events)
│   └── YYYY-MM-DD-title.md
├── _research/           # Research strand pages
│   ├── economy.md
│   ├── culture.md
│   ├── politics.md
│   └── intersection.md
├── assets/
│   ├── css/style.css    # Stylesheet
│   └── images/          # Images (add team photos here)
├── index.md             # Homepage content
├── Gemfile              # Ruby dependencies
└── README.md            # This file
```

---

## Common Editing Tasks

### To add a team photo:
1. Add image to `assets/images/team/`
2. Update `_data/team.yml`:
   ```yaml
   - name: Mirko Canevaro
     image: /assets/images/team/canevaro.jpg
   ```

### To add funder logos:
1. Add logo images to `assets/images/logos/`
2. Edit `_includes/footer.html` to include `<img>` tags

### To change colours or fonts:
Edit `assets/css/style.css` — the CSS variables at the top control the colour scheme.

---

## Writing Content in Markdown

All content pages use Markdown. Quick reference:

```markdown
# Heading 1
## Heading 2
### Heading 3

**bold text**
*italic text*

[Link text](https://example.com)

![Image alt text](/assets/images/example.jpg)

- Bullet point
- Another point

1. Numbered item
2. Another item

> Blockquote text

---  (horizontal rule)
```

---

## Custom Domain Setup

To use a custom domain like `classdem.ed.ac.uk`:

1. Add a `CNAME` file to the repository root containing just:
   ```
   classdem.ed.ac.uk
   ```

2. Configure DNS with your domain provider (University IT)

3. Update `_config.yml`:
   ```yaml
   url: "https://classdem.ed.ac.uk"
   ```

---

## Need Help?

- **Jekyll documentation**: https://jekyllrb.com/docs/
- **GitHub Pages**: https://docs.github.com/en/pages
- **Markdown guide**: https://www.markdownguide.org/

For site-specific questions, ask Claude Code — it can read and edit all these files directly.

---

*Last updated: January 2025*
