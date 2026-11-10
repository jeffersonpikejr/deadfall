# DEADFALL — Roadmap

A living plan. Phases ship one at a time; each is playable. Dates are ship dates.

---

## ✅ Phase 1 — Cross-platform foundation (2026-07-10)
- Repo + GitHub Pages deploy; play in-browser on any device.
- Automatic **desktop vs. mobile** detection with live re-detection.
- Desktop scheme: WASD + **mouse twin-stick aim**, click/Space attack, E/right-click interact, Shift/Tab/M/Esc.
- Fixed the portrait-pause that froze desktop play; hardened input handling against synthetic-mouse and focus-loss bugs.

## ✅ Phase 2 — Performance + survival depth (2026-07-10)
- **Perf:** fixed the unbounded blood-decal leak (hard cap + viewport culling) that dropped framerate over a session.
- **Flashlight cone:** directional light thrown along your facing/aim, plus a small always-on personal glow. Night is darker and more tactical; the mouse aims the beam.
- **Inventory management:** per-item **DROP** (items land on the ground, retrievable via ✋/E), and a **SORT** toggle (type → name → count).
- **Luggage:** equippable bags (Fanny Pack +2, School Backpack +5, Duffel +8) in a dedicated bag slot that raise carry capacity from the base 12. Found in closets; you start with a fanny pack.

## ✅ Phase 3 — Barricading & safehouses (2026-07-11)
- **Planks** material — found in hardware/tool loot and **salvaged by breaking down looted furniture** (🔨 / `Q`).
- **Barricade** doors & windows: spend planks to nail on boards (up to 5), sharply raising the HP zombies must chew through. **Carpentry** (previously an unused skill) makes each board tougher and levels with use. **Tear down** your own boards (via ✋/E) to recover planks and reopen.
- **Claim a safehouse**: designate a cleared building as yours — it gets a **persistent stash** (deposit/withdraw beyond your backpack, accessed from the bag while inside) and is your save anchor. Permadeath preserved (no respawn).
- Contextual 🔨 build button on mobile; `Q` on desktop.

## ✅ Phase 4 — Under Siege (deeper safehouses, 2026-07-11)
- **Siege events** — when you hole up in your safehouse at night, the horde converges on it and assaults your barricades (wave scales with the day count). An **⚠ UNDER SIEGE ⚠** banner flags it; dawn breaks the assault and rewards Carpentry. The payoff loop for barricading.
- **Rest** — a **REST UNTIL DAWN** action in the safehouse bag passes the hours, healing HP and stamina while draining food/water — but a siege jolts you awake mid-rest.
- **Opt-in respawn** — a **New Game toggle** (default OFF, preserving permadeath). When on, dying at a claimed safehouse wakes you there with 40 HP; everything you were carrying drops as a recoverable death-cache where you fell (a corpse run). No safehouse = death is still final.

---

## ✅ Phase 5 — The Overhaul: a roguelite with a way out (2026-11-10)
Ships the old candidates **B (crafting)** and **C (objectives & narrative)**, plus most of the backlog, on a rebuilt world and renderer.

- **Controls** — dodge roll with invulnerability frames (`Space` / 💨 / `B`), hold-to-attack, two weapon slots with swap, reloads, quick-heal, throw-to-cursor, flashlight toggle, a desktop hotbar; on touch the attack button doubles as an aim stick (with auto-facing when you don't aim) plus a quick-action row; **full gamepad support** including menus; a pause menu with volume / screen-shake / damage-number settings; a smoothed look-ahead camera that zooms in on large screens.
- **Graphics** — the town is painted into cached tile chunks (textured ground, brick/siding/metal walls, 25 kinds of furniture, per-table containers, vehicles, fixtures); animated procedural sprites for the player and every infected type; **ray-cast line of sight** (you see only what you could see, light stops at walls, rooms stay hidden until opened); coloured light from the flashlight, fires, flares, streetlights and muzzle flash; particles, hit-stop, damage numbers, swing trails, dusk/dawn grading, storms with lightning.
- **Procedural generation** — a jittered-BSP street grid inside a ring road, optional river and bridges, districts by distance and noise, landmark compounds, lots, and multi-room furnished interiors; a connectivity pass that guarantees every building and story item is reachable. Map grew to 128×128.
- **Roguelike story** — ten origins; three seeded escape routes (**The Signal / The Long Road / The Line**) built on a shared objective chain with hold-out finales; five lore threads whose last page reveals a hidden cache; a journal and a per-run chronicle; win and death screens with score, epitaph and unlocks.
- **Loot** — five quality tiers, 17 affixes, 10 legendary uniques, tiered containers, locks (lockpick / crowbar / sledge), search time, car trunks (and alarms), zombie drops, supply airdrops; 16 melee weapons and 6 firearms with their own ammunition.
- **Crafting** — eight materials, 17 recipes (some bench-only), weapon and armor repair, spike traps, pipe bombs, noisemakers; four safehouse stations.
- **Progression** — character levels with a 1-of-3 perk draft (23 perks), escalating threat by day (tougher dead, elite modifiers, new types, the power failing, the hunting Alpha), and meta-progression that unlocks origins across runs.
- **AI** — a shared flow field: hunters path around walls, pick an opening and break it; brutes charge, spitters shoot, the Alpha rallies.
- Also: broken doors/windows can be re-boarded, containers keep what your pack can't hold, storms, a waypoint map, safehouse claim from the pack. **Save schema is now v4 — earlier saves are not carried over.**

---

## 🔜 Phase 6 — candidate directions (pick one to focus)

**D. Living town / factions** — other survivors (trade, recruit, or rob), a wandering trader, rival scavengers who strip buildings before you, dynamic events (a horde migrates, a building burns). The largest remaining gap: the town is still empty of people.

**E2. Safehouse network** — claim **multiple** safehouses and **fast-travel** between them when the coast is clear; sieges that probe your weakest wall; more stations (garden, radio, watch post).

**F. More ways out** — a fourth and fifth route (the river and a boat; the hospital roof), route-specific bosses, and branching objectives so two runs on the same route still differ.

**G. Run modifiers & daily seed** — optional mutators (permanent night, no guns, fast dead), difficulty tiers, a daily seed with a local leaderboard.

## 🧊 Backlog / smaller polish
- Vehicles (risk/reward: fast + very loud).
- Save slots and multiple concurrent seeds.
- Key rebinding; a colour-blind-friendly rarity palette.
- A proper on-screen tutorial for the first run instead of timed hints.
- Hand-tuning pass on balance (loot rates, XP curve, hold-out wave sizes) from real play data.

---

_Steering: tell me which Phase 6 letter (or backlog item) to build next, and I'll spec + implement it as the next phase._
