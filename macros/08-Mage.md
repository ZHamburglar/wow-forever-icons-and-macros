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

> [!tip] Why it's valuable
> A bare /cast macro keeps your main nuke on one key with full cooldown visibility — no targeting logic needed for your spammable frost filler.

### Ice Lance (frozen target burst — talent)
```lua
#showtooltip
/cast Ice Lance
```

> [!tip] Why it's valuable
> Single-button frozen-target burst — no conditional, just press when your target is rooted or frozen for triple damage.

### Frost Nova (AoE root)
```lua
#showtooltip
/cast Frost Nova
```

> [!tip] Why it's valuable
> One press roots everything around you — a macro for Frost Nova means you don’t fumble through keybinds when mobs are already in your face.

### Cone of Cold (frontal slow)
```lua
#showtooltip
/cast Cone of Cold
```

> [!tip] Why it's valuable
> A dedicated cone key saves you from aiming — press when the pack is stacked in front of you to slow everything without retargeting.

### Blizzard (AoE channel)
```lua
#showtooltip
/cast Blizzard
```

> [!tip] Why it's valuable
> One-button AoE channel — no target, no positioning gymnastics, just press and let the slow + damage zone do the work.

### Ice Barrier (frost shield — talent)
```lua
#showtooltip
/cast Ice Barrier
```
*(Talent-gated (Frost tree). The classic frost damage shield — no water elemental in 1.60.1, so this is your frost defensive.)*

> [!tip] Why it's valuable
> Self-cast frost shield with no conditions — a single press saves the spell-book hunt when you need the damage absorption right now.

### Frost Blast (frost utility)
```lua
#showtooltip
/cast Frost Blast
```
*(Forever ability — verify its effect in your Spellbook; takes the slot of the removed pet-Freeze.)*

> [!tip] Why it's valuable
> A dedicated button for Frost Blast so you can react instantly — no need to drag the spell from your book mid-combat.

