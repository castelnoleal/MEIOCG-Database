# MEIOCG Database

Centralized card-data repository for MEIOCG projects.

## Planned consumers

- Duel Synapse
- MEIOCG card-search tools
- Future MEIOCG applications

## Architecture

The repository is designed around static, versioned data so applications can retrieve data from GitHub/CDN infrastructure instead of repeatedly querying an external card API.

```text
MEIOCG-Database
├── data/
│   ├── cards.json
│   ├── cards.min.json
│   └── metadata.json
├── indexes/
│   ├── name.json
│   ├── id.json
│   ├── archetype.json
│   └── type.json
├── images/
│   ├── thumbnails/
│   └── cards/
└── index.html
```

## Data source

The initial Yu-Gi-Oh! dataset is intended to be imported from YGOPRODeck and stored locally, following its API guidance to cache/store pulled data and avoid unnecessary API calls.

Source: https://ygoprodeck.com/api-guide/

## Important

This repository is currently the empty foundation. Do not treat the database as complete until `metadata.json` reports a populated dataset.

MEIOCG is an independent project and is not affiliated with or endorsed by Konami or YGOPRODeck.
