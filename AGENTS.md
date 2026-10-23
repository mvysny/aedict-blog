# Aedict blog — AGENTS.md

## What this is

The Aedict Dictionary Blog, available for reading at https://mvysny.github.io/aedict-blog/.

## Design docs

| File | Owns | Loaded |
|---|---|---|
| `README.md` | the pitch and the site's URL | — |
| `AGENTS.md` (this) | invariants, the map, conventions, commands | every turn |

Every fact lives in exactly one of these; the others link to it.

## Invariants

- **A post's URL is the title part of its filename, for good.** `permalink: /:title/` makes `_posts/2019-09-10-Daijirin.md` live at `/aedict-blog/Daijirin/`; renaming the file breaks the `../Daijirin/` links in other posts and every inbound link from outside.
- **Site-internal URLs carry `{{ site.baseurl }}` or are relative.** The site lives under `/aedict-blog`, so a root-absolute `/images/x.png` 404s.
- **A repo-only file goes into `exclude:` in `_config.yml`.** Jekyll publishes every file it isn't told to skip, `AGENTS.md` included.
- **Only plugins the `github-pages` gem whitelists.** Pages builds in legacy mode with no Gemfile; anything else is silently ignored.

## Module map

- `_posts/` — the blog posts, one Markdown file each.
- `about.md`, `404.md`, `index.html` — the standalone pages and the post list.
- `_layouts/`, `_includes/`, `_sass/`, `style.scss` — the Jekyll Now v1.2.0 theme.
- `_config.yml` — site name, footer links, `baseurl`, permalink, kramdown, plugins.
- `images/` — images for posts and pages; so far only the 404 page's.

## Conventions

- **Jekyll Now on GitHub Pages.** Jekyll and the theme own the rendering; this repo owns the posts, the pages and `_config.yml`.
- **Post files are `_posts/YYYY-MM-DD-Title.md`**, zero-padded, with `layout: post` and `title:` front matter.
- **Markdown is kramdown in GFM mode**, rouge highlighting; posts use `#` headings below the layout's title.
- **Pages are root-level `.md` files** with `layout: page`, `title:` and an explicit `permalink:`.
- **Theme files stay upstream's** unless a change is needed; the site's identity lives in `_config.yml`.
- **Pushing to `master` publishes.** No branches or PRs; commit messages say what changed (older history uses a placeholder `a`).

## Commands

- `gem install github-pages && jekyll serve` — local preview at http://127.0.0.1:4000/aedict-blog/.
- `gh api repos/mvysny/aedict-blog/pages/builds/latest` — status and error of the last Pages build after a push.

## Maintenance of this file

Loaded every turn; cap 34 KB, a module's own `AGENTS.md` 10 KB. Over it, in this order:
delete what has no home — status, history, class lists, what the code already says; trim
each line to its fact plus one clause and send the explanation home — why →
`design/decisions.md`, how across symbols → `design/architecture.md`, how in one symbol →
its doc comment, what upstream does → `design/research.md`; only then a module's own
`AGENTS.md`, peripheral modules first, never the core. Never paraphrase a lazy entry into a
line here.
