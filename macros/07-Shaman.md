# Shaman Macros — WoW: Forever

Totem dropping, weapon enchant upkeep, purge/interrupt, and the classic Chain Heal. Classic-era (1.60.1) Shaman.

> [!tip] Totem macro pattern
> Each totem slot (Earth/Fire/Air/Water) holds one totem at a time. A **totem-dropper** macro fires the right totem per context — press for the situation.

---

## 🌩️ Elemental DPS

### Lightning Bolt (main nuke)
```lua
#showtooltip
/cast Lightning Bolt
```

> [!tip] Why it's valuable
> Saves a keybind while keeping your main nuke visible on the action bar with cooldown and range info.

### Chain Lightning (AoE)
```lua
#showtooltip
/cast Chain Lightning
```

> [!tip] Why it's valuable
> A single button for your primary AoE nuke — saves keybind space while keeping cooldown tracking on your bar.

### Lava Burst (instant nuke — talent)
```lua
#showtooltip
/cast Lava Burst
```

> [!tip] Why it's valuable
> Instant-cast burst on one button — press for an immediate damage spike when Lava Burst is talented.

### Flame Shock (DoT)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Flame Shock
```

> [!tip] Why it's valuable
> Mouseover-first targeting means you never lose your current target when applying the DoT — critical for keeping Flame Shock up during multi-target fights.

### Frost Shock (slow)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Frost Shock
```

> [!tip] Why it's valuable
> Mouseover targeting lets you slow a secondary target without switching from your main kill target, saving a reaction tick while kiting.

### Earth Shock (interrupt)
```lua
#showtooltip
/cast [@focus,harm,nodead][@mouseover,harm,nodead][] Earth Shock
```

> [!tip] Why it's valuable
> Priority targeting (focus → mouseover → current) lets you interrupt the right caster instantly without retargeting — a lifesaver in chaotic pulls.

### Elemental Mastery (burst — talent)
```lua
#showtooltip
/cast Elemental Mastery
```
*(Talent-gated (Elemental tree). Guarantees a crit on your next spell — the classic Shaman burst button. No Thunderstorm in 1.60.1.)*

> [!tip] Why it's valuable
> One press guarantees a crit on your next nuke. This macro keeps the ability visible so you never forget it’s ready during a burn phase.

---

## ⚔️ Enhancement

### Stormstrike (talent)
```lua
#showtooltip
/cast Stormstrike
/startattack
```

> [!tip] Why it's valuable
> Combining /cast Stormstrike with /startattack saves a GCD — the auto-attack starts instantly instead of waiting for your next swing.

### Frostbrand Weapon (off-hand frost buff)
```lua
#showtooltip
/cast Frostbrand Weapon
/use 17
```
*(Frost damage weapon enchant for the off-hand — the classic alternative to the removed Lava Lash. `/use 17` = off-hand weapon slot, correct.)*

> [!tip] Why it's valuable
> Bakes the off-hand weapon slot (/use 17) into one button so you never enchant the wrong hand — saves a fumbled click in your rotation.

### Earthbind Totem (slow kiting)
```lua
#showtooltip
/cast Earthbind Totem
```

> [!tip] Why it's valuable
> Drops a slow totem without switching targets, preserving your offensive momentum while keeping the kiter at range.

### Windfury Weapon (main-hand buff)
```lua
#showtooltip
/cast Windfury Weapon
/use 16
```
*(`/use 16` = main-hand weapon slot, correct.)*

> [!tip] Why it's valuable
> Enchants the main hand and applies Windfury in one press — eliminates the two-step hassle and ensures you hit the right slot during pre-pull.

### Flametongue Weapon (off-hand buff)
```lua
#showtooltip
/cast Flametongue Weapon
/use 17
```

> [!tip] Why it's valuable
> Single-button off-hand enchant for Flametongue — removes the slot-fumbling step so you rebuff faster between pulls.

### Rockbiter Weapon (threat/AP buff)
```lua
#showtooltip
/cast Rockbiter Weapon
/use 16
```

> [!tip] Why it's valuable
> Weapon enchant and main-hand slot in one press — speeds up your pre-pull ritual and prevents misclicks on the wrong weapon slot.

---

## 💚 Restoration Healing

### Chain Heal (smart heal — mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Chain Heal
```

> [!tip] Why it's valuable
> Mouseover priority means you heal the raid frame you’re hovering without losing your current target — the difference between saving and losing a tank.

### Healing Wave (big heal)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Healing Wave
```

> [!tip] Why it's valuable
> Cast on mouseover or self-cast fallback eliminates target-switching delay — every fraction of a second counts when the tank is dipping.

### Lesser Healing Wave (fast heal)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Lesser Healing Wave
```

> [!tip] Why it's valuable
> A fast, cheap heal with mouseover priority — press the moment damage lands without wasting a GCD on target swapping.

### Riptide (HoT + heal — talent)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Riptide
```

> [!tip] Why it's valuable
> Mouseover-driven HoT application — pre-hotting the tank between pulls is one hover and a press, no retargeting needed.

### Water Shield (mana regen self — talent)
```lua
#showtooltip
/cast [@player] Water Shield
```
*(Talent-gated (Restoration tree). The classic shield that returns mana on hit — Earth Shield does not exist in 1.60.1.)*

