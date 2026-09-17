# Portfolio site

Source of [natalija-stepurko.github.io/portfolio-website](https://natalija-stepurko.github.io/portfolio-website/).

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

## Custom domain (optional)

In the repository's **Settings → Pages**, enter the domain under **Custom domain** and
save (GitHub adds a `CNAME` file to the repo). At the registrar add a `CNAME` record
pointing `www` (or the bare domain via ALIAS/ANAME) to `natalija-stepurko.github.io`.
Tick **Enforce HTTPS** once the certificate appears. Then update the `og:url` meta tag
in `index.html` to the new address.

## Notes

- Keep the repository public: GitHub Pages on a private repository requires a paid plan.
- The "Explore the results" buttons link to project pages on claude.ai; those stay where
  they are and must remain shared for the links to work.
- Do not edit `index.html` directly on GitHub if Claude is also updating it — edit the
  copy in the folder instead, so the two never diverge.
