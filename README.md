# Playing to the Plants — EPK

A dark, botanical-themed electronic press kit. Built with Jekyll so
GitHub Pages builds and deploys it automatically — no build tools, no
CI to maintain.

## One-time setup

1. Create a GitHub repo and push this folder to it.
2. In the repo, go to **Settings → Pages**, set "Source" to your default
   branch (usually `main`), root folder. GitHub handles the rest.
3. In `_config.yml`:
   - Set `title`, `description`, `booking_email`, `press_email`.
   - Set `repository` to `your-github-username/your-repo-name` — needed
     for local builds (`bundle exec jekyll serve`) to resolve metadata;
     GitHub Pages itself infers this automatically once deployed.
   - Set `buttondown_username` once you've created a free account at
     [buttondown.email](https://buttondown.email).
4. Replace placeholder content:
   - Bandcamp/SoundCloud embed src values in `_data/music.yml`
   - YouTube video IDs in `_data/videos.yml`
   - Photos in `_data/gallery.yml` (drop image files into `assets/img/`)
   - Tour dates in `_data/shows.yml`
   - Nav labels/blurbs in `_data/nav.yml` if you ever add/remove a page
   - EPK text in `epk.md`
   - Band photo at `assets/img/band-photo.jpg` (referenced in `index.md`)

## Ongoing editing (for the band)

Everything you'll regularly touch is either:

- **Markdown** (`epk.md`, `index.md`, etc.) — page copy.
- **YAML data** (`_data/*.yml`) — tour dates, releases, videos, photos,
  nav links. Add or remove list items; no HTML editing needed.

Edit directly in the GitHub web UI: open the file, click the pencil icon,
edit, commit. The site rebuilds automatically in ~1 minute.

## Local preview (optional, for whoever's doing dev work)

```bash
bundle install
bundle exec jekyll serve
```

Visit `http://localhost:4000`.

## Structure

```
_config.yml           Site title, contact emails, repository, Buttondown username
_data/nav.yml          Site navigation — header + homepage link cards
_data/shows.yml        Tour dates — Events page
_data/music.yml        Releases — Music page (audio embeds)
_data/videos.yml       Videos — Videos page (YouTube embeds)
_data/gallery.yml      Photos — Pictures page
_data/links.yml        Social/streaming links — footer
_includes/             Reusable partials:
  audio-embed.html       Bandcamp/SoundCloud embed, used by music.md
  video-embed.html       YouTube embed, used by videos.md
  mailing-list.html      Buttondown signup form
  icon-sprite.html       Line icons used in nav/cards (leaf, music, film, etc.)
  hero-pttp-plant.html          Decorative animated vine graphic on homepage
  leaf-divider.html      Small decorative divider used across all pages
  logo.html               Inline band logo (color follows CSS `currentColor`)
_layouts/default.html  Page shell — header/nav/footer
assets/css/style.scss  All site styling — dark botanical theme + floral buttons
assets/img/            Photos, band logo, favicon source
index.md               Home — hero pitch, photo, nav grid, mailing list
epk.md, events.md, music.md, videos.md, pictures.md, contact.md
                        The six main site pages
```

## Design notes

- **Dark botanical theme**: deep forest green background, flower pink
  and gold accents, an organic serif (Fraunces) for headings.
- **Signature detail**: every button has a hand-drawn floral texture
  baked in as an inline SVG background — see `.btn` in `style.scss`.
- **Mobile-first nav**: the hamburger menu is pure CSS (a checkbox
  toggle), no JavaScript required.
- **Why Jekyll, not Astro/React/a CMS**: GitHub Pages builds Jekyll
  natively — no build pipeline, no Node dependencies, no CI workflow
  file to maintain or let rot. Content lives as plain markdown/YAML,
  editable directly in GitHub's web UI. If this ever needs to grow into
  something more dynamic, the content in `_data/` and the markdown
  pages migrate cleanly to a generator like Astro — only the templates
  (`_layouts/`, `_includes/`) would need rewriting.
