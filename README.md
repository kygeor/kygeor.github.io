# kygeor.github.io

Personal academic website of Kyriakos C. Georgiou, built with [al-folio](https://github.com/alshedivat/al-folio) (v1.x) and served by GitHub Pages at <https://kygeor.github.io>.

## Where things live

| What                   | File                                                                            |
| ---------------------- | ------------------------------------------------------------------------------- |
| Bio, photo, address    | `_pages/about.md`, `assets/img/prof_pic.jpg`                                    |
| Publications           | `_bibliography/papers.bib` (`selected = {true}` puts a paper on the front page) |
| News on the front page | `_news/*.md`                                                                    |
| Writings (blog posts)  | `_posts/YYYY-MM-DD-slug.md`                                                     |
| Unpublished drafts     | `_drafts/` (see `_drafts/post-template.md`)                                     |
| Talks                  | `_pages/talks.md`                                                               |
| Teaching & outreach    | `_pages/teaching.md`                                                            |
| CV page                | `_pages/cv.md`                                                                  |
| Social links           | `_data/socials.yml`                                                             |
| Repositories page      | `_data/repositories.yml`                                                        |
| Site settings          | `_config.yml`                                                                   |

## Writing a post

Copy `_drafts/post-template.md` to `_posts/2026-12-01-my-post.md`, edit, commit and push. MathJax is enabled, so `$$ ... $$` works inline and in display, and `\begin{equation}` with `\label`/`\eqref` works too.

## Deployment

Every push to `main` runs `.github/workflows/deploy.yml`, which builds the site and pushes the result to the `gh-pages` branch. In the repository settings, **Pages → Build and deployment → Source** must be set to **Deploy from a branch**, branch `gh-pages`, folder `/ (root)`.

## Local preview (optional)

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

or with Docker: `docker compose up` and open <http://localhost:8080>.

The framework's own documentation is in `docs/` (start with `docs/CUSTOMIZE.md`).
