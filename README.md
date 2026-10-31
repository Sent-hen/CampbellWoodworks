# Campbell Woodworks

Website for Campbell Woodworks (Michael Campbell, Athens, TX). It's a static Jekyll site hosted on GitHub Pages.

## Adding or updating a piece

Each piece is one file in `_pieces/`. Copy an existing one and change the front matter:

```yaml
title: Adirondack Chair
category: Outdoor Furniture   # used for the shop filter buttons
status: available             # available | custom (made to order) | sold
price: "$250"                 # optional. Leave it out to show "Call for price"
featured: true                # show on the home page (first 4 by order)
order: 1                      # sort order
summary: One line shown on the card.
image: /images/pieces/your-photo.jpg   # optional. Without it a placeholder shows
gallery:                               # optional extra photos
  - /images/pieces/another-photo.jpg
details:
  - Bullet points on the detail page
```

The text below the `---` is the description on the piece's page.

- **Sold:** set `status: sold`. The piece leaves the Shop page but stays in Our Work.
- **Photos:** put them in `images/pieces/`. About 1200px on the long side is plenty.

Phone, email, address, market and Facebook link live in `_config.yml`.

## Run locally

```bash
jekyll serve --livereload
```

Then open http://localhost:4000/CampbellWoodworks/.

## Publish

Push to `main`, then in the repo go to **Settings → Pages** and pick **Deploy from a branch → main / (root)**.
The site goes live at https://sent-hen.github.io/CampbellWoodworks/. For a custom domain, set `url` and `baseurl: ""` in `_config.yml`.
