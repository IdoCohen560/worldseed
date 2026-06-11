# Worldseed

A civilization simulator played indirectly. You are the Voice: autonomous towns farm, learn, trade, quarrel, and pray on a procedurally generated planet — and now and then they ask for your counsel. Answer well and their faith in you grows; leave them waiting and they decide alone, trusting you a little less each time. If faith reaches zero, the world stops listening.

**Play it:** open `index.html` in any browser — the whole game is one self-contained file with no dependencies.

## Features

- **Seeded worlds** — the same seed always grows the same planet. Share a seed to share a world.
- **Real economy** — food, wood, stone, metal, and knowledge, with seasons, spoilage, irrigation, overfarmed soil, and famine as an emergent outcome.
- **32-tech tree across 8 eras** — from Fire to Spaceflight; ideas spread along trade routes, printing, and signals.
- **Trade routes with risk** — routes smooth famines and share knowledge, but plagues travel the same roads.
- **Diplomacy and war** — relations drift with culture, religion, borders, and crowding; wars end in truce, surrender, or conquest, and conquered peoples remember their old banners.
- **Notable people** — leaders, inventors, prophets, generals, and explorers with lifespans, epithets, and legends recorded in the Chronicle.
- **Decision memory** — towns judge how your past counsel turned out ("They remember") and adjust their faith accordingly.
- **Culture and religion** — four culture axes drift over time; faiths form, spread, schism, and may worship the Voice itself.
- **A living map** — droughts, floods, and volcanoes permanently reshape terrain; ashlands heal into fertile slopes.
- **The road to the stars** — astronomy charts moons and planets you name; spacefaring towns launch a vessel, achieve footfall, and found an offworld colony.
- **20 milestones**, three map views, three save slots, and a filterable Chronicle of everything that ever happened.

## Development

The simulation core is testable headlessly:

```bash
# extract the inline script and run the built-in smoke test under Node
sed -n '/^<script>$/,/^<\/script>$/p' index.html | sed '1d;$d' > /tmp/ws.js && node /tmp/ws.js
```

Worldseed is an original, from-scratch work — code, text, and art. Its design is inspired by the indirect-guidance genre.
