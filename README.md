# S Projects website

A standalone, lightweight static website intended for the `s-creator01/s-creator01.github.io` GitHub Pages user-site repository. No app repository is included or modified.

## Preview locally

Run `python3 build.py` after editing project records, then `python3 -m http.server 8000` in this directory and open <http://localhost:8000/>. Python is needed only to regenerate the pages; the generated HTML and assets are static.

## Update projects

Edit `projects.json`: each record supplies its name, slug, status, descriptions, platform and optional `website` and `source` URLs. Run `python3 build.py` and commit both the JSON and regenerated HTML. Only add a download or store link after verifying it and the release status. To add a project, add a record and its icon mapping in `build.py`; the project page and listings are generated together. Edit the downloads page template in `build.py` when verified releases become available. The site uses root-relative links and is intended for a GitHub Pages user site at the domain root.

## Publish later

After review, place the complete site in the separate `s-creator01/s-creator01.github.io` repository. Configure Settings → Pages → Deploy from a branch → `main` / `(root)`, if needed. Check the published pages and links before sharing. The sitemap and robots file contain the intended domain and should be changed if another domain is chosen.
