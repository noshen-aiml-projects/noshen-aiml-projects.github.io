# noshen-aiml-projects.github.io

Personal portfolio of **Noshen Habib** — AI/ML Engineer and UC Berkeley MIDS student.

Live site: <https://noshen-aiml-projects.github.io>

Built with [Jekyll](https://jekyllrb.com/) and the [al-folio](https://github.com/alshedivat/al-folio) starter.

## Where things live

| What             | File(s)                                                                  |
| ---------------- | ------------------------------------------------------------------------ |
| Site settings    | `_config.yml`                                                            |
| About / homepage | `_pages/about.md`, photo at `assets/img/prof_pic.jpg`                    |
| Projects         | `_projects/*.md` (ordered by `importance`)                               |
| Articles         | `_posts/YYYY-MM-DD-title.md`                                             |
| CV (page + PDF)  | `_data/cv.yml` — the PDF is re-rendered by CI with RenderCV on each push |
| Social links     | `_data/socials.yml`                                                      |

## Local development

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```
