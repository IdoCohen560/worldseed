<div align="center">

# Worldseed

**A civilization simulator you play indirectly.** You are the Voice — autonomous towns farm, learn,
trade, quarrel, and pray on a procedurally generated planet, and now and then they turn to you for
counsel. Answer well and their faith grows; leave them waiting and they decide alone, trusting you a
little less each time. If faith reaches zero, the world stops listening.

### [▶ Play it now → worldseed-game.netlify.app](https://worldseed-game.netlify.app)

<sub>No install, no sign-up — it runs instantly in any browser.</sub>

![play](https://img.shields.io/badge/play-worldseed--game.netlify.app-00d4ff?style=flat-square)
![single file](https://img.shields.io/badge/build-single_HTML_file-2e8b57?style=flat-square)
![dependencies](https://img.shields.io/badge/dependencies-none-2ea44f?style=flat-square)
![tech](https://img.shields.io/badge/vanilla-JavaScript-f7df1e?style=flat-square&logo=javascript&logoColor=000)

</div>

---

Worldseed is a whole world in a single HTML file. There is no build step, no server, and no
account — you open a page and a planet grows. You don't command the towns directly; you **advise**
them, and the weight of your advice is the faith they place in you. Everything else — the wars, the
famines, the religions that spring up to worship you or to reject you — is emergent.

## The core loop

1. **A planet grows from a seed.** The same seed always grows the same world, so a seed is a save you can share.
2. **Towns live on their own.** They farm, trade, invent, migrate, and go to war without you.
3. **Now and then, they ask.** A decision surfaces — a war, a migration, a heresy — and you counsel them.
4. **Faith remembers.** Towns judge how your past counsel turned out and trust you more, or less. At zero faith, they stop asking.

## Features

- **Seeded worlds** — the same seed always grows the same planet. Share a seed to share a world.
- **A real economy** — food, wood, stone, metal, and knowledge, with seasons, spoilage, irrigation, overfarmed soil, and famine as an emergent outcome.
- **A 32-tech tree across 8 eras** — from Fire to Spaceflight; ideas spread along trade routes, printing, and signals.
- **Trade routes with risk** — routes smooth famines and share knowledge, but plagues travel the same roads.
- **Diplomacy and war** — relations drift with culture, religion, borders, and crowding; wars end in truce, surrender, or conquest, and conquered peoples remember their old banners.
- **Notable people** — leaders, inventors, prophets, generals, and explorers with lifespans, epithets, and legends recorded in the Chronicle.
- **Decision memory** — towns judge how your past counsel turned out ("They remember") and adjust their faith accordingly.
- **Culture and religion** — four culture axes drift over time; faiths form, spread, schism, and may come to worship the Voice itself.
- **A living map** — droughts, floods, and volcanoes permanently reshape terrain; ashlands heal into fertile slopes.
- **The road to the stars** — astronomy charts moons and planets you name; spacefaring towns launch a vessel, achieve footfall, and found an offworld colony.
- **20 milestones**, three map views, three save slots, and a filterable Chronicle of everything that ever happened.

## Play

**Online — [worldseed-game.netlify.app](https://worldseed-game.netlify.app).** Nothing to install.

**Offline —** clone the repo and open the file directly; the whole game is self-contained:

```bash
git clone https://github.com/IdoCohen560/worldseed.git
open worldseed/index.html   # or just double-click it
```

## Development

The simulation core is testable headlessly — extract the inline script and run the built-in smoke test under Node:

```bash
sed -n '/^<script>$/,/^<\/script>$/p' index.html | sed '1d;$d' > /tmp/ws.js && node /tmp/ws.js
```

---

<div align="center">
<sub>Worldseed is an original, from-scratch work — code, text, and art. Its design is inspired by the indirect-guidance genre.</sub>
</div>
