# Communication Primer (Jekyll + GitHub Pages)

This repository contains a Jekyll website scaffold for introducing non-technical audiences to major schools of communication theory and their use in 21st-century communication problems, including AI-mediated contexts.

## Site structure

The scaffold includes:

- Home page: `/home/runner/work/comm-primer/comm-primer/index.md`
- Subpage 1: `/home/runner/work/comm-primer/comm-primer/transmission-view-and-its-limits.md`
- Subpage 2: `/home/runner/work/comm-primer/comm-primer/meaning-and-culture.md`
- Subpage 3: `/home/runner/work/comm-primer/comm-primer/interpretation-and-power.md`
- Subpage 4: `/home/runner/work/comm-primer/comm-primer/interpretation-and-intention.md`
- Subpage 5: `/home/runner/work/comm-primer/comm-primer/what-the-reader-should-do.md`
- Subpage 6: `/home/runner/work/comm-primer/comm-primer/how-i-built-this-site.md`
- Shared layout: `/home/runner/work/comm-primer/comm-primer/_layouts/default.html`
- Stylesheet: `/home/runner/work/comm-primer/comm-primer/assets/css/style.scss`
- Image folder: `/home/runner/work/comm-primer/comm-primer/assets/images/`
- Jekyll config: `/home/runner/work/comm-primer/comm-primer/_config.yml`
- GitHub Actions workflow: `/home/runner/work/comm-primer/comm-primer/.github/workflows/jekyll.yml`

## Publish and deployment behavior

The GitHub Actions workflow builds and deploys the site to GitHub Pages:

- Trigger: every push to `main`
- File: `.github/workflows/jekyll.yml`
- Build action: `actions/jekyll-build-pages@v1`
- Deploy action: `actions/deploy-pages@v4`

To use GitHub Pages deployment, make sure Pages is configured in your repository settings to use **GitHub Actions** as the source.

## Create and edit content

1. Open any `.md` page file listed above.
2. Keep the front matter block (`---`) at the top.
3. Update:
   - `title` for the page name
   - `permalink` only if you want to change the URL
   - body text for your analysis, examples, and references
4. Save and commit; the workflow runs automatically on `main`.

### Add a new page

1. Create a new Markdown file in the repository root, for example `new-topic.md`.
2. Add front matter:

   ```yaml
   ---
   layout: default
   title: New Topic
   permalink: /new-topic/
   ---
   ```

3. Add your content below front matter.
4. Add a navigation link in `/home/runner/work/comm-primer/comm-primer/_layouts/default.html` inside the `<nav>` list.

## Work with images

- Put image files in `/home/runner/work/comm-primer/comm-primer/assets/images/`
- Reference images from Markdown like this:

  ```markdown
  ![Describe the image for accessibility]({{ '/assets/images/your-image-file.png' | relative_url }})
  ```

Always use descriptive alt text for accessibility.

## Customize site-wide settings

Edit `/home/runner/work/comm-primer/comm-primer/_config.yml`:

- `title`: site title
- `description`: default site description
- `url`: should stay `https://darbyclose.github.io` unless username changes
- `baseurl`: should stay `/comm-primer` unless repository name changes
- `repository`: should stay `Darbyclose/comm-primer` unless owner/repo changes

After changing config, commit and push to `main` so GitHub Actions rebuilds the site.

## Customize the visual design

Edit `/home/runner/work/comm-primer/comm-primer/assets/css/style.scss` and adjust CSS variables in `:root`.

### Primary variables

- `--bg`: page background
- `--surface`: card/background for content blocks
- `--surface-alt`: subtle background accents
- `--text`: main text color
- `--muted`: subdued text color
- `--primary`: primary highlight color
- `--primary-soft`: soft hero/header tone
- `--accent`: interactive accent color
- `--border`: border color
- `--focus`: keyboard focus outline/link emphasis

Keep text/focus contrast high for readability and accessibility.

## Accessibility checklist for new content

- Use heading hierarchy in order (`h1` then `h2`, etc.).
- Keep paragraph length manageable.
- Add alt text for all images.
- Use descriptive link text.
- Avoid color-only meaning in diagrams or callouts.
- Test keyboard navigation after adding major layout content.

## Local preview (optional)

If you want to run the site locally, install Ruby and Jekyll, then use:

```bash
bundle exec jekyll serve
```

If your environment does not include dependencies yet, install them first with Bundler.
