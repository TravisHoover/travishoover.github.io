# travishoover.dev

Personal portfolio site for Travis Hoover, hosted on GitHub Pages at
[travishoover.dev](https://travishoover.dev).

Plain HTML and CSS — no build step. Edit `index.html` / `index.css` and push to
`master` to deploy.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole site — one page, with inline JS for scroll reveal and nav highlighting |
| `index.css` | All styling |
| `404.html` | Custom GitHub Pages 404, styled to match |
| `og.png` | 1200×630 social preview card (LinkedIn, Slack, X, iMessage) |
| `avatar.png` | Portrait and favicon, self-hosted rather than hotlinked |
| `robots.txt`, `sitemap.xml` | Search engine hygiene |
| `CNAME` | Custom domain for GitHub Pages |

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Notes for editing

- **Bump the stylesheet cache-buster.** `index.html` links `index.css?v=N`.
  Increment `N` in both `index.html` and `404.html` whenever you change the CSS,
  or returning visitors will keep the old stylesheet.
- **Regenerate `og.png` if the hero copy changes**, so the social preview keeps
  matching the page. It's a 1200×630 screenshot of a card using the same fonts
  and gradient as the hero.
- **Absolute URLs in the meta tags.** Open Graph and Twitter tags need full
  `https://travishoover.dev/...` URLs — relative paths break link previews.
