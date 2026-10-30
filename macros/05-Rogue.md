# Rogue Macros — WoW: Forever

Stealth openers, vanish tricks, poison upkeep, and combo point finishers. Classic-era (Forever) Rogue.

> [!tip] Stealth state
> Use `[stealth]` to fire stealth-only spells (Ambush, Garrote) and fall back to normal rotation outside stealth.

---

## 🗡️ Rotation & Damage

### Sinister Strike (CP builder)
```lua
#showtooltip
/startattack
/cast Sinister Strike
```

### Mutilate (build fast)
```lua
#showtooltip
/startattack
/cast Mutilate
```

### Eviscerate (finisher)
```lua
#showtooltip
/cast Eviscerate
/startattack
```

### Slice and Dice (haste buff)
```lua
#showtooltip
/cast Slice and Dice
/startattack
```

### Rupture (finisher DoT)
```lua
#showtooltip
/cast Rupture
/startattack
```

### Stealth Opener — Ambush / Garrote
```lua
#showtooltip
/cast [stealth] Ambush; [nostealth] Sinister Strike
```

### Backstab (behind target)
```lua
#showtooltip
/startattack
/cast Backstab
```

---

## 🥷 Stealth & Vanish

### Vanish + Cheap Shot (re-CC)
```lua
#showtooltip
/cast Vanish
/cast Cheap Shot
```

### Stealth Toggle (Prowl-style)
```lua
#showtooltip
/cast Stealth
```

### Pick Pocket + Stealth (farm)
```lua
#showtooltip
/cast Pick Pocket
/cast Stealth
```

### Sap (CC — focus or target)
```lua
#showtooltip
/cast [@focus,harm,nodead][harm] Sap
```

### Distract (misdirect NPCs)
```lua
#showtooltip
/cast Distract
```

---

## ⚡ Burst & Finishers

### Cold Blood + Eviscerate (guaranteed crit)
```lua
#showtooltip
/cast Cold Blood
/cast Eviscerate
```

### Adrenaline Rush + Blade Flurry (AoE burst)
```lua
#showtooltip
/cast Adrenaline Rush
/cast Blade Flurry
```

> [!tip] Classic burst toolkit
> Fan of Knives, Killing Spree, and Cloak of Shadows are not available in Classic (Forever). Classic rogue burst relies on **Adrenaline Rush** (talent), **Blade Flurry** (talent), **Cold Blood** (talent), and **Vanish + Cheap Shot** for re-positioning.

---

## 🧊 Defensives & Control

### Evasion (dodge)
```lua
#showtooltip
/cast Evasion
```

### Sprint (escape/chase)
```lua
#showtooltip
/cast Sprint
```

### Kick (interrupt — mouseover/focus)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][@focus,harm,nodead][] Kick
```

### Gouge (4s stun, from front)
```lua
#showtooltip
/cast Gouge
```

### Kidney Shot (stun finisher)
```lua
#showtooltip
/cast Kidney Shot
/startattack
```

### Blind (CC — focus)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Blind
```

---

## 🧪 Poisons & Utilities

### Apply Deadly Poison to Main Hand
```lua
#showtooltip
/use Deadly Poison
/use 16
```
*(Main hand = slot 16, off-hand = 17)*

### Apply Instant Poison to Off-Hand
```lua
#showtooltip
/use Instant Poison
/use 17
```

### Poison Toggle (Deadly + Instant both weapons)
```lua
#showtooltip
/use Deadly Poison
/use 16
/use Instant Poison
/use 17
```

### Detect Traps (stealth detect / disarm)
```lua
#showtooltip
/cast Detect Traps
```

---

## 📋 Suggested Keybinds

| Key | Macro | Why |
|-----|-------|-----|
| 1 | Sinister Strike | CP builder |
| 2 | Slice and Dice | Buff |
| 3 | Eviscerate | Finisher |
| 4 | Rupture | DoT |
| Q | Kick | Interrupt |
| E | Gouge | CC |
| R | Vanish | Escape |
| F | Evasion | Defensive |
| Shift-1 | Cold Blood + Eviscerate | Burst |
| Mouse4 | Stealth | Stealth |

---

> [!note] Custom server check
> Subtlety vs Assassination changes openers (Ambush vs Mutilate). Pick the opener your spec actually has — both macros are listed.