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

---

## 🔜 Phase 3 — candidate directions (pick one to focus)

**A. Barricading & safehouses** — nail furniture across doors/windows (uses the Carpentry skill, which already exists but does little); claim a building as a respawn/stash point; zombies siege weak points. Deepens the "hole up vs. move" tension.

**B. Crafting & scavenging economy** — break down junk into components; craft bandages, molotovs, spears, reinforced weapons at a workbench; weapon repair. Gives loot a second life and rewards the skill system.

**C. Objectives & narrative spine** — a reason to push into Downtown: find the radio, reach the evac point, survive N nights. Optional story beats/notes in buildings. Turns the sandbox into a run with an arc and an ending you play toward.

**D. Living town / factions** — other survivors (trade, recruit, or rob), rival scavengers, dynamic events (a horde migrates, a building burns). Makes the town feel inhabited.

## 🧊 Backlog / smaller polish
- Vehicles (risk/reward: fast + very loud).
- Weather-driven events (storms that mask sound but hurt visibility).
- Difficulty / permadeath modes; run stats & a death screen leaderboard.
- Audio settings + a mute toggle; controller support.
- Save slots and multiple concurrent seeds.

---

_Steering: tell me which Phase 3 letter (or backlog item) to build next, and I'll spec + implement it as the next phase._
