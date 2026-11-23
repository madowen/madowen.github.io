# madowen.github.io

Portfolio of Alex Catalán, built with Jekyll on the
[devlopr-jekyll](https://github.com/sujaykundu777/devlopr-jekyll) theme (MIT licence)
and deployed to GitHub Pages by the workflow in `.github/workflows/pages.yml`.
Every push to `master` rebuilds the site at https://madowen.github.io.

The previous blog is preserved in the `old-blog` branch.

## Editing content

Almost everything lives in `_config.yml`:

- `author`, `author_headline`, `author_pitch`, `author_bio`, `author_email`: hero, About and Contact text.
- `author_skills`: one entry per skills row (`label` and `items`).
- `footer_text`: the footer line.
- `author_project_details`: the Featured Work cards, in display order.

### Project cards (`author_project_details`)

```yaml
- project_title: Red Dead Online          # card title
  project_info: Rockstar North · 2019 · Online Mission Script Designer   # meta line
  project_description: Designed the kill cam system...                    # main text
  project_url: https://www.youtube.com/watch?v=J4nMeH6DaOI               # where the image links to
  youtube_id: J4nMeH6DaOI    # optional: shows the YouTube thumbnail (the part after "v=")
  project_links:             # optional extra links under the text
    - text: Red Dead Online
      url: https://www.rockstargames.com/reddeadonline
  project_caption: Official trailer © Rockstar Games.   # optional small italic line
  project_quote: while simultaneously providing a few excellent hours of puzzling.  # optional single press quote
  project_quote_source: Kotaku   # outlet name shown under the quote
  project_quote_url: https://kotaku.com/...            # optional link on the outlet name
  project_quotes:            # optional list; if present, used instead of the single quote fields
    - text: Don't let that fool you because it's one of the coolest video games in GTA 6.
      source: GameSpot
      url: https://www.gamespot.com/articles/all-joysystem-video-games-in-gta-6/
  visibility: true           # set to false to hide the card
```

Without `youtube_id`, the card shows a styled block with the project title.
If `project_url` is also missing, the block is not a link (useful while a video is still to be added).

Edit the file on GitHub (pencil icon), commit, and the site updates in a minute or two.

## Running locally

```sh
bundle install
bundle exec jekyll serve
```

Colours and fonts are in `_sass/_alex.scss`.
