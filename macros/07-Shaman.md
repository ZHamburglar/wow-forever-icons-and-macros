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

### Chain Lightning (AoE)
```lua
#showtooltip
/cast Chain Lightning
```

### Lava Burst (instant nuke — talent)
```lua
#showtooltip
/cast Lava Burst
```

### Flame Shock (DoT)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Flame Shock
```

### Frost Shock (slow)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Frost Shock
```

### Earth Shock (interrupt)
```lua
#showtooltip
/cast [@focus,harm,nodead][@mouseover,harm,nodead][] Earth Shock
```

### Elemental Mastery (burst — talent)
```lua
#showtooltip
/cast Elemental Mastery
```
*(Talent-gated (Elemental tree). Guarantees a crit on your next spell — the classic Shaman burst button. No Thunderstorm in 1.60.1.)*

---

## ⚔️ Enhancement

### Stormstrike (talent)
```lua
#showtooltip
/cast Stormstrike
/startattack
```

### Frostbrand Weapon (off-hand frost buff)
```lua
#showtooltip
/cast Frostbrand Weapon
/use 17
```
*(Frost damage weapon enchant for the off-hand — the classic alternative to the removed Lava Lash. `/use 17` = off-hand weapon slot, correct.)*

### Earthbind Totem (slow kiting)
```lua
#showtooltip
/cast Earthbind Totem
```

### Windfury Weapon (main-hand buff)
```lua
#showtooltip
/cast Windfury Weapon
/use 16
```
*(`/use 16` = main-hand weapon slot, correct.)*

### Flametongue Weapon (off-hand buff)
```lua
#showtooltip
/cast Flametongue Weapon
/use 17
```

### Rockbiter Weapon (threat/AP buff)
```lua
#showtooltip
/cast Rockbiter Weapon
/use 16
```

---

## 💚 Restoration Healing

### Chain Heal (smart heal — mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Chain Heal
```

### Healing Wave (big heal)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Healing Wave
```

### Lesser Healing Wave (fast heal)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Lesser Healing Wave
```

### Riptide (HoT + heal — talent)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Riptide
```

### Water Shield (mana regen self — talent)
```lua
#showtooltip
/cast [@player] Water Shield
```
*(Talent-gated (Restoration tree). The classic shield that returns mana on hit — Earth Shield does not exist in 1.60.1.)*

### Healing Stream Totem (party HoT)
```lua
#showtooltip
/cast Healing Stream Totem
```

### Mana Spring Totem (mana regen)
```lua
#showtooltip
/cast Mana Spring Totem
```

---

## 🧊 Utility & Control

### Purge (dispel enemy buffs — mouseover)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][@focus,harm,nodead][] Purge
```

### Cure Poison / Disease (mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Cure Poison
/cast [@mouseover,help,nodead][@player] Cure Disease
```
*(Classic's friendly dispels — no Cleanse Spirit in 1.60.1.)*

### Ghost Wolf (travel)
```lua
#showtooltip
/cast Ghost Wolf
```

### Water Walking (toggle)
```lua
#showtooltip
/cast Water Walking
```

### Far Sight (scout)
```lua
#showtooltip
/cast Far Sight
```

### Reincarnation (self-rez, once per 30m)
```lua
#showtooltip
/cast Reincarnation
```

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

### Grounding Totem (spell absorb)
```lua
#showtooltip
/cast Grounding Totem
```
*(No Fire Elemental Totem in 1.60.1 — Searing/Magma Totem are your only fire totems.)*

---

## 🪄 Totem-Dropper Combo

### AoE Totem Drop (Earth + Fire + Air + Water)
```lua
#showtooltip
/castsequence reset=combat Strength of Earth Totem, Searing Totem, Grace of Air Totem, Mana Spring Totem
```
*(One button cycles through all four totem slots — replace totems with your spec's picks. Grace of Air Totem is the classic air totem — Wrath of Air Totem doesn't exist in 1.60.1.)*

### Single-Button Storm Totem (context)
```lua
#showtooltip
/cast [mod:shift] Earthbind Totem; [mod:ctrl] Tremor Totem; [mod:alt] Grounding Totem; Searing Totem
```
*(Shift=slow, Ctrl=fear-break, Alt=spell-absorb, default=damage)*

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