# Priest Macros — WoW: Forever

Mouseover healing, dispels, and shadow DPS. Classic-era (1.60.1) Priest — works for Holy/Disc/Shadow specs.

> [!tip] Healing macros
> Every heal below is **mouseover-first** (heals whoever you hover) with **self-cast fallback** when no mouseover. Hover the raid frame, press, done.

---

## 💚 Healing (Holy/Disc)

### Flash Heal (fast mouseover heal)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Flash Heal
```

### Renew (HoT mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Renew
```

### Greater Heal (big slow heal)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Greater Heal
```

### Prayer of Healing (party AoE)
```lua
#showtooltip
/cast Prayer of Healing
```

### Power Word: Shield (mouseover bubble)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Power Word: Shield
```

### Binding Heal (self + target — talent)
```lua
#showtooltip
/cast [@mouseover,help,nodead] Binding Heal
```
*(Talent-gated (Holy tree). Classic's version of the instant "heal me + heal target" button.)*

### Desperate Prayer (self emergency)
```lua
#showtooltip
/cast [@player] Desperate Prayer
```
> [!warning] Classic save
> Desperate Prayer + Power Word: Shield is your classic big-save combo — no Guardian Spirit in 1.60.1.

---

## 🧹 Dispels & Cures

### Dispel Magic (mouseover, both directions)
```lua
#showtooltip
/cast [@mouseover,harm,nodead] Dispel Magic; [@mouseover,help,nodead] Dispel Magic; [harm] Dispel Magic; [help] Dispel Magic
```

### Cure Disease (mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Cure Disease
```

### Abolish Disease (self)
```lua
#showtooltip
/cast [@player] Abolish Disease
```
*(Classic has no Mass Dispel — single-target Dispel Magic is your only purge. No AoE dispel exists in 1.60.1.)*

---

## 🌑 Shadow DPS

### Shadow Word: Pain (DoT)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Shadow Word: Pain
```

### Mind Blast (nuke)
```lua
#showtooltip
/cast Mind Blast
/startattack
```

### Mind Flay (channel — talent)
```lua
#showtooltip
/cast Mind Flay
```

### Devouring Plague (DoT + heal)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Devouring Plague
```

### Holy Nova (AoE — talent)
```lua
#showtooltip
/cast Holy Nova
```
*(Talent-gated (Holy tree). The classic instant AoE that damages enemies **and** heals the party — replaces Mind Sear for AoE.)*

### Shadowform (toggle — talent)
```lua
#showtooltip
/cast Shadowform
```

### Vampiric Embrace (self-heal on damage — talent)
```lua
#showtooltip
/cast Vampiric Embrace
```

### Silence (interrupt — focus, talent)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Silence
```

---

## 🧊 Utility & Buffs

### Power Word: Fortitude (party buff)
```lua
#showtooltip
/cast Power Word: Fortitude
```

### Divine Spirit (spirit buff)
```lua
#showtooltip
/cast Divine Spirit
```

### Inner Fire (armor buff)
```lua
#showtooltip
/cast Inner Fire
```

### Fear Ward (pre-fight buff)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Fear Ward
```

### Psychic Scream (fear)
```lua
#showtooltip
/cast Psychic Scream
```

### Shackle Undead (CC — focus)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Shackle Undead
```

### Power Infusion (haste burst — self/target, talent)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Power Infusion
```

### Mana Burn (burn enemy mana)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Mana Burn
```

---

## 📋 Suggested Keybinds

| Key | Macro | Why |
|---|---|---|
| 1 | Flash Heal | Fast heal |
| 2 | Renew | HoT |
| 3 | Greater Heal | Big heal |
| 4 | Power Word: Shield | Bubble |
| Q | Dispel Magic | Purge |
| E | Psychic Scream | Fear |
| R | Prayer of Healing | Party save |
| F | Desperate Prayer | Emergency |
| Shift-1 | Power Infusion | Burst |
| Mouse4 | Renew | Mouseover HoT |

---

> [!note] Custom server check
> Verify against your Spellbook on Forever: **Penance** and **Prayer of Mending** exist as Forever talents — if you've skilled them, add mouseover macros with the same `[@mouseover,help,nodead]` pattern. Holy Nova is talent-gated, so it only works with 1+ point in it. There is no Circle of Healing / Guardian Spirit / Lightwell / Mass Dispel in 1.60.1 — don't trust addon suggestions that list them.