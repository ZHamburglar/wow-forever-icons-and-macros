# Paladin Macros — WoW: Forever

Seal juggling, Judgment spam, blessing buffs, and mouseover heals. Classic-era (Forever) Paladin.

> [!tip] Seal & Judgment
> Classic Paladins stack a **Seal** (buff) and fire **Judgment** (nuke). Keeping your Seal up is the core rotation.

---

## ⚔️ Rotation & Damage

### Judgment (main nuke — any seal)
```lua
#showtooltip
/cast Judgment
/startattack
```

> [!tip] Why it's valuable
> Your main nuke fires on one key with /startattack attached, so the swing starts the same GCD - the most-used button in the rotation earns the most central bind.

### Seal of Command + Judgment (ret opener)
```lua
#showtooltip
/cast Seal of Command
/cast Judgment
```

> [!tip] Why it's valuable
> Refreshes Seal of Command and fires Judgment in one press - the ret opener stacks the seal's proc damage with the nuke for a huge opening hit.

### Seal of Righteousness (single-target)
```lua
#showtooltip
/cast Seal of Righteousness
```

> [!tip] Why it's valuable
> One key keeps your single-target seal up, adding Holy damage to every swing - you never sit in the wrong seal for the fight.

### Exorcism (undead/demon nuke)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Exorcism
```

> [!tip] Why it's valuable
> Fires at your mouseover enemy and falls back to your current target - undead and demons melt without you ever switching targets mid-fight.

### Hammer of Wrath (execute)
```lua
#showtooltip
/cast Hammer of Wrath
```

> [!tip] Why it's valuable
> The instant-cast execute - one key throws the hammer the moment the target drops below 20% health, so sub-20% kills start with zero delay.

### Holy Wrath (AoE undead/demon)
```lua
#showtooltip
/cast Holy Wrath
```

> [!tip] Why it's valuable
> One key blasts every undead and demon around you - the AoE that wins trash pulls and death-touched packs without per-target targeting.

### Consecration (AoE ground)
```lua
#showtooltip
/cast Consecration
```

> [!tip] Why it's valuable
> Lays down ground AoE that ticks on everything inside - your sustained AoE damage and threat in one key, the backbone of paladin tanking and pack pulls.

---

## 🛡️ Tanking (Protection)

### Holy Shield (talent — threat generator)
```lua
#showtooltip
/cast Holy Shield
/startattack
```
> [!tip] Classic tanking
> Holy Shield is a talent. Paladins in Classic have no taunt — use **Righteous Fury** + **Consecration** for sustained threat.

### Righteous Fury (threat buff toggle)
```lua
#showtooltip
/cast Righteous Fury
```

> [!tip] Why it's valuable
> One key keeps your threat buff up - without it every Consecration and Judgment tick is threat you never get credit for.

---

## 💚 Healing & Support

### Flash of Light (mouseover heal)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Flash of Light
```

> [!tip] Why it's valuable
> The efficient fast heal lands on whoever you hover, or yourself with [@player] - triage the raid without ever changing target, and self-cast if nothing is hovered.

### Holy Light (big heal)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Holy Light
```

> [!tip] Why it's valuable
> The big heal reaches your mouseover or yourself in one press - zero target-switching when someone is about to die.

### Holy Shock (burst heal or damage)
```lua
#showtooltip
/cast [@mouseover,help,nodead][harm] Holy Shock
```

> [!tip] Why it's valuable
> One key does double duty - instant burst heal on your mouseover ally or instant nuke on your enemy, chosen automatically by the [help] and [harm] conditions.

### Cleanse (mouseover dispel)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Cleanse
```

> [!tip] Why it's valuable
> Removes disease, magic, and poison from whoever you hover, or yourself - the paladin's most-spammed support spell, with target priority built in.

### Lay on Hands (self emergency)
```lua
#showtooltip
/cast [@player] Lay on Hands
```

> [!tip] Why it's valuable
> [@player] guarantees this full heal lands on you in a panic - no mouseover misfires when the screen is chaos and life is on the line.

---

## 🧊 Utility & Defensives

### Blessing of Protection (bubble self/save)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Blessing of Protection
```

> [!tip] Why it's valuable
> Saves the hovered ally or yourself from all physical damage for 10 seconds - mouseover priority means the save lands the instant a melee add targets them.

### Divine Shield (immune)
```lua
#showtooltip
/cast Divine Shield
```

> [!tip] Why it's valuable
> One press makes you immune to all damage for the bubble's duration - the ultimate survival key for dropping threat, dodging a wipe mechanic, or buying time.

### Blessing of Freedom (root/slow break)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Blessing of Freedom
```

> [!tip] Why it's valuable
> Instantly breaks roots and slows on whoever you hover, or yourself - free the tank or the kiter without ever switching targets.

### Hammer of Justice (stun — focus or target)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Hammer of Justice
```

> [!tip] Why it's valuable
> Stuns your focus, or your current target if no focus is set - the [@focus] priority keeps your CC locked on the kill target without re-targeting.

### Repentance (CC — focus)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Repentance
```

> [!tip] Why it's valuable
> A 6-second long-range CC on your focus or current target - the paladin's strongest crowd control, ready on one key for healer or kill-target lockdown.

### Turn Undead (undead fear)
```lua
#showtooltip
/cast Turn Undead
```

> [!tip] Why it's valuable
> One key fears the undead target for up to 10 seconds - the soloing answer to dungeon trash, with no target juggling.

---

## 🛐 Blessings (Buff Macros)

### Might on Mouseover / Self
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Blessing of Might
```

> [!tip] Why it's valuable
> Buffs your melee attackers in one hover-and-press - no target, buff, re-target cycle, and the [@player] fallback self-buffs when you are solo.

### Kings (survival buff)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Blessing of Kings
```

> [!tip] Why it's valuable
> The survival buff lands on whoever you hover or yourself - spreading Blessing of Kings across the raid in seconds instead of one player at a time.

### Wisdom (mana buff)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Blessing of Wisdom
```

> [!tip] Why it's valuable
> The mana-restoring buff lands on whoever you hover - keep your group's mana up with one key and no target-switching.

### Greater Blessing Party Buff
```lua
#showtooltip
/cast Greater Blessing of Kings
```

> [!tip] Why it's valuable
> Casts Greater Blessing of Kings on your entire party with one press - replaces five individual buff casts with a single raid-prep key.

### Blessing Check (what's on target?)
```lua
#showtooltip
/run local b=1; for i=1,32 do local n=UnitBuff("target",i); if n and string.find(n,"Blessing") then print(n); b=0 end end
```

> [!tip] Why it's valuable
> One press prints which Blessing is active on your target - so you never waste a GCD re-buffing or drop a critical buff mid-fight.

---

## 📋 Suggested Keybinds

| Key | Macro | Why |
|-----|-------|-----|
| 1 | Judgment | Main nuke |
| 2 | Seal of Righteousness | Seal upkeep |
| 3 | Hammer of Wrath | Execute |
| 4 | Consecration | AoE |
| Q | Hammer of Justice | Stun |
| E | Cleanse | Dispel |
| R | Holy Shock | Burst |
| F | Blessing of Protection | Save |
| Shift-1 | Divine Shield | Immune |
| Mouse4 | Flash of Light | Mouseover heal |

---

> [!note] Custom server check
> If a custom talent renamed a seal or judgment, verify the exact name in your Spellbook. `#showtooltip` shows what's bound, so you'll know instantly.