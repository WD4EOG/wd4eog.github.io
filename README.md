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

The site has four sections: **About**, **Blog**, **Shack** and **People**.

| File | What it controls |
| --- | --- |
| `_data/meetups.yml` | Meetings and nets (About page). The first one is also featured on the home page. |
| `_data/calendar.yml` | The calendar's `embed_url` (and an optional `link_url`), on the About page. |
| `_data/resources.yml` | Grouped learning links under "Get licensed" on the About page. |
| `_data/equipment.yml` | Equipment cards on the Shack page. |
| `_data/repeaters.yml` | The repeater table on the Shack page. |
| `_data/mesh_nodes.yml` | MeshCore routers on the Shack page. |
| `_data/dashboards.yml` | Dashboards under "Live data" on the Shack page: `title`, `description`, `url`, `height`. |
| `_data/guides.yml` | How-to guides (SOPs) on the Shack page. Put PDFs in `assets/docs/`. |
| `_data/people.yml` | The group photo and officer cards on the People page. |
| `_data/club.yml` | Contact email and links at the bottom of the People page. |
| `_data/navigation.yml` | Links in the header bar. |

YAML tips: indentation matters (use spaces, not tabs), and put text in "double quotes".

Page text is in **`_pages/`** (`about.md`, `shack.md`, …) and the home page is **`index.md`**.
These are Markdown, and plain HTML works inside them too.
Site-wide settings (title, footer links) are in **`_config.yml`**.

- **Colors and fonts** are at the top of **`assets/css/main.scss`**.
- **Photos** live in `assets/img/`.
- The N0NBH solar widget on the Shack page requires full attribution. Keep its link and credit.

### Writing a blog post
Add a Markdown file to **`_posts/`** named `YYYY-MM-DD-short-title.md` (for example `2026-11-04-replacing-the-antenna.md`) that starts with:

```
---
title: "Your post title"
---
```

Then write the post below it. The newest posts show up on the Blog page and the home page.

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
