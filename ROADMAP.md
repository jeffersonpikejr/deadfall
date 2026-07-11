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

---

## 🔜 Phase 4 — candidate directions (pick one to focus)

**B. Crafting & scavenging economy** — break down junk into components; craft bandages, molotovs, spears, reinforced weapons at a workbench; weapon repair. Gives loot a second life and rewards the skill system.

**C. Objectives & narrative spine** — a reason to push into Downtown: find the radio, reach the evac point, survive N nights. Optional story beats/notes in buildings. Turns the sandbox into a run with an arc and an ending you play toward.

**D. Living town / factions** — other survivors (trade, recruit, or rob), rival scavengers, dynamic events (a horde migrates, a building burns). Makes the town feel inhabited.

**E. Safehouse depth** — respawn-at-safehouse mode, tool/nail requirements for barricades, fast-travel between claimed buildings, zombie siege events that target your weak points.

## 🧊 Backlog / smaller polish
- Vehicles (risk/reward: fast + very loud).
- Weather-driven events (storms that mask sound but hurt visibility).
- Difficulty / permadeath modes; run stats & a death screen leaderboard.
- Audio settings + a mute toggle; controller support.
- Save slots and multiple concurrent seeds.

---

_Steering: tell me which Phase 3 letter (or backlog item) to build next, and I'll spec + implement it as the next phase._
