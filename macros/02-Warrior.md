# Warrior Macros — WoW: Forever

Stance dancing, Charge/Intercept combos, and Execute smashing. WotLK-era Warrior with 3 stances.

> [!tip] Stance IDs
> `[stance:1]` = Battle, `[stance:2]` = Defensive, `[stance:3]` = Berserker

---

## ⚔️ Rotation & Damage

### Charge + Rend (opener)
```lua
#showtooltip
/cast [stance:1] Charge; [stance:3] Intercept
/cast Rend
```
*(Battle stance → Charge, Berserker → Intercept, then Rend)*

### Mortal Strike + Auto-Attack
```lua
#showtooltip
/startattack
/cast [stance:1] Mortal Strike
```

### Whirlwind (Berserker stance auto-switch)
```lua
#showtooltip
/cast [stance:3] Whirlwind
```

### Execute (any stance)
```lua
#showtooltip
/cast Execute
/startattack
```

### Overpower (proc watcher)
```lua
#showtooltip
/cast [stance:1] Overpower
```

### Slam (no cast bar cancel)
```lua
#showtooltip
/stopcasting
/cast Slam
```

### Thunder Clap + Demo Shout (AoE threat)
```lua
#showtooltip
/cast [stance:2] Thunder Clap
/cast Demoralizing Shout
```

---

## 🛡️ Tanking (Protection)

### Shield Slam (Defensive auto-switch)
```lua
#showtooltip
/cast [stance:2] Shield Slam
/startattack
```

### Taunt Macro — mouseover or focus
```lua
#showtooltip
/cast [@mouseover,harm,nodead][@focus,harm,nodead][] Taunt
```

### Shield Block + Shield Bash (interrupt)
```lua
#showtooltip
/cast Shield Block
/cast [stance:2] Shield Bash
```

### Spell Reflection (survival)
```lua
#showtooltip
/cast [stance:2] Shield Block
/cast [stance:2] Disarm
```
> [!warning] Spell Reflection removed
> Spell Reflection doesn't exist in Forever (Classic-era Warrior). Use **Shield Block + Disarm** in Defensive stance as the anti-melee defensive instead.

### Last Stand + Shield Wall emergency
```lua
#showtooltip
/cast Last Stand
/cast Shield Wall
```

---

## 🧨 Burst & Cooldowns

### Recklessness + Death Wish (big burst)
```lua
#showtooltip
/cast Recklessness
/cast Death Wish
```

### Bloodrage + Berserker Rage (rage engine)
```lua
#showtooltip
/cast Bloodrage
/cast Berserker Rage
```

### Retaliation (parry everything)
```lua
#showtooltip
/cast Retaliation
```

### Victory Rush self-heal
```lua
#showtooltip
/cast [@player] Victory Rush
```

---

## 🧊 Utility & Control

### Hamstring (slow kiting)
```lua
#showtooltip
/cast Hamstring
/startattack
```

### Piercing Howl (AoE slow)
```lua
#showtooltip
/cast Piercing Howl
```

### Intimidating Shout (fear)
```lua
#showtooltip
/cast Intimidating Shout
```

### Mocking Blow (off-tank taunt)
```lua
#showtooltip
/cast [stance:1] Mocking Blow
```

### Stance-Dance (Battle → Defensive → back)
```lua
#showtooltip
/cast [stance:1] Defensive Stance; [stance:2] Battle Stance; [stance:3] Battle Stance
```
*(One button: always returns to Battle stance from any)*

### Berserker Stance (for Intercept/Whirlwind)
```lua
#showtooltip
/cast [stance:3] Berserker Stance
```

### Charge + Taunt (pull combo)
```lua
#showtooltip
/cast Charge
/cast Taunt
```

---

## 📋 Suggested Keybinds

| Key | Macro | Why |
|---|---|---|
| 1 | Mortal Strike | Main damage |
| 2 | Overpower | Proc |
| 3 | Execute | Finisher |
| 4 | Whirlwind | AoE |
| Q | Charge/Intercept | Gap closer |
| E | Intimidating Shout | Emergency CC |
| R | Hamstring | Slow |
| F | Spell Reflection | Defensive |
| Shift-1 | Recklessness + Death Wish | Burst |
| Mouse4 | Stance Dance | Mobility |

---

> [!note] Custom server check
> If a custom talent renamed any ability (e.g. a new finisher), open your Spellbook and use the exact name. The `#showtooltip` will show you what's actually bound.