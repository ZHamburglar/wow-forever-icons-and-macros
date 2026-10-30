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

> [!tip] Why it's valuable
> One press starts your attack and builds a combo point - the /startattack line means you never waste a swing while energy regenerates.

### Mutilate (build fast)
```lua
#showtooltip
/startattack
/cast Mutilate
```

> [!tip] Why it's valuable
> Fast two-combo-point builder with auto-attack folded in - a single keybind that both opens the fight and ramps your combo points quickly.

### Eviscerate (finisher)
```lua
#showtooltip
/cast Eviscerate
/startattack
```

> [!tip] Why it's valuable
> Your finisher on one key, with /startattack keeping you swinging even if the cast fails - no dropped auto-attacks while you dump combo points.

### Slice and Dice (haste buff)
```lua
#showtooltip
/cast Slice and Dice
/startattack
```

> [!tip] Why it's valuable
> One press refreshes your attack-speed buff and keeps you attacking - the /startattack line ensures the haste is never wasted on a stationary rogue.

### Rupture (finisher DoT)
```lua
#showtooltip
/cast Rupture
/startattack
```

> [!tip] Why it's valuable
> Applies your finisher DoT while /startattack keeps the pressure up - a single key for maintaining damage over time between burst windows.

### Stealth Opener — Ambush / Garrote
```lua
#showtooltip
/cast [stealth] Ambush; [nostealth] Sinister Strike
```

> [!tip] Why it's valuable
> The [stealth] conditional fires Ambush while hidden and falls back to Sinister Strike out of stealth - one keybind covers both opener and normal rotation.

### Backstab (behind target)
```lua
#showtooltip
/startattack
/cast Backstab
```

> [!tip] Why it's valuable
> Auto-attack plus Backstab in one press - you only need to be behind the target and hit one key, so positioning plays stay reaction-time friendly.

---

## 🥷 Stealth & Vanish

### Vanish + Cheap Shot (re-CC)
```lua
#showtooltip
/cast Vanish
/cast Cheap Shot
```

> [!tip] Why it's valuable
> One button vanishes you and instantly stuns the target - the classic escape-and-re-CC combo that saves two keypresses when things go sideways.

### Stealth Toggle (Prowl-style)
```lua
#showtooltip
/cast Stealth
```

> [!tip] Why it's valuable
> A dedicated key for Stealth means you never lose a second reaching the button - faster openers and easier re-stealth after a Vanish.

### Pick Pocket + Stealth (farm)
```lua
#showtooltip
/cast Pick Pocket
/cast Stealth
```

> [!tip] Why it's valuable
> One press loots the target and re-enters Stealth - the farming combo keeps your pickpocket runs moving without dropping stealth.

### Sap (CC — focus or target)
```lua
#showtooltip
/cast [@focus,harm,nodead][harm] Sap
```

> [!tip] Why it's valuable
> The focus-first targeting locks down a second enemy without switching targets - crowd control on a different mob than your kill target in one press.

### Distract (misdirect NPCs)
```lua
#showtooltip
/cast Distract
```

> [!tip] Why it's valuable
> Redirects patrolling NPCs on one key - you control exactly where mobs look so you can slip past or line up a clean pull.

---

## ⚡ Burst & Finishers

### Cold Blood + Eviscerate (guaranteed crit)
```lua
#showtooltip
/cast Cold Blood
/cast Eviscerate
```

> [!tip] Why it's valuable
> Guarantees your Eviscerate crits on a single button - the burst combo that turns a full combo-point dump into one massive spike.

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

> [!tip] Why it's valuable
> A one-press dodge boost that saves you when damage spikes - the reaction-time defensive for when melee pressure gets heavy.

### Sprint (escape/chase)
```lua
#showtooltip
/cast Sprint
```

> [!tip] Why it's valuable
> Instant speed on one key - the escape-or-chase button that gets you out of danger or onto a runner without touching your movement keys.

### Kick (interrupt — mouseover/focus)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][@focus,harm,nodead][] Kick
```

> [!tip] Why it's valuable
> Mouseover and focus fallbacks mean the interrupt always lands on the right caster without retargeting - a reaction-time save against big enemy casts.

### Gouge (4s stun, from front)
```lua
#showtooltip
/cast Gouge
```

> [!tip] Why it's valuable
> A front-facing 4-second stun on one key - the classic CC that stops casts and buys breathing room without needing stealth.

### Kidney Shot (stun finisher)
```lua
#showtooltip
/cast Kidney Shot
/startattack
```

> [!tip] Why it's valuable
> Your stun finisher plus /startattack in one press - the control button that locks down a target while you keep building damage.

### Blind (CC — focus)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Blind
```

> [!tip] Why it's valuable
> Focus-first casting CCs a second target without retargeting - a one-key panic control for when adds need to disappear for 10 seconds.

---

## 🧪 Poisons & Utilities

### Apply Deadly Poison to Main Hand
```lua
#showtooltip
/use Deadly Poison
/use 16
```
*(Main hand = slot 16, off-hand = 17)*

> [!tip] Why it's valuable
> Applies Deadly Poison straight to your main hand in one press - no inventory dragging or spellbook hunting, so upkeep happens between pulls in seconds.

### Apply Instant Poison to Off-Hand
```lua
#showtooltip
/use Instant Poison
/use 17
```

> [!tip] Why it's valuable
> One press coats the off-hand with Instant Poison - the same no-fuss upkeep for your second weapon, keeping both poisons up with minimal downtime.

### Poison Toggle (Deadly + Instant both weapons)
```lua
#showtooltip
/use Deadly Poison
/use 16
/use Instant Poison
/use 17
```

> [!tip] Why it's valuable
> Reapplies Deadly and Instant to both weapons in a single press - the pre-pull routine that saves two extra keypresses and guarantees no forgotten weapon.

### Detect Traps (stealth detect / disarm)
```lua
#showtooltip
/cast Detect Traps
```

> [!tip] Why it's valuable
> A dedicated key reveals traps ahead - the classic pre-pull safety check so you and the group never stumble into a trap blind.

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
