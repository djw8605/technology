# OSG Technology Area

This repository contains the internal documents for the OSG Technology Area.

- [Github hosted](http://osg-htc.org/technology)

## Other OSG documentation on Github

- [OSG Council](https://osg-htc.org/council)
- [OSG Production](https://osg-htc.org/production)

## Building the site

The site is built with [Zensical](https://zensical.org/) and configured in `zensical.toml`.
Zensical requires Python 3.11 or newer.

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
zensical serve
```

Then visit <http://localhost:8000/technology/>.
Run `zensical build --strict` to produce the static site in `site/` and fail on broken links, as CI does.

Pull requests are validated by `.github/workflows/validate-zensical.yml`.
Pushes to `master` are built and published to the `gh-pages` branch by `.github/workflows/deploy-zensical.yml`.

## Resources

- [Zensical documentation](https://zensical.org/docs/get-started/)
- [Customizing Zensical templates](https://zensical.org/docs/customization/)
- [Markdown documentation](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
