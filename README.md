# Pokémon GO Rewind

**Relive every launch, remember game milestones.**

A single-page website that shows every Pokémon released on any given day in Pokémon GO history, along with game milestones. Navigate by date to see what happened on that day across all years.

🔗 **Live site:** [pogorewind.vercel.app](https://pogorewind.vercel.app/)

## Features

- Browse releases by day — see every Pokémon that debuted, went shiny, shadow, or Dynamax on any calendar date
- Game milestones timeline — Community Days, raids, GO Fest, and more
- Date navigation — arrow keys, calendar picker, and today button
- Pokémon sprites served directly from this repo
- The site loads its data at runtime from two CSV files in this repo.

### `datas_debut.csv`

Each row is a Pokémon form with its release dates. Columns (semicolon-delimited):

| Column | Description |
|---|---|
| Número | National dex number |
| ID | Sprite ID (e.g. `0001`, `0025-00-01`) |
| Nome | Portuguese name |
| Name | English name |
| Estreia | Regular debut date (DD/MM/YYYY) |
| Brilhante | Shiny release date |
| Sombroso | Shadow release date |
| Sombroso Brilhante | Shiny Shadow release date |
| Dinamax | Dynamax release date |
| Dinamax Brilhante | Shiny Dynamax release date |

Date fields empty if not yet released.

### `events.csv`

Each row is a game event or milestone. Columns (semicolon-delimited):

| Column | Description |
|---|---|
| Tipo de evento | Event type in Portuguese |
| Event type | Event type in English |
| Nome | Event name in Portuguese |
| Name | Event name in English |
| Data | Event date (DD/MM/YYYY) |
| ImageName | Image filename in the repo root (without `.png`) |

### Sprites

Sprites are stored in the `sprites/` folder, named by their ID:

- Regular: `{ID}.png` (e.g. `0025.png`)
- Shiny: `{ID}+S.png` (e.g. `0025+S.png`)

### Event images

Event/milestone images go in the repo root as `.png` files. The `ImageName` column in `events.csv` should match the filename without the extension (e.g. `GO_Community_Day_Logo` → `GO_Community_Day_Logo.png`).

## Hosted on

- **Vercel** — static hosting for the HTML page
- **GitHub** — raw file hosting for sprites, CSVs, and event images

## Support

If you enjoy this project, consider buying me a coffee:

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/J3J21VUCOZ)

## Author

Made by [Gabrielense](https://www.reddit.com/user/Gabrielense/)
