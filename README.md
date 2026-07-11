# DEADFALL

A single-file, top-down survival-horror roguelite. The town of Deadfall fell in a single night — no rescue is coming. Scavenge, fight, and see how long you last.

**▶ Play in your browser: https://jeffersonpikejr.github.io/deadfall/**

## Controls

The game **auto-detects your device** and swaps controls + UI to match. It also re-detects live, so a touchscreen laptop lands in whichever scheme you actually use.

### 🖥 Desktop (keyboard + mouse)
| Input | Action |
|---|---|
| `W` `A` `S` `D` / arrows | Move |
| Mouse | Aim (twin-stick — you face the cursor) |
| Left click / `Space` | Attack / fire (hold to keep swinging) |
| `E` / right click | Loot · pick up dropped items · doors · windows |
| `Shift` | Sprint (loud — draws the horde) |
| `Tab` / `I` / `B` | Backpack — equip · drop · sort · armor · bags · skills |
| `M` | Full map |
| `Esc` | Close bag / map |

### 📱 Mobile (touch)
Left thumb drives a floating virtual stick; the right-hand pad holds **✊ Attack · ✋ Interact · 🏃 Sprint · 🎒 Bag**. Tap the minimap for the full map. Played in **landscape** — a rotate prompt appears in portrait.

## Gameplay notes

- **Seeded worlds** — enter a seed on the menu to replay the same town, or leave it blank for random.
- Districts (Downtown, Suburbs, Industrial, Rural) hide different loot. The police armory is always out there somewhere.
- New horrors walk after dark: screamers that call the horde, gas-filled bloaters, night stalkers.
- **Nightfall is dark.** A flashlight throws a **cone of light** wherever you aim — everything outside it stays black. Batteries keep it alive.
- **Manage your pack.** Every item can be dropped to the ground (and picked back up); **SORT** tidies the bag by type, name, or count. Find bigger **bags** (fanny pack → backpack → duffel) to raise your carry capacity.
- Rain masks your footsteps. Skills (Blunt, Blade, Aiming, Fitness, Carpentry, First Aid) grow with use.
- Manage health, satiation, hydration, and stamina. Bleeding, fractures, and infection will end you as surely as a bite.
- Your run auto-saves; **Continue** resumes it from the menu. See [ROADMAP.md](ROADMAP.md) for what's next.

## Tech

Zero dependencies — one self-contained `index.html` (canvas rendering, Web Audio synth SFX, `localStorage` saves). Deployed via GitHub Pages.

## Local development

Any static server works, e.g.:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```
