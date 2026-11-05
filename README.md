# wd4eog.github.io

WD4EOG club website and blog, live at https://wd4eog.github.io/.

A [Jekyll](https://jekyllrb.com/) site using the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme, hosted on GitHub Pages.
GitHub builds the site automatically on every push. There's no JavaScript to edit.

## Basic plan

- About us
- Blog
	- contains updates on projects of other things we do as a club
- Shack
	- equipment and radio list and photos
  - SOP for our setups: docs, PDF guides to how to use stuff
- People
	- Group pic of members
  - Have contact info and call sign and a small bio of officers

## Updating content

Most content lives in the YAML files in **`_data/`**. Edit one, commit it, and the site rebuilds.

| File | What it controls |
| --- | --- |
| `_data/meetups.yml` | Meetings and nets. The first one is featured on the home page. |
| `_data/dashboards.yml` | Dashboards: `title`, `description`, `url`, `height`. |
| `_data/calendar.yml` | The calendar's `embed_url` (and an optional `link_url`). |
| `_data/repeaters.yml` | The repeater table. |
| `_data/mesh_nodes.yml` | MeshCore routers on the Repeaters page. |
| `_data/resources.yml` | Grouped links on the Resources page. |
| `_data/club.yml` | Contact email and links at the bottom of the About page. |
| `_data/navigation.yml` | Links in the header bar. |

YAML tips: indentation matters (use spaces, not tabs), and put text in "double quotes".

Page text is in **`_pages/`** (`about.md`, `dashboards.md`, …) and the home page is **`index.md`**.
These are Markdown, and plain HTML works inside them too.
Site-wide settings (title, footer links) are in **`_config.yml`**.

- **Colors and fonts** are at the top of **`assets/css/main.scss`**.
- **Photos** live in `assets/img/`.
- The N0NBH solar widget on the Dashboards page requires full attribution. Keep its link and credit.

### Embed requirements
- URLs **must start with `https://`**. The site is served over HTTPS, and browsers block `http://` iframes.
- Grafana must allow embedding: set `allow_embedding = true` in `grafana.ini` (or use public dashboards), and allow anonymous viewing if visitors shouldn't need to log in.
- Add `&kiosk` to a Grafana URL to hide its menus.

## Previewing locally (optional)

This needs Ruby. Install it from [rubyinstaller.org](https://rubyinstaller.org/) (choose "with Devkit"), then in this folder run:

```
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000. Or just push to GitHub and check the live site.

## Deploying (GitHub Pages)

1. Push to `main` on [WD4EOG/wd4eog.github.io](https://github.com/WD4EOG/wd4eog.github.io).
2. One-time setup in the repo: **Settings → Pages → Build and deployment**, choose *Deploy from a branch*, then pick `main` and `/ (root)`.
3. The site is published at https://wd4eog.github.io/. You can set a custom domain on the same page.
