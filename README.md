# flatfive.pro

The site for [FlatFive](https://apps.apple.com/), a jazz chord flashcard app for iPhone and
iPad. Jekyll, deployed by GitHub Pages.

## Pages

| Path | Purpose |
| --- | --- |
| `/` | What the app is |
| `/guide/` | The user guide |
| `/privacy/` | Privacy policy — the URL App Store Connect wants |

## Local preview

```sh
bundle install
bundle exec jekyll serve
```

`bigdecimal` is pinned to `~> 3.1` because 4.x resolves to a native build that some local
Rubies cannot load.

## Custom domain

Served at <https://flatfive.pro>. The `CNAME` file sets the domain; DNS is four apex `A`
records at GitHub (`185.199.108–111.153`) plus a `www` CNAME to `seinwave.github.io`.
`www.flatfive.pro` redirects to the bare domain.