### Frost Ward (magic absorb)
```lua
#showtooltip
/cast Frost Ward
```
*(Absorbs incoming frost damage — the classic reactive button vs frost casters. Replaces Deep Freeze, which doesn't exist in 1.60.1.)*

> [!tip] Why it's valuable
> One-press magic absorb vs frost casters — no targeting, no macro logic, just press before the volley lands.

---

## 🔥 Fire Spec

### Fireball (main nuke)
```lua
#showtooltip
/cast Fireball
```

> [!tip] Why it's valuable
> Bare /cast macro for your fire filler — minimal keybind use while keeping cooldown and range info on your bar.

### Pyroblast (big nuke — talent)
```lua
#showtooltip
/cast Pyroblast
```

> [!tip] Why it's valuable
> A dedicated Pyroblast button means you can weave it between instant casts without hunting through your spellbook.

### Fire Blast (instant)
```lua
#showtooltip
/cast Fire Blast
```

> [!tip] Why it's valuable
> Instant fire nuke on a single key — press between cast-time spells for optimal GCD usage without extra keybind clutter.

### Scorch (fast filler)
```lua
#showtooltip
/cast Scorch
```

> [!tip] Why it's valuable
> Low-cooldown instant filler on one button — essential for keeping your GCD busy during movement phases.

### Combustion (fire burst — talent)
```lua
#showtooltip
/cast Combustion
```
*(Talent-gated (Fire tree). The classic fire cooldown that guarantees crits and spreads Ignite — replaces Living Bomb.)*

> [!tip] Why it's valuable
> One-press fire burst cooldown — activates your crit-guarantee and Ignite spread without scrolling through your bars mid-burn phase.

### Blast Wave (instant AoE + knockback — talent)
```lua
#showtooltip
/cast Blast Wave
```
*(Talent-gated (Fire tree). AoE fire damage that knocks enemies back — takes the slot of the removed Dragon's Breath.)*

> [!tip] Why it's valuable
> Instant AoE knockback on a single key — the difference between living and dying when melee mobs close on you.

### Flamestrike (AoE)
```lua
#showtooltip
/cast Flamestrike
```

> [!tip] Why it's valuable
> AoE fire zone on one button — no target required, just ground-target where the pack is stacked.

---

## 🔮 Arcane Spec

### Arcane Blast (stacking nuke — talent)
```lua
#showtooltip
/cast Arcane Blast
```

> [!tip] Why it's valuable
> Your stacking arcane nuke on a single key — press repeatedly to build Arcane Charges for maximum burst.

### Arcane Missiles (channel)
```lua
#showtooltip
/cast Arcane Missiles
```

> [!tip] Why it's valuable
> Channeled arcane damage with no conditional logic — one button, just press and hold target for guaranteed hits.

### Arcane Explosion (instant AoE)
```lua
#showtooltip
/cast Arcane Explosion
```

> [!tip] Why it's valuable
> Instant arcane AoE on one key — press when surrounded, no target swapping required, excellent for farming.

### Presence of Mind (instant next cast — talent)
```lua
#showtooltip
/cast Presence of Mind
/cast Arcane Blast
```

> [!tip] Why it's valuable
> Chains Presence of Mind into Arcane Blast in one press — turns your slowest nuke into an instant cast with zero delay between the two clicks.

### Arcane Power (burst — talent)
```lua
#showtooltip
/cast Arcane Power
```

> [!tip] Why it's valuable
> A dedicated Arcane Power button — press for your damage-spike cooldown without fumbling through keybinds during the burn window.

### Evocation (mana refill)
```lua
#showtooltip
/cast Evocation
```

> [!tip] Why it's valuable
> One-press mana refill — no conditions, no target, just press when your mana bar gets low between pulls.

---

## 🧊 Utility & Control

### Polymorph (CC — focus)
```lua
#showtooltip
/cast [@focus,harm,nodead][harm] Polymorph
```

> [!tip] Why it's valuable
> Focus-target polymorph priority — sheep your assist target instantly without breaking your current cast target.

### Counterspell (interrupt — focus)
```lua
#showtooltip
/cast [@focus,harm,nodead][@mouseover,harm,nodead][] Counterspell
```

> [!tip] Why it's valuable
> Focus → mouseover → target priority lets you interrupt the correct caster without ever retargeting — a reaction-time cheat code.

### Mana Shield (absorb damage with mana)
```lua
#showtooltip
/cast Mana Shield
```
*(The classic arcane "second health bar" — takes the slot of Spellsteal, which doesn't exist in 1.60.1.)*

> [!tip] Why it's valuable
> One-button mana-for-health absorb — no macro logic needed, just press before the incoming hit connects.

### Remove Lesser Curse (self/mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Remove Lesser Curse
```
*(Classic name — Remove Curse is the post-1.60.1 uprank.)*

> [!tip] Why it's valuable
> Mouseover-friendly curse removal with self-cast fallback — cleanses a friendly or yourself in one press without losing your target.

### Blink (teleport)
```lua
#showtooltip
/cast Blink
```

> [!tip] Why it's valuable
> Forward teleport on a single key — your panic button / gap closer, no targeting needed, press and move.

### Ice Block (self freeze — talent)
```lua
#showtooltip
/cast Ice Block
```

> [!tip] Why it's valuable
> A one-press invulnerability button — freezes you in ice to wait out a death timer or drop aggro. No target logic required.

### Cold Snap (reset frost CDs — talent)
```lua
#showtooltip
/cast Cold Snap
```

> [!tip] Why it's valuable
> Resets all frost cooldowns in one press — double Frost Nova or double Ice Block in the same fight with zero extra keybind overhead.

### Teleport: Dalaran (Forever)
```lua
#showtooltip
/cast Teleport: Dalaran
```
*(Forever-exclusive Dalaran teleport — handy quick-access. No Invisibility in 1.60.1.)*

> [!tip] Why it's valuable
> A dedicated Dalaran portal button — saves your hearthstone and spellbook search for the Forever-exclusive teleport.

### Arcane Brilliance (party Int buff)
```lua
#showtooltip
/cast Arcane Brilliance
```
*(Party-wide Arcane Intellect — takes the slot of Mirror Image, which doesn't exist in 1.60.1.)*

> [!tip] Why it's valuable
> Party-wide Intellect buff on one button — press before a pull to buff the whole group without clicking each member individually.

### Slow Fall (feather fall)
```lua
#showtooltip
/cast Slow Fall
```

> [!tip] Why it's valuable
> One-press feather fall — no target, no cast-bar drama, just press before you hit the ground.

### Summon Food + Water (conjure)
```lua
#showtooltip
/cast Conjure Food
/cast Conjure Water
```

> [!tip] Why it's valuable
> Two conjure spells on one key — creates both food and water in sequence, saving an action bar slot for your sustain combo.

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

> [!tip] Why it's valuable
> A dedicated Mage Armor button — one press for mana-regen armor without scrolling through your spellbook between pulls.

### Ice Armor (upgraded Frost Armor)
```lua
#showtooltip
/cast Ice Armor
```
*(Classic keeps both spell ranks — Frost Armor is the low-level version, Ice Armor the upgrade. No Molten Armor in 1.60.1.)*

> [!tip] Why it's valuable
> Ice Armor on one key — the upgraded frost armor with a single press, no need to drag the spell from your book every time.

### Frost Armor (low-level armor)
```lua
#showtooltip
/cast Frost Armor
```

> [!tip] Why it's valuable
> Low-level frost armor on one button — useful as a backup when you need the weaker but faster-cast version while leveling.

### Arcane Intellect (buff — mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Arcane Intellect
```

> [!tip] Why it's valuable
> Mouseover-friendly Int buff with self-cast fallback — buff a raid member you’re hovering or yourself without retargeting.

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