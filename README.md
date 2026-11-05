Deployed at: https://wd4eog.github.io/
Maintained by the Clemson amateur radio club

## Todo list

- [ ] About us page
	- [ ] add history
- [ ] Shack page
	- [ ] add repeater info
	- [ ] add equipment and a few selected pictures
- [ ] Officers
	- [ ] may be add bio's and a picture
- [ ] Blog
	- [ ] this is where new content will go

## Where content lives

Page text is in `_pages/` (`about.md`, `Shack.md`, `officers.md`) and the home page is `index.html`.
Blog posts go in `_posts/` as `YYYY-MM-DD-title.md` (copy an existing post for the front matter).
Lists that change often are YAML files in `_data/`:

| File | What it controls |
| --- | --- |
| `meetups.yml` | Meetings and nets (About page; the first one is also on the home page) |
| `calendar.yml` | Calendar embed URL (About page) |
| `resources.yml` | "Get licensed" links (About page) |
| `equipment.yml` | Equipment cards (Shack page) |
| `repeaters.yml` | Repeater table (Shack page) |
| `mesh_nodes.yml` | MeshCore routers (Shack page) |
| `dashboards.yml` | Grafana/embedded dashboards, `https://` only (Shack page) |
| `guides.yml` | How-to guides/SOPs; put PDFs in `assets/docs/` (Shack page) |
| `people.yml` | Group photo and officer cards (Officers page) |
| `club.yml` | Contact email and links (Officers page) |
| `navigation.yml` | Header links |

Images go in `assets/images/`. Layout styles for the cards and photo grids are in `assets/css/main.scss`; colors come from the `minimal_mistakes_skin` in `_config.yml`.
