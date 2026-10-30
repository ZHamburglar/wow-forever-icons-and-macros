# Cross-Class Macros — Work on Every Class

Universal QoL macros that any of the 9 classes can use. Grouped by purpose.

---

## 🎒 Bags, Loot & Mounts

### Auto-Loot Corpse
```lua
/script if not IsModifiedClick() then ToggleFrame("LootFrame") end
```
*(Opens loot frame without Shift — combine with auto-loot setting for one-click looting)*

### Quick Mount (Random Favorite)
```lua
#showtooltip
/run local c=0; for i=1,GetNumCompanionInfos() do local n,id=GetCompanionInfo("MOUNT",i) end
/cast [nocombat] Summon Random Favorite Mount
```
> [!tip] WotLK client
> Use `Summon Random Favorite Mount` (added 3.1) or bind each mount to a `#showtooltip /cast MountName` macro if you prefer specific mounts.

### Simple Mount (named)
```lua
#showtooltip
/cast [nocombat] Swift Wind Rider
```
*(Replace with your mount's exact name — check the icon library for the right icon!)*

---

## 🧪 Consumables & Combat Items

### Healthstone → Potion (combat)
```lua
/use [combat] Healthstone
/use [combat] Major Healing Potion
```

### Mana Potion → Mana Gem (Mage-style, any class)
```lua
/use [combat] Major Mana Potion
/use [combat] Mana Gem
```

### Bandage Self (no mouseover)
```lua
#showtooltip
/use [@player] Heavy Runecloth Bandage
```

### Buff Food + Drink in one press
```lua
/use [nomounted] Scroll of Agility
```
*(Or simply: `/use Grilled Grouper` — food macros are item-specific)*

---

## ⚔️ Targeting & Combat

### Smart Attack — nearest enemy + attack
```lua
#showtooltip
/targetenemy [noharm][dead]
/startattack
```

### Attack + Cast (fill with your nuke)
```lua
#showtooltip
/startattack
/cast [harm] Lightning Bolt
```

### Target Last Target (after healing)
```lua
/targetlasttarget
```

### Tab-Target-Assist (focus kill order)
```lua
#showtooltip
/target [@focus,harm,nodead]
/startattack
```

---

## 🛡️ Trinkets & Racials

### Use Both Trinkets
```lua
#showtooltip
/use 13
/use 14
```

### On-Use Trinket + Racial Burst
```lua
#showtooltip
/cast Blood Fury
/use 13
/use 14
```
*(Replace Blood Fury with your racial — Orc Blood Fury, Troll Berserking, Tauren War Stomp all exist in Forever)*

### Trinket Swap Macro (equip-on-use trinket)
```lua
/equip 13 Trinket of the Cursed
/use 13
```
> [!warning] Trinket swap
> Can only swap **out of combat**. In combat it just uses the equipped one — add `[nocombat]` to the equip line.

---

## 🎯 Focus System (Essential for PvP & Raids)

### Set Focus (first press) / Cast at Focus (second)
```lua
#showtooltip
/focus [@focus,noexists]
/cast [@focus,harm,nodead][] SpellName
```
*(Replace SpellName with your interrupt/CC — e.g. Counterspell, Kick, Earth Shock)*

### Clear Focus
```lua
/clearfocus
```

### Mouseover-Focus (healers love this)
```lua
#showtooltip
/focus [@mouseover,help,nodead]
```

---

## 💚 Mouseover Patterns (Healers / Interrupters)

### Mouseover Heal (self if no mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Healing Touch
```
*(Replace Healing Touch with your heal — works for Rejuvenation, Flash Heal, etc.)*

### Mouseover Harm (dots, nukes, interrupts)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm,nodead] Moonfire
```

### Mouseover Friendly Buff
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Power Word: Fortitude
```

---

## 🧊 Self-Heal & Emergency

### Emergency Self-Heal
```lua
#showtooltip
/cast [@player] Lay on Hands
```
*(Every class: replace with your biggest self-heal — Healthstone works too)*

### Pot + Heal Emergency (cooldown-staggered)
```lua
/use [combat] Major Healing Potion
/cast [combat] Healing Wave
```

---

## ⚡ GCD & Casting QoL

### Stopcast + Cast (fake-cast bait / instant reaction)
```lua
/stopcasting
/cast Counterspell
```

### Castsequence — two spells in one button (with reset)
```lua
#showtooltip
/castsequence reset=15 Frostbolt, Fire Blast
```
*(Resets after 15s idle or when the sequence ends)*

---

## 📦 Full Macro List (copy-ready)

| # | Name | Line |
|---|---|---|
| 1 | Auto Loot | `/script if not IsModifiedClick() then ToggleFrame("LootFrame") end` |
| 2 | Random Mount | `/cast [nocombat] Summon Random Favorite Mount` |
| 3 | Healthstone+Potion | `/use [combat] Healthstone` + `/use [combat] Major Healing Potion` |
| 4 | Trinkets | `/use 13` + `/use 14` |
| 5 | Racial Burst | `/cast Blood Fury` + `/use 13` + `/use 14` |
| 6 | Smart Attack | `/targetenemy [noharm][dead]` + `/startattack` |
| 7 | Focus CC | `/focus [@focus,noexists]` + `/cast [@focus,harm,nodead][] Counterspell` |
| 8 | Mouseover Heal | `/cast [@mouseover,help,nodead][@player] Healing Touch` |
| 9 | Mouseover Harm | `/cast [@mouseover,harm,nodead][harm,nodead] Moonfire` |
| 10 | Stopcast | `/stopcasting` + `/cast Counterspell` |
| 11 | Castsequence | `/castsequence reset=15 Frostbolt, Fire Blast` |
| 12 | Target Last | `/targetlasttarget` |
| 13 | Clear Focus | `/clearfocus` |
| 14 | Mouseover Focus | `/focus [@mouseover,help,nodead]` |

---

> [!note] Every class file assumes these patterns
> The **mouseover-heal**, **mouseover-harm**, **focus-CC**, and **stopcast** patterns repeat in every class file — they're the most valuable macros in the game. Master these four and you're 80% done.