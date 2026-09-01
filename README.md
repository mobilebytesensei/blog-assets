# blog-assets

Public image host for **blogs.mobilebytesensei.com**.

## Why this repo exists

Medium fetches post images server-side at publish time. That fetch proved unreliable
against our Cloudflare-fronted domain: images served `200 image/png` to every
user-agent tested, yet rendered as a broken `<img>` on Medium. An image from a
well-known public host rendered fine in the same post, which isolated the fault to
delivery rather than to Medium's markdown support.

So the site serves images from its own domain, and Medium is pointed at
`raw.githubusercontent.com`, which it fetches reliably.

Contents are **generated** — rendered from SVG sources in the private `medium-blogs`
repo. Do not hand-edit; regenerate and re-sync.

```
posts/{slug}/hero.png      cover, 1200x630 rendered @2x
posts/{slug}/{slug}.png    concept diagram
support/bmc-support.png    buy-me-a-coffee card
```
