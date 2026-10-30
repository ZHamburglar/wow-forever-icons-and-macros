# Advanced QoL Macros — Every Class

The **second layer** of the macro library: hybrid buttons, priority chains, and swap tricks that veteran players use. These are class-agnostic — they work on any of the 9 classes.

> [!info] Why this file exists
> The cross-class file (01) covered the essentials. This file covers the **advanced** patterns: one button that does two different things, interrupts that auto-pick the best target, and gear/target tricks that save action bar space and reaction time.

---

## 🔀 Hybrid Buttons (One Key, Two Jobs)

### Heal Friend / Damage Enemy (universal)
```lua
#showtooltip
/cast [help] Flash Heal; [harm] Smite
```
> [!tip] Why it's useful
> This is the **most valuable macro pattern in the game**. It reads your target: friendly → heal them, hostile → damage them. One keybind replaces two. Replace the spells with your class's equivalents (e.g. Paladin: `Holy Light` / `Exorcism`; Shaman: `Healing Wave` / `Lightning Bolt`; Druid: `Regrowth` / `Moonfire`).

### Buff Self / Buff Mouseover (smart buff)
```lua
#showtooltip
/cast [@mouseover,help,nodead] Blessing of Might; [@player] Blessing of Might
```
> [!tip] Why it's useful
> Hover a party member → buffs them. No mouseover → buffs you. One button handles both "buff the tank" and "rebuff myself after death." Works for any class buff (Mark of the Wild, Arcane Intellect, Power Word: Fortitude…).

### Cast At Mouseover / Fall Back To Target
```lua
#showtooltip
/cast [@mouseover,harm,nodead][] Counterspell
```
> [!tip] Why it's useful
> Interrupts and CCs land on whoever you hover *without changing your target*. You keep DPSing the main target while kicking the healer you're hovering. The `[]` fallback means: no mouseover → normal target. This single pattern wins PvP fights.

---

## 🎯 Priority Chains (Auto-Pick the Best Target)

### Interrupt: Focus > Mouseover > Target
```lua
#showtooltip
/cast [@focus,harm,nodead] Kick; [@mouseover,harm,nodead] Kick; [harm] Kick
```
> [!tip] Why it's useful
> The interrupt lands on **focus first** (your designated enemy healer), else mouseover, else current target. One button always does the *right* interrupt — you never scramble to switch targets mid-cast. Replace `Kick` with your class interrupt (Counterspell, Earth Shock, Silencing Shot, Shield Bash, Spell Lock).

### CC: Focus Target of Focus (kill the off-healer)
```lua
#showtooltip
/cast [@focustarget,harm,nodead][] Polymorph
```
> [!tip] Why it's useful
> `@focustarget` = your focus's current target. Set the enemy tank as focus and this button always CCs whoever *they're* fighting (usually the healer you want locked down). Shown as Polymorph (mage); swap in your own CC — Fear (warlock), Sap (rogue), Repentance (paladin), Hibernate (druid) — same pattern.

### Heal: Target of Target (tank assist)
```lua
#showtooltip
/cast [@targettarget,help,nodead][] Flash Heal
```
> [!tip] Why it's useful
> Heals whoever your target is attacking — the classic **tank-heal assist**. Set the boss as your target, spam this button, and you automatically heal the tank tanking it. No raid-frame mouseover needed for single-tank fights. Replace with your class heal.

### Assist Focus (DPS the kill target)
```lua
#showtooltip
/target [@focus,harm,nodead]
/startattack
```
> [!tip] Why it's useful
> Sets focus as your kill target and starts attacking. Raid leaders assign focus; this button aligns you with the kill order instantly — no more DPSing the wrong mob.

---

## ⚙️ Gear & Consumable Swaps

### Weapon Swap (2H ↔ 1H+Shield)
```lua
#showtooltip
/equipslot 16, Sulfuras, the Extinguished Hand
/equipslot 17, Bulwark of Azzinoth
```
> [!tip] Why it's useful
> Warriors/Paladins/Shamans swap between 2H (DPS) and 1H+Shield (tank/survive) constantly. One button swaps both slots. *(Slot 16 = main hand, 17 = off hand. Replace with your actual weapon names — out of combat only.)*

### Trinket Use + Trinket Swap (equip-on-use)
```lua
#showtooltip
/use 13
/use 14
```
> [!tip] Why it's useful
> On-use trinkets have 2-min cooldowns; you often want **two different trinkets** (one burst, one defensive). Having both on one button fires them in sequence — the second press uses the second trinket. Simpler than swapping gear mid-fight.

