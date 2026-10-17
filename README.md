# Syntropy AI website

Static one-page site for Syntropy AI — data and AI services on Microsoft Azure, Databricks and Snowflake.
No build step: plain HTML, CSS and JavaScript, ready for GitHub Pages.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole site (styles and scripts are inline) |
| `404.html` | Page shown for broken links |
| `.nojekyll` | Tells GitHub Pages to serve files as-is |

## Publish on GitHub Pages

A `<name>.github.io` address needs a GitHub account **or organisation** called `<name>`.
For `syntropy-agi.github.io`:

1. Create a free GitHub organisation named `syntropy-agi` (github.com → your avatar → Your organizations → New organization).
2. In that organisation, create a **public** repository named exactly `syntropy-agi.github.io`.
3. Upload these files to the repository root (Add file → Upload files), or push with git:

   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/syntropy-agi/syntropy-agi.github.io.git
   git push -u origin main
   ```

4. Repository → Settings → Pages → Source: **Deploy from a branch**, Branch: `main`, folder `/ (root)`.
5. After a minute or two the site is live at https://syntropy-agi.github.io

## Things to edit before going live

- **Contact email** — change `CONTACT_EMAIL` near the top of the `<script>` in `index.html`
  (the placeholder `hello@syntropy-ai.example` is used in the visible link and the form).
- **Location line** in the contact section ("Based in Copenhagen…").
- **Sectors** list and **engagement models** wording, to match what you actually offer.

## Custom domain (optional)

If you buy a domain such as `syntropy-ai.com`, add it under Settings → Pages → Custom domain,
then create the DNS records GitHub shows you. Update the `canonical` and `og:url` tags in `index.html` to the new address.
