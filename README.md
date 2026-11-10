# DEADFALL

A single-file, top-down survival-horror roguelite. The town of Deadfall fell in a single night. Every run builds a different town from a seed, hides a different way out of it, and writes down how you did.

**▶ Play in your browser: https://jeffersonpikejr.github.io/deadfall/**

## The run

1. **Choose who you were.** Ten origins (three open, seven earned) set your starting kit, skills and first perk.
2. **Wake up, search the house.** A note tells you which way out this town has:
   - **The Signal** — power the radio tower, broadcast, and hold the school field for the helicopter.
   - **The Long Road** — find a battery, fuel and the keys for the tow truck at the garage (the keys are on a man who didn't make it).
   - **The Line** — three people each held one digit of the checkpoint gate code. Find all three.
3. **Cross town for what the route needs**, come back, start it, and **hold out** while everything in Deadfall comes for the noise.
4. **Get out** — or don't. Either way the end screen reads your run back to you, scores it, and unlocks what you earned.

The town gets worse the longer you stay: tougher dead, elite variants, the power failing on day 3, and an Alpha that starts hunting you by night.

## Controls

The game **auto-detects your device** and swaps controls + UI to match, live.

### 🖥 Desktop (keyboard + mouse)
| Input | Action |
|---|---|
| `W` `A` `S` `D` / arrows | Move |
| Mouse | Aim (you face the cursor; the camera leans toward it) |
| Left click (hold) / `Enter` | Attack / fire |
| `Space` | **Dodge roll** — brief invulnerability, costs stamina |
| `E` / right click | Search · pick up · doors · climb windows · vault fences · use fixtures |
| `Q` | Build — barricade · re-board a broken opening · salvage furniture · claim safehouse |
| `R` | Reload |
| `1` `2` / `X` / mouse wheel | Weapon slots / swap |
| `H` | Quick heal — treats your worst wound with what you carry |
| `G` | Throw (lands at the cursor) |
| `F` | Flashlight on/off (off = harder to see, and to be seen) |
| `Shift` | Sprint (loud) |
| `Tab` / `I` / `B` · `C` · `J` | Pack · Craft · Journal |
| `M` | Map — click it to drop a waypoint |
| `Esc` / `P` | Pause — volume, screen shake, damage numbers, save & quit |

### 📱 Mobile (touch, landscape)
Left thumb drives a floating stick. Right pad: **Attack** (hold to keep swinging, **drag to aim**; otherwise it auto-faces the nearest threat) · **💨 Dodge** · **✋ Search/Use** · **🏃 Sprint** · **🎒 Pack**, with a quick row for **swap · heal · throw · reload · light** and a contextual **🔨 Build** button. Tap the minimap for the full map.

### 🎮 Gamepad
Left stick move · right stick aim · `RT` attack · `A` use · `B` dodge · `X` reload · `Y` pack · `LB` heal · `RB` swap · `LT` sprint · d-pad: map / build / throw / light · `Start` pause. Menus are fully navigable (d-pad + `A`/`B`, bumpers switch tabs).

## Systems

- **Procedural towns.** A ring road and a recursively split street grid, an optional river with bridges, districts (Downtown, Suburbs, Industrial Row, the Rural Fringe), and landmarks — police station, hospital, supermarket, school, church, fire station, garage, gas station, radio tower, army checkpoint, park. Buildings have furnished multi-room interiors. A final pass guarantees everything the story needs is reachable. Enter a seed to replay a town.
- **Line of sight.** You only see what you could actually see. Light doesn't pass through walls, and whatever is behind a closed door stays hidden until you open it. Night is dark: a flashlight cone, streetlights (until the grid dies), fire and muzzle flash are all you get.
- **Combat.** Melee arcs with knockdown, crits, cleave and hit-stop; firearms with magazines, reloads, spread and noise (pistol, revolver, SMG, shotgun, rifle, crossbow). Dodge through lunges and charges. Brutes charge and stun themselves on walls; spitters lob acid; screamers call the horde; bloaters burst into gas.
- **Loot.** Five quality tiers (Worn → Legendary), rolled affixes (*Serrated*, *Suppressed*, *Bite-proof*…) and ten named uniques. Better tiers in more dangerous places; safes need a lockpick, a crowbar or a sledge. The dead drop things. Supply drops fall from day 2.
- **Crafting.** Rags, tape, scrap, nails, powder and parts become bandages, molotovs, pipe bombs, noisemakers, spike traps, ammunition and repair kits. Some recipes need a workbench (hardware stores, garages, or your own).
- **Progression.** Skills grow with use; character levels grant a **perk draft** (pick 1 of 3, 23 perks). Meta-progression unlocks new origins across runs.
- **Safehouse.** Claim a building, barricade it, stash gear, rest until dawn — and survive the siege. Build stations: workbench, cot, rain collector, tripwire alarm. Optional **safehouse respawn** (off by default; permadeath is the default).
- **Story.** Lore threads scattered through the right buildings; finish one and a hidden cache appears on your map. The journal tracks objectives, notes and a chronicle of the run.
- Your run auto-saves; **Continue** resumes it from the menu. See [ROADMAP.md](ROADMAP.md) for what's next.

## Tech

Zero dependencies — one self-contained `index.html` (canvas rendering with cached tile chunks and a ray-cast visibility polygon, Web Audio synth SFX, `localStorage` saves). Deployed via GitHub Pages.

## Local development

Any static server works, e.g.:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```
