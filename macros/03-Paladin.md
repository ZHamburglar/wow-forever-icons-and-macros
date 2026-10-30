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

### Seal of Command + Judgment (ret opener)
```lua
#showtooltip
/cast Seal of Command
/cast Judgment
```

### Seal of Righteousness (single-target)
```lua
#showtooltip
/cast Seal of Righteousness
```

### Exorcism (undead/demon nuke)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Exorcism
```

### Hammer of Wrath (execute)
```lua
#showtooltip
/cast Hammer of Wrath
```

### Holy Wrath (AoE undead/demon)
```lua
#showtooltip
/cast Holy Wrath
```

### Consecration (AoE ground)
```lua
#showtooltip
/cast Consecration
```

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

---

## 💚 Healing & Support

### Flash of Light (mouseover heal)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Flash of Light
```

### Holy Light (big heal)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Holy Light
```

### Holy Shock (burst heal or damage)
```lua
#showtooltip
/cast [@mouseover,help,nodead][harm] Holy Shock
```

### Cleanse (mouseover dispel)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Cleanse
```

### Lay on Hands (self emergency)
```lua
#showtooltip
/cast [@player] Lay on Hands
```

---

## 🧊 Utility & Defensives

### Blessing of Protection (bubble self/save)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Blessing of Protection
```

### Divine Shield (immune)
```lua
#showtooltip
/cast Divine Shield
```

### Blessing of Freedom (root/slow break)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Blessing of Freedom
```

### Hammer of Justice (stun — focus or target)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Hammer of Justice
```

### Repentance (CC — focus)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Repentance
```

### Turn Undead (undead fear)
```lua
#showtooltip
/cast Turn Undead
```

---

## 🛐 Blessings (Buff Macros)

### Might on Mouseover / Self
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Blessing of Might
```

### Kings (survival buff)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Blessing of Kings
```

### Wisdom (mana buff)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Blessing of Wisdom
```

### Greater Blessing Party Buff
```lua
#showtooltip
/cast Greater Blessing of Kings
```

### Blessing Check (what's on target?)
```lua
#showtooltip
/run local b=1; for i=1,32 do local n=UnitBuff("target",i); if n and string.find(n,"Blessing") then print(n); b=0 end end
```

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