> [!tip] Why it's valuable
> Forces self-cast with [@player] so you never accidentally lose the shield on someone else — critical for mana sustain during long boss fights.

### Healing Stream Totem (party HoT)
```lua
#showtooltip
/cast Healing Stream Totem
```

> [!tip] Why it's valuable
> A one-button party HoT totem with no target requirement — press and forget, the totem handles the healing spread.

### Mana Spring Totem (mana regen)
```lua
#showtooltip
/cast Mana Spring Totem
```

> [!tip] Why it's valuable
> Drops a sustained mana-regen totem in one keypress — essential for keeping your party’s mana pool healthy across long trash pulls.

---

## 🧊 Utility & Control

### Purge (dispel enemy buffs — mouseover)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][@focus,harm,nodead][] Purge
```

> [!tip] Why it's valuable
> Mouseover → focus → target priority means you can peel a dangerous enemy buff without ever swapping off the boss — a huge reaction-time saver.

### Cure Poison / Disease (mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Cure Poison
/cast [@mouseover,help,nodead][@player] Cure Disease
```
*(Classic's friendly dispels — no Cleanse Spirit in 1.60.1.)*

> [!tip] Why it's valuable
> Two dispels stacked on one key — mouseover heals the friendly you’re hovering, self-casts if no target is valid. Saves a crucial action bar slot.

### Ghost Wolf (travel)
```lua
#showtooltip
/cast Ghost Wolf
```

> [!tip] Why it's valuable
> A dedicated travel-form button — one press to shift into Ghost Wolf without scrolling through your shapeshift bar.

### Water Walking (toggle)
```lua
#showtooltip
/cast Water Walking
```

> [!tip] Why it's valuable
> Single-button water walking toggle — saves clicking the spell book when you hit a water crossing.

### Far Sight (scout)
```lua
#showtooltip
/cast Far Sight
```

> [!tip] Why it's valuable
> One-press scouting ability — no target, no conditions, just press to extend your view into the next pull.

### Reincarnation (self-rez, once per 30m)
```lua
#showtooltip
/cast Reincarnation
```

> [!tip] Why it's valuable
> A bare /cast macro for your self-rez — one press when you’re down and the 30-minute cooldown is ready.

### Mana Tide Totem (raid mana — talent)
```lua
#showtooltip
/cast Mana Tide Totem
```
> [!warning] No Bloodlust in 1.60.1
> Classic Shamans have **no Bloodlust/Heroism** — the raid mana button is this Restoration talent (drops a totem that refills party mana over ~12s). Don't double-drop it with another Shaman's.

### Tremor Totem (fear break)
```lua
#showtooltip
/cast Tremor Totem
```

> [!tip] Why it's valuable
> A one-button fear-break totem — drop it preemptively before a feared pull or reactively when the pack turns to run.

### Grounding Totem (spell absorb)
```lua
#showtooltip
/cast Grounding Totem
```
*(No Fire Elemental Totem in 1.60.1 — Searing/Magma Totem are your only fire totems.)*

> [!tip] Why it's valuable
> One button drops your spell-absorb totem — essential for caster-heavy packs where you need to nullify the first incoming nuke.

---

## 🪄 Totem-Dropper Combo

### AoE Totem Drop (Earth + Fire + Air + Water)
```lua
#showtooltip
/castsequence reset=combat Strength of Earth Totem, Searing Totem, Grace of Air Totem, Mana Spring Totem
```
*(One button cycles through all four totem slots — replace totems with your spec's picks. Grace of Air Totem is the classic air totem — Wrath of Air Totem doesn't exist in 1.60.1.)*

> [!tip] Why it's valuable
> A /castsequence totem-dropper cycles through all four totem slots in one key — saves three action bar slots and sets up your full totem array in four GCDs.

### Single-Button Storm Totem (context)
```lua
#showtooltip
/cast [mod:shift] Earthbind Totem; [mod:ctrl] Tremor Totem; [mod:alt] Grounding Totem; Searing Totem
```
*(Shift=slow, Ctrl=fear-break, Alt=spell-absorb, default=damage)*

> [!tip] Why it's valuable
> Modifier keys (Shift/Ctrl/Alt) pack four totems into one button — slow, fear-break, spell-absorb, or damage at a single modifier press without hunting through your bars.

---

## 📋 Suggested Keybinds

| Key | Macro | Why |
|---|---|---|
| 1 | Lightning Bolt | Main nuke |
| 2 | Lava Burst | Instant |
| 3 | Flame Shock | DoT |
| 4 | Chain Lightning | AoE |
| Q | Earth Shock | Interrupt |
| E | Purge | Enemy dispel |
| R | Ghost Wolf | Travel |
| F | Healing Wave | Mouseover heal |
| Shift-1 | Mana Tide Totem | Raid mana |
| Mouse4 | Riptide | HoT |

---

> [!note] Custom server check
> **Maelstrom Weapon** exists as a Forever Enhancement talent — if you've skilled it, the classic 5-stack instant Lightning Bolt pattern works here. If your talents differ from this list (e.g. you skip Riptide or Mana Tide Totem), swap the names in these macros to match your Spellbook. Classic Shaman has no Bloodlust, Fire Elemental Totem, Earth Shield, or Thunderstorm — any addon listing those is showing post-1.60.1 spells.