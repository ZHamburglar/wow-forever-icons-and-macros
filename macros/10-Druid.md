# Druid Macros — WoW: Forever

Form shifting, mouseover HoTs, and the classic cat/bear/travel swap. Classic-era Druid (level 60) — the server's signature class (the leveling guide is built around it).

> [!tip] Form IDs (Druid)
> `[stance:1]` = Bear, `[stance:2]` = Aquatic, `[stance:3]` = Cat, `[stance:4]` = Travel, `[stance:5]` = Moonkin/Boomkin

---

## 🐻🐱 Form Management

### Bear Form (tank)
```lua
#showtooltip
/cast [nostance:1] Bear Form
```

### Cat Form (DPS/stealth)
```lua
#showtooltip
/cast [nostance:3] Cat Form
```

### Travel Form (mount speed)
```lua
#showtooltip
/cast [nostance:4] Travel Form
```

### Aquatic Form (swim fast)
```lua
#showtooltip
/cast [nostance:2] Aquatic Form
```

### Moonkin Form (ranged DPS)
```lua
#showtooltip
/cast [nostance:5] Moonkin Form
```

### Dire Bear Form (tankier bear — level 40)
```lua
#showtooltip
/cast [nostance:1] Dire Bear Form
```
> [!warning] Flight Form removed
> Flight Form (TBC+) doesn't exist on Forever — no flying at level 60. Dire Bear Form (40) is the classic upgrade to Bear Form: more armor, more threat, same stance 1.

### One-Button Form Switcher (cat/bear/travel)
```lua
#showtooltip
/cast [mod:shift] Bear Form; [mod:ctrl] Cat Form; [mod:alt] Travel Form; [nocombat] Travel Form; [combat] Cat Form
```
*(Shift=Bear, Ctrl=Cat, Alt=Travel — default: Travel out of combat, Cat in combat)*

### Shift-to-Heal-and-Back (powerful!)
```lua
#showtooltip
/cast [nostance:3] Cat Form
/cast [stance:3] Healing Touch
```
> [!tip] Shift-heal macro
> Press once in cat → shifts to caster and starts Healing Touch. This is the core leveling heal — the guide uses exactly this pattern.

### Cancel Form (return to caster)
```lua
#showtooltip
/cast [stance:1] Bear Form; [stance:3] Cat Form; [stance:5] Moonkin Form
```
*(Press in any form → drops back to caster form)*

---

## 🌿 Restoration Healing (mouseover)

### Rejuvenation (HoT — mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Rejuvenation
```

### Regrowth (direct + HoT — mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Regrowth
```

### Healing Touch (big heal)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Healing Touch
```

### Swiftmend (talent — consume HoT for instant)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Swiftmend
```

### Revive (out-of-combat rez — mouseover)
```lua
#showtooltip
/cast [@mouseover,dead] Revive; [@target,dead] Revive
```
> [!warning] Lifebloom removed
> Lifebloom (TBC+) doesn't exist on Forever — classic HoTs are Rejuvenation and Regrowth. Revive is the classic out-of-combat rez; keep the raid rez (Rebirth) for combat.

### Wild Growth (talent — party HoT)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Wild Growth
```

### Tranquility (channel AoE heal)
```lua
#showtooltip
/cast Tranquility
```

### Innervate (mana regen)
```lua
#showtooltip
/cast [@player] Innervate
```

### Rebirth (combat rez — mouseover)
```lua
#showtooltip
/cast [@mouseover,dead] Rebirth; [@player] Rebirth
```

### Nature's Swiftness + Healing Touch (instant big heal)
```lua
#showtooltip
/cast Nature's Swiftness
/cast Healing Touch
```

### Abolish Poison (self/mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Abolish Poison
```

---

## 🐾 Feral DPS (Cat Form)

### Prowl (stealth)
```lua
#showtooltip
/cast [nostealth] Prowl
```

### Ravage Opener (stealth-only)
```lua
#showtooltip
/cast [stealth] Ravage; [nostealth] Claw
```
*(In stealth → Ravage. Out of stealth → Claw. Perfect single-button opener — no Mangle on Forever.)*

### Rake (cat bleed + CP builder)
```lua
#showtooltip
/cast Rake
/startattack
```
> [!warning] Mangle removed
> Mangle (TBC+) doesn't exist on Forever. Rake (level 24) is the classic cat's bleed + combo-point builder — refresh the bleed every ~8s, use Shred between refreshes.

### Shred (behind target)
```lua
#showtooltip
/cast Shred
/startattack
```

### Berserk (talent burst)
```lua
#showtooltip
/cast Berserk
```
> [!warning] Tiger's Fury removed
> Tiger's Fury (TBC+) doesn't exist on Forever. Berserk (talent) is the classic-era cat burst — 50% energy costs for 15s, so you can chain Shred/Rip without waiting on energy.

### Rip (5-CP DoT finisher)
```lua
#showtooltip
/cast Rip
```

### Ferocious Bite (direct finisher)
```lua
#showtooltip
/cast Ferocious Bite
```

