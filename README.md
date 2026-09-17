# Portfolio site

Source of [natalija-stepurko.com](https://natalija-stepurko.com/) (served by GitHub Pages; also reachable at natalija-stepurko.github.io/portfolio-website).

`index.html` is the complete page, ready to serve as a static site. It is self-contained
(styles, figures and data are inline); the only external resource is Google Fonts.

## How it is published

GitHub Pages serves this repository from the `main` branch, root folder. Every push to
`main` redeploys the site, usually within a minute.

## Updating the site

This repository lives in the `01 Website` folder of the portfolio materials. Whenever the
page changes in a Claude session, the updated `index.html` is written to that folder.
To publish it:

```
git add index.html
git commit -m "Update portfolio"
git push
```

or drag the file onto the repository page on GitHub and commit.

## Custom domain

The site is served at `natalija-stepurko.com`. The `CNAME` file in this repository tells
GitHub Pages which domain to answer for; do not delete it. DNS is managed at Namecheap:
four `A` records on `@` pointing at GitHub's Pages addresses and a `CNAME` record on
`www` pointing at `natalija-stepurko.github.io`. **Enforce HTTPS** is ticked in
Settings → Pages.

## Notes

- Keep the repository public: GitHub Pages on a private repository requires a paid plan.
- The "Explore the results" buttons link to project pages on claude.ai; those stay where
  they are and must remain shared for the links to work.
- Do not edit `index.html` directly on GitHub if Claude is also updating it — edit the
  copy in the folder instead, so the two never diverge.
