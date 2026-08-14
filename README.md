# 32 Years and Counting

Our family blog, at [www.32yearsandcounting.co.uk](https://www.32yearsandcounting.co.uk).

Built with [Jekyll](https://jekyllrb.com) and hosted free on GitHub Pages. Every colour on the site is drawn from our logo — deep navy, warm gold, soft blush, and a cream paper background.

## Adding a new blog post

Create a file in `_posts/` named `YYYY-MM-DD-your-title.md`:

```markdown
---
title: "Your Post Title"
tags: [family]
author: "Jim"
excerpt: "A sentence or two describing the post."
---

Your story goes here.
```

Commit and push to `main` — GitHub Actions rebuilds and publishes the site automatically within a minute or two. You can watch progress under the repo's **Actions** tab.

## Adding a new article

Same idea, but the file goes in `_articles/` instead. Articles are for longer, less time-bound reads.

## Editing pages

- `index.html` — the homepage
- `about.md` — the About Us page (replace the placeholder story with your own!)
- `contact.html` — Contact form + guestbook. Wire the form up to [Formspree](https://formspree.io) (free) by replacing `YOUR_FORM_ID`.
- `_config.yml` — site title, tagline, and your names

## Running locally (optional)

If you ever want to preview changes on your own computer before pushing:

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

## Custom domain

The `CNAME` file points GitHub Pages at `www.32yearsandcounting.co.uk`. In your domain registrar's DNS settings, add:

- A `CNAME` record for `www` pointing to `<your-github-username>.github.io`
- (Optional) `A` records for the bare domain pointing to GitHub's IPs, so `32yearsandcounting.co.uk` also works — see [GitHub's docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site) for the current IP list.

Then in the repo's **Settings → Pages**, confirm the custom domain and enable **Enforce HTTPS** once it's verified.