### Primal Bite (talent finisher)
```lua
#showtooltip
/cast Primal Bite
```
*(Talent finisher — add to the bar once you've specced into it.)*

### Dash (speed burst)
```lua
#showtooltip
/cast Dash
```

### Pounce (stealth stun — level 36)
```lua
#showtooltip
/cast [stealth] Pounce
```
> [!warning] Survival Instincts removed
> Survival Instincts (TBC+) doesn't exist on Forever. Pounce (36) is the classic cat's opening stun — good for add control and PvP openers.

### Cower (threat dump)
```lua
#showtooltip
/cast Cower
```

---

## 🐻 Feral Tank (Bear Form)

### Bear Form + Enrage (rage engine)
```lua
#showtooltip
/cast [nostance:1] Bear Form
/cast Enrage
```

### Lacerate (bear bleed + threat — level 42)
```lua
#showtooltip
/cast Lacerate
/startattack
```
> [!warning] Mangle removed
> Mangle (bear) is TBC+ and doesn't exist on Forever. Lacerate (42) is the classic bear's threat generator and bleed — stack it to 5 on the boss (see the raid file for the stacker).

### Swipe (AoE threat)
```lua
#showtooltip
/cast Swipe
```

### Maul (single-target threat)
```lua
#showtooltip
/cast Maul
/startattack
```

### Demoralizing Roar (AoE attack debuff)
```lua
#showtooltip
/cast Demoralizing Roar
```

### Growl (taunt)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][@focus,harm,nodead][] Growl
```

### Bash (stun)
```lua
#showtooltip
/cast Bash
```

### Frenzied Regeneration (self-heal)
```lua
#showtooltip
/cast [@player] Frenzied Regeneration
```

### Feral Charge (gap closer)
```lua
#showtooltip
/cast Feral Charge
```

### Challenging Roar (AoE taunt)
```lua
#showtooltip
/cast Challenging Roar
```

---

## 🔮 Balance (Moonkin)

### Wrath (fast nuke)
```lua
#showtooltip
/cast Wrath
```

### Starfire (big nuke)
```lua
#showtooltip
/cast Starfire
```

### Moonfire (instant DoT — mouseover)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Moonfire
```

### Insect Swarm (talent DoT)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Insect Swarm
```

### Faerie Fire (armor debuff)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Faerie Fire
```

### Hurricane (AoE channel)
```lua
#showtooltip
/cast Hurricane
```

### Nature's Grasp (root attackers on hit)
```lua
#showtooltip
/cast Nature's Grasp
```
> [!warning] Force of Nature removed
> Force of Nature (TBC+) doesn't exist on Forever. Nature's Grasp is the classic balance survival tool — 45s buff that roots anything that melees you.

### Barkskin (damage reduction)
```lua
#showtooltip
/cast Barkskin
```

### Moonfire + Wrath rotation (single button)
```lua
#showtooltip
/castsequence reset=6 Moonfire, Wrath, Wrath, Wrath
```

---

## 🧊 Utility & Control

### Omen of Clarity (free spell proc — mouseover)
```lua
#showtooltip
/cast Omen of Clarity
```
> [!warning] Cyclone removed
> Cyclone (TBC+) doesn't exist on Forever — classic CC is Hibernate and Entangling Roots below. Omen of Clarity is the classic proccy buff: your next damage/heal spell costs no mana.

### Entangling Roots (root)
```lua
#showtooltip
/cast Entangling Roots
```

### Mark of the Wild (party buff)
```lua
#showtooltip
/cast Mark of the Wild
```

### Thorns (self/mouseover buff)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Thorns
```

### Remove Curse (self/mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Remove Curse
```

### Hibernate (beast/serpent CC)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Hibernate
```

### Soothe Animal (remove enrage)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Soothe Animal
```
*(Forever renames Soothe → Soothe Animal.)*

---

## 📋 Suggested Keybinds

| Key | Macro | Why |
|---|---|---|
| 1 | Rake / Wrath | Main build/nuke |
| 2 | Ravage Opener | Stealth opener |
| 3 | Rip / Ferocious Bite | Finisher |
| 4 | Berserk (talent) | Burst |
| Q | Growl / Faerie Fire | Debuff |
| E | Dash / Feral Charge | Mobility |
| R | Rejuvenation | Mouseover HoT |
| F | Healing Touch | Mouseover heal |
| Shift-1 | Shift-to-heal-and-back | Leveling heal |
| Mouse4 | Travel Form | Travel |

---

> [!note] Custom server check
> WoW: Forever is a **Classic-era (level 60) client** — no Mangle, Tiger's Fury, Survival Instincts, Cyclone, Flight Form, Force of Nature, or Lifebloom. The macros above use the classic kit: Claw/Rake/Shred for cat CPs, Rip/Ferocious Bite/Primal Bite (talent) finishers, Pounce (36) stun, Lacerate (42) + Dire Bear Form (40) for bear, Soothe Animal, and Revive. Form stances are fixed: Bear=1, Aquatic=2, Cat=3, Travel=4, Moonkin=5. If a spell is greyed out it's talent-gated (Swiftmend, Wild Growth, Insect Swarm, Berserk, Feral Charge, Primal Bite, Moonkin Form) — spend the points and the same macro works.