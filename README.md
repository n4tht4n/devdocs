# devdocs

> Distilled and very condensed development documentation 😉.

This is my try to provide distilled development documentation and make it easily accessible via
[GitHub Pages](https://pages.github.com).

The page is deployed automatically and is reachable at: [https://n4tht4n.github.io/devdocs/](https://n4tht4n.github.io/devdocs/)

## MkDocs

The page is based on [MkDocs](https://www.mkdocs.org) using [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

So all the Markdown source files are located in the `./docs` folder.

[squidfunk](https://github.com/squidfunk) provides a [Docker image](https://hub.docker.com/r/squidfunk/mkdocs-material)
to make it very easy to test and build the page.

```bash
# to serve the docs with a live preview
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material

# to build the docs
docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material build

# deploying it to GitHub Pages (from your local machine)
docker run --rm -it -v ~/.ssh:/root/.ssh -v ${PWD}:/docs squidfunk/mkdocs-material gh-deploy
```
