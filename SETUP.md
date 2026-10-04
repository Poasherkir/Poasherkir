# Notes

Quick notes for keeping this profile running.

## What updates itself

| Workflow | When | What it makes |
| :-- | :-- | :-- |
| `summary-cards.yml` | daily, 06:00 UTC | the stats cards in `profile-summary-card-output/` |
| `arcade.yml` | daily, 06:30 UTC + every push | Pac-Man on the `arcade` branch |
| `snake.yml` | every 12 h + every push | the snake on the `output` branch |
| `3d-contrib.yml` | daily, 18:00 UTC | the 3D calendar in `profile-3d-contrib/` |

They all use the built-in `GITHUB_TOKEN`, so there's nothing to set up.

## Changing the header

The name, subtitle and rotating lines are `<text>` tags near the bottom of
`assets/header.svg`. Keep each line under about 45 characters and write `&` as
`&amp;`. Then check the file still works:

```bash
python -c "import xml.dom.minidom;xml.dom.minidom.parse('assets/header.svg');print('XML OK')"
```

## Changing the tech stack icons

The icon rows in `assets/stack/` are saved from skillicons.dev. To change one,
download `https://skillicons.dev/icons?i=<names>&theme=dark` and save it over the file.

## One-time settings

- Turn on **Include private contributions on my profile** in
  [profile settings](https://github.com/settings/profile) so private work shows up.
- Pin up to six repos on the profile page. They show up right under the README.
