# stephen-huang website

Jekyll site for GitHub Pages, styled after jemdoc (classic academic homepage look).

## Preview locally

With Ruby installed:

```
bundle install
bundle exec jekyll serve
```

Or with Docker (no Ruby needed), from this folder:

```
docker run --rm -it -p 4000:4000 -v "${PWD}:/src" -v jekyll-gems:/usr/local/bundle -w /src ruby:3.3 bash -c "bundle install && bundle exec jekyll serve --host 0.0.0.0 --force_polling"
```

Then open http://localhost:4000.

## Editing

- Pages: `index.md`, `experience.md`, `projects.md`, `courses.md`, `skills.md`, `publications.md`, `blog.md`
- Left menu (categories and links): `_data/navigation.yml`
- New blog post: add `_posts/YYYY-MM-DD-title.md` with front matter `layout: post` and `title: ...`
- Styles: `assets/css/jemdoc.css`
- Page frame (menu + footer): `_layouts/default.html`
- Yellow info box: wrap text in `<div class="infoblock"><div class="blockcontent" markdown="1"> ... </div></div>`

PDFs in the project root are excluded from the build (`_config.yml`) and from git (`.gitignore`).
