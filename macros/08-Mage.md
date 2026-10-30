# Mage Macros — WoW: Forever

Poly focus, blink, ice block, and the classic water/food conjure. Classic-era (1.60.1) Mage.

> [!tip] Frostbolt vs Fireball
> Both specs listed — swap to whichever your talents support (Frost spec uses Frostbolt, Fire uses Fireball, Arcane uses Arcane Blast). No water elemental or spellsteal in 1.60.1.

---

## ❄️ Frost Spec

### Frostbolt (main nuke)
```lua
#showtooltip
/cast Frostbolt
```

### Ice Lance (frozen target burst — talent)
```lua
#showtooltip
/cast Ice Lance
```

### Frost Nova (AoE root)
```lua
#showtooltip
/cast Frost Nova
```

### Cone of Cold (frontal slow)
```lua
#showtooltip
/cast Cone of Cold
```

### Blizzard (AoE channel)
```lua
#showtooltip
/cast Blizzard
```

### Ice Barrier (frost shield — talent)
```lua
#showtooltip
/cast Ice Barrier
```
*(Talent-gated (Frost tree). The classic frost damage shield — no water elemental in 1.60.1, so this is your frost defensive.)*

### Frost Blast (frost utility)
```lua
#showtooltip
/cast Frost Blast
```
*(Forever ability — verify its effect in your Spellbook; takes the slot of the removed pet-Freeze.)*

### Frost Ward (magic absorb)
```lua
#showtooltip
/cast Frost Ward
```
*(Absorbs incoming frost damage — the classic reactive button vs frost casters. Replaces Deep Freeze, which doesn't exist in 1.60.1.)*

---

## 🔥 Fire Spec

### Fireball (main nuke)
```lua
#showtooltip
/cast Fireball
```

### Pyroblast (big nuke — talent)
```lua
#showtooltip
/cast Pyroblast
```

### Fire Blast (instant)
```lua
#showtooltip
/cast Fire Blast
```

### Scorch (fast filler)
```lua
#showtooltip
/cast Scorch
```

### Combustion (fire burst — talent)
```lua
#showtooltip
/cast Combustion
```
*(Talent-gated (Fire tree). The classic fire cooldown that guarantees crits and spreads Ignite — replaces Living Bomb.)*

### Blast Wave (instant AoE + knockback — talent)
```lua
#showtooltip
/cast Blast Wave
```
*(Talent-gated (Fire tree). AoE fire damage that knocks enemies back — takes the slot of the removed Dragon's Breath.)*

### Flamestrike (AoE)
```lua
#showtooltip
/cast Flamestrike
```

---

## 🔮 Arcane Spec

### Arcane Blast (stacking nuke — talent)
```lua
#showtooltip
/cast Arcane Blast
```

### Arcane Missiles (channel)
```lua
#showtooltip
/cast Arcane Missiles
```

### Arcane Explosion (instant AoE)
```lua
#showtooltip
/cast Arcane Explosion
```

### Presence of Mind (instant next cast — talent)
```lua
#showtooltip
/cast Presence of Mind
/cast Arcane Blast
```

### Arcane Power (burst — talent)
```lua
#showtooltip
/cast Arcane Power
```

### Evocation (mana refill)
```lua
#showtooltip
/cast Evocation
```

---

## 🧊 Utility & Control

### Polymorph (CC — focus)
```lua
#showtooltip
/cast [@focus,harm,nodead][harm] Polymorph
```

### Counterspell (interrupt — focus)
```lua
#showtooltip
/cast [@focus,harm,nodead][@mouseover,harm,nodead][] Counterspell
```

### Mana Shield (absorb damage with mana)
```lua
#showtooltip
/cast Mana Shield
```
*(The classic arcane "second health bar" — takes the slot of Spellsteal, which doesn't exist in 1.60.1.)*

### Remove Lesser Curse (self/mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Remove Lesser Curse
```
*(Classic name — Remove Curse is the post-1.60.1 uprank.)*

### Blink (teleport)
```lua
#showtooltip
/cast Blink
```

### Ice Block (self freeze — talent)
```lua
#showtooltip
/cast Ice Block
```

### Cold Snap (reset frost CDs — talent)
```lua
#showtooltip
/cast Cold Snap
```

### Teleport: Dalaran (Forever)
```lua
#showtooltip
/cast Teleport: Dalaran
```
*(Forever-exclusive Dalaran teleport — handy quick-access. No Invisibility in 1.60.1.)*

### Arcane Brilliance (party Int buff)
```lua
#showtooltip
/cast Arcane Brilliance
```
*(Party-wide Arcane Intellect — takes the slot of Mirror Image, which doesn't exist in 1.60.1.)*

### Slow Fall (feather fall)
```lua
#showtooltip
/cast Slow Fall
```

### Summon Food + Water (conjure)
```lua
#showtooltip
/cast Conjure Food
/cast Conjure Water
```

### Conjure Mana Ruby (mana gem)
```lua
#showtooltip
/cast Conjure Mana Ruby
/use Mana Ruby
```
> [!warning] Gem charge
> Mana gems have limited charges (usable once per charge). Re-create when empty — the macro creates then uses. At lower levels the spell is **Conjure Mana Agate / Jade / Citrine** — same pattern, swap the names.

---

## 🛡️ Armors & Buffs

### Mage Armor (mana regen)
```lua
#showtooltip
/cast Mage Armor
```

### Ice Armor (upgraded Frost Armor)
```lua
#showtooltip
/cast Ice Armor
```
*(Classic keeps both spell ranks — Frost Armor is the low-level version, Ice Armor the upgrade. No Molten Armor in 1.60.1.)*

### Frost Armor (low-level armor)
```lua
#showtooltip
/cast Frost Armor
```

### Arcane Intellect (buff — mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Arcane Intellect
```

---

## 📋 Suggested Keybinds

| Key | Macro | Why |
|---|---|---|
| 1 | Frostbolt/Fireball | Main nuke |
| 2 | Ice Lance/Fire Blast | Instant |
| 3 | Polymorph | CC |
| 4 | Frost Nova | AoE root |
| Q | Counterspell | Interrupt |
| E | Blink | Mobility |
| R | Ice Block | Survival |
| F | Mana Shield | Damage absorb |
| Shift-1 | Arcane Power + Presence | Burst |
| Mouse4 | Remove Lesser Curse | Self/mouseover |

---

> [!note] Custom server check
> If your server adds post-Classic spells (e.g. Spellsteal, Invisibility, water elemental), the macro pattern stays the same — just swap names to match your Spellbook. On pure Forever (1.60.1) the spells above are the real ones: no water elemental, no Dragon's Breath, no Molten Armor, and the curse removal is **Remove Lesser Curse**.