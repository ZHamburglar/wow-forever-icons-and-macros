# Cross-Class Macros — Work on Every Class

Universal QoL macros that any of the 9 classes can use. Grouped by purpose.

---

## 🎒 Bags, Loot & Mounts

### Auto-Loot Corpse
```lua
/script if not IsModifiedClick() then ToggleFrame("LootFrame") end
```
*(Opens loot frame without Shift — combine with auto-loot setting for one-click looting)*

> [!tip] Why it's valuable
> One press opens the loot frame without holding Shift, so with auto-loot enabled you can chain-loot entire packs with a single key - no modifiers and no slowdown between corpses.

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

> [!tip] Why it's valuable
> A dedicated mount key beats spellbook or scroll-wheel fumbling when you need to leave quickly, and the [nocombat] conditional guarantees it never misfires mid-fight.

---

## 🧪 Consumables & Combat Items

### Healthstone → Potion (combat)
```lua
/use [combat] Healthstone
/use [combat] Major Healing Potion
```

> [!tip] Why it's valuable
> Stacks your Healthstone and healing potion on one key, both combat-gated - two layers of emergency healing from a single button press.

### Mana Potion → Mana Gem (Mage-style, any class)
```lua
/use [combat] Major Mana Potion
/use [combat] Mana Gem
```

> [!tip] Why it's valuable
> Fires your mana potion then the Mana Gem in one press, both [combat]-gated so nothing is wasted outside a fight - an instant two-step mana refill on one bind.

### Bandage Self (no mouseover)
```lua
#showtooltip
/use [@player] Heavy Runecloth Bandage
```

> [!tip] Why it's valuable
> [@player] guarantees the bandage lands on you no matter what is targeted - a zero-risk self-top-up between pulls that saves the healer's mana.

### Buff Food + Drink in one press
```lua
/use [nomounted] Scroll of Agility
```
*(Or simply: `/use Grilled Grouper` — food macros are item-specific)*

> [!tip] Why it's valuable
> One key applies your buff food without opening bags, and [nomounted] stops you from wasting the buff while mounted - a small bind that pays off every dungeon.

---

## ⚔️ Targeting & Combat

### Smart Attack — nearest enemy + attack
```lua
#showtooltip
/targetenemy [noharm][dead]
/startattack
```

> [!tip] Why it's valuable
> Combines targeting and attacking in one press - [noharm][dead] snaps you to the nearest enemy when your target is wrong or dead, then starts the swing immediately.

### Attack + Cast (fill with your nuke)
```lua
#showtooltip
/startattack
/cast [harm] Lightning Bolt
```

> [!tip] Why it's valuable
> Starts your auto-attack and fires your nuke on the same key so no GCD is wasted waiting for the swing, and [harm] keeps it from hitting friendly targets.

### Target Last Target (after healing)
```lua
/targetlasttarget
```

> [!tip] Why it's valuable
> After healing or CC, one press snaps you straight back to the enemy you were fighting - no re-tabbing and no reaction delay.

### Tab-Target-Assist (focus kill order)
```lua
#showtooltip
/target [@focus,harm,nodead]
/startattack
```

> [!tip] Why it's valuable
> Locks onto your focus target with [@focus,harm,nodead] and starts attacking - replaces frantic Tab-tabbing with one guaranteed hit on the kill-order target.

---

## 🛡️ Trinkets & Racials

### Use Both Trinkets
```lua
#showtooltip
/use 13
/use 14
```

> [!tip] Why it's valuable
> Pops both trinket slots with one key - the standard way to line up two on-use effects for a bigger, cleaner burst window.

### On-Use Trinket + Racial Burst
```lua
#showtooltip
/cast Blood Fury
/use 13
/use 14
```
*(Replace Blood Fury with your racial — Orc Blood Fury, Troll Berserking, Tauren War Stomp all exist in Forever)*

> [!tip] Why it's valuable
> Stacks your racial cooldown with both trinkets in a single press, so the entire burst window lines up exactly when you press it - not a GCD later.

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

> [!tip] Why it's valuable
> First press sets your focus; later presses cast your interrupt or CC at it - [@focus,harm,nodead][] means the right target takes the hit without any re-targeting mid-fight.

### Clear Focus
```lua
/clearfocus
```

> [!tip] Why it's valuable
> One press wipes the focus slot so your focus macros stop firing at a dead or wrong target after a kill - removes a whole class of mis-casts.

### Mouseover-Focus (healers love this)
```lua
#showtooltip
/focus [@mouseover,help,nodead]
```

> [!tip] Why it's valuable
> Sets focus on whatever friendly unit you hover - healers and interrupters can assign their focus target without ever changing their current target.

---

## 💚 Mouseover Patterns (Healers / Interrupters)

### Mouseover Heal (self if no mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Healing Touch
```
*(Replace Healing Touch with your heal — works for Rejuvenation, Flash Heal, etc.)*

> [!tip] Why it's valuable
> Heals the unit under your cursor and falls back to yourself with [@player] - the fastest way to heal without breaking target, with no whiff risk.

### Mouseover Harm (dots, nukes, interrupts)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm,nodead] Moonfire
```

> [!tip] Why it's valuable
> Fires your DoT or nuke at the hovered enemy with a [harm,nodead] fallback to your current target - switch between damage and healing with zero targeting.

### Mouseover Friendly Buff
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Power Word: Fortitude
```

> [!tip] Why it's valuable
> Buffs whoever you hover, or yourself when nothing is under the cursor - spreads raid buffs in seconds without targeting each player individually.

---

## 🧊 Self-Heal & Emergency

### Emergency Self-Heal
```lua
#showtooltip
/cast [@player] Lay on Hands
```
*(Every class: replace with your biggest self-heal — Healthstone works too)*

> [!tip] Why it's valuable
> [@player] guarantees the heal lands on you even in a panic - no mouseover accidents when seconds decide whether you live.

### Pot + Heal Emergency (cooldown-staggered)
```lua
/use [combat] Major Healing Potion
/cast [combat] Healing Wave
```

> [!tip] Why it's valuable
> Potion and heal combo on one key, both combat-gated - the pot's instant cushion lands first, then the heal cast, from a single panicked press.

---

## ⚡ GCD & Casting QoL

### Stopcast + Cast (fake-cast bait / instant reaction)
```lua
/stopcasting
/cast Counterspell
```

> [!tip] Why it's valuable
> Cancels whatever you are casting and fires Counterspell instantly - the reaction-time edge every interrupt needs, and a perfect fake-cast for baiting enemy interrupts.

### Castsequence — two spells in one button (with reset)
```lua
#showtooltip
/castsequence reset=15 Frostbolt, Fire Blast
```
*(Resets after 15s idle or when the sequence ends)*

> [!tip] Why it's valuable
> Chains Frostbolt into Fire Blast on one button and resets after 15 seconds idle - a mini-rotation on a single bind that never drifts out of sync.

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