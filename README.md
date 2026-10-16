# The V Lab

The home page of The V Lab: open learning guides, data analysis projects and R tooling, with a focus on large datasets and healthcare administrative data.

**Live site:** https://vthelab.com/

## Pages

| Page | What it covers |
|---|---|
| `index.html` | Lab overview, learning tracks, featured project, recent updates |
| `learn.html` | Searchable catalog of all 22 English guides across five tracks |
| `projects.html` | Project 001 (synthetic NACRS & DAD), Project 002 (Calgary housing dashboard) and the Alberta Health Data Atlas |
| `project002.html` | Project 002: Calgary Housing Observatory |
| `tools.html` | VLabR R package and Python Lab |
| `about.html` | How the lab works, track hubs, contact |

## How it connects to the other repositories

This site is a portal. Course pages stay in their own repositories and are linked from here:

- [Statistics_Study](https://github.com/The-V-Lab/Statistics_Study) — biostatistics (14 guides)
- [Epidemiology_Study](https://github.com/The-V-Lab/Epidemiology_Study) — epidemiology (3 guides)
- [Data_Visulization](https://github.com/The-V-Lab/Data_Visulization) — ggplot2 and Plotly
- [RMarkdown_Skills](https://github.com/The-V-Lab/RMarkdown_Skills) — R Markdown
- [SNOWFLAKE_Skills](https://github.com/The-V-Lab/SNOWFLAKE_Skills) and [ArcGIS_Study](https://github.com/The-V-Lab/ArcGIS_Study) — linked to the repositories until GitHub Pages is enabled there
- [Project001_HealthData](https://github.com/The-V-Lab/Project001_HealthData) and [HealthcareData_Knowledge](https://github.com/The-V-Lab/HealthcareData_Knowledge) — projects
- [VLabR](https://github.com/The-V-Lab/VLabR) and [Python_Lab](https://github.com/The-V-Lab/Python_Lab) — tools

## Publishing

Plain HTML and CSS, no build step. Hosted on [Render](https://render.com) as a Static Site (service `the-v-lab`) built from this repository: branch `main`, no build command, publish directory `.`. Every push to `main` redeploys automatically.

Custom domain **vthelab.com** (DNS at Porkbun): `ALIAS` on the root and `CNAME` on `www`, both pointing to `the-v-lab.onrender.com`; `www` redirects to the root. All canonical and Open Graph URLs use `https://vthelab.com/`, and `404.html` uses root-relative paths, so the site must be served from the domain root.

`.nojekyll` stops GitHub from running Jekyll if Pages is ever switched back to branch deploy. Shared styles live in `assets/styles.css` and use the same navy and teal palette as the course pages, with a dark-mode variant.