### Mana/Health Potion Priority Chain
```lua
#showtooltip
/use [combat] Healthstone
/use [combat] Major Healing Potion
```
> [!tip] Why it's useful
> Healthstones (from Warlocks or crafted) share the potion cooldown but heal more per use. This chain tries the **better** consumable first, falls back to the potion. One button, always the best heal available.

---

## 🏃 Movement & Escape Combos

### Sprint + Vanish / Escape Combo (Rogue-style)
```lua
#showtooltip
/cast Sprint
/cast Vanish
```
> [!tip] Why it's useful
> Losing a fight? One key = speed + stealth-drop. Works on any class with a movement+stealth/invisibility pair (Rogue: Sprint+Vanish, Mage: Blink+Invisibility, Hunter: Disengage+Feign Death, Druid: Dash+Prowl).

### Stopcasting + Instant (fake-cast bait)
```lua
#showtooltip
/stopcasting
/cast Counterspell
```
> [!tip] Why it's useful
> Starts a long cast (e.g. heal) to bait the enemy's interrupt, then **instantly cancels and fires your own interrupt**. The stopcast line cancels whatever you were doing — critical for interrupt wars. Replace `Counterspell` with any instant cast.

### Fall Back To Mount (out of combat)
```lua
#showtooltip
/cast [nocombat] Summon Random Favorite Mount
```
> [!tip] Why it's useful
> Pressing a DPS button out of combat wastes it; this button mounts you instead. Bind it to your travel key — it auto-mounts when safe and does nothing (or casts) in combat. *(Add a fallback spell after the mount for in-combat use.)*

---

## 📦 Inventory & Interaction Tricks

### Repair All (vendor NPC)
```lua
#showtooltip
/script RepairAllItems()
```
> [!tip] Why it's useful
> One click repairs everything while standing at a repair NPC — no right-click menus. Pairs with the **Reinforce** Legacy perk (reduced repair cost).

### Auto-Loot Toggle (fast looting)
```lua
#showtooltip
/script SetCVar("autoLootDefault", 1 - GetCVar("autoLootDefault"))
```
> [!tip] Why it's useful
> Toggles auto-loot on/off with one button. On = every corpse loots instantly (great for the leveling grind); off = shift-click selective looting in dungeons.

### Interact With Mouseover (gather/npc)
```lua
#showtooltip
/interact
```
> [!tip] Why it's useful
> WotLK-era `/interact` interacts with whatever you're targeting — bind it to a key and you can gather herbs/ores, open quest chests, and talk to quest givers without precisely clicking tiny hitboxes. *(Requires a target; combine with `[@mouseover]` targeting if your UI supports it.)*

---

## 🧠 Mental Model

> [!note] The "why" in one line
> - **Hybrid buttons** save action bar space → fewer keys to learn, faster reactions.
> - **Priority chains** remove target-switching → your interrupt/CC/heal always hits the right unit.
> - **Swap macros** replace gear juggling → one key = best gear for the moment.
> - **Escape combos** bundle survival → panicking players press ONE key, not three.

---

## 📋 Master List

| # | Macro | Pattern | Best For |
|---|---|---|---|
| 1 | Heal/Damage hybrid | `[help] heal; [harm] dmg` | Every class |
| 2 | Smart buff | `[@mouseover,help][] buff` | Buff classes |
| 3 | Mouseover cast | `[@mouseover,harm][] spell` | Interrupts/CC |
| 4 | Interrupt priority | focus > mouseover > target | PvP/raids |
| 5 | CC focus target | `[@focustarget][] CC` | Arena/world PvP |
| 6 | Tank-heal assist | `[@targettarget,help][]` | Healers |
| 7 | Assist focus | `/target [@focus]` | Raid DPS |
| 8 | Weapon swap | `/equipslot 16/17` | Hybrid classes |
| 9 | Potion chain | HS > pot | Everyone |
| 10 | Escape combo | move + stealth | Everyone |
| 11 | Stopcast bait | `/stopcasting` + instant | Interrupt wars |
| 12 | Repair all | `/script RepairAllItems()` | Everyone |
| 13 | Auto-loot toggle | CVar flip | Leveling |
| 14 | Interact | `/interact` | Gather/quests |