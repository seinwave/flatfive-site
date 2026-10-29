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

## Moving to the custom domain

Once `flatfive.pro` resolves, two changes:

1. In `_config.yml`, set `url: "https://flatfive.pro"` and `baseurl: ""`.
2. Add a `CNAME` file at the repo root containing `flatfive.pro`.

Then point DNS at GitHub Pages — four `A` records for the apex
(`185.199.108.153`, `.109.153`, `.110.153`, `.111.153`), or an `ALIAS`/`ANAME` to
`seinwave.github.io` if the registrar supports it. Enable *Enforce HTTPS* in the repo's
Pages settings once the certificate is issued.
