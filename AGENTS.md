# zettai.github.io

The personal website of Luis Salas Gonzales, served by GitHub Pages at
[zettai.github.io](https://zettai.github.io). It is public: every file
committed here is on the web unless `_config.yml` excludes it.

## What this is

One hand-written `index.html` with inline CSS, no framework and no build
step, plus images, icons, `robots.txt`, `sitemap.xml` and two search-engine
verification files. Articles written in `~/code/ror` are published here as
hand-written HTML pages after they are published on the internal wiki.

## Setup

Clone over the personal SSH alias, never over HTTPS through `gh`:

```bash
git clone git@github.com-zettai:zettai/zettai.github.io.git ~/code/zettai.github.io
```

Git picks the personal identity (`luisszkl@gmail.com`) from the remote URL.
Check with `git config user.email` before the first commit.

## Commands

| Task | Command |
| --- | --- |
| preview | `python3 -m http.server 8000` in the repo root, then open http://localhost:8000; stop it when done |
| build | none; GitHub Pages builds on push |
| check | `~/code/ror/bin/ror audit zettai.github.io` |

## Conventions

- Public site: no employer, client or internal wiki material. Only public
  sources may be linked or quoted.
- GitHub Pages runs Jekyll here. Files starting with `.` or `_` are not
  published; anything else is, unless it is in the `exclude` list in
  `_config.yml`. Add every repo-only file (such as this one) to that list.
- Keep the two verification files (`google7816415f591fb717.html` and the
  `.txt` file at the root) where they are.
- When a page is added or changed, update its `<lastmod>` in `sitemap.xml`.
- Commits are scoped to the files you changed, by path.
- Push only with the owner's approval, as the `zettai` account over the SSH
  alias. Never log `gh` in as `zettai`.

## Gotchas

- A push publishes within a minute or two; there is no staging.
- Images are served as committed; keep them small.
