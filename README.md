# jinghu.media

Personal site for [Jing Hu](https://www.2ndorderthinkers.com/) — one page, no tracking, no build step.

## How it works

- `index.html` — the whole site, single file. Edit it, push, done.
- `posts.json` — the last 5 Substack posts. **Do not edit by hand** — overwritten by the RSS job.
- `.github/workflows/update-rss.yml` — runs every 2 hours, pulls `https://www.2ndorderthinkers.com/feed`, rewrites `posts.json`, commits only if something changed. Safe to trigger manually from the Actions tab.
- `CNAME` — tells GitHub Pages the custom domain is `jinghu.media`.

## Local preview

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```